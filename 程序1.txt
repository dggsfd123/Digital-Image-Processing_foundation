clear all;
clc
CM = imread('C:\DIP\assignment1\cameraman.bmp'); 
%CM = rgb2gray(CM);  %change to gray figure
answer_1 = size(CM);
answer_2 = CM(50,130);
answer_3 = CM(5,100:1:130);
imwrite(CM,'C:\DIP\assignment1\cameraman.jpg');%compress the pic
R = imread('C:\DIP\assignment1\rose.bmp'); 
R = imresize(R,[512,512]);
answer_5_1 = R(1:2:end,1:2:end);%length and width reduction
R_trans = [];
answer_5_2 = [];
for i = 1:1:256
    R_trans = [R_trans;answer_5_1(i,1:1:end);answer_5_1(i,1:1:end)];
end
for i = 1:1:256
    answer_5_2 = [answer_5_2,R_trans(1:1:end,i),R_trans(1:1:end,i)];
end
imshow(answer_5_2);%vague