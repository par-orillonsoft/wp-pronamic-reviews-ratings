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


## Other WordPress Reviews and Ratings solutions

*	[Rating-Widget](http://wordpress.org/plugins/rating-widget/)
*	[WP-PostRatings](http://wordpress.org/plugins/wp-postratings/)
*	[Multi Rating](http://wordpress.org/plugins/multi-rating/)
*	[WordPress Comment Rating Plugin](http://codecanyon.net/item/wordpress-comment-rating-plugin/6582710)
*	[kk Star Ratings](http://wordpress.org/plugins/kk-star-ratings/)
*	[10+ Useful WordPress Rating Plugins](http://www.tripwiremagazine.com/2012/10/wordpress-rating-plugins.html)

