# Similarity

### Overview
* [wikipedia/Category:Similarity](https://en.wikipedia.org/wiki/Category:Similarity_and_distance_measures)

### 公式
* Jaccard
  + Classical Jaccard:
    $$
    J(A,B) = \frac{|A \cap B|}{|A \cup B|}
    $$
* Cosine similarity
  + Classical Cosine：
    $$
    \text{similarity}
    = \cos(\theta)
    = {\mathbf{A} \cdot \mathbf{B} \over \|\mathbf{A}\| \|\mathbf{B}\|}
    = \frac{ \sum\limits_{i=1}^{n}{A_i B_i} }
      { \sqrt{\sum\limits_{i=1}^{n}{A_i^2}} \sqrt{\sum\limits_{i=1}^{n}{B_i^2}} }
    $$
  + Treat voter equally：
    $$
    Sim(I_i,I_j)
    = \frac{U(I_i)\cap U(I_j)}
    {\sqrt{\left | U(I_i) \right |}\sqrt{\left | U(I_j) \right |}}
    $$
