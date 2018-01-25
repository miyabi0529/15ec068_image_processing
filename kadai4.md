#課題４　画像のヒストグラム  
画素の濃度ヒストグラムを生成せよ．

clear; % 変数のオールクリア

ORG=imread('neko.jpg'); % 原画像の入力  
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar;  
pause;  

上記の操作によって表示される画像を図１に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai4.1.PNG" width="500">  

図１　課題４の原画像

imhist(ORG); % ヒストグラムの表示  

その後，上記の操作によって表示される画像を図２に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai4.2.PNG" width="500">  

図２　ヒストグラム
