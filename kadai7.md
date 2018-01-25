#課題7　ダイナミックレンジの拡大  
画素のダイナミックレンジを０から２５５にせよ． 

ORG = imread('neko.jpg'); % 画像の読み込み  
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
pause;  
imhist(ORG); % 濃度ヒストグラムを生成、表示  
pause;  

上記の操作によって表示される画像を図１，ヒストグラムを図２に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai7.1.PNG" width="500">  

図１　課題７の原画像

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai7.2.PNG" width="500">  

図２　原画像のヒストグラム

ORG = double(ORG);  
mn = min(ORG(:)); % 濃度値の最小値を算出  
mx = max(ORG(:)); % 濃度値の最大値を算出  
ORG = (ORG-mn)/(mx-mn)*255;  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
pause;  
ORG = uint8(ORG); % この行について考察せよ  
imhist(ORG); % 濃度ヒストグラムを生成、表示  

上記の操作によって表示される画像を図３，ヒストグラムを図４に示す．

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai7.3.PNG" width="500">  

図３　ダイナミックレンジ拡大後の原画像

<img src="https://github.com/miyabi0529/15ec068_image_processing/blob/master/kadai7.4.PNG" width="500">  

図４　ダイナミックレンジ拡大後のヒストグラム  

uint8とは，「1バイト符号なし整数形式に変換する」という意味である．よって，ORG = uint8(ORG);の文は「ORGを1バイト符号なし整数形式に変換する」という文であると考えられる．
