   _____________________
  //                   \\
 //    CODE TESTING     \\
//                       \\
\\- - - - - - - - - - - -//
 \\    Unit Testing	//
  \\- - - - - - - - - -//
How do you know which unit tests to write and when you have written enough tests?
Well. This is the eternal question if testing. There are two reasonable answers to this: 1) when you 
are convinced that you have tested enough and 2) when you are out of time and/or budget


   _____________________
  //                   \\
 //   CONCURENT LOGIN   \\
//                       \\
\\- - - - - - - - - - - -//
 \\ Good practical books//
  \\- - - - - - - - - -//
1. Allow concurrent logins <-- most sites
2. Allow concurrent logins but report that someone else is logged it -
like Gmail does <-- many sites. this is not bad especially the google way
such as putting a bigger, more noticeable line if they see a specific
problem (for example deviation from behavioral patterns)
3. Don't allow them and kick out any logged in user when a new one logs in
<-- few sites. often thick clients etc. In many cases this is due to
application functionality more than security needs ;)
4. Don't allow them and lock out all new logins till old ones have logged
out <-- that can cause functionality problems, such as the admin that
locked a bunch of files and interfaces and then went on vacation.
5. Give a warning popup when logging in to say the account is in use
elsewhere as well <-- I like this one, but it's not a one-size-fits-all
solution. nobody wants this annoyance on their social network site.
6. Allow but report back to an admin or log tracker or similar <-- depends
on the site. on large traffic sites you can't really have multiple logins
reporting to admin.


if to break this into a very rough site-type classification:

1. Retail - no reason not to allow multiple connections. users want to be
able to log in from their tablet, but also from their phone and/or laptop.
You can require additional authentication (password for example) before
important operations. Concurrency - not necessarily a problem.
2. Banking/similar - Although you don't really have to allow concurrent
connections, most sites won't block it. Again, you need to look at the
risk. A lot of the controls are done on different levels - such as
monitoring the standard 'behavior' patterns of a user and then checking
whether the new login matches that and if needed utilizing a secondary
security mechanism
3. Social sites (FB, linkedin, or
whatever-young-people-are-using-these-days) - again - concurrent logins are
usually needed. FB and similar send you an email saying 'new device' and
you can also configure to disable.
4. sensitive interfaces - usually not a lot of users. be the annoying
security person and play with settings as much as you want :)


the bigger question here is - what are you trying to achieve?

disabling concurrent logins because security? I'm not sure that's the way
to go for most apps. notifying the user - yes you can do that, most of them
won't know what to do with it.

2FA (not bullet proof, but efficient in most scenarios these days),
notifications of new device, extra security layer if behavior is
non-standard (different country in a short time, etc) is probably better
than just 'don't do concurrent logins'.


   _____________________
  //                   \\
 //   NON-Programming   \\
//                       \\
\\- - - - - - - - - - - -//
 \\     But usefull     //
  \\- - - - - - - - - -//
http://learn.shayhowe.com/advanced-html-css/performance-organization/
