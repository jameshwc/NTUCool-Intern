# 191016 NetConnectionNotAllowedError (4hrs)
$ docker-compose run --rm web bundle exec rspec spec
/home/docker/.gem/ruby/2.4.0/gems/soap4r-ruby1.9-2.0.5/lib/soap/mapping/encodedregistry.rb:150: warning: constant ::Fixnum is deprecated
/home/docker/.gem/ruby/2.4.0/gems/soap4r-ruby1.9-2.0.5/lib/soap/mapping/encodedregistry.rb:216: warning: constant ::Fixnum is deprecated
DEPRECATION WARNING: `secrets.secret_token` is deprecated in favor of `secret_key_base` and will be removed in Rails 6.0. (called from at /usr/src/app/config/environment.rb:28)
truncating all tables...
finished resetting test db in 36.977658765 seconds
/home/docker/.gem/ruby/2.4.0/gems/ritex-1.0.1/lib/ritex/mathml/entities.rb:55: warning: key "rightleftharpoons" is duplicated and overwritten on line 101
/home/docker/.gem/ruby/2.4.0/gems/ritex-1.0.1/lib/ritex/mathml/entities.rb:178: warning: key "eqslantgtr" is duplicated and overwritten on line 179
/home/docker/.gem/ruby/2.4.0/gems/ritex-1.0.1/lib/ritex/mathml/entities.rb:225: warning: key "ntrianglelefteq" is duplicated and overwritten on line 229
/home/docker/.gem/ruby/2.4.0/gems/ritex-1.0.1/lib/ritex/mathml/entities.rb:244: warning: key "nsupseteq" is duplicated and overwritten on line 245
/home/docker/.gem/ruby/2.4.0/gems/ritex-1.0.1/lib/ritex/mathml/functions.rb:94: warning: key "rowspan" is duplicated and overwritten on line 98
/home/docker/.gem/ruby/2.4.0/gems/ritex-1.0.1/lib/ritex/mathml/functions.rb:93: warning: key "colspan" is duplicated and overwritten on line 99
WARNING: Shared example group 'a locked api item' has been previously defined at:
/usr/src/app/spec/apis/locked_spec.rb:21
...and you are now defining it at:
/usr/src/app/spec/apis/locked_spec.rb:21
The new definition will overwrite the original one.
/usr/src/app/spec/apis/v1/courses_api_spec.rb:762: warning: key "license" is duplicated and overwritten on line 767
/usr/src/app/spec/apis/v1/courses_api_spec.rb:833: warning: key "license" is duplicated and overwritten on line 838
2019-10-16 08:39:46 WARN Selenium [DEPRECATION] Selenium::WebDriver::Chrome#driver_path= is deprecated. Use Selenium::WebDriver::Chrome::Service#driver_path= instead.
/usr/src/app/spec/lib/token_scopes_spec.rb:21: warning: already initialized constant ApiScopeMapper
/usr/src/app/spec/apis/v1/scopes_api_controller_spec.rb:26: warning: previous definition of ApiScopeMapper was here
/usr/src/app/spec/models/master_courses/master_migration_spec.rb:1239: warning: key :content_id is duplicated and overwritten on line 1239
WARNING: Shared example group 'Canvas::DraftStateValidations' has been previously defined at:
/usr/src/app/spec/lib/canvas/draft_state_validations_spec.rb:21
...and you are now defining it at:
/usr/src/app/spec/lib/canvas/draft_state_validations_spec.rb:21
The new definition will overwrite the original one.
/usr/src/app/spec/models/quizzes_next/service_spec.rb:21: warning: already initialized constant Service
/usr/src/app/spec/models/conditional_release/conditional_release_service_spec.rb:23: warning: previous definition of Service was here
/usr/src/app/spec/selenium/cdn_spec.rb:30: warning: already initialized constant EXAMPLE_CDN_HOST
/usr/src/app/spec/selenium/brandable_css_js_spec.rb:23: warning: previous definition of EXAMPLE_CDN_HOST was here
Run options: exclude {:pact_live_events=>true}
Randomized with seed 47928
found available port: 172.18.0.4:42363
using CHROME driver
Thread: provisioning remote chrome driver
Starting web server... Done!
An error occurred in a `before(:suite)` hook.
Failure/Error:
driver = Selenium::WebDriver.for(
:remote,
:url => selenium_url,
:desired_capabilities => desired_capabilities
)
WebMock::NetConnectNotAllowedError:
Real HTTP connections are disabled. Unregistered request: POST http://selenium-chrome:4444/wd/hub/session with body '{"desiredCapabilities":{"browserName":"chrome","version":"","platform":"ANY","javascriptEnabled":true,"cssSelectorsEnabled":true,"takesScreenshot":false,"nativeEvents":false,"rotatable":false,"chromeOptions":{"args":["disable-dev-shm-usage","no-sandbox","window-size=1680,1050"],"w3c":false}},"capabilities":{"firstMatch":[{"browserName":"chrome"}]}}' with headers {'Accept'=>'application/json', 'Accept-Encoding'=>'gzip;q=1.0,deflate;q=0.6,identity;q=0.3', 'Content-Length'=>'350', 'Content-Type'=>'application/json; charset=UTF-8', 'User-Agent'=>'selenium/3.142.3 (ruby linux)'}
You can stub this request with the following snippet:
stub_request(:post, "http://selenium-chrome:4444/wd/hub/session").
with(
body: "{\"desiredCapabilities\":{\"browserName\":\"chrome\",\"version\":\"\",\"platform\":\"ANY\",\"javascriptEnabled\":true,\"cssSelectorsEnabled\":true,\"takesScreenshot\":false,\"nativeEvents\":false,\"rotatable\":false,\"chromeOptions\":{\"args\":[\"disable-dev-shm-usage\",\"no-sandbox\",\"window-size=1680,1050\"],\"w3c\":false}},\"capabilities\":{\"firstMatch\":[{\"browserName\":\"chrome\"}]}}",
headers: {
'Accept'=>'application/json',
'Accept-Encoding'=>'gzip;q=1.0,deflate;q=0.6,identity;q=0.3',
'Content-Length'=>'350',
'Content-Type'=>'application/json; charset=UTF-8',
'User-Agent'=>'selenium/3.142.3 (ruby linux)'
}).
to_return(status: 200, body: "", headers: {})
============================================================

# /home/docker/.gem/ruby/2.4.0/gems/webmock-3.7.6/lib/webmock/http_lib_adapters/net_http.rb:114:in `request'
# /home/docker/.gem/ruby/2.4.0/gems/selenium-webdriver-3.142.3/lib/selenium/webdriver/remote/http/default.rb:129:in `response_for'
# /home/docker/.gem/ruby/2.4.0/gems/selenium-webdriver-3.142.3/lib/selenium/webdriver/remote/http/default.rb:82:in `request'
# /home/docker/.gem/ruby/2.4.0/gems/selenium-webdriver-3.142.3/lib/selenium/webdriver/remote/http/common.rb:64:in `call'
# /home/docker/.gem/ruby/2.4.0/gems/selenium-webdriver-3.142.3/lib/selenium/webdriver/remote/bridge.rb:167:in `execute'
# /home/docker/.gem/ruby/2.4.0/gems/selenium-webdriver-3.142.3/lib/selenium/webdriver/remote/bridge.rb:102:in `create_session'
# /home/docker/.gem/ruby/2.4.0/gems/selenium-webdriver-3.142.3/lib/selenium/webdriver/remote/bridge.rb:56:in `handshake'
# /home/docker/.gem/ruby/2.4.0/gems/selenium-webdriver-3.142.3/lib/selenium/webdriver/remote/driver.rb:39:in `initialize'
# /home/docker/.gem/ruby/2.4.0/gems/selenium-webdriver-3.142.3/lib/selenium/webdriver/common/driver.rb:58:in `new'
# /home/docker/.gem/ruby/2.4.0/gems/selenium-webdriver-3.142.3/lib/selenium/webdriver/common/driver.rb:58:in `for'
# /home/docker/.gem/ruby/2.4.0/gems/selenium-webdriver-3.142.3/lib/selenium/webdriver.rb:88:in `for'
# ./spec/selenium/test_setup/selenium_driver_setup.rb:353:in `selenium_remote_driver'
# ./spec/selenium/test_setup/selenium_driver_setup.rb:314:in `chrome_driver'
# ./spec/selenium/test_setup/selenium_driver_setup.rb:196:in `block in create_driver'
# ./spec/selenium/test_setup/selenium_driver_setup.rb:319:in `with_retries'
# ./spec/selenium/test_setup/selenium_driver_setup.rb:191:in `create_driver'
# ./spec/selenium/test_setup/selenium_driver_setup.rb:152:in `start_driver'
# ./spec/selenium/test_setup/selenium_driver_setup.rb:105:in `block in run'

Finished in 3.5 seconds (files took 12 minutes 49 seconds to load)
0 examples, 0 failures, 1 error occurred outside of examples
Randomized with seed 47928

