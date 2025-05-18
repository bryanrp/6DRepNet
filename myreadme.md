## train

- We are using ETH-XGaze. I added a new dataset class called ETHXGaze. In train.py or test.py, make sure to use ETHXGaze as the dataset type
- I added --output_path option in train.py. Make sure to pass in the correct output folder path
- Make sure to set --dataset to "ETHXGaze"

```
python sixdrepnet/train.py --dataset "ETHXGaze" --data_dir="C:\Users\victus\Documents\git-project\capstone\dataset-sample\xgaze-full\Image" --filename_list "C:\Users\victus\Documents\git-project\capstone\dataset-sample\xgaze-small\Label\train.label" --output_path "output/xgaze-small-0/snapshots" --num_epoch 40
```

```
python sixdrepnet/test.py --dataset "ETHXGaze" --data_dir="C:\Users\victus\Documents\git-project\capstone\dataset-sample\xgaze-full\Image" --filename_list "C:\Users\victus\Documents\git-project\capstone\dataset-sample\xgaze-small\Label\test.label" --snapshot="output/xgaze-small-0/model-0.pth --output_csv="output/xgaze-small-0/log/test.log"
```

## test

after getting the .tar, convert it to .pth using sixdrepnet/convert.py