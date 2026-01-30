Symfony Console Getting Started project
===

Requirements
---
- Linux distro 6.6.87.2 or greater
- Composer 2.9
- php 8.1

## How to use

Execute:

```bash
composer install
```

Check version with `composer show -i 2> /dev/null` | grep -F 'symfony/console'

Output:
```bash
symfony/console                  6.4.32 Eases the creation of beautiful and testable co...
```

## Usage

The this is a simple and very stupid script where returns 0 (successful execution).

```bash
./application/application.php foo && echo success || failure
```

It returns `success`.

Changing the code as

```diff
@@ -11,7 +11,7 @@
 $application = new Application();

 $application->register('foo')
-            ->setCode(fn(InputInterface $input,OutputInterface $output) => Command::SUCCESS);
+            ->setCode(fn(InputInterface $input,OutputInterface $output) => Command::FAILURE);

 $application->run();
```

It returns `failure`.

