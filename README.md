
### Filtering the unbox message.

There is a `apply_fitlers` for the `'unbox_message'`, this let's you overwrite the second paragraph's content. The documentation & support link will be `sprintf`'d into place, so make sure you include the `%1$s` & `%2$s` flags - [read more about sprintf](http://php.net/manual/en/function.sprintf.php).

Here is an example of how to use the filter:
`
add_filter('unbox_message', 'my_theme_unbox_message');
function my_theme_unbox_message ($msg) {
	$permalinks_page_url = admin_url( 'options-permalink.php' );
	return 'Let\'s get started! First, read your <a target="_blank" href="%1$s">theme\'s documentation</a>, then <a href="' . $permalinks_page_url . '">update your permalinks</a>. If you have any questions, please <a target="_blank" href="%2$s">contact us</a> for help.';
}
`

