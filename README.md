# libZwami
A java library for converting to and from the Zwami date format

# Zwami
*Zwami* is a constructed date format created and optimized for ease-of-organization and size-efficiency, it only uses six characters and it is easily organised by alphanumerical order.

*Zwami* is generally in the format of **MCDYmd** where:

**M** is the nth millenium since the beginning of the Era (since year 1)

**C** is the nth century of M starting from 1 ending with A (explained below)

**D** is the nth decade of C starting from 1 ending with A

**Y** is the nth year of D starting from 1 ending with A

**m** is the month of Y starting from 1 ending with C

**d** is the day of m starting from 1 ending with V on months with 31 days and U on months with 30 days, and so on and so forth.

Because we are aiming for a small, compact date format, it's best to use one-digit per piece of information, in order to achieve this, we have to use a base32 number system, specifically, the [base32hex system](https://en.wikipedia.org/wiki/Base32#base32hex).

Examples:

1999-04-09 becomes 2AAA49

2001-09-11 becomes 31129B

2015-12-19 becomes 3126CJ

1969-07-16 becomes 2A7A7G

in alphanumerical order, they become:

2A7A7G, 2AAA49, 31129B, 3126CJ
