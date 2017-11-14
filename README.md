# wordpress-tips-najm

### 1- get all post meta to special post type
```
  echo $meta = get_post_meta( 8000 );
  print_r($meta);
  ```
  
### 2- select for special wp-query
```
$args = array(
    'post_type' => 'pixad-autos',
    'meta_key'       => '_auto_stock_status',
    'posts_per_page' => -1,
    'order' => 'DESC',
    'meta_query' => array(
        'key' => '_auto_stock_status',
        'value' => 'out of stock',
        'compare' => '='
    )

);
$filtredOutOfStock = new WP_Query($args);
```

### 3-get all post type for post type
```
foreach ( get_post_types( '', 'names' ) as $post_type ) {
   echo '<p>' . $post_type . '</p>';
}
```

