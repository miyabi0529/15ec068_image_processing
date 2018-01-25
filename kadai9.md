#課題９ メディアンフィルタと先鋭化  
メディアンフィルターを適用し，ノイズ除去を体験せよ．

ORG = imread('neko.jpg'); % 画像の読み込み  
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
pause;  

上記の操作によって表示される画像を図１に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai9.1.PNG" width="500">  

図１　課題９の原画像

ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
pause;  

上記の操作によって表示される画像を図２に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai9.2.PNG" width="500">  

図２　ノイズ添付後

IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  
pause;  

上記の操作によって表示される画像を図３に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai9.3.PNG" width="500">  

図３　雑音除去後(平滑化フィルタ)

IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  
pause;  

上記の操作によって表示される画像を図４に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai9.4.PNG" width="500">  

図４　雑音除去後(メディアンフィルタ)

f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計  
IMG = filter2(f,IMG,'same'); % フィルタの適用  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  
pause;  

上記の操作によって表示される画像を図５に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai9.5.PNG" width="500">  

図５　フィルタ適用後
