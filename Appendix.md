# TemPEST
Supplementary material of TemPEST: Soft TEMplate Based Personalized EDM Subject Generation Through Collaborative Summarization.

## Data Distribution
Figure below shows the distributions of click-through number frequencies on *KKday* dataset. We can observe that it is long-tailed. This poses a great challenge to the recommender model, as it needs to be powerful enough to deal with both the head users/items (sparse) and trail user/items (active).

![Distributions of click-through frequencies.](https://i.imgur.com/CWgdAFC.png)


## Ablation studies
The results of each sub-task with and without joint modeling are listed below. The results manifest that joint modeling does improve the performance for both tasks since one of the advantages of our proposed model is the capability of contributing to the two sub-tasks with the fused representation.

Subject Generation:

|Joint Modeling|B-1|B-2|B-3|B-4|R-1|R-L|
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
|w/ |24.36|5.31|3.15|1.97|65.47|8.33|
|w/o|22.92|4.82|2.82|1.76|62.14|6.15|

Recommendation:

|Joint Modeling|Recall@10|NDCG@10|
|:--:|:--:|:--:|
|w/ |0.1921|0.0632|
|w/o|0.1871|0.0619|



## Case Study

Table below shows another case study of the personalized subject generation task. Similar to the previous one in Table 7. The sample generated from BiSET looks similar to its template in structure and vocabularies. While different users get different outcomes of styles and words especially place names in this case. As we can see, for example, user 1's sample is a smoother and shorter, meanwhile user 2's one includes "one day tour" as a key component. Both user 1 and 2 tend to be more informative. On the contrary, user 3's sample also includes "Must-Visit" which indicating a stronger style. 

![](https://i.imgur.com/oGrr0xc.jpg)


We also visualize the effects of different input templates as shown in Table below. We mark the output words that repeat the words in template bold. We observe that with the bi-directional selective mechanism, the generated subjects alter based on the template it is conditioned on. The output not only copies the words from templates but also learns the relative locations. Besides, even if the template occurs some undesired location names, the generated subjects are still able to replace them with the ones that appear in the given article. 

 ![](https://i.imgur.com/87g9O5k.jpg)
