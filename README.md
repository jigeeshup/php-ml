# PHP-ML - Machine Learning library for PHP

[![Build Status](https://scrutinizer-ci.com/g/php-ai/php-ml/badges/build.png?b=develop)](https://scrutinizer-ci.com/g/php-ai/php-ml/build-status/develop)
[![Documentation Status](https://readthedocs.org/projects/php-ml/badge/?version=develop)](http://php-ml.readthedocs.org/en/develop/?badge=develop)
[![Total Downloads](https://poser.pugx.org/php-ai/php-ml/downloads.svg)](https://packagist.org/packages/php-ai/php-ml)
[![License](https://poser.pugx.org/php-ai/php-ml/license.svg)](https://packagist.org/packages/php-ai/php-ml)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/php-ai/php-ml/badges/quality-score.png?b=develop)](https://scrutinizer-ci.com/g/php-ai/php-ml/?branch=develop)

Fresh approach to Machine Learning in PHP. Algorithms, Cross Validation, Preprocessing, Feature Extraction and much more in one library.

Simple example of classification:
```php
use Phpml\Classification\KNearestNeighbors;

$samples = [[1, 3], [1, 4], [2, 4], [3, 1], [4, 1], [4, 2]];
$labels = ['a', 'a', 'a', 'b', 'b', 'b'];

$classifier = new KNearestNeighbors();
$classifier->train($samples, $labels);

$classifier->predict([3, 2]); 
// return 'b'
```

## Documentation

To find out how to use PHP-ML follow [Documentation](http://php-ml.readthedocs.org/).

## Installation

Currently this library is in the process of developing, but You can install it with Composer:

```
composer require php-ai/php-ml
```

## Features

* Classification
    * [SVC](http://php-ml.readthedocs.io/en/latest/machine-learning/classification/svc/)
    * [k-Nearest Neighbors](http://php-ml.readthedocs.io/en/latest/machine-learning/classification/k-nearest-neighbors/)
    * [Naive Bayes](http://php-ml.readthedocs.io/en/latest/machine-learning/classification/naive-bayes/)
* Regression
    * [Least Squares](http://php-ml.readthedocs.io/en/latest/machine-learning/regression/least-squares/)
    * [SVR](http://php-ml.readthedocs.io/en/latest/machine-learning/regression/svr/)
* Clustering
    * [k-Means](http://php-ml.readthedocs.io/en/latest/machine-learning/clustering/k-means/)
    * [DBSCAN](http://php-ml.readthedocs.io/en/latest/machine-learning/clustering/dbscan/)
* Metric
    * [Accuracy](http://php-ml.readthedocs.io/en/latest/machine-learning/metric/accuracy/)
    * [Confusion Matrix](http://php-ml.readthedocs.io/en/latest/machine-learning/metric/confusion-matrix/)
* Workflow
    * [Pipeline](http://php-ml.readthedocs.io/en/latest/machine-learning/workflow/pipeline)
* Cross Validation
    * [Random Split](http://php-ml.readthedocs.io/en/latest/machine-learning/cross-validation/random-split/)
    * [Stratified Random Split](http://php-ml.readthedocs.io/en/latest/machine-learning/cross-validation/stratified-random-split/)
* Preprocessing
    * [Normalization](http://php-ml.readthedocs.io/en/latest/machine-learning/preprocessing/normalization/)
    * [Imputation missing values](http://php-ml.readthedocs.io/en/latest/machine-learning/preprocessing/imputation-missing-values/)
* Feature Extraction
    * [Token Count Vectorizer](http://php-ml.readthedocs.io/en/latest/machine-learning/feature-extraction/token-count-vectorizer/)
    * [Tf-idf Transformer](http://php-ml.readthedocs.io/en/latest/machine-learning/feature-extraction/tf-idf-transformer/)
* Datasets
    * [CSV](http://php-ml.readthedocs.io/en/latest/machine-learning/datasets/csv-dataset/)
    * Ready to use:
        * [Iris](http://php-ml.readthedocs.io/en/latest/machine-learning/datasets/demo/iris/)
        * [Wine](http://php-ml.readthedocs.io/en/latest/machine-learning/datasets/demo/wine/)
        * [Glass](http://php-ml.readthedocs.io/en/latest/machine-learning/datasets/demo/glass/)
* Math
    * [Distance](http://php-ml.readthedocs.io/en/latest/math/distance/)
    * [Matrix](http://php-ml.readthedocs.io/en/latest/math/matrix/)
    * [Statistic](http://php-ml.readthedocs.io/en/latest/math/statistic/)
    

## Contribute

- Issue Tracker: github.com/php-ai/php-ml/issues
- Source Code: github.com/php-ai/php-ml

After installation, you can launch the test suite in project root directory (you will need to install dev requirements with Composer)

```
bin/phpunit
```

## License

PHP-ML is released under the MIT Licence. See the bundled LICENSE file for details.

## Author

Arkadiusz Kondas (@ArkadiuszKondas)
