#課題10 画像のエッジ抽出  
次のプログラムを参考にして，エッジ抽出を体験せよ．

ORG = imread('neko.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); %カラーからグレイへの変換  
imagesc(ORG); colormap('gray'); colorbar;% 画像表示  
pause; % 一時停止  

上記の操作によって表示される画像を図１に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai10.1.PNG" width="500">  

図１　課題１０の原画像

IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）  
imagesc(IMG); colormap('gray'); colorbar;% 画像表示  
pause; % 一時停止  

上記の操作によって表示される画像を図２に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai10.2.PNG" width="500">  

図２　エッジ抽出(プレウィット法)

IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）  
imagesc(IMG); colormap('gray'); colorbar;% 画像表示  
pause; % 一時停止  

上記の操作によって表示される画像を図３に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai10.3.PNG" width="500">  

図３　エッジ抽出(ソベル法)

IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）  
imagesc(IMG); colormap('gray'); colorbar;% 画像表示  
pause; % 一時停止  

上記の操作によって表示される画像を図４に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai10.4.PNG" width="500">  

図４　エッジ抽出(キャニー法)
