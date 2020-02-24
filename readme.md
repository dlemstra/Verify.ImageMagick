<!--
GENERATED FILE - DO NOT EDIT
This file was generated by [MarkdownSnippets](https://github.com/SimonCropp/MarkdownSnippets).
Source File: /readme.source.md
To change this file edit the source file and then run MarkdownSnippets.
-->

# <img src="/src/icon.png" height="30px"> Verify.ImageMagick

[![Build status](https://ci.appveyor.com/api/projects/status/7k8hh0guut2ioak2?svg=true)](https://ci.appveyor.com/project/SimonCropp/Verify-ImageMagick)
[![NuGet Status](https://img.shields.io/nuget/v/Verify.ImageMagick.svg)](https://www.nuget.org/packages/Verify.ImageMagick/)

Extends [Verify](https://github.com/SimonCropp/Verify) to allow verification of documents via [ImageMagick.net](https://github.com/dlemstra/Magick.NET).

Converts documents (pdfs) to png for verification.

Support is available via a [Tidelift Subscription](https://tidelift.com/subscription/pkg/nuget-verify.aspose?utm_source=nuget-verify.aspose&utm_medium=referral&utm_campaign=enterprise).

<!-- toc -->
## Contents

  * [Usage](#usage)
    * [PDF](#pdf)
  * [File Samples](#file-samples)
  * [Security contact information](#security-contact-information)<!-- endtoc -->


## NuGet package

https://nuget.org/packages/Verify.ImageMagick/


## Usage

Given a test with the following definition:

<!-- snippet: TestDefinition -->
<a id='snippet-testdefinition'/></a>
```cs
public class Samples :
    VerifyBase
{
    public Samples(ITestOutputHelper output) :
        base(output)
    {
    }

    static Samples()
    {
        VerifyImageMagick.Initialize();
    }
```
<sup><a href='/src/Tests/Samples.cs#L9-L22' title='File snippet `testdefinition` was extracted from'>snippet source</a> | <a href='#snippet-testdefinition' title='Navigate to start of snippet `testdefinition`'>anchor</a></sup>
<!-- endsnippet -->


### PDF


#### Verify a file

<!-- snippet: VerifyPdf -->
<a id='snippet-verifypdf'/></a>
```cs
[Fact]
public Task VerifyPdf()
{
    return VerifyFile("sample.pdf");
}
```
<sup><a href='/src/Tests/Samples.cs#L24-L32' title='File snippet `verifypdf` was extracted from'>snippet source</a> | <a href='#snippet-verifypdf' title='Navigate to start of snippet `verifypdf`'>anchor</a></sup>
<!-- endsnippet -->


#### Verify a Stream

<!-- snippet: VerifyPdfStream -->
<a id='snippet-verifypdfstream'/></a>
```cs
[Fact]
public Task VerifyPdfStream()
{
    var settings = new VerifySettings();
    settings.UseExtension("pdf");
    return Verify(File.OpenRead("sample.pdf"), settings);
}
```
<sup><a href='/src/Tests/Samples.cs#L34-L44' title='File snippet `verifypdfstream` was extracted from'>snippet source</a> | <a href='#snippet-verifypdfstream' title='Navigate to start of snippet `verifypdfstream`'>anchor</a></sup>
<!-- endsnippet -->


#### Result

[Samples.VerifyPdf.00.verified.png](/src/Tests/Samples.VerifyPdf.00.verified.png):

<img src="/src/Tests/Samples.VerifyPdf.00.verified.png" width="200px">


## File Samples

http://file-examples.com/


## Security contact information

To report a security vulnerability, use the [Tidelift security contact](https://tidelift.com/security). Tidelift will coordinate the fix and disclosure.


## Icon

[Swirl](https://thenounproject.com/term/swirl/1568686/) designed by [creativepriyanka](https://thenounproject.com/creativepriyanka) from [The Noun Project](https://thenounproject.com/creativepriyanka).
