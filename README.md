#replacing  BasicBlock of DLA34 to CSP (Cross stage partial connections) </br>
steps of the notebook: </br>
*. no pretrain of both models for fair comparation </br>
*. as limit of GPU time, only train three cataloges of COCO dataset (car, bus,truck)  </br>
*. model = DLA([1, 1, 1, 2, 2, 1],[16, 32, 64, 128, 256, 512], block=BasicBlock, **kwargs)   #original   dla34 model </br>
*. model = DLA([1, 1, 1, 2, 2, 1],[16, 32, 64, 128, 256, 512], block=C3, **kwargs) # change BasicBlock to CSP   </br> </br>

 question:why mAP drop 20%?
