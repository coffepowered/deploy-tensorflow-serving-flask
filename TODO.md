
# TODO 

- [ ] deploy a custom model locally
- [ ] check [tf bridge on heroku elements](https://elements.heroku.com/buttons/heroku/tf-bridge)
- [ ] deploy to heroku as a test


# Study notes
The tutorial is heavily based on [Tensorflow Serving with Docker](https://www.tensorflow.org/tfx/serving/docker) official guide. 
In the tf serving tutorial, `docker run` is made as follows:

``` 
docker run -t --rm -p 8501:8501 \
    -v "$TESTDATA/saved_model_half_plus_two_cpu:/models/half_plus_two" \
    -e MODEL_NAME=half_plus_two \
    tensorflow/serving &
```

What seems to be new here is that there is a `model.py`

## Questions
* Why this was not fully done with tf serving [RESTful API](https://www.tensorflow.org/tfx/serving/api_rest)?
* Why is preprocessing made inside `model.py` ?!
* Go deeper on [gRPC API](https://grpc.io/docs/languages/python/quickstart/)
