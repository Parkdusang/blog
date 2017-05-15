---
title: ":computer: Image Processing total"
layout: post
date: 2016-02-12 12:10
tag:
- CPP
- OpenCV
image:  https://Parkdusang.github.io/blog/assets/images/jekyll-logo-light-solid.png
headerImage: true
projects: true
hidden: true # don't count this post in blog pagination
description: "This is a simple and minimalist template for Jekyll for those who likes to eat noodles."
category: project
author: Dusang
externalLink: false
---
## Summary:

지금까지 사용했던 OpenCV를 이용한 이미지 프로세싱 기술을 하나씩 풀어서 기술한 페이지입니다.
이 페이지는 계속 업데이트를 하고 있습니다.

#### Especial Elements
- [Skill](#skill)
- [Content](#content)
  * [Gaussian](#gaussian)
  * [ImageWarping](#imagewarping)
- [Link](#link)

---
## Skill

- C++
- OpenCV

---
## Content


### Default ###

You must be read image and Image process

loading image
{% highlight cpp %}
string imageName("lena_color.png");
Mat image;
image = imread(imageName.c_str(), IMREAD_COLOR);
//defensive code
if(image.empty()){
    cout << "Could not open or find the image" << endl;
    return -1;
}
namedWindow("Display window" , WINDOW_AUTOSIZE);
imshow("Display window", image);
{% endhighlight %}

### Gaussian ###

Making GaussianMask
Mask is Two dimensional Mark and square
Pick up the size and make the mask.

{% highlight cpp %}
void GaussianMask(float sigma, float **Mask ,int maskSize){

    double r;
    double sum = 0.0,pi = 3.14;
    int limitSize = maskSize/2;
    for (int i = (-1) * limitSize ; i <= limitSize; i++)
    {
        for(int j = (-1) * limitSize; j <= limitSize; j++)
        {
            r = sqrt(i*i + j*j);
            Mask[i + limitSize][j + limitSize] = (exp(-(r*r)/(2*sigma*sigma)))/(pi * (2*sigma*sigma));
            sum += Mask[i + limitSize][j + limitSize];
        }
    }

    for(int i = 0; i < maskSize; ++i){
        for(int j = 0; j < maskSize; ++j){
            Mask[i][j] /= sum;
            //Mask[i][j] *= 20;
        }
    }
}
{% endhighlight %}



<div class="side-by-side">
    <div class="toleft">
        <img class="image" height="400" src="{{ site.url }}/{{ 'assets/images/imagepro/1_1.png' }}" alt="Alt Text">
        <figcaption class="caption">Before applying the Mark</figcaption>
    </div>
    <div class="toright">
        <img class="image" height="400" src="{{ site.url }}/{{ 'assets/images/imagepro/1_2.png' }}" alt="Alt Text">
        <figcaption class="caption">After applying the Mark</figcaption>
    </div>
</div>

***
### ImageWarping ###

Create a matrix using three points from one point to another.

For example Code
{% highlight cpp %}
Point2f srcTri[3];
Point2f dstTri[3];
Mat warp_mat( 2, 3, CV_32FC1 );
/// Set the dst image the same type and size as src
warp_dst = Mat::zeros( src.rows, src.cols, src.type() );

srcTri[0] = Point2f( 0,0  );
srcTri[1] = Point2f( src.cols - 1, 0 );
srcTri[2] = Point2f( 0, src.rows - 1 );

dstTri[0] = Point2f( src.cols*0.0, src.rows*0.33 );
dstTri[1] = Point2f( src.cols*0.85, src.rows*0.25 );
dstTri[2] = Point2f( src.cols*0.15, src.rows*0.7 );
/// Get the Affine Transform
warp_mat = getAffineTransform( srcTri, dstTri );

warpAffine( src, warp_dst, warp_mat, warp_dst.size() );

{% endhighlight %}
<div class="side-by-side">
    <div class="toleft">
        <img class="image" height="400" src="{{ site.url }}/{{ 'assets/images/imagepro/2_1.png' }}" alt="Alt Text">
        <figcaption class="caption">Before Warping image</figcaption>
    </div>
    <div class="toright">
        <img class="image" height="400" src="{{ site.url }}/{{ 'assets/images/imagepro/2_2.png' }}" alt="Alt Text">
        <figcaption class="caption">After Warping image</figcaption>
    </div>
</div>



---
## Link
이 코드는 현재 깃허브에 올려놨습니다.
- [Github](https://github.com/Parkdusang/Categoryclassification). 하이퍼링크를 클릭하시면 깃허브 페이지로 이동합니다.

---
