# STCN_evaluation

STCN (Space Time Correspondence Network) is simpler, more efficient and faster than STM (Space-Time Network), which was introduced in 2019. 
<br /> Figure shows the architecture of STCN. %A new video frame named query and memory will pass through a key encoder and provide key data.
<br />Each new video frame, also named query, passes through a key encoder to construct an affinity matrix between the query and the memory keys.
<br />This affinity matrix, based on the negative L2 distance, captures the correspondences between objects.
<br />STCN uses only one affinity matrix to gain memory and computation efficiency unlike STM. For encoders, STCN has a lighter network than STM.
<br />At the final stage of decoding, STCN generates the new masks. 
<br />Also, it does not need the last frame key and values unlike STM and only depends on the affinity matrix. Thus, it allows to have a better memory efficiency. 

![image](https://user-images.githubusercontent.com/80272042/151388126-7b74983e-a117-4139-9599-d62f4873f9f5.png)


## tasks definitions

* The **first** task of the project is to replicate some of the results from the paper at the inference time,by using authors’ implementation.
* The **second** task of the project is to verify performance on Something-Something dataset which was not used in original paper.
* The **final** task is to use one of the existing image segmentation approaches for the initialization of the video segmentation method and compare it to manual annotation results. In this part we tested with Mask-RCNN, Detectron 2 PointRend and LOST+CRF methods

## results
![Alt Text](https://ibb.co/F68KwWw"><img src="https://i.ibb.co/H7GVz2z/bmx-trees.gif)

#References
