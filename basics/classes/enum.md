# Enum



```csharp
enum MeditationForms
 {
 Mindfulness,
 SilentIllumination,
 Contemplation,
 Observation

}

/*
Creating an instance of an enum is as easy as assigning a member
of the enum to a new variable. For instance:
*/
var mindfulness = MeditationForms.Mindfulness;

/*
While the underlying type of the instance above will be an integer,
enums are first class types in the C# language. The type of the
variable 'mindfulness' will be the enum itself.
*/
Assert.Equal(typeof(MeditationForms), mindfulness.GetType());

//MeditationForms Observation = (MeditationForms)3; 
//this Fails the assertion because it is done on runtime

//Assert.Equal(1,quietForm); this assert doesnt work, enum becomes its own type
var quietForm = (MeditationForms)1; //we need to type cast 1 to the enum type
Assert.Equal(MeditationForms.SilentIllumination, quietForm);


Assert.True(Enum.IsDefined(typeof(MeditationForms), "Observation"));
```

```csharp
[Flags]
enum DayOfTheWeek
{
    Monday,
    Tuesday,
    Wednesday,
    Thursday,
    Friday,
    Saturday,
    Sunday
}
public void EnumsCanBeFlags()
{
    /*
    Enums can represent a combination of choices. When an enum is
    decorated with the '[Flag]' attribute, it changes the underlying
    type to a bit field. This allows for multiple members to be assigned
    to a single value.

    Notice we're using the OR operator to concatenate multiple days.

    We're missing Friday!
    */

    var workWeek = DayOfTheWeek.Monday | DayOfTheWeek.Tuesday | DayOfTheWeek.Wednesday | DayOfTheWeek.Thursday | DayOfTheWeek.Friday;
    Assert.True(workWeek.HasFlag(DayOfTheWeek.Friday)); // Assuming you work Fridays :)
}
```

