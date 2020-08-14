# Markets Laravel Admin Panel

## Important Links

[Server Requirements](https://support.smartersvision.com/help-center/articles/7/9/3/introduction).

[How to Update to last version?](https://support.smartersvision.com/help-center/articles/7/9/11/update).

[FAQ](https://support.smartersvision.com/help-center/categories/8/laravel-application-faq).

# API DOCUMENTATION

## Fetch Markets:GET

#### End Point: http://127.0.0.1:8000/api/markets

## Fetch Products: GET

#### End Point: http://127.0.0.1:8000/api/products

## Fetch Currencies: GET

#### End Point: http://127.0.0.1:8000/api/currencies

## Fetch Fields: GET

#### End Point: http://127.0.0.1:8000/api/currencies

## Fetch Categories: GET

#### End Point: http://127.0.0.1:8000/api/categories

## Fetch Settings: GET

#### End Point: http://127.0.0.1:8000/api/settings

## Fetch Settings: GET

#### End Point: http://127.0.0.1:8000/api/settings

##### Route::prefix('driver')->group(function () {

##### Route::post('login', 'API\Driver\UserAPIController@login');

##### Route::post('register', 'API\Driver\UserAPIController@register');

##### Route::post('send_reset_link_email', 'API\UserAPIController@sendResetLinkEmail');

##### Route::get('user', 'API\Driver\UserAPIController@user');

##### Route::get('logout', 'API\Driver\UserAPIController@logout');

##### Route::get('settings', 'API\Driver\UserAPIController@settings');

##### });

##### Route::post('login', 'API\UserAPIController@login');

##### Route::post('register', 'API\UserAPIController@register');

##### Route::post('send_reset_link_email', 'API\UserAPIController@sendResetLinkEmail');

##### Route::get('user', 'API\UserAPIController@user');

##### Route::get('logout', 'API\UserAPIController@logout');

##### Route::get('settings', 'API\UserAPIController@settings');

##### Route::resource('fields', 'API\FieldAPIController');

##### Route::resource('categories', 'API\CategoryAPIController');

##### Route::resource('markets', 'API\MarketAPIController');

##### Route::resource('faq_categories', 'API\FaqCategoryAPIController');

##### Route::resource('products', 'API\ProductAPIController');

##### Route::resource('galleries', 'API\GalleryAPIController');

##### Route::resource('product_reviews', 'API\ProductReviewAPIController');

##### Route::resource('faqs', 'API\FaqAPIController');

##### Route::resource('market_reviews', 'API\MarketReviewAPIController');

##### Route::resource('currencies', 'API\CurrencyAPIController');

##### Route::resource('option_groups', 'API\OptionGroupAPIController');

##### Route::resource('options', 'API\OptionAPIController');

##### Route::middleware('auth:api')->group(function () {

##### Route::group(['middleware' => ['role:driver']], function () {

##### Route::prefix('driver')->group(function () {

##### Route::resource('orders', 'API\OrderAPIController');

##### Route::resource('notifications', 'API\NotificationAPIController');

##### Route::post('users/{id}', 'API\UserAPIController@update');

##### Route::resource('faq_categories', 'API\FaqCategoryAPIController');

##### Route::resource('faqs', 'API\FaqAPIController');

##### });

##### });

##### Route::group(['middleware' => ['role:manager']], function () {

##### Route::prefix('manager')->group(function () {

##### Route::resource('drivers', 'API\DriverAPIController');

##### Route::resource('earnings', 'API\EarningAPIController');

##### Route::resource('driversPayouts', 'API\DriversPayoutAPIController');

##### Route::resource('marketsPayouts', 'API\MarketsPayoutAPIController');

##### });

##### });

##### Route::post('users/{id}', 'API\UserAPIController@update');

##### Route::resource('order_statuses', 'API\OrderStatusAPIController');

##### Route::get('payments/byMonth', 'API\PaymentAPIController@byMonth')->name('payments.byMonth');

##### Route::resource('payments', 'API\PaymentAPIController');

##### Route::get('favorites/exist', 'API\FavoriteAPIController@exist');

##### Route::resource('favorites', 'API\FavoriteAPIController');

##### Route::resource('orders', 'API\OrderAPIController');

##### Route::resource('product_orders', 'API\ProductOrderAPIController');

##### Route::resource('notifications', 'API\NotificationAPIController');

##### Route::get('carts/count', 'API\CartAPIController@count')->name('carts.count');

##### Route::resource('carts', 'API\CartAPIController');

##### Route::resource('delivery_addresses', 'API\DeliveryAddressAPIController');
