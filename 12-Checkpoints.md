Store the full state of model periodically so that we have partially trained models available.
These partially trained models can serve as the final model for early stopping or as starting points for continued training

Checkpointing saves the full model state at the end of every epoch. Keras provides a callback in fit()

* Early stopping - stop when valdation error goes up.
* Checkpoint selection
* Regularization
* Two splits
* Fine-tuning - Resume from a checkpoint from before the training loss starts to plateau and train on fresh data
* Redefining an epoch
** Steps per epoch
** Retraining with more data
** Virtual epochs

