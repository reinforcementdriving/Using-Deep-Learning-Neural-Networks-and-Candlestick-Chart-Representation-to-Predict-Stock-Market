python get_data.py -sd 2017-01-01 -t ^FTSE -s yahoo -p training

python preprocess.py -i stockdatas/^FTSE.csv -l 5 -m olhc2cs

python preprocess.py -m createLabel -i stockdatas/^FTSE.csv -l 5

python preprocess.py -m img2dt -i dataset/5/img -lf FTSE_label_5.txt

python resnet18.py -i dataset/10/img/classes -d 200 -c 3 -e 5 -b 16 -o adam

2784,288
EWT
4144,272