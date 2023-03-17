# Frequently Asked Questions

??? info "How do you use the Client?"

    As described in [Clients](clients), the official client is not ready yet. You are free to use
    a {{ name }} compatible client to connect, but no support will be provided.

??? info "I am getting the error 'Cannot GET /', how fix?"

    If you see that error message, it means that your server is configured correctly. Hooray!
    Unfortunately, our official client isn't done yet (see question above).

??? info "Voice/Video when?"

    Currently, there is no voice or video support in any {{ name }} instance.
    This is a very difficult feature to get working, especially given that
    we must implement it the exact same way as Discord.com for client compatibility.
    [We would be incredibly thankful for any assistance.](/contributing)

??? info "Free Nitro?"

    Please do not use Discord trademarks to refer to anything regarding {{ name }}.
    As an instance owner, you can grant yourself or others *premium* features which may be used to determine your abilities
    *client-side*. However, {{ name }}-server currently does not have any distinction between premium and free users.
    All users can access all features, given they have the [rights](setup/server/security/rights.md) to do so.

    You cannot give yourself premium features on Discord.com using a {{ name }} instance.

??? info "How do I boost my guild? Or, how do I buy premium?"

    You cannot buy premium features through {{ name }}, as {{ name }} does not support any payment backend.

    Additionally, {{ name }} does not currently have any distinction between premium and free users or guilds.
    All users and guilds have access to all features server-side.

    In the case of users, you may run into issues with the client preventing you from using certain features,
    if the user's `premium_type` or `premium` values are not set correctly. By default, {{ name }} will do this for you, however.

    In the case of guilds, you may run into issues with uploading animated icons or banners, etc.
    If so, simply give the guild the [features](setup/server/configuration/guildFeatures.md) you require.
    You can set them to be given to all guilds by default using the [config](setup/server/configuration/index.md) `guild_defaultFeatures` array.

??? info "Can I log in with my Discord account?"

    No. {{ name }} and Discord are entirely separate services, with their own separate databases
    and authentication. {{ name }} cannot access any private data from Discord.com.
    As always, you should not provide login credentials for Discord.com, or any other service,
    to others.

??? info "Does {{ name }} use the same servers as Discord?"

    No. Discord servers, as in the bare-metal running the service, are completely inaccessible
    to people, outside of course the Discord.com service provided. It is impossible for us to use their
    infrastructure. {{ name }} instances are hosted entirely by their owner(s).

    If you mean Discord 'server' as in a *guild*, also no. {{ name }} is not a proxy for
    Discord guilds. {{ name }} does not create Discord.com accounts or ask for your own at any time
    (outside of OAuth features provided by the instance such as account connections or 'login with' buttons)
    If {{ name }} was to try this, Discord's automated spam filters would surely block your instance,
    and ban any offending accounts.

    Lastly, you can simply view [our codebase](https://github.com/{{ name }}/{{ name }}-server).
    A simple proxy would not need to be this complex or large.
    We implement the entire Discord.com API, Gateway, among others.
    None of this would be necessary if we were simply abusing Discord.com.

??? info "Do you use Discord.com code?"

    Absolutely not. If a potential contributor makes any indication of being a Discord employee,
    or to have access to leaked Discord.com code, we take measures in line with our [Code of Conduct](/contributing/conduct.md)
    to ensure the {{ name }} codebase is free of any proprietary code. We want absolutely nothing to do with it.

??? info "Is this illegal?"

    The {{ name }} maintainers do not believe it to be, no. See: [Oracle v. Google](https://en.wikipedia.org/wiki/Google_LLC_v._Oracle_America,_Inc.).

??? info "Why are you doing this, anyway?"

    1. We love free, open source software.
    2. There are many existing bots, applications, users, features, and ideas surrounding Discord.com.
    3. {{ name }} allows these users and developers to maintain a familiar ecosystem with minimal friction.
    4. Reimplementing allows us to extend the Discord protocol in ways Discord.com may not deem feasible, economical, whateverical.
    5. This includes privacy features, such as end to end encryption for example.
    6. The reverse engineering effort by our team may be useful to outside developers looking to understand how similar services work.
    7. The Discord protocol, despite its API complexity, is quite simple and linear. No complex conflict resolution like Matrix, for example.

??? info "Editing the database is annoying, is there a graphical interface for this?"

    Currently no, there is no graphical interface for managing your {{ name }} instance.
    An admin dashboard is planned, but we currently have higher priorities right now.

??? info "When will this feature be available?"

    We do not provide ETAs. Users tend to take them as deadlines, and for a small team of <5 maintainers
    who do not get payment for their work, this is unreasonable.

??? info "It's pretty funny how you have a Discord.com guild for support."

    We know. Also that's not a question.
