Task 1:
cp image.jpg image_steg.jpg
steghide embed -cf image_steg.jpg -ef message.txt
steghide info image_steg.jpg > info.txt
nano info.txt

Task 2:
diff image.jpg image_steg.jpg > diff.txt
nano diff.txt

Task 3:
mkdir extract
mv image_steg.jpg extract
cd extract
steghide extract -sf image_steg.jpg
nano message.txt
