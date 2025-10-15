# Stock Markov Predictor
Predicts short-term stock movement bins using an order-k Markov chain trained on discretized daily returns.


## What the code does

Builds a Markov model from binned daily changes (markov_chain), storing a probability distribution of the next bin for every length-k history.

Samples next states from those distributions (weight_number).

Forecasts future bins given the last k bins (predict), with a simple random fallback for unseen histories.

Evaluates predictions using mean-squared error (mse).

Runs experiments over different orders and averages stochastic error across trials (run_experiment).

Demo pipeline (run): loads data, bins changes, plots, and tests orders [1,3,5,7,9].
