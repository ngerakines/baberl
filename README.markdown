
# About

Baberl is an interface to the iconv library.

# Usage

Using it is simple.

    1> {ok, {baberl, BaberlPid}} = baberl:start().
    {ok, {baberl, #Port<0.1122>}}
    2> baberl:convert(BaberlPid, "", "UTF-8", <<"foo">>).
    {ok,<<"foo">>
    3> baberl:convert(BaberlPid, "UTF-8", "ASCII//translit//IGNORE", unicode:characters_to_binary("fooÔ")).
    {ok,<<"foo^O">>}

Hurray!

The baberl.app file is also included for OTP distribution.

# License

Copyright (c) 2009 Electronic Arts, Inc.

This library was developed by Electronic Arts and is open source under the MIT license.

# Credits

Kevin A. Smith <kevin@hypotheticalabs.com><br/>
Nick Gerakines <nick@gerakines.net>
