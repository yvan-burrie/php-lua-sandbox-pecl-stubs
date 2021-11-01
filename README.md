# PHP Lua Sandbox PECL Stubs

Stubs for the [PHP LuaSandbox PECL package](https://www.php.net/manual/en/book.luasandbox.php).

These stubs come from my contributions ([#882](https://github.com/JetBrains/phpstorm-stubs/pull/882), [#900](https://github.com/JetBrains/phpstorm-stubs/pull/900)) to the [JetBrains PhpStorm stubs](https://github.com/JetBrains/phpstorm-stubs/blob/master/LuaSandbox/LuaSandbox.php).

The `LuaSandbox.php` file contains the following stubs (with official doc-blocks):

```php
class LuaSandbox {
    public function callFunction(string $name, array $arguments): array|bool;
    public function disableProfiler(): void;
    public function enableProfiler($period = 0.02): bool;
    public function getCPUUsage(): float;
    public function getMemoryUsage(): int;
    public function getPeakMemoryUsage(): int;
    public function getProfilerFunctionReport(int $units = LuaSandbox::SECONDS): array;
    public static function getVersionInfo(): array;
    public function loadBinary(string $code, string $chunkName = ''): LuaSandboxFunction;
    public function loadString(string $code, string $chunkName = ''): LuaSandboxFunction;
    public function pauseUsageTimer(): bool;
    public function registerLibrary(string $libname, array $functions): array;
    public function setCPULimit(int $limit): bool|float;
    public function setMemoryLimit(int $limit): void;
    public function unpauseUsageTimer(): void;
    public function wrapPhpFunction(callable $function): LuaSandboxFunction;
}

class LuaSandboxFunction {
    public function call(string $arguments): array|bool;
    public function dump(): string;
}

class LuaSandboxError           extends Exception {}
class LuaSandboxRuntimeError    extends LuaSandboxError {}
class LuaSandboxFatalError      extends LuaSandboxError {}
class LuaSandboxErrorError      extends LuaSandboxFatalError {}
class LuaSandboxMemoryError     extends LuaSandboxFatalError {}
class LuaSandboxSyntaxError     extends LuaSandboxFatalError {}
class LuaSandboxTimeoutError    extends LuaSandboxFatalError {}
```
