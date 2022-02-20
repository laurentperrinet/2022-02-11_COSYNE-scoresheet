# Crowd-sourcing raw scores for your COSYNE reviewer feedback

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/laurentperrinet/2022-02-11_COSYNE-scoresheet/main?labpath=2022-02-11_COSYNE-scoresheet.ipynb)

Following that message:

> Dear community, 

> COSYNE is a great conference which plays a pivotal role in our field. If you have submitted an abstract (or several) you have recently received your scores. I am not affiliated to COSYNE - yet willing to contribute in some way: I would like to ask one minute of your time to report the raw scores from your reviewers. I will summarize in a few lines the results in one week time (11/02). The more numerous your feedbacks the better their precision!

> Thanks!

As of 2022-02-20, I had received $N = 98$ answers from the [google form](https://forms.gle/hjzWVemM4Jy9cBbZ9) (out of them, $95$ are valid) out of the $881$ submitted abstracts. In short, the result is that the total score $S$ is simply the linear sum of the scores $s_i$ given by each reviewer $i$ relatively weighted by the confidence levels $\pi_i$ (as stated in the email we received from the chairs):

$$
S = \frac{ \sum_i \pi_i\cdot s_i}{\sum_i \pi_i}
$$

Or if you prefer
$$
S = \sum_i  \frac{\pi_i}{\sum_j \pi_j} \cdot s_i
$$

We deduce from that formula that the threshold is close to $6.34$ this year:

![2022-02-11_COSYNE-razor](https://github.com/laurentperrinet/2022-02-11_COSYNE-scoresheet/raw/main/2022-02-11_COSYNE-razor.png)

More details in the [notebook](https://github.com/laurentperrinet/2022-02-11_COSYNE-scoresheet/blob/main/2022-02-11_COSYNE-scoresheet.ipynb) (or directly in this [post](https://laurentperrinet.github.io/sciblog/posts/2022-02-11-cosyne-reviewer-feedback.html)) which can also be [forked here](https://github.com/laurentperrinet/2022-02-11_COSYNE-scoresheet) and [interactively modified on binder](https://mybinder.org/v2/gh/laurentperrinet/2022-02-11_COSYNE-scoresheet/main?labpath=2022-02-11_COSYNE-scoresheet.ipynb).

EDIT: On 2022-02-20, I have updated the notebook to account for new answers, I have now received $N = 98$ answers (out of them, $95$ are valid), yet nothing changed qualitatively. On 2022-02-11, I had received $N = 82$ answers from the [google form](https://forms.gle/hjzWVemM4Jy9cBbZ9) (out of them, $79$ are valid) and the estimated threshold wass close to $6.05$.
