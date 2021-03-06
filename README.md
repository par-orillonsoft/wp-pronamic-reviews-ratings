# [Pronamic Reviews and Ratings](http://www.happywp.com/plugins/pronamic-reviews-ratings/)

The Pronamic Reviews Ratings plugin for WordPress is a powerful, extendable reviews and ratings plugin.


## Register Rating Type

```php
<?php

function prefix_reviews_ratings_init() {
	pronamic_register_rating_type( 'trustworthy', __( 'Trustworthy', 'text_domain' ) );
	pronamic_register_rating_type( 'objective', __( 'Objective', 'text_domain' ) );
	pronamic_register_rating_type( 'complete', __( 'Complete', 'text_domain' ) );
	pronamic_register_rating_type( 'well_written', __( 'Well-written', 'text_domain' ) );
}

add_action( 'pronamic_reviews_ratings_init', 'prefix_reviews_ratings_init' );

```


## Post Type Support

```php
<?php

function prefix_reviews_ratings_init() {
	add_post_type_support( 'page', 'pronamic_ratings' );
}

add_action( 'pronamic_reviews_ratings_init', 'prefix_reviews_ratings_init' );

```


## Post Type Rating Types Support

```php
<?php

function prefix_init() {
	register_post_type( 'book', array(
		'public'                => true,
		'label'                 => __( 'Books', 'text_domain' ),
		'pronamic_rating_types' => array(
			'trustworthy',
			'objective',
			'complete',
			'well_written',
		),
	) );

	register_post_type( 'magazine', array(
		'public'                => true,
		'label'                 => __( 'Magazines', 'text_domain' ),
		'pronamic_rating_types' => array(
			'trustworthy',
			'well_written',
		),
	) );
}

add_action( 'init', 'prefix_init' );

```


## Reviews Ratings Scores

```php
<?php

function prefix_pronamic_reviews_ratings_scores( $scores ) {
	$scores = array( 10, 8, 6, 4, 2 );

	return $scores;
}

add_filter( 'pronamic_reviews_ratings_scores', 'prefix_pronamic_reviews_ratings_scores' );

```


## Metadata

All the rating values are stored as meta data with the [WordPress metadata API](http://codex.wordpress.org/Metadata_API).

```
_pronamic_rating_value_$name
_pronamic_rating_count_$name
```


## Schema.org

*	http://schema.org/reviews
*	http://schema.org/Review
*	http://schema.org/Rating
*	http://schema.org/AggregateRating


## Tools for testing Schema.org markup

*	[Google Structured Data Testing Tool](http://www.google.nl/webmasters/tools/richsnippets)
*	[Structured Data Linter](http://linter.structured-data.org/)
*	[Stack Overflow question - Tool for testing Schema.org markup](http://stackoverflow.com/q/6496114)
	

## WooCommerce Reviews and Ratings solution

*	https://github.com/woothemes/woocommerce/blob/v2.1.6/includes/class-wc-comments.php
*	https://github.com/woothemes/woocommerce/blob/v2.1.6/templates/single-product-reviews.php#L52


## Other WordPress Reviews and Ratings solutions

*	[Rating-Widget](http://wordpress.org/plugins/rating-widget/)
*	[WP-PostRatings](http://wordpress.org/plugins/wp-postratings/)
*	[Multi Rating](http://wordpress.org/plugins/multi-rating/)
*	[WordPress Comment Rating Plugin](http://codecanyon.net/item/wordpress-comment-rating-plugin/6582710)
*	[kk Star Ratings](http://wordpress.org/plugins/kk-star-ratings/)
*	[10+ Useful WordPress Rating Plugins](http://www.tripwiremagazine.com/2012/10/wordpress-rating-plugins.html)
*	[Adding Custom Fields In WordPress’ Comment Form](http://wp.smashingmagazine.com/2012/05/08/adding-custom-fields-in-wordpress-comment-form/)

## JavaScript solutions

*	[jQuery Raty - A Star Rating Plugin](http://wbotelhos.com/raty)
*	[RateIt - a jQuery (star) rating plugin](http://rateit.codeplex.com/)
