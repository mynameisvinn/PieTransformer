# attention is all we need
simplest example of attention.

## what does the data look like?
we generate {X, y} from scratch. $X$ is a ndim array of features. $y$ is the corresponding target, and equals XOR of $X_1$ and $X_2$ (ie $y$ is true if either $X_1$ or $X_2$ is true, otherwise it is false). all other features in $X$ is random uniform noise.

## which features should we attend to?
since $y$ is XOR of $X_1$ and $X_2$, we would expect the attention vector to attend to both $X_1$ and $X_2$. (knowing either $X_1$ and $X_2$ is insufficient.)

moreover, since all other features in $X$ is random noise - and therefore are uninformative features - we would expect attention vector to ignore all other features.