.. default-domain:: nscp

.. module:: NSClientServer
    :synopsis: A server that listens for incoming check_nt connection and processes incoming requests.

===========================================
:module:`NSClientServer` --- NSClientServer
===========================================
A server that listens for incoming check_nt connection and processes incoming requests.





**Commands (Overview)**: 

**TODO:** Add a list of all external commands (this is not check commands)

**Configuration (Overview)**:


Common Keys:

.. csv-table:: 
    :class: contentstable 
    :delim: | 
    :header: "Path / Section", "Key", "Description"

    :confpath:`/settings/default` | :confkey:`~/settings/default.allowed hosts` | ALLOWED HOSTS
    :confpath:`/settings/default` | :confkey:`~/settings/default.bind to` | BIND TO ADDRESS
    :confpath:`/settings/default` | :confkey:`~/settings/default.cache allowed hosts` | CACHE ALLOWED HOSTS
    :confpath:`/settings/default` | :confkey:`~/settings/default.inbox` | INBOX
    :confpath:`/settings/default` | :confkey:`~/settings/default.password` | PASSWORD
    :confpath:`/settings/default` | :confkey:`~/settings/default.timeout` | TIMEOUT
    :confpath:`/settings/NSClient/server` | :confkey:`~/settings/NSClient/server.performance data` | PERFORMANCE DATA
    :confpath:`/settings/NSClient/server` | :confkey:`~/settings/NSClient/server.port` | PORT NUMBER
    :confpath:`/settings/NSClient/server` | :confkey:`~/settings/NSClient/server.use ssl` | ENABLE SSL ENCRYPTION

Advanced keys:

.. csv-table:: 
    :class: contentstable 
    :delim: | 
    :header: "Path / Section", "Key", "Default Value", "Description"

    :confpath:`/settings/default` | :confkey:`~/settings/default.encoding` | NRPE PAYLOAD ENCODING
    :confpath:`/settings/default` | :confkey:`~/settings/default.socket queue size` | LISTEN QUEUE
    :confpath:`/settings/default` | :confkey:`~/settings/default.thread pool` | THREAD POOL
    :confpath:`/settings/NSClient/server` | :confkey:`~/settings/NSClient/server.allowed ciphers` | ALLOWED CIPHERS
    :confpath:`/settings/NSClient/server` | :confkey:`~/settings/NSClient/server.allowed hosts` | ALLOWED HOSTS
    :confpath:`/settings/NSClient/server` | :confkey:`~/settings/NSClient/server.bind to` | BIND TO ADDRESS
    :confpath:`/settings/NSClient/server` | :confkey:`~/settings/NSClient/server.ca` | CA
    :confpath:`/settings/NSClient/server` | :confkey:`~/settings/NSClient/server.cache allowed hosts` | CACHE ALLOWED HOSTS
    :confpath:`/settings/NSClient/server` | :confkey:`~/settings/NSClient/server.certificate` | SSL CERTIFICATE
    :confpath:`/settings/NSClient/server` | :confkey:`~/settings/NSClient/server.certificate format` | CERTIFICATE FORMAT
    :confpath:`/settings/NSClient/server` | :confkey:`~/settings/NSClient/server.certificate key` | SSL CERTIFICATE
    :confpath:`/settings/NSClient/server` | :confkey:`~/settings/NSClient/server.dh` | DH KEY
    :confpath:`/settings/NSClient/server` | :confkey:`~/settings/NSClient/server.password` | PASSWORD
    :confpath:`/settings/NSClient/server` | :confkey:`~/settings/NSClient/server.socket queue size` | LISTEN QUEUE
    :confpath:`/settings/NSClient/server` | :confkey:`~/settings/NSClient/server.ssl options` | VERIFY MODE
    :confpath:`/settings/NSClient/server` | :confkey:`~/settings/NSClient/server.thread pool` | THREAD POOL
    :confpath:`/settings/NSClient/server` | :confkey:`~/settings/NSClient/server.timeout` | TIMEOUT
    :confpath:`/settings/NSClient/server` | :confkey:`~/settings/NSClient/server.verify mode` | VERIFY MODE







… default
---------

.. confpath:: /settings/default
    :synopsis: 






    .. csv-table:: 
        :class: contentstable 
        :delim: | 
        :header: "Key", "Default Value", "Description"
    
        :confkey:`allowed hosts` | 127.0.0.1 | ALLOWED HOSTS
        :confkey:`bind to` |  | BIND TO ADDRESS
        :confkey:`cache allowed hosts` | 1 | CACHE ALLOWED HOSTS
        :confkey:`encoding` |  | NRPE PAYLOAD ENCODING
        :confkey:`inbox` | inbox | INBOX
        :confkey:`password` |  | PASSWORD
        :confkey:`socket queue size` | 0 | LISTEN QUEUE
        :confkey:`thread pool` | 10 | THREAD POOL
        :confkey:`timeout` | 30 | TIMEOUT

    **Sample**::

        # 
        # 
        [/settings/default]
        allowed hosts=127.0.0.1
        bind to=
        cache allowed hosts=1
        encoding=
        inbox=inbox
        password=
        socket queue size=0
        thread pool=10
        timeout=30


    .. confkey:: allowed hosts
        :synopsis: ALLOWED HOSTS

        **ALLOWED HOSTS**

        | A comaseparated list of allowed hosts. You can use netmasks (/ syntax) or * to create ranges.

        **Path**: /settings/default

        **Key**: allowed hosts

        **Default value**: 127.0.0.1

        **Used by**: :module:`CheckMKServer`,  :module:`NRPEServer`,  :module:`NSCAServer`,  :module:`NSClientServer`,  :module:`WEBServer`

        **Sample**::

            [/settings/default]
            # ALLOWED HOSTS
            allowed hosts=127.0.0.1


    .. confkey:: bind to
        :synopsis: BIND TO ADDRESS

        **BIND TO ADDRESS**

        | Allows you to bind server to a specific local address. This has to be a dotted ip address not a host name. Leaving this blank will bind to all available IP addresses.

        **Path**: /settings/default

        **Key**: bind to

        **Default value**: 

        **Used by**: :module:`CheckMKServer`,  :module:`NRPEServer`,  :module:`NSCAServer`,  :module:`NSClientServer`,  :module:`WEBServer`

        **Sample**::

            [/settings/default]
            # BIND TO ADDRESS
            bind to=


    .. confkey:: cache allowed hosts
        :synopsis: CACHE ALLOWED HOSTS

        **CACHE ALLOWED HOSTS**

        | If host names (DNS entries) should be cached, improves speed and security somewhat but won't allow you to have dynamic IPs for your Nagios server.

        **Path**: /settings/default

        **Key**: cache allowed hosts

        **Default value**: 1

        **Used by**: :module:`CheckMKServer`,  :module:`NRPEServer`,  :module:`NSCAServer`,  :module:`NSClientServer`,  :module:`WEBServer`

        **Sample**::

            [/settings/default]
            # CACHE ALLOWED HOSTS
            cache allowed hosts=1


    .. confkey:: encoding
        :synopsis: NRPE PAYLOAD ENCODING

        **NRPE PAYLOAD ENCODING**



        **Advanced** (means it is not commonly used)

        **Path**: /settings/default

        **Key**: encoding

        **Default value**: 

        **Used by**: :module:`CheckMKServer`,  :module:`NRPEServer`,  :module:`NSCAServer`,  :module:`NSClientServer`,  :module:`WEBServer`

        **Sample**::

            [/settings/default]
            # NRPE PAYLOAD ENCODING
            encoding=


    .. confkey:: inbox
        :synopsis: INBOX

        **INBOX**

        | The default channel to post incoming messages on

        **Path**: /settings/default

        **Key**: inbox

        **Default value**: inbox

        **Used by**: :module:`CheckMKServer`,  :module:`NRPEServer`,  :module:`NSCAServer`,  :module:`NSClientServer`,  :module:`WEBServer`

        **Sample**::

            [/settings/default]
            # INBOX
            inbox=inbox


    .. confkey:: password
        :synopsis: PASSWORD

        **PASSWORD**

        | Password used to authenticate against server

        **Path**: /settings/default

        **Key**: password

        **Default value**: 

        **Used by**: :module:`CheckMKServer`,  :module:`NRPEServer`,  :module:`NSCAServer`,  :module:`NSClientServer`,  :module:`WEBServer`

        **Sample**::

            [/settings/default]
            # PASSWORD
            password=


    .. confkey:: socket queue size
        :synopsis: LISTEN QUEUE

        **LISTEN QUEUE**

        | Number of sockets to queue before starting to refuse new incoming connections. This can be used to tweak the amount of simultaneous sockets that the server accepts.

        **Advanced** (means it is not commonly used)

        **Path**: /settings/default

        **Key**: socket queue size

        **Default value**: 0

        **Used by**: :module:`CheckMKServer`,  :module:`NRPEServer`,  :module:`NSCAServer`,  :module:`NSClientServer`,  :module:`WEBServer`

        **Sample**::

            [/settings/default]
            # LISTEN QUEUE
            socket queue size=0


    .. confkey:: thread pool
        :synopsis: THREAD POOL

        **THREAD POOL**



        **Advanced** (means it is not commonly used)

        **Path**: /settings/default

        **Key**: thread pool

        **Default value**: 10

        **Used by**: :module:`CheckMKServer`,  :module:`NRPEServer`,  :module:`NSCAServer`,  :module:`NSClientServer`,  :module:`WEBServer`

        **Sample**::

            [/settings/default]
            # THREAD POOL
            thread pool=10


    .. confkey:: timeout
        :synopsis: TIMEOUT

        **TIMEOUT**

        | Timeout when reading packets on incoming sockets. If the data has not arrived within this time we will bail out.

        **Path**: /settings/default

        **Key**: timeout

        **Default value**: 30

        **Used by**: :module:`CheckMKServer`,  :module:`NRPEServer`,  :module:`NSCAServer`,  :module:`NSClientServer`,  :module:`WEBServer`

        **Sample**::

            [/settings/default]
            # TIMEOUT
            timeout=30




… NSClient / server
-------------------

.. confpath:: /settings/NSClient/server
    :synopsis: NSCLIENT SERVER SECTION

**NSCLIENT SERVER SECTION**

    | Section for NSClient (NSClientServer.dll) (check_nt) protocol options.


    .. csv-table:: 
        :class: contentstable 
        :delim: | 
        :header: "Key", "Default Value", "Description"
    
        :confkey:`allowed ciphers` | ALL:!ADH:!LOW:!EXP:!MD5:@STRENGTH | ALLOWED CIPHERS
        :confkey:`allowed hosts` | 127.0.0.1 | ALLOWED HOSTS
        :confkey:`bind to` |  | BIND TO ADDRESS
        :confkey:`ca` | ${certificate-path}/ca.pem | CA
        :confkey:`cache allowed hosts` | 1 | CACHE ALLOWED HOSTS
        :confkey:`certificate` | ${certificate-path}/certificate.pem | SSL CERTIFICATE
        :confkey:`certificate format` | PEM | CERTIFICATE FORMAT
        :confkey:`certificate key` |  | SSL CERTIFICATE
        :confkey:`dh` | ${certificate-path}/nrpe_dh_512.pem | DH KEY
        :confkey:`password` |  | PASSWORD
        :confkey:`performance data` | 1 | PERFORMANCE DATA
        :confkey:`port` | 12489 | PORT NUMBER
        :confkey:`socket queue size` | 0 | LISTEN QUEUE
        :confkey:`ssl options` |  | VERIFY MODE
        :confkey:`thread pool` | 10 | THREAD POOL
        :confkey:`timeout` | 30 | TIMEOUT
        :confkey:`use ssl` | 0 | ENABLE SSL ENCRYPTION
        :confkey:`verify mode` | none | VERIFY MODE

    **Sample**::

        # NSCLIENT SERVER SECTION
        # Section for NSClient (NSClientServer.dll) (check_nt) protocol options.
        [/settings/NSClient/server]
        allowed ciphers=ALL:!ADH:!LOW:!EXP:!MD5:@STRENGTH
        allowed hosts=127.0.0.1
        bind to=
        ca=${certificate-path}/ca.pem
        cache allowed hosts=1
        certificate=${certificate-path}/certificate.pem
        certificate format=PEM
        certificate key=
        dh=${certificate-path}/nrpe_dh_512.pem
        password=
        performance data=1
        port=12489
        socket queue size=0
        ssl options=
        thread pool=10
        timeout=30
        use ssl=0
        verify mode=none


    .. confkey:: allowed ciphers
        :synopsis: ALLOWED CIPHERS

        **ALLOWED CIPHERS**

        | The chipers which are allowed to be used.
        | The default here will differ is used in "insecure" mode or not. check_nrpe uses a very old chipers and should preferably not be used. For details of chipers please see the OPEN ssl documentation: https://www.openssl.org/docs/apps/ciphers.html

        **Advanced** (means it is not commonly used)

        **Path**: /settings/NSClient/server

        **Key**: allowed ciphers

        **Default value**: ALL:!ADH:!LOW:!EXP:!MD5:@STRENGTH

        **Used by**: :module:`NSClientServer`

        **Sample**::

            [/settings/NSClient/server]
            # ALLOWED CIPHERS
            allowed ciphers=ALL:!ADH:!LOW:!EXP:!MD5:@STRENGTH


    .. confkey:: allowed hosts
        :synopsis: ALLOWED HOSTS

        **ALLOWED HOSTS**

        | A comaseparated list of allowed hosts. You can use netmasks (/ syntax) or * to create ranges. parent for this key is found under: /settings/default this is marked as advanced in favor of the parent.

        **Advanced** (means it is not commonly used)

        **Path**: /settings/NSClient/server

        **Key**: allowed hosts

        **Default value**: 127.0.0.1

        **Used by**: :module:`NSClientServer`

        **Sample**::

            [/settings/NSClient/server]
            # ALLOWED HOSTS
            allowed hosts=127.0.0.1


    .. confkey:: bind to
        :synopsis: BIND TO ADDRESS

        **BIND TO ADDRESS**

        | Allows you to bind server to a specific local address. This has to be a dotted ip address not a host name. Leaving this blank will bind to all available IP addresses. parent for this key is found under: /settings/default this is marked as advanced in favor of the parent.

        **Advanced** (means it is not commonly used)

        **Path**: /settings/NSClient/server

        **Key**: bind to

        **Default value**: 

        **Used by**: :module:`NSClientServer`

        **Sample**::

            [/settings/NSClient/server]
            # BIND TO ADDRESS
            bind to=


    .. confkey:: ca
        :synopsis: CA

        **CA**



        **Advanced** (means it is not commonly used)

        **Path**: /settings/NSClient/server

        **Key**: ca

        **Default value**: ${certificate-path}/ca.pem

        **Used by**: :module:`NSClientServer`

        **Sample**::

            [/settings/NSClient/server]
            # CA
            ca=${certificate-path}/ca.pem


    .. confkey:: cache allowed hosts
        :synopsis: CACHE ALLOWED HOSTS

        **CACHE ALLOWED HOSTS**

        | If host names (DNS entries) should be cached, improves speed and security somewhat but won't allow you to have dynamic IPs for your Nagios server. parent for this key is found under: /settings/default this is marked as advanced in favor of the parent.

        **Advanced** (means it is not commonly used)

        **Path**: /settings/NSClient/server

        **Key**: cache allowed hosts

        **Default value**: 1

        **Used by**: :module:`NSClientServer`

        **Sample**::

            [/settings/NSClient/server]
            # CACHE ALLOWED HOSTS
            cache allowed hosts=1


    .. confkey:: certificate
        :synopsis: SSL CERTIFICATE

        **SSL CERTIFICATE**



        **Advanced** (means it is not commonly used)

        **Path**: /settings/NSClient/server

        **Key**: certificate

        **Default value**: ${certificate-path}/certificate.pem

        **Used by**: :module:`NSClientServer`

        **Sample**::

            [/settings/NSClient/server]
            # SSL CERTIFICATE
            certificate=${certificate-path}/certificate.pem


    .. confkey:: certificate format
        :synopsis: CERTIFICATE FORMAT

        **CERTIFICATE FORMAT**



        **Advanced** (means it is not commonly used)

        **Path**: /settings/NSClient/server

        **Key**: certificate format

        **Default value**: PEM

        **Used by**: :module:`NSClientServer`

        **Sample**::

            [/settings/NSClient/server]
            # CERTIFICATE FORMAT
            certificate format=PEM


    .. confkey:: certificate key
        :synopsis: SSL CERTIFICATE

        **SSL CERTIFICATE**



        **Advanced** (means it is not commonly used)

        **Path**: /settings/NSClient/server

        **Key**: certificate key

        **Default value**: 

        **Used by**: :module:`NSClientServer`

        **Sample**::

            [/settings/NSClient/server]
            # SSL CERTIFICATE
            certificate key=


    .. confkey:: dh
        :synopsis: DH KEY

        **DH KEY**



        **Advanced** (means it is not commonly used)

        **Path**: /settings/NSClient/server

        **Key**: dh

        **Default value**: ${certificate-path}/nrpe_dh_512.pem

        **Used by**: :module:`NSClientServer`

        **Sample**::

            [/settings/NSClient/server]
            # DH KEY
            dh=${certificate-path}/nrpe_dh_512.pem


    .. confkey:: password
        :synopsis: PASSWORD

        **PASSWORD**

        | Password used to authenticate against server parent for this key is found under: /settings/default this is marked as advanced in favor of the parent.

        **Advanced** (means it is not commonly used)

        **Path**: /settings/NSClient/server

        **Key**: password

        **Default value**: 

        **Used by**: :module:`NSClientServer`

        **Sample**::

            [/settings/NSClient/server]
            # PASSWORD
            password=


    .. confkey:: performance data
        :synopsis: PERFORMANCE DATA

        **PERFORMANCE DATA**

        | Send performance data back to Nagios (set this to 0 to remove all performance data).

        **Path**: /settings/NSClient/server

        **Key**: performance data

        **Default value**: 1

        **Used by**: :module:`NSClientServer`

        **Sample**::

            [/settings/NSClient/server]
            # PERFORMANCE DATA
            performance data=1


    .. confkey:: port
        :synopsis: PORT NUMBER

        **PORT NUMBER**

        | Port to use for check_nt.

        **Path**: /settings/NSClient/server

        **Key**: port

        **Default value**: 12489

        **Used by**: :module:`NSClientServer`

        **Sample**::

            [/settings/NSClient/server]
            # PORT NUMBER
            port=12489


    .. confkey:: socket queue size
        :synopsis: LISTEN QUEUE

        **LISTEN QUEUE**

        | Number of sockets to queue before starting to refuse new incoming connections. This can be used to tweak the amount of simultaneous sockets that the server accepts. parent for this key is found under: /settings/default this is marked as advanced in favor of the parent.

        **Advanced** (means it is not commonly used)

        **Path**: /settings/NSClient/server

        **Key**: socket queue size

        **Default value**: 0

        **Used by**: :module:`NSClientServer`

        **Sample**::

            [/settings/NSClient/server]
            # LISTEN QUEUE
            socket queue size=0


    .. confkey:: ssl options
        :synopsis: VERIFY MODE

        **VERIFY MODE**

        | Comma separated list of verification flags to set on the SSL socket.

          ==================== ==================================================================================================================================================================================================================================== 
          default-workarounds  Various workarounds for what I understand to be broken ssl implementations                                                                                                                                                           
          -------------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ 
          no-sslv2             Do not use the SSLv2 protocol.                                                                                                                                                                                                       
          no-sslv3             Do not use the SSLv3 protocol.                                                                                                                                                                                                       
          no-tlsv1             Do not use the TLSv1 protocol.                                                                                                                                                                                                       
          single-dh-use        Always create a new key when using temporary/ephemeral DH parameters. This option must be used to prevent small subgroup attacks, when the DH parameters were not generated using "strong" primes (e.g. when using DSA-parameters).  
          ==================== ====================================================================================================================================================================================================================================





        **Advanced** (means it is not commonly used)

        **Path**: /settings/NSClient/server

        **Key**: ssl options

        **Default value**: 

        **Used by**: :module:`NSClientServer`

        **Sample**::

            [/settings/NSClient/server]
            # VERIFY MODE
            ssl options=


    .. confkey:: thread pool
        :synopsis: THREAD POOL

        **THREAD POOL**

        | parent for this key is found under: /settings/default this is marked as advanced in favor of the parent.

        **Advanced** (means it is not commonly used)

        **Path**: /settings/NSClient/server

        **Key**: thread pool

        **Default value**: 10

        **Used by**: :module:`NSClientServer`

        **Sample**::

            [/settings/NSClient/server]
            # THREAD POOL
            thread pool=10


    .. confkey:: timeout
        :synopsis: TIMEOUT

        **TIMEOUT**

        | Timeout when reading packets on incoming sockets. If the data has not arrived within this time we will bail out. parent for this key is found under: /settings/default this is marked as advanced in favor of the parent.

        **Advanced** (means it is not commonly used)

        **Path**: /settings/NSClient/server

        **Key**: timeout

        **Default value**: 30

        **Used by**: :module:`NSClientServer`

        **Sample**::

            [/settings/NSClient/server]
            # TIMEOUT
            timeout=30


    .. confkey:: use ssl
        :synopsis: ENABLE SSL ENCRYPTION

        **ENABLE SSL ENCRYPTION**

        | This option controls if SSL should be enabled.

        **Path**: /settings/NSClient/server

        **Key**: use ssl

        **Default value**: 0

        **Used by**: :module:`NSClientServer`

        **Sample**::

            [/settings/NSClient/server]
            # ENABLE SSL ENCRYPTION
            use ssl=0


    .. confkey:: verify mode
        :synopsis: VERIFY MODE

        **VERIFY MODE**

        | Comma separated list of verification flags to set on the SSL socket.

          ================ ======================================================================================================================================== 
          none             The server will not send a client certificate request to the client, so the client will not send a certificate.                          
          ---------------- ---------------------------------------------------------------------------------------------------------------------------------------- 
          peer             The server sends a client certificate request to the client and the certificate returned (if any) is checked.                            
          fail-if-no-cert  if the client did not return a certificate, the TLS/SSL handshake is immediately terminated. This flag must be used together with peer.  
          peer-cert        Alias for peer and fail-if-no-cert.                                                                                                      
          workarounds      Various bug workarounds.                                                                                                                 
          single           Always create a new key when using tmp_dh parameters.                                                                                    
          client-once      Only request a client certificate on the initial TLS/SSL handshake. This flag must be used together with verify-peer                     
          ================ ========================================================================================================================================





        **Advanced** (means it is not commonly used)

        **Path**: /settings/NSClient/server

        **Key**: verify mode

        **Default value**: none

        **Used by**: :module:`NSClientServer`

        **Sample**::

            [/settings/NSClient/server]
            # VERIFY MODE
            verify mode=none


