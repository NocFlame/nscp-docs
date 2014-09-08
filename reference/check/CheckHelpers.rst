.. default-domain:: nscp

.. module:: CheckHelpers
    :synopsis: Various helper function to extend other checks.

=======================================
:module:`CheckHelpers` --- CheckHelpers
=======================================
Various helper function to extend other checks.

**Queries (Overview)**:

A list of all avalible queries (check commands)

.. csv-table:: 
    :class: contentstable 
    :delim: | 
    :header: "Command", "Description"

    :query:`check_always_critical` | Run another check and regardless of its return code return CRITICAL.
    :query:`check_always_ok` | Run another check and regardless of its return code return OK.
    :query:`check_always_warning` | Run another check and regardless of its return code return WARNING.
    :query:`check_critical` | Just return CRITICAL (anything passed along will be used as a message).
    :query:`check_multi` | Run more then one check and return the worst state.
    :query:`check_negate` | Run a check and alter the return status codes according to arguments.
    :query:`check_ok` | Just return OK (anything passed along will be used as a message).
    :query:`check_timeout` | Run a check and timeout after a given amount of time if the check has not returned.
    :query:`check_version` | Just return the NSClient++ version.
    :query:`check_warning` | Just return WARNING (anything passed along will be used as a message).
    :query:`filter_perf` | Run a check and filter performance data.


**Aliases (Overview)**:

A list of all short hand aliases for queries (check commands)



.. csv-table:: 
    :class: contentstable 
    :delim: | 
    :header: "Command", "Description"

    checkalwayscritical | Alias for: :query:`check_always_critical`
    checkalwaysok | Alias for: :query:`check_always_ok`
    checkalwayswarning | Alias for: :query:`check_always_warning`
    checkcritical | Alias for: :query:`check_critical`
    checkmultiple | Alias for: :query:`check_multi`
    checkok | Alias for: :query:`check_ok`
    checkversion | Alias for: :query:`check_version`
    checkwarning | Alias for: :query:`check_warning`
    negate | Alias for: :query:`check_negate`
    timeout | Alias for: :query:`check_timeout`


**Commands (Overview)**: 

**TODO:** Add a list of all external commands (this is not check commands)



Queries
=======
A quick reference for all avalible queries (check commands) in the CheckHelpers module.

:query:`check_always_critical`
------------------------------
.. query:: check_always_critical
    :synopsis: Run another check and regardless of its return code return CRITICAL.

**Usage:**



.. csv-table:: 
    :class: contentstable 
    :delim: | 
    :header: "Option", "Default Value", "Description"

    :option:`help` | N/A | Show help screen (this screen)
    :option:`help-pb` | N/A | Show help screen as a protocol buffer payload
    :option:`help-short` | N/A | Show help screen (short format).


Arguments
*********
.. option:: help
    :synopsis: Show help screen (this screen)

    | Show help screen (this screen)

.. option:: help-pb
    :synopsis: Show help screen as a protocol buffer payload

    | Show help screen as a protocol buffer payload

.. option:: help-short
    :synopsis: Show help screen (short format).

    | Show help screen (short format).


:query:`check_always_ok`
------------------------
.. query:: check_always_ok
    :synopsis: Run another check and regardless of its return code return OK.

**Usage:**



.. csv-table:: 
    :class: contentstable 
    :delim: | 
    :header: "Option", "Default Value", "Description"

    :option:`help` | N/A | Show help screen (this screen)
    :option:`help-pb` | N/A | Show help screen as a protocol buffer payload
    :option:`help-short` | N/A | Show help screen (short format).


Arguments
*********
.. option:: help
    :synopsis: Show help screen (this screen)

    | Show help screen (this screen)

.. option:: help-pb
    :synopsis: Show help screen as a protocol buffer payload

    | Show help screen as a protocol buffer payload

.. option:: help-short
    :synopsis: Show help screen (short format).

    | Show help screen (short format).


:query:`check_always_warning`
-----------------------------
.. query:: check_always_warning
    :synopsis: Run another check and regardless of its return code return WARNING.

**Usage:**



.. csv-table:: 
    :class: contentstable 
    :delim: | 
    :header: "Option", "Default Value", "Description"

    :option:`help` | N/A | Show help screen (this screen)
    :option:`help-pb` | N/A | Show help screen as a protocol buffer payload
    :option:`help-short` | N/A | Show help screen (short format).


Arguments
*********
.. option:: help
    :synopsis: Show help screen (this screen)

    | Show help screen (this screen)

.. option:: help-pb
    :synopsis: Show help screen as a protocol buffer payload

    | Show help screen as a protocol buffer payload

.. option:: help-short
    :synopsis: Show help screen (short format).

    | Show help screen (short format).


:query:`check_critical`
-----------------------
.. query:: check_critical
    :synopsis: Just return CRITICAL (anything passed along will be used as a message).

**Usage:**



.. csv-table:: 
    :class: contentstable 
    :delim: | 
    :header: "Option", "Default Value", "Description"

    :option:`help` | N/A | Show help screen (this screen)
    :option:`help-pb` | N/A | Show help screen as a protocol buffer payload
    :option:`help-short` | N/A | Show help screen (short format).


Arguments
*********
.. option:: help
    :synopsis: Show help screen (this screen)

    | Show help screen (this screen)

.. option:: help-pb
    :synopsis: Show help screen as a protocol buffer payload

    | Show help screen as a protocol buffer payload

.. option:: help-short
    :synopsis: Show help screen (short format).

    | Show help screen (short format).


:query:`check_multi`
--------------------
.. query:: check_multi
    :synopsis: Run more then one check and return the worst state.

**Usage:**



.. csv-table:: 
    :class: contentstable 
    :delim: | 
    :header: "Option", "Default Value", "Description"

    :option:`help` | N/A | Show help screen (this screen)
    :option:`help-pb` | N/A | Show help screen as a protocol buffer payload
    :option:`help-short` | N/A | Show help screen (short format).
    :option:`command` |  | Commands to run (can be used multiple times)
    :option:`arguments` |  | Deprecated alias for command
    :option:`separator` | ,  | Separator between messages
    :option:`prefix` |  | Message prefix
    :option:`suffix` |  | Message suffix


Arguments
*********
.. option:: help
    :synopsis: Show help screen (this screen)

    | Show help screen (this screen)

.. option:: help-pb
    :synopsis: Show help screen as a protocol buffer payload

    | Show help screen as a protocol buffer payload

.. option:: help-short
    :synopsis: Show help screen (short format).

    | Show help screen (short format).

.. option:: command
    :synopsis: Commands to run (can be used multiple times)

    | Commands to run (can be used multiple times)

.. option:: arguments
    :synopsis: Deprecated alias for command

    | Deprecated alias for command

.. option:: separator
    :synopsis: Separator between messages

    | Separator between messages

.. option:: prefix
    :synopsis: Message prefix

    | Message prefix

.. option:: suffix
    :synopsis: Message suffix

    | Message suffix


:query:`check_negate`
---------------------
.. query:: check_negate
    :synopsis: Run a check and alter the return status codes according to arguments.

**Usage:**



.. csv-table:: 
    :class: contentstable 
    :delim: | 
    :header: "Option", "Default Value", "Description"

    :option:`help` | N/A | Show help screen (this screen)
    :option:`help-pb` | N/A | Show help screen as a protocol buffer payload
    :option:`help-short` | N/A | Show help screen (short format).
    :option:`ok` |  | The state to return instead of OK
    :option:`warning` |  | The state to return instead of WARNING
    :option:`critical` |  | The state to return instead of CRITICAL
    :option:`unknown` |  | The state to return instead of UNKNOWN
    :option:`command` |  | Wrapped command to execute
    :option:`arguments` |  | List of arguments (for wrapped command)


Arguments
*********
.. option:: help
    :synopsis: Show help screen (this screen)

    | Show help screen (this screen)

.. option:: help-pb
    :synopsis: Show help screen as a protocol buffer payload

    | Show help screen as a protocol buffer payload

.. option:: help-short
    :synopsis: Show help screen (short format).

    | Show help screen (short format).

.. option:: ok
    :synopsis: The state to return instead of OK

    | The state to return instead of OK

.. option:: warning
    :synopsis: The state to return instead of WARNING

    | The state to return instead of WARNING

.. option:: critical
    :synopsis: The state to return instead of CRITICAL

    | The state to return instead of CRITICAL

.. option:: unknown
    :synopsis: The state to return instead of UNKNOWN

    | The state to return instead of UNKNOWN

.. option:: command
    :synopsis: Wrapped command to execute

    | Wrapped command to execute

.. option:: arguments
    :synopsis: List of arguments (for wrapped command)

    | List of arguments (for wrapped command)


:query:`check_ok`
-----------------
.. query:: check_ok
    :synopsis: Just return OK (anything passed along will be used as a message).

**Usage:**



.. csv-table:: 
    :class: contentstable 
    :delim: | 
    :header: "Option", "Default Value", "Description"

    :option:`help` | N/A | Show help screen (this screen)
    :option:`help-pb` | N/A | Show help screen as a protocol buffer payload
    :option:`help-short` | N/A | Show help screen (short format).


Arguments
*********
.. option:: help
    :synopsis: Show help screen (this screen)

    | Show help screen (this screen)

.. option:: help-pb
    :synopsis: Show help screen as a protocol buffer payload

    | Show help screen as a protocol buffer payload

.. option:: help-short
    :synopsis: Show help screen (short format).

    | Show help screen (short format).


:query:`check_timeout`
----------------------
.. query:: check_timeout
    :synopsis: Run a check and timeout after a given amount of time if the check has not returned.

**Usage:**



.. csv-table:: 
    :class: contentstable 
    :delim: | 
    :header: "Option", "Default Value", "Description"

    :option:`help` | N/A | Show help screen (this screen)
    :option:`help-pb` | N/A | Show help screen as a protocol buffer payload
    :option:`help-short` | N/A | Show help screen (short format).
    :option:`timeout` |  | The timeout value
    :option:`command` |  | Wrapped command to execute
    :option:`arguments` |  | List of arguments (for wrapped command)
    :option:`return` |  | The return status


Arguments
*********
.. option:: help
    :synopsis: Show help screen (this screen)

    | Show help screen (this screen)

.. option:: help-pb
    :synopsis: Show help screen as a protocol buffer payload

    | Show help screen as a protocol buffer payload

.. option:: help-short
    :synopsis: Show help screen (short format).

    | Show help screen (short format).

.. option:: timeout
    :synopsis: The timeout value

    | The timeout value

.. option:: command
    :synopsis: Wrapped command to execute

    | Wrapped command to execute

.. option:: arguments
    :synopsis: List of arguments (for wrapped command)

    | List of arguments (for wrapped command)

.. option:: return
    :synopsis: The return status

    | The return status


:query:`check_version`
----------------------
.. query:: check_version
    :synopsis: Just return the NSClient++ version.

**Usage:**





Arguments
*********

:query:`check_warning`
----------------------
.. query:: check_warning
    :synopsis: Just return WARNING (anything passed along will be used as a message).

**Usage:**



.. csv-table:: 
    :class: contentstable 
    :delim: | 
    :header: "Option", "Default Value", "Description"

    :option:`help` | N/A | Show help screen (this screen)
    :option:`help-pb` | N/A | Show help screen as a protocol buffer payload
    :option:`help-short` | N/A | Show help screen (short format).


Arguments
*********
.. option:: help
    :synopsis: Show help screen (this screen)

    | Show help screen (this screen)

.. option:: help-pb
    :synopsis: Show help screen as a protocol buffer payload

    | Show help screen as a protocol buffer payload

.. option:: help-short
    :synopsis: Show help screen (short format).

    | Show help screen (short format).


:query:`filter_perf`
--------------------
.. query:: filter_perf
    :synopsis: Run a check and filter performance data.

**Usage:**



.. csv-table:: 
    :class: contentstable 
    :delim: | 
    :header: "Option", "Default Value", "Description"

    :option:`help` | N/A | Show help screen (this screen)
    :option:`help-pb` | N/A | Show help screen as a protocol buffer payload
    :option:`help-short` | N/A | Show help screen (short format).
    :option:`sort` | none | The sort order to use: none, normal or reversed
    :option:`limit` | 0 | The maximum number of items to return (0 returns all items)
    :option:`command` |  | Wrapped command to execute
    :option:`arguments` |  | List of arguments (for wrapped command)


Arguments
*********
.. option:: help
    :synopsis: Show help screen (this screen)

    | Show help screen (this screen)

.. option:: help-pb
    :synopsis: Show help screen as a protocol buffer payload

    | Show help screen as a protocol buffer payload

.. option:: help-short
    :synopsis: Show help screen (short format).

    | Show help screen (short format).

.. option:: sort
    :synopsis: The sort order to use: none, normal or reversed

    | The sort order to use: none, normal or reversed

.. option:: limit
    :synopsis: The maximum number of items to return (0 returns all items)

    | The maximum number of items to return (0 returns all items)

.. option:: command
    :synopsis: Wrapped command to execute

    | Wrapped command to execute

.. option:: arguments
    :synopsis: List of arguments (for wrapped command)

    | List of arguments (for wrapped command)



