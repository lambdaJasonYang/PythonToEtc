# Float,Double,Decimal

<table>
  <thead>
    <tr>
      <th style="text-align:left">Detail</th>
      <th style="text-align:left">Float</th>
      <th style="text-align:left">Double</th>
      <th style="text-align:left">Decimal</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">name</td>
      <td style="text-align:left">Single Precision</td>
      <td style="text-align:left">Double Precision</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">C#</td>
      <td style="text-align:left">System.Single</td>
      <td style="text-align:left">System.Double</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">bits</td>
      <td style="text-align:left">32 bits</td>
      <td style="text-align:left">64 bits</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">digit precision</td>
      <td style="text-align:left">7 digits</td>
      <td style="text-align:left">15 digits</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>Precise math</p>
        <p>equality?</p>
      </td>
      <td style="text-align:left">No</td>
      <td style="text-align:left">No</td>
      <td style="text-align:left">Yes</td>
    </tr>
    <tr>
      <td style="text-align:left">[min,max]</td>
      <td style="text-align:left">
        <p>3.40282347E+38f,</p>
        <p>3.40282347E+38f</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">suffix</td>
      <td style="text-align:left">2.13<b>f</b>
      </td>
      <td style="text-align:left">2.13<b>d</b>
      </td>
      <td style="text-align:left">2.13<b>m</b>
      </td>
    </tr>
  </tbody>
</table>

{% tabs %}
{% tab title="C\#" %}
{% code title="Precise math equality?" %}
```csharp
float f = 0.3f + 0.6f;
Assert.True(f != 0.9f); //UNEXPECTED BEHAVIOR
//odd behavior

//This behaviour is the most important consideration when 
//deciding whether to use
//Floating Point number types (`float` and `double`) 
//or the `decimal` type.

decimal d = 0.1m;
decimal result = d + d + d + d + d + d + d;
Assert.True(result == 0.7m); //EXPECTED BEHAVIOR
//USE DECIMAL WHEN DEALING WITH EQUALITY

```
{% endcode %}
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Use decimal type when dealing with == of numbers
{% endhint %}

```csharp
float x = 0.1f //float
double y = 0.2d //double
decimal z = 0.3m //decimal

var result = z + (decimal)x
//operations with decimal require CASTING
```

{% tabs %}
{% tab title="String to Number" %}
```csharp
var F = float.Parse("3.4E+38", CultureInfo.InvariantCulture);

var D = decimal.Parse("593,543,950,336", CultureInfo.InvariantCulture);
```
{% endtab %}
{% endtabs %}

