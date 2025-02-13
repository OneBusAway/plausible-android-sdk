# Plausible Android

This is an **unofficial** Android SDK to record events with a [Plausible](https://plausible.io) backend.

## Usage

### Configuration

For simple use cases, you can just declare the domain for which you'd like to send events in your `strings.xml` file:

```xml
<string name="plausible_domain">example.com</string>
```

If you're self-hosting Plausible, you'll need to provide the URL for your instance as well:

```xml
<string name="plausible_host">https://plausible.my-company.com</string>
```

By default, the SDK will be enabled at app startup, though you can prevent this to allow users to
opt-in or opt-out like so:

```xml
<string name="plausible_enable_startup">false</string>
```

You can then manually enable the sdk with the following:

```java
Plausible.enable(true)
```

### Sending Events

#### Page Views

```java
Plausible.pageView("/settings")
```

#### Custom Events

```java
Plausible.event("ctaClick")
```

## License

    Copyright 2022 William Patrick Brawner, 2025 Open Transit Software Foundation

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
