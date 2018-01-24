#課題３　閾値処理
閾値を4パターン設定し,閾値処理した画像を示せ．


clear; % 変数のオールクリア

ORG=imread('neko.jpg'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
pause;  

上記の操作によって表示される画像を図１に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai3.1.PNG" width="500">  
図１　課題３の原画像  

IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換
imagesc(IMG); colormap(gray); colorbar;  
pause;  

輝度値が64以上の画素を1，その他を0に変換したときの画像を図２に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai3.2.PNG" width="500">  
図２　輝度値が64以上のとき  

IMG = ORG > 96;  
imagesc(IMG); colormap(gray); colorbar;  
pause;  

輝度値が96以上の画素を1，その他を0に変換したときの画像を図３に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai3.3.PNG" width="500">  
図３　輝度値が96以上のとき  

IMG = ORG > 128;  
imagesc(IMG); colormap(gray); colorbar;  
pause;  

輝度値が128以上の画素を1，その他を0に変換したときの画像を図４に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai3.4.PNG" width="500">  
図４　輝度値が128以上のとき    

IMG = ORG > 192;  
imagesc(IMG); colormap(gray); colorbar;  

輝度値が192以上の画素を1，その他を0に変換したときの画像を図５に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai3.5.PNG" width="500">  
図５　輝度値が192以上のとき  
