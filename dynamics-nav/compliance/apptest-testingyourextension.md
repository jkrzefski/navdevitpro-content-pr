﻿## Testing your Extension ##

Several key things lead to your extension passing the Microsoft validation process. However, one of the most important checks you can do is to take the time and test your extension before submitting it for validation. This allows you to catch some of the basic errors that could lead to validation failures. Following are some points to keep in mind when doing your testing.

- Always test in a true D365 SaaS environment. If you test in on-prem, you might miss errors that would be seen on SaaS.
- Ensure that your extension can be published without code signing errors. You must not use the -skipverification flag.
- The extension should be able to be installed without errors.
- If you are using the Assisted Setup, ensure that you can use your wizard to completion without errors.
- Walk through the setup and usage of your extension to verify it works as expected (**remember to test as a user that doesn’t have SUPER permissions**).
- Check that you can uninstall and unpublish your extension without any errors.
- Make sure you can republish and reinstall your extension without any errors.