Contributing
============

Before proposing a pull request, please check the following:

* Your code should follow the [PSR-2 coding standard](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md). Use [php-cs-fixer](https://github.com/fabpot/PHP-CS-Fixer) to fix inconsistencies.
* If you commit a new feature, be prepared to help maintaining it. Watch the project on GitHub, and please comment on issues or PRs regarding the feature you contributed.
* You should test your feature well.
* You should run `php build` and commit the PHAR file so it is part of your pull request. You may need to change `phar.readonly` php.ini setting to `0` or run the command as `php -d phar.readonly=0 build`.

Once your code is merged, it is available for free to everybody under the MIT License. Publishing your pull request on the PHPloy GitHub repository means that you agree with this license for your contribution.

Thank you for your contribution! PHPloy wouldn't be so great without you.

## Testing

*Sepcial thanks to [@mbrugger](https://github.com/mbrugger) for implementing the testing functionality, a long awaited feature.*

To get starting with testing, please fullow the steps below:

1. Install [docker](https://docs.docker.com/engine/installation/)
2. Start the test server
```
vagrant@vagrant-ubuntu-trusty-64:/vagrant/PHPloy$ ./tests/start_test_server.sh
```
3. run the tests
```
vagrant@vagrant-ubuntu-trusty-64:/vagrant/PHPloy$ vendor/bin/phpunit tests
PHPUnit 4.8.26 by Sebastian Bergmann and contributors.
...
Time: 2.32 seconds, Memory: 4.25MB
OK (3 tests, 4 assertions)
vagrant@vagrant-ubuntu-trusty-64:/vagrant/PHPloy$ 
```
4. Stop the sftp server
```
vagrant@vagrant-ubuntu-trusty-64:/vagrant/PHPloy$ ./tests/stop_test_server.sh 
```
More details to come...
