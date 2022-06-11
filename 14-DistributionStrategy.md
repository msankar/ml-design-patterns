Training loop is carried out at scale over multiple workers, often with caching, hardware acceleration and parallelization.
data parellelism 
- synhchronous training - workers train on diff data slices in parallel and gradient values are aggregated at the end of each training step. (all-reduce), tf.distribute.MirroredStrategy/MultiWorkerStrategy, DistributedDataParallel in pytorch
- asynch training - workers train on different data slices, model weights and parameters are updated asynchronously through parameter server architecture. Keras ParameterServerStrategy

model parallelism
- Each server operates over same mini-batch of data during training but carries out computations related only to their separate components of the model.
- low latency, use when amount of computation per neuron activity is high
- ASIC (app-specific integrated circuits) TPU, FPGA

Batch size
Server I/O costs minimize by overlapping data fetch and model execution.
