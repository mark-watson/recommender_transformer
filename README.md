# recommender_transformer

## Mark Watson's notes:

I cloned this repo by Mansar Youness to experiment with on my home GPU rig. Please see his original work at:

- https://github.com/CVxTz/recommender_transformer
- https://towardsdatascience.com/build-your-own-movie-recommender-system-using-bert4rec-92e4e34938c5

I use alternative recommendation model types at my job. In my own time I want to experiment with Transformer recommendation systems to see if they may be viable at work.

Run (just 2 epochs to see if things are setup correctly):

    python recommender/training.py --data_csv_path ml-25m/ratings.csv --epochs 2

Blog : https://towardsdatascience.com/build-your-own-movie-recommender-system-using-bert4rec-92e4e34938c5 

## Mansar Youness's blog article

Blog : https://towardsdatascience.com/build-your-own-movie-recommender-system-using-bert4rec-92e4e34938c5 

### Setup (GPU)
```
conda create -n py38 python=3.8
conda activate py38
conda install pytorch torchvision cudatoolkit=11.1 -c pytorch -c conda-forge
conda install -c conda-forge jupyterlab
conda install -c conda-forge matplotlib
git clone https://github.com/CVxTz/recommender_transformer
cd recommender_transformer
pip install .
```
### Docker (CPU)
```bash
docker build . -t recommender
docker run recommender sh -c "python3.8 -m pytest"
```

### References

[BERT4Rec: Sequential Recommendation with Bidirectional
Encoder Representations from Transformer](https://arxiv.org/abs/1904.06690)
