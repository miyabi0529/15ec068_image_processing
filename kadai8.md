#課題８ ラベリング  
二値化された画像の連結成分にラベルをつけよ．

ORG = imread('neko.jpg'); % 画像の読み込み  
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
pause;  

上記の操作によって表示される画像を図１に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai8.1.PNG" width="500">  

図１　課題８の原画像

IMG = ORG > 128; % 閾値128で二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  
pause;  

上記の操作によって表示される画像を図２に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai8.2.PNG" width="500">  

図２　閾値128で二値化した画像

IMG = bwlabeln(IMG);  
imagesc(IMG); colormap(jet); colorbar; % 画像の表示  
pause;  

上記の操作によって表示される画像を図３に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai8.3.PNG" width="500">  

図３　ラベリングした画像
