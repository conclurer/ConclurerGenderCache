# ConclurerGenderCache

This is a companion module for [ConclurerGenderApi](https://github.com/conclurer/ConclurerGenderApi).

**How to use it?**

Just include ConclurerGenderCache before including ConclurerGenderApi.

```php
$modules->get("ConclurerGenderCache");

$gender = $module->get("ConclurerGenderApi");

// First run
$result = $gender->name("Torsten")->fetch();
echo get_class($result); // => ConclurerGenderApiResult

// Cached Result
$result = $gender->name("Torsten")->fetch();
echo get_class($result); // => ConclurerGenderCacheResult
```