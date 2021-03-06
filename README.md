# A Discriminatively Learned CNN Embedding for Person Re-identification

In this package, we provide our training and testing code for the paper [A Discriminatively Learned CNN Embedding for Person Re-identification] (https://arxiv.org/abs/1611.05666).
 
We also include matconvnet-beta23 modified for our paper. All codes have been test on Ubuntu14.04 with Matlab R2015b.

* [Xuanyi Dong](https://github.com/D-X-Y) also realize our paper in [Caffe](https://github.com/D-X-Y/caffe-reid).

![](https://github.com/layumi/2016_person_re-ID/blob/master/dis2016.jpg)
#Dataset
Market1501 (You can find it on https://liangzheng.org)

#To test
1. Use `start-zzd.sh` to start matlab. (You need to add your CUDA path in it. Then just type `./start-zzd.sh` to run it.)

2. Compile matconvnet. (You just need to uncomment and modify some lines in `gpu_compile.m` and run it. Try it~)
If you fail in compilation, you may refer to http://www.vlfeat.org/matconvnet/install/

3. After compilation, run `test2/test_gallery_res.m` to extract the features of gallery. They will store in a .mat file. You can use it to do evaluation.
(For example, you may modify the [Market1501 baseline code](http://www.liangzheng.org/Project/project_reid.html) to evaluate our model. It may take a while.)

#To train
1. Compile matconvnet. If you fail in compilation, you can refer to http://www.vlfeat.org/matconvnet/install/

2. Add your dataset path into `prepare_data.m` and run it. Make sure the code outputs the right image path.

3. Run `train_id_net_res_2stream.m` to have fun.

#Thanks
Thanks for Xuanyi Dong to realize our paper in Caffe.

Thanks for Weihang Chen to report the bug in `prepare_data.m`.