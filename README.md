# Economic activities census on the ground floor of Barcelona

## Exploratory Data Analysis

### Dataset reference:
https://opendata-ajuntament.barcelona.cat/data/en/dataset/cens-activitats-comercials

Dataset includes data from 3 different years: 2014, 2016, and 2019.

However, according to the reference:

"El fitxer del 2014 està creat amb diferent metodologia que el del 2016, això fa que les dades no siguin comparables. El cens 2019 és una evolució del cens 2016 i ambdues bases de dades són comparables. (...)"

Data from 2014 is not comparable to 2016 and 2019; only 2016 and 2019 datasets were used.

Author: Bruna Correa

### Build docker image to run the notebook

```
docker build -t bcn_eco_ground_img .
```

### Run notebook server in docker

```bash
docker run -it --rm \
    -p 8888:8888 \
    -v $(pwd)/notebooks:/home/jovyan/notebooks \
    -v $(pwd)/data:/data/ \
    bcn_eco_ground_img \
    jupyter notebook --notebook-dir /home/jovyan/notebooks
```

### Download 2019 and 2016 .csv data from:

https://opendata-ajuntament.barcelona.cat/data/en/dataset/cens-activitats-comercials

And move the files to the '/data' directory.
