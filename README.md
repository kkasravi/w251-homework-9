
https://w251hw05.s3.us-west-1.amazonaws.com/ILSVRC2012_img_train.tar
https://w251hw05.s3.us-west-1.amazonaws.com/ILSVRC2012_img_val.tar
https://w251hw05.s3.us-west-1.amazonaws.com/ILSVRC2012_devkit_t12.tar.gz
https://w251hw05.s3.us-west-1.amazonaws.com/cinic.zip

sudo mkdir /data
sudo chmod 777 /data
sudo mkfs -t xfs /dev/nvme1n1
sudo mount /dev/nvme1n1 /data
cd /data
nohup curl https://w251hw05.s3.us-west-1.amazonaws.com/ILSVRC2012_img_train.tar --output ILSVRC2012_img_train.tar &
UUID=098fbe86-b931-4fab-a1b3-c51abcf4a3b3 /data xfs defaults,nofail 0 2
sudo umount /data
sudo mount -a
