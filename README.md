# STCN_evaluation

STCN (Space Time Correspondence Network) is simpler, more efficient and faster than STM (Space-Time Network), which was introduced in 2019. 
<br /> **Figure 1** shows the architecture of STCN. A new video frame named query and memory will pass through a key encoder and provide key data.
Each new video frame, also named query, passes through a key encoder to construct an affinity matrix between the query and the memory keys.
<br />The affinity matrix, based on the negative L2 distance, captures the correspondences between objects.
<br />STCN uses only one affinity matrix to gain memory and computation efficiency unlike STM. For encoders, STCN has a lighter network than STM.
At the final stage of decoding, STCN generates the new masks. 
Also, it does not need the last frame key and values unlike STM and only depends on the affinity matrix. Thus, it allows to have a better memory efficiency. 

![image](https://user-images.githubusercontent.com/80272042/151395512-eb7bc0e2-0431-4f75-9bbc-0baff08fe4c8.png)



## tasks definitions

* The **first** task of the project is to replicate some of the results from the paper at the inference time,by using authors’ implementation.
* The **second** task of the project is to verify performance on Something-Something dataset which was not used in original paper.
* The **final** task is to use one of the existing image segmentation approaches for the initialization of the video segmentation method and compare it to manual annotation results. In this part we tested with Mask-RCNN, Detectron 2 PointRend and LOST+CRF methods

## results

* LOST + CRF
<br />![Alt Text](https://media.giphy.com/media/UsPALjbeJwppExZ9T6/giphy.gif)

* Mask R-CNN
<br />![Alt Text](https://media.giphy.com/media/lDBj61kILs19YEwHbd/giphy.gif)

* Pointrend
<br />![Alt Text](https://media.giphy.com/media/JYdMfSmUeLXSdiZJ5h/giphy.gif)


## References
<br />[1] https://hkchengrex.github.io/STCN/
<br />[2] https://github.com/joaanna/something_else
<br />[3] https://github.com/matterport/Mask_RCNN
<br />[4] https://github.com/facebookresearch/detectron2/tree/main/projects/PointRend
<br />[5] https://github.com/valeoai/LOST
<br />[6] https://github.com/lucasb-eyer/pydensecrf
<br />[7] https://github.com/davisvideochallenge/davis2017-evaluation
<br />[8] M.  Caron,  H.  Touvron,  I.  Misra,  H.  J ́egou,  J.  Mairal,  P.  Bo-janowski, and A. Joulin.  Emerging properties in self-supervisedvision transformers.arXiv preprint arXiv:2104.14294, 2021.
<br />[9] H. K. Cheng, Y.-W. Tai, and C.-K. Tang.  Rethinking space-timenetworks with improved memory coverage for efficient video ob-ject segmentation. InNeurIPS, 2021.
<br />[10] R.   Goyal,   S.   Ebrahimi   Kahou,   V.   Michalski,   J.   Materzyn-ska,  S.  Westphal,  H.  Kim,  V.  Haenel,  I.  Fruend,  P.  Yianilos,M.  Mueller-Freitag,  et  al.The  ”something  something”  videodatabase for learning and evaluating visual common sense. InPro-ceedings of the IEEE international conference on computer vision,pages 5842–5850, 2017.
<br />[11] K. He, G. Gkioxari, P. Doll ́ar, and R. Girshick.  Mask r-cnn.  InProceedings  of  the  IEEE  international  conference  on  computervision, pages 2961–2969, 2017.
<br />[12] A. Kirillov,  Y. Wu,  K. He,  and R. Girshick.   Pointrend:  Imagesegmentation as rendering. InProceedings of the IEEE/CVF con-ference on computer vision and pattern recognition, pages 9799–9808, 2020.
<br />[13] P.  Kr ̈ahenb ̈uhl  and  V.  Koltun.   Efficient  inference  in  fully  con-nected crfs with gaussian edge potentials.Advances in neural in-formation processing systems, 24:109–117, 2011.
<br />[14] J. Materzynska, T. Xiao, R. Herzig, H. Xu, X. Wang, and T. Dar-rell.Something-else:   Compositional  action  recognition  withspatial-temporal  interaction  networks.InProceedings  of  theIEEE/CVF Conference on Computer Vision and Pattern Recog-nition, pages 1049–1059, 2020.
<br />[15] S. W. Oh, J.-Y. Lee, N. Xu, and S. J. Kim.  Video object segmen-tation using space-time memory networks.  InProceedings of theIEEE/CVF International Conference on Computer Vision, pages9226–9235, 2019.
<br />[16] O.  Sim ́eoni,  G.  Puy,  H.  V.  Vo,  S.  Roburin,  S.  Gidaris,  A.  Bur-suc,  P.  P ́erez,  R.  Marlet,  and  J.  Ponce.Localizing  objectswith self-supervised transformers and no labels.arXiv preprintarXiv:2109.14279, 2021.
