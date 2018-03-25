{% include "/header.md" %}

# Lesson Three - Email Marketing

# Career Readiness
Class Discussion - What Catches your eye when you get an Email?

# Key Questions
* Why is email marketing important?
    * What Email Marketing Platform Should I use?
* What do you mean by "Coding backwards"
* Is email actually dead?
# Demonstration

 **Lets take HTML standards and throw it out the window**
 
    ```
    <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
            <html xmlns="http://www.w3.org/1999/xhtml">
     <head>
         <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
            <title></title>
             <style></style>
    </head>
    <body>
        <table border="0" cellpadding="0" cellspacing="0" height="100%" width="100%" id="bodyTable">
            <tr>
                <td align="center" valign="top">
                    <table border="0" cellpadding="20" cellspacing="0" width="600" id="emailContainer">
                        <tr>
                            <td align="center" valign="top">
                                This is where my content goes.
                            </td>
                        </tr>
                    </table>
                </td>
            </tr>
        </table>
    </body>
    </html>
    ```

**Lets get even more crazy with INLINE Styling**
 
 ```
<a href="#" target="_blank" style="color:#FFFFFF; text-decoration:none;">Read More Stories On Our Blog</a>

 ```

#Creating Mailchimp Coded Sections
 **Mailchimp uses their own "code" language that create interactive editable areas within a email template**

For example if you are creating a **editable** block where a user will be able to drop in and edit their own content.

'mc:edit="header"'

**Now how does this look code wise?**

`
   <td align="center" valign="top" mc:edit="blockLeft1">
                                This is where my content goes.
                            </td>
`

What Mailchimp does is scan your email and look for these little mc calls and it knows within its builder that this will be editable by the user.

**Somethings to consider...**
* Don't use the same edit name for the fields. It will create duplicated block sections
* Never do editable areas within editable areas
* Make each name unique

#Email Standards To Avoid Blacklisting
 1. Must include unsubscribe Button
 2. no JS code ever
 3. No Numbers or consecutive capital letters  or too many special characters in the subject line - Example "!!! CHECK OUT THIS NEW WEBSITE !!!! "
 4. Images **MUST** be HTTPS'ed
 5. Images **MUST** include Alt tags

# Tips For Making Email Templates
1. Tables tables tables.
2. Inline Styling
3. Test , retest, and do it all over again
4. Dreamweaver Actually Works great for emails
5. There are no take backs once you press that send button


# Project
Code Your Own Mailchimp Template
 1. It must fit to mailchimp guidelines
 2. Each Block Must be able to be edited by the user.
 3. The subject must be able the new ACA wordpress class
 4. the content must be about the new ACA wordpress class.

**We will be sending out test emails to everyone next class.**

## Resources
[Mailchimp Template Creation](https://templates.mailchimp.com/)


{% include "/footer.md" %}
