#課題６　画像の二値化  
下記のプログラムを参考にして画像を二値化せよ．

clear; % 変数のオールクリア  
ORG=imread('Lenna.png'); % 原画像の入力  
ORG = rgb2gray(ORG);  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
pause; % 一時停止  

上記の操作によって表示される画像を図１に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai6.1.PNG" width="500">  

図１　課題６の原画像

IMG = ORG>128; % 128による二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  
pause;  

上記の操作によって表示される画像を図２に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai6.3.PNG" width="500">  

図２　閾値128による二値化

IMG = dither(ORG); % ディザ法による二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

上記の操作によって表示される画像を図３に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai6.2.PNG" width="500">  

図３　ディザ法による二値化
