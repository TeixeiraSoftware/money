# TeixeiraSoftware.Finance.Money [![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)](https://twitter.com/intent/tweet?text=A%20simple%20money%20class%20library&url=https://TeixeiraSoftware.github.io/TeixeiraSoftware.Finance.Money/&hashtags=money,finance,software,dotnet,crossplatform)

[![license](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/TeixeiraSoftware/TeixeiraSoftware.Finance.Money/blob/master/LICENSE)
[![Pull Requests](https://img.shields.io/badge/Pull%20Requests-Welcome-brightgreen.svg)](https://github.com/TeixeiraSoftware/TeixeiraSoftware.Finance.Money/blob/master/CONTRIBUTING.md)
[![NuGet](https://img.shields.io/nuget/dt/currency.svg)](https://www.nuget.org/packages/TeixeiraSoftware.Finance.Money/)

A simple cross platform money class library for .Net.

The implementation of this library is compatible with .Net Standard 2.0 (see [https://docs.microsoft.com/en-us/dotnet/standard/net-standard](https://docs.microsoft.com/en-us/dotnet/standard/net-standard) for details).

TeixeiraSoftware.Finance.Money is a value type.

### Installation

Install through NuGet Package Manager:
```
Install-Package TeixeiraSoftware.Finance.Money
```

### Dependencies

This package depends on TeixeiraSoftware.Finance.Currency, available [here](https://www.nuget.org/packages/TeixeiraSoftware.Finance.Money/) in nuget.org

### Usage
First of all, import the namespace, for convenience:
``` c#
using TeixeiraSoftware.Finance;
```

Then, just start using it:

``` c#
// XXX represents the ISO 4217 code of the currency
var tenMoneys = new Money(12.3m, Currency.XXX);
var aMillionMoneys new Moneys(1000000, Currency.GetByLetterCode("XXX"));
```

It is possible to get Currency instances by various ways. See the[TeixeiraSoftware.Finance.Currency](https://TeixeiraSoftware.github.io/TeixeiraSoftware.Finance.Currency/) package documentation for more info.

You can do math operations:

``` c#
// operator +
var halfMoney = new Money(0.25m, Currency.XXX) + 0.25m;
var tenMoneys = 1.5m + new Money(8.5m, Currency.XXX);
var aHundredMoneys = tenMoneys + 90;
var aThousandMoneys = 900 + aHundredMoneys;
var moreMoney = aHundredMoneys + aThousandMoneys;

// operator -
var oneMoney = new Money(2, Currency.XXX) - 1;
var tenMoneys = 1 - new Money(11, Currency.XXX);
var nineMoneys = tenMoneys - 1;
var eightMoneys = 1 - tenMoneys;
var sevenMoneys = eightMoneys - oneMoney;

// operator /
var wowSuchMoney = aThousandMoneys / 2;

// operator *
var muchCoins = aThousandMoneys * 2;
var veryValuable = 1000 * aThousandMoneys;
```

And you can compare money! How incredible is that? :p

The available operators are: ==, !=, >, >=, < and <=. And the .Equals method is also available.

``` c#
if (aThousandMoneys == muchCoins)
{
    // some fancy code here
}

if (aThousandMoneys != new Money(10, Currency.XTS))
{
    // more fancy code here
}

if (veryValuable.Equals(wowSuchMoney))
{
    // aaaand... more fancy code :)
}

if (muchCoins > veryValuable)
{
    // you write a lot of fancy code, don't you?
}

// and so on, you got it :D
```

### Contributing
I'm currently looking for help to improve the project. You can see some topics that you can help with in the [issues section of the project's GitHub page](https://github.com/TeixeiraSoftware/TeixeiraSoftware.Finance.Money/issues).
You can also contribute by doing unit tests, documentation, making pull requests or sharing the project.
