---
-api-id: T:Windows.Foundation.WwwFormUrlDecoder
-api-type: winrt class
---

<!-- Class syntax.
public class WwwFormUrlDecoder : Windows.Foundation.Collections.IIterable<Windows.Foundation.IWwwFormUrlDecoderEntry>, Windows.Foundation.Collections.IVectorView<Windows.Foundation.IWwwFormUrlDecoderEntry>, Windows.Foundation.IWwwFormUrlDecoderRuntimeClass
-->

# Windows.Foundation.WwwFormUrlDecoder

## -description
Parses a URL query string, and exposes the results as a read-only vector (list) of name-value pairs from the query string.

## -remarks
Use the [WwwFormUrlDecoder](wwwformurldecoder.md) class to parse a query string into name-value pairs, based on the number and placement of "&" and "=" symbols. Each name-value pair is represented by an [IWwwFormUrlDecoderEntry](iwwwformurldecoderentry.md) object, which has a [Name](wwwformurldecoderentry_name.md) property and a [Value](ireferencearray_1_value.md) property (both strings).

Use [GetFirstValueByName](wwwformurldecoder_getfirstvaluebyname.md) to find a specific named query string parameter. All languages can use this method. You'd typically use [GetFirstValueByName](wwwformurldecoder_getfirstvaluebyname.md) rather than [GetAt](wwwformurldecoder_getat.md) because the order of items in a query string usually isn't important, whereas the parameter name is the important identifier of the parts of a query. Or, if you're not sure what names exist in the query string, you might enumerate over the complete [WwwFormUrlDecoder](wwwformurldecoder.md) collection.

The [Uri.QueryParsed](uri_queryparsed.md) property returns a complete [WwwFormUrlDecoder](wwwformurldecoder.md) based on a [Uri](uri.md) instance. So if you're using Visual C++ component extensions (C++/CX) or JavaScript code, and you already have a [Uri](uri.md) instance, you won't need to construct a new [WwwFormUrlDecoder](wwwformurldecoder.md) object, the [Uri](uri.md) instance already has one. You might construct a [WwwFormUrlDecoder](wwwformurldecoder.md) if you have a string representing a URL or its query string component from other sources, such as from a [Windows.Web.Http](../windows.web.http/windows_web_http.md) API.

> [!NOTE]
> This collection is a vector rather than a map in case the original order has any meaning to an implementation, and also because it's legal for the same name to appear in the query string twice, whereas it's not legal for maps to have duplicate keys.

### Collection member lists

For .NET usage, [WwwFormUrlDecoder](wwwformurldecoder.md) has the projected APIs of a generic [IReadOnlyList](https://msdn.microsoft.com/library/windows/apps/hh192385) with a [IWwwFormUrlDecoderEntry](iwwwformurldecoderentry.md) constraint. The APIs that are available for each language are indicated in the member lists.

For JavaScript, [WwwFormUrlDecoder](wwwformurldecoder.md) has the members shown in the member lists. In addition, [WwwFormUrlDecoder](wwwformurldecoder.md) supports a **length** property, members of **Array.prototype**, and using an index to access items.

### .NET usage

.NET code can't use the [Windows.Foundation.Uri](uri.md) class (you use [System.Uri](https://msdn.microsoft.com/library/system.uri.aspx) instead). But .NET code can and should use [WwwFormUrlDecoder](wwwformurldecoder.md). Using [WwwFormUrlDecoder](wwwformurldecoder.md) is simpler and less error-prone than string-splitting on "&amp;" and "=" characters. That gets complicated because of encoding. To use [WwwFormUrlDecoder](wwwformurldecoder.md), call the [WwwFormUrlDecoder](wwwformurldecoder_wwwformurldecoder.md) constructor, passing in the [Query](https://msdn.microsoft.com/library/system.uri.query.aspx) value from your [System.Uri](https://msdn.microsoft.com/library/system.uri.aspx). This initializes a new [WwwFormUrlDecoder](wwwformurldecoder.md) object. Then use [GetFirstValueByName](wwwformurldecoder_getfirstvaluebyname.md) to find a specific named query string parameter. Or, if you don't know what's going to be in the query string, enumerate over the collection to determine the query string parameters that are available.

Use the [IWwwFormUrlDecoderEntry](iwwwformurldecoderentry.md) interface for the type of the items in the collection (this is how the items are typed by [IndexOf](wwwformurldecoder_indexof.md)). Don't use the [WwwFormUrlDecoderEntry](wwwformurldecoderentry.md) class, it isn't available for .NET usage.

[WwwFormUrlDecoder](wwwformurldecoder.md) also has the projected APIs of a generic [IReadOnlyList](https://msdn.microsoft.com/library/windows/apps/hh192385) with a [IWwwFormUrlDecoderEntry](iwwwformurldecoderentry.md) constraint, but these APIs aren't commonly used.

> [!NOTE]
> `System.Web.HttpUtility.ParseQueryString` isn't available for .NET for Windows Runtime app. [WwwFormUrlDecoder](wwwformurldecoder.md) is the recommended replacement for it.


<!--Begin NET note for IEnumerable support-->
### Enumerating the collection in C# or Microsoft Visual Basic

[WwwFormUrlDecoder](wwwformurldecoder.md) is enumerable, so you can use language-specific syntax such as **foreach** in C# to enumerate the items in the collection. The compiler does the type-casting for you and you won't need to cast to `IEnumerable<IWwwFormUrlDecoderEntry>` explicitly. If you do need to cast explicitly, for example if you want to call [GetEnumerator](https://msdn.microsoft.com/library/windows/apps/system.collections.ienumerable.getenumerator), cast to [IEnumerable&lt;T&gt;](https://msdn.microsoft.com/library/windows/apps/system.collections.ienumerable) with an [IWwwFormUrlDecoderEntry](iwwwformurldecoderentry.md) constraint.


<!--End NET note for IEnumerable support-->

## -examples

## -see-also
[IWwwFormUrlDecoderEntry](iwwwformurldecoderentry.md), [Uri.QueryParsed](uri_queryparsed.md)
