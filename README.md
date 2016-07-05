ChartJs Widget
==============

[![Latest Version](https://img.shields.io/github/tag/piotrmus/yii2-chartjs2-widget.svg?style=flat-square&label=release)](https://github.com/piotrmus/yii2-chartjs2-widget/tags)
[![Software License](https://img.shields.io/badge/license-BSD-brightgreen.svg?style=flat-square)](LICENSE.md)
[![Total Downloads](https://img.shields.io/packagist/dt/piotrmus/yii2-chartjs2-widget.svg?style=flat-square)](https://packagist.org/packages/piotrmus/yii2-chartjs2-widget)

Renders a [ChartJs plugin](http://www.chartjs.org/docs/) widget

Installation
------------

Run

```
composer require piotrmus/yii2-chartjs2-widget:~1.0
```
or add

```json
"piotrmus/yii2-chartjs2-widget" : "~1.0"
```

to the require section of your application's `composer.json` file.

Usage
-----

```php
use piotrmus\chartjs\ChartJs2;

<?= ChartJs2::widget([
    'type' => 'bar',
    'data' => [
        'labels' => ["Red", "Blue", "Yellow", "Green", "Purple", "Orange"],
        'datasets' => [
            [
                'label' => '# of Votes',
                'data' => [12, 19, 3, 5, 2, 3],
                'backgroundColor' => [
                    'rgba(255, 99, 132, 0.2)',
                    'rgba(54, 162, 235, 0.2)',
                    'rgba(255, 206, 86, 0.2)',
                    'rgba(75, 192, 192, 0.2)',
                    'rgba(153, 102, 255, 0.2)',
                    'rgba(255, 159, 64, 0.2)'
                ],
                'borderColor' => [
                    'rgba(255,99,132,1)',
                    'rgba(54, 162, 235, 1)',
                    'rgba(255, 206, 86, 1)',
                    'rgba(75, 192, 192, 1)',
                    'rgba(153, 102, 255, 1)',
                    'rgba(255, 159, 64, 1)'
                ],
                'borderWidth' => 1,
            ]
        ]
    ],
    'options' => [
        'id' => 'test',
        'width' => 100,
        'height' => 50
    ],
    'chartOptions' => [
        'scales' => [
            'yAxes' => [
                [
                    'ticks' => [
                        'beginAtZero' => true
                    ]
                ]]
        ]
    ],
]) ?>
```
