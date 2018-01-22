#課題２　階調数と疑似輪郭
２階調，４階調，８階調の画像を生成せよ．

clear; % 変数のオールクリア　　
ORG=imread('Lenna.png'); % 原画像の入力　　
ORG = rgb2gray(ORG); colormap(gray); colorbar;　　
imagesc(ORG); axis image; % 画像の表示　　
pause; % 一時停止　　

上記の操作によって表示される画像を図１に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai2.1.PNG" width="500">
図１　課題２の原画像


% ２階調画像の生成
IMG = ORG>128;
imagesc(IMG); colormap(gray); colorbar;  axis image;
pause;

２階調画像は上記の操作によって生成することができる．生成された２階調画像を図２に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai2.2.PNG" width="500">
図２　２階調画像


% ４階調画像の生成
IMG0 = ORG>64;
IMG1 = ORG>128;
IMG2 = ORG>192;
IMG = IMG0 + IMG1 + IMG2;
imagesc(IMG); colormap(gray); colorbar;  axis image;

４階調画像は上記の操作によって生成することができる．生成された４階調画像を図３に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai2.3.PNG" width="500">
図３　４階調画像


IMG0 = ORG>32;
IMG1 = ORG>64;
IMG2 = ORG>96;
IMG3 = ORG>128;
IMG4 = ORG>160;
IMG5 = ORG>192;
IMG6 = ORG>224;
IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6;
imagesc(IMG); colormap(gray); colorbar;  axis image;

８階調画像は上記の操作によって生成することができる．生成された８階調画像を図４に示す．
<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai2.4.PNG" width="500">
図４　８階調画像


このように２階調，４階調，８階調と変化させていくと画像に用いられる色の種類が増えていき，よりなめらかな画像になっていることが分かる．
