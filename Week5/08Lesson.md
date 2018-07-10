{% include "/header.md" %}

# Lesson Seven - Theme Development

Students Will...
* Start to understand basic theme development

## Key Questions
* What is the common layout of a theme?
* What is the difference between building my own vs customizing a existing theme?
* What is a child theme? and How do I make one?
* What are page templates? 

## Demonstration
* We Will be going over page templates and how the pieces come together.
	* Page templates are broken into sections
		* Header
		* Content(with or without a sidebar)
		* Footer

[wordpress 2012 theme](https://wordpress.org/themes/twentytwelve/)
### Default Page Template

    ```
	<?php
	/**
 	* Template Name: Full-width Page Template, No Sidebar
 	*
	* Description: Twenty Twelve loves the no-sidebar look as much as
	* you do. Use this page template to remove the sidebar from any page.
	*
	* Tip: to remove the sidebar from all posts and pages simply remove
	* any active widgets from the Main Sidebar area, and the sidebar will
	* disappear everywhere.
	*
	* @package WordPress
	* @subpackage Twenty_Twelve
	* @since Twenty Twelve 1.0
	*/
	<!-- wordpress header call-->
	get_header(); ?>

		<div id="primary" class="site-content">
			<div id="content" role="main">
				<!-- The wordpress loop access the database-->
				<?php while ( have_posts() ) : the_post(); ?>
				<!-- The template calls grab the content from the page section->
					<?php get_template_part( 'content', 'page' ); ?>

					<!-- this is the wordpress comments call-->
					<?php comments_template( '', true ); ?>

					<!-- The wordpress loop closes the database-->
				<?php endwhile; // end of the loop. ?>

			</div><!-- #content -->
		</div><!-- #primary -->
	<!-- The Wordpress footer call-->
	<?php get_footer(); ?>



	```


## Widget Area
* What is the widget area and how do I make more?

	```
	<?php
	/**
	* The sidebar containing the main widget area
	*
	* If no active widgets are in the sidebar, hide it completely.
	*
	* @package WordPress
	* @subpackage Twenty_Twelve
	* @since Twenty Twelve 1.0
	*/
	?>

		<?php if ( is_active_sidebar( 'sidebar-1' ) ) : ?>
			<div id="secondary" class="widget-area" role="complementary">
				<?php dynamic_sidebar( 'sidebar-1' ); ?>
			</div><!-- #secondary -->
		<?php endif; ?>
	```



## Functions (The Brains of Your Wordpress Theme)
* How does the functions.php file act as the brain? and how do I control it?
	* It initates your sidebars, menus,comments
	* It can also be used to create admin back end options such as customization and custom post types


	```
	/**
	* Register sidebars.
	*
	* Registers our main widget area and the front page widget areas.
	*
	* @since Twenty Twelve 1.0
	*/
	function twentytwelve_widgets_init() {
		register_sidebar( array(
		'name' => __( 'Main Sidebar', 'twentytwelve' ),
		'id' => 'sidebar-1',
		'description' => __( 'Appears on posts and pages except the optional Front Page template, which has its own widgets', 'twentytwelve' ),
		'before_widget' => '<aside id="%1$s" class="widget %2$s">',
		'after_widget' => '</aside>',
		'before_title' => '<h3 class="widget-title">',
		'after_title' => '</h3>',
	) );
	}
	```





## Plugins 
* Plugins can help accent a theme and help cut down development time
* Some of my Favorite Go To Plugins
	1. Yoast SEO
	2. Page builder by site origin
	3. wp migrate DB
	4. rollback 
	5. wordfence 
	6. smush it
	7. google analytics 


## Tips For Building a Wordpress Theme
* Not Everything needs to be full custom
* Learn The Theme First
* Build Small Risk Small
* Drawing it can help people visualize

## Project for Next Class
* Change the 2012 theme layout and colors without using ANY interior editor only from the CSS main theme files

## Resources
* [WP Theme Codex](https://codex.wordpress.org/Theme_Development)
* [Smashing Magazine](https://www.smashingmagazine.com/)
   

{% include "/footer.md" %}
