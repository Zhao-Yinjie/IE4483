

|                   | Time | Space | Completeness       | Optimality              |
| ----------------- | ---- | ----- | ------------------ | ----------------------- |
| BFS               | b^d  | b^d   | Y                  | Y                       |
| DFS               | b^d  | b*d   | N                  | N                       |
| DFS w Iter Dpng   | b^d  | b*d   | Y                  | Y                       |
| Best First Greedy | b^d  | b^d   | N                  | N                       |
| Best First Astar  | b^d  | b^d   | Y                  | Y                       |
| Minimax           | b^d  | b*d   | Y (if finite tree) | Y (if optimal opponent) |

| Nodes     | Cond1                       | Cond2                       |
| --------- | --------------------------- | --------------------------- |
| Grandpa   | Alpha (Max)                 | Beta (Min)                  |
| Parent    | Beta (Min)                  | Alpha (Max)                 |
| Condition | Alpha >= Beta               | Beta <= Alpha               |
| Action    | Stop searching under Parent | Stop searching under Parent |

**Apriori**: Frequent itemset has frequent subsets, infrequent itemset has infrequent supersets

- Closed Frequent Itemset: all immediate superset have less support
- Maximal Frequent Itemset: no frequent superset

**FP Growth**: remove infrequent, order, then grow the tree; **Conditional Pattern Base**: to go from bottom to top to list all parent path of an item.
$$
Best\ First\ Search\ (greedy)\ f(n) = g(n)+h(n),g(n)=0.\ \ if\ g(n)\ not\ 0, A^*.\\
Support(X \to Y)=\frac{\sigma (X \cup Y)}{|T|}=P(X \cup Y);\ \ Condidence(X \to Y)=\frac{\sigma (X \cup Y)}{\sigma (X)}=\frac{P(X \cup Y)}{P(X)}=P(Y|X); 
\\ Two \ tasks\ in\ ARM: 1. Frequent\ Itemset\ Generation\ 2. Rule\ generation \\
Lift(X,Y)=\frac{Conf(X\to Y)}{Sup(Y)}=\frac{P(Y|X)}{P(Y)}. \ \ (=1 \Rightarrow independent;>1\Rightarrow posi\ corr; <1 \Rightarrow  neg\ corr)
$$

$$
**ID3**\ \ Info(D)=-\sum_{i=1}^{m}p_ilog_2(p_i);\ Info_A(D)=\sum_{j=1}^{v}\frac{|D_j|}{|D|}Info(D_j);\ Gain(A)=Info(D)-Info_A(D)\\
**C4.5** \ \ SplitInfo_A(D) = \sum_{j=1}^{v}\frac{|D_j|}{|D|}Info(\frac{|D_j|}{|D|}); \ GainRatio_A(D)=\frac{Gain(A)}{SplitInfo_A(D)}\\
Gini(D)=a-\sum_{i=1}^2p_i^2; \ \ Gini_A(D)=\sum_{j=1}^{v}\frac{|D_j|}{|D|}Gini(D_j) \\
sensitivity=\frac{TP}{P}; \ \ specificity=\frac{TN}{N}; \ \ precision=\frac{TP}{TP+FP}; \ \ recall= \frac{TN}{TN+FN}\\ 
acc = sensitivity(\frac{P}{P+N})+specificity(\frac{N}{P+N});\ \ F=\frac{2*precision*recall}{precision+recall}
$$

$$
Clustering:
Eulidean\ distance: d(x,y)=\|x-y||_2;\ Manhattan:d(x,y)=||x-y||_1;\ \\
Infinity: max_{1\le j\le d}|x_j-y_j|=lim_{t \to \infin}(\sum_{j=1}^{d}(x_j-y_j)^r)^{\frac{1}{r}} \\
BP: output\ units:\delta_k=\sigma'(net_k)(t_k-o_k); \ hidden\ units:\delta_j=\sigma'(net_j)\sum_k \delta_kw_{kj};\ \Delta b_j = \eta_b \delta_j;\\
Bayes'\ Theorem: P(A|B)=\frac{P(B|A)P(A)}{P(B)} (under\ assumption:P(a_1,...,a_d|v_j)=\Pi_{i=1}^{d}P(a_i|v_j)) \\
PCA: max_{(||V||_2=1)}\frac{1}{N}\sum^{N}_{i-1}(v^Tx_i)^2;\ Singular\ Value\ Decomposition\ A=U\begin{bmatrix} \Sigma \\ 0 \end{bmatrix} V^T,\\
where\ U\ and\ V\ are\ orthogonal\ and\ \Sigma=diag(\sigma_1,..., \sigma_n), \sigma_1>\sigma_2>...>\sigma_n>0
$$

| <img src="C:\Users\Admin\AppData\Roaming\Typora\typora-user-images\image-20221120142849199.png" alt="image-20221120142849199" style="zoom:50%;" /> | <img src="C:\Users\Admin\AppData\Roaming\Typora\typora-user-images\image-20221120143048415.png" alt="image-20221120143048415" style="zoom:50%;" /> |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| <img src="C:\Users\Admin\AppData\Roaming\Typora\typora-user-images\image-20221120144708693.png" alt="image-20221120144708693" style="zoom:50%;" /> | <img src="C:\Users\Admin\AppData\Roaming\Typora\typora-user-images\image-20221120155418391.png" alt="image-20221120155418391" style="zoom:50%;" /> |
| <img src="C:\Users\Admin\AppData\Roaming\Typora\typora-user-images\image-20221120155539843.png" alt="image-20221120155539843" style="zoom:50%;" /> | <img src="C:\Users\Admin\AppData\Roaming\Typora\typora-user-images\image-20221120155756111.png" alt="image-20221120155756111" style="zoom: 50%;" /> |
|                                                              |                                                              |



​								 













