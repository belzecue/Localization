# Localization
A simple way to translate strings in a project

A more detailed description can be found on my blog: https://www.anton.website/a-simple-localization-system/

Import Localization.cs and StringLocalizer.cs. Create a CSV file inside the StreamingAssets folder.
An example CSV file can be found in the StreamingAssets folder of this repository.

To get a translated string in the code use Localizer.Get(language, ID) method. The language name must
be the same as in the top row of the CSV file. The IDs should be generated from the CSV file or
added manually to Translation enum. The enum values should correspond to the string values in the
first column of the CSV file. Use Localization -> Generate Translation Constants method to generate
the enum file automatically.

To get a translated string with the currently set language use Localizer.Get(ID) method.

To localize a text component (TextmeshProUGUI) add a StringLocalizer component next to the text
component. The defaultString variable will be used as an ID for the localization.
