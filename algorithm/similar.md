# Similarity

### Overview
* [wikipedia/Category:Similarity](
  https://en.wikipedia.org/wiki/Category:Similarity_and_distance_measures)

### List
* Jaccard
  + Classical Jaccard
    $$
      J(A,B)
      = \frac{|A \cap B|}
        {|A \cup B|}
    $$
  + Considering voter's weight
    $$
      Sim(I_i,I_j)
      = \frac{ \sum_{u \in U(I_i) \cap U(I_j)} W_u }
        {|U(I_i) \cup U(I_j)|}
    $$
    1. if voter's weight is equal
      $$
        W_u = 1
      $$
    2. vote more, weight less
      $$
        W_u = \frac{1}{N(u)^\alpha}
      $$
* Cosine similarity
  + Classical Cosine
    $$
      \text{similarity}
      = \cos(\theta)
      = { \mathbf{A} \cdot \mathbf{B}
        \over \|\mathbf{A}\| \|\mathbf{B}\| }
      = \frac{ \sum\limits_{i=1}^{n} {A_i B_i} }
        { \sqrt{ \sum\limits_{i=1}^{n} {A_i^2} }
          \sqrt{ \sum\limits_{i=1}^{n} {B_i^2} } }
    $$
  + Considering voter's weight
    $$
      Sim(I_i,I_j)
      = \frac{ \sum_{u \in U(I_i) \cap U(I_j)} W_u^2}
        { \sqrt{ \sum_{u \in U(I_i)} {W_u^2} }
          \sqrt{ \sum_{u \in U(I_j)} {W_u^2} } }
    $$
    1. if voter's weight is equal:
    $$
      W_u = 1
    $$
    2. vote more, weight less
    $$
      W_u = \frac{1}{log_2(3+N(u))}
      \quad or \quad
      W_u = \frac{1}{N(u)^\alpha}
    $$
* Adamic/Adar index
  + Classical Adamic
    $$
    A(x,y) = \sum_{u \in N(x) \cap N(y)} \frac{1}{\log{|N(u)|}}
    $$
