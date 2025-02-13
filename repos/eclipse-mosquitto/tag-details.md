<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eclipse-mosquitto`

-	[`eclipse-mosquitto:1.6-openssl`](#eclipse-mosquitto16-openssl)
-	[`eclipse-mosquitto:1.6.15-openssl`](#eclipse-mosquitto1615-openssl)
-	[`eclipse-mosquitto:2`](#eclipse-mosquitto2)
-	[`eclipse-mosquitto:2-openssl`](#eclipse-mosquitto2-openssl)
-	[`eclipse-mosquitto:2.0`](#eclipse-mosquitto20)
-	[`eclipse-mosquitto:2.0-openssl`](#eclipse-mosquitto20-openssl)
-	[`eclipse-mosquitto:2.0.20`](#eclipse-mosquitto2020)
-	[`eclipse-mosquitto:2.0.20-openssl`](#eclipse-mosquitto2020-openssl)
-	[`eclipse-mosquitto:latest`](#eclipse-mosquittolatest)
-	[`eclipse-mosquitto:openssl`](#eclipse-mosquittoopenssl)

## `eclipse-mosquitto:1.6-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:a6e456ccc4685c5f0ab716cf70346ad44e729b3fa5b655c73d326b4d0085b207
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-mosquitto:1.6-openssl` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:ce8eb21f19fc0909608c9f53059beaba1420e898d4d7daa3371f9078c4c2e5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4058621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad05bd77f856d91b5fbc367b377b6ac53d7038e607f4856100966c8abd3a19b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:f54a5150a7602eaef3169b83e73d5927b20aef2fcaefcba18b532bd63b328fff`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3417974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f0d03dd32ee39939df7770bba7d904bd709a485e9cdb2dc1db7e78e70ff5f0`  
		Last Modified: Wed, 15 Jan 2025 06:00:08 GMT  
		Size: 640.4 KB (640407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb10d18cc52fc60af7a95dea4478ee169b57d8abd94e5a1719636178b52a6fb8`  
		Last Modified: Wed, 15 Jan 2025 06:00:07 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:31651bc01c3ab90e3897b9a8d94353d1d4d54f5184e7f9f38838ce11add0230d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 KB (198034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5da65fe19663db58a36b88ca25cc3635a20d92bc4221178559c221f08552e2`

```dockerfile
```

-	Layers:
	-	`sha256:85d5faacd6311be7f2c516fb1877f94247b942f53d9e039ce28388a6ef10e0c5`  
		Last Modified: Wed, 08 Jan 2025 17:58:35 GMT  
		Size: 177.9 KB (177924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83ea76b909a5c737245e1d0ca151c39b98ea23c555b3737830930da751977328`  
		Last Modified: Wed, 08 Jan 2025 17:58:35 GMT  
		Size: 20.1 KB (20110 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:92d1d26311297d03436e954ef1efc1bbd2e7e4508955a80654390e266d62bfb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd8e9df88f2dd19ad0ae3b7879d6b96abe99196d6a0742ae3a984c3ca0d0d82`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.18.11-armhf.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:803cf02755db9f4dbb0d52a3ff280052dd523cdfdb9e9be6494b4edd548d6dc6`  
		Last Modified: Tue, 14 Jan 2025 20:51:05 GMT  
		Size: 3.2 MB (3159977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982b4b3ea73f68baba7ae3131ab8972a5325a591cbf845eec376248bb0428fab`  
		Last Modified: Wed, 15 Jan 2025 13:20:37 GMT  
		Size: 614.1 KB (614120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2043f80c50b150209283a57636fd4e9d248e3ccaed373fc47209e8841e3d6f6e`  
		Last Modified: Tue, 07 Jan 2025 04:52:57 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:597593beb9589da97bc89d16690a60845cc493d830190abbb99b208e42ad9333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (19957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a62bfb0802bf2a88e530f6ece44053a0f0ea2ad5975a3d921ebd306bfec733`

```dockerfile
```

-	Layers:
	-	`sha256:17a6401dfe8bb43f892c70a369a8cb56fc503096c24df8e1a5cbd30cd0956f69`  
		Last Modified: Wed, 08 Jan 2025 18:22:06 GMT  
		Size: 20.0 KB (19957 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:563ea4312bdb4615ac4b61e862aaf54ea5e918fa057796b8576ece5cf5bf557c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3982582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27bbeac0200f02e2f4024e1c228a1a125e5b270d8fa7ff006b919658b42cae4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.18.11-aarch64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:f6b431426dd566e612639f03cd46e521b3133a043bb6b60edeeeef80d513e870`  
		Last Modified: Tue, 14 Jan 2025 20:34:06 GMT  
		Size: 3.3 MB (3341861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee833ac9acdbb04195dd00e61acb3c37feab6edbf90d860d24acb543ed2d4070`  
		Last Modified: Thu, 13 Feb 2025 17:13:01 GMT  
		Size: 640.5 KB (640482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13edf7e5f27c66f05853eb65be343799c26ca7694b868b439084f54afaa12475`  
		Last Modified: Sat, 08 Feb 2025 03:58:27 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:507260262d65eb48c0c5ef9a52cd5b714c47f56243043f54efa58e8fe6c79c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 KB (198148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0624cec73ee6893372fa0ddaa6dec1ebc09480589cff94118b2e2b4e910ed1`

```dockerfile
```

-	Layers:
	-	`sha256:0d64989292eb0e6d1852a9cc2e725038f3f9656f5ca37fd7a524ef44e7d7a139`  
		Last Modified: Wed, 08 Jan 2025 18:23:38 GMT  
		Size: 178.0 KB (177956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df2ffb5d5d9066c4d21acfed7b025660c258980afe69f50fbb756b162c7268cc`  
		Last Modified: Wed, 08 Jan 2025 18:23:38 GMT  
		Size: 20.2 KB (20192 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:f07bf2d484807d5d470c0931b2e83cfd290b603503ac2e4c2a6861cf340bfa35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3918594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2ed95744d43336d8d46d09d578bac60ae0eed85b20b808c53fc864cb34f1a6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.18.11-x86.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:bd5e0f642fd4fa0e53e323e5bdaa4e3ef6549fc49ad76da06114328d35f9e4ce`  
		Last Modified: Tue, 14 Jan 2025 21:24:43 GMT  
		Size: 3.3 MB (3251158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901be931a6394e45abeedbf57d2426812cc5be6fc578ef0948a3ed26f9255c80`  
		Last Modified: Wed, 08 Jan 2025 17:58:33 GMT  
		Size: 667.2 KB (667196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51dd60c5a4556ebe2cfb2a698d56eb62a8f7db4fe7fa68503df980e7eb07ed4`  
		Last Modified: Wed, 08 Jan 2025 17:58:33 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:83087574c9443a61bb1500e509c1f496a73062a4f927c21aecf4d73b267c25b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 KB (197999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d317ac455c7e2a2a69021d3925fc3fbe6d0fb48befce649c1e05221b1caae54`

```dockerfile
```

-	Layers:
	-	`sha256:5ff6ccfb377f1fd5d43bb705e5b4b65ad391c6bfe19e697609372ef798d3fefd`  
		Last Modified: Wed, 08 Jan 2025 17:58:33 GMT  
		Size: 177.9 KB (177909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b34fb12ac3847333d72c1d665daa5a06526edaa8315cde4feb3085ae4eb4797c`  
		Last Modified: Wed, 08 Jan 2025 17:58:33 GMT  
		Size: 20.1 KB (20090 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:1495752c821a478383534113a8b038089f20d95c0c053c9ed9c34f9353713b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4052404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d694e002c2926b3b7bafb4f4a542eaf984898c5749a8d75d7dc935adfa1913a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.18.11-ppc64le.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:6259f25643973acaf5182679ac24f10e7bcb8be462646ba81a87b013ec80c9ed`  
		Last Modified: Tue, 14 Jan 2025 20:33:51 GMT  
		Size: 3.4 MB (3359277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d88f4d5ff3aba0143ceeb4b35d96a14689b35da7dce37ffbde6802203077de`  
		Last Modified: Wed, 08 Jan 2025 18:17:21 GMT  
		Size: 692.9 KB (692887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc4ec82c8cb3a28d72fdf0ab9bd50c6db4c2df47918f40174b0120e8c07588c`  
		Last Modified: Wed, 08 Jan 2025 18:17:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:a7fded12d01b0051e11539c0a47448b6b84352ea4dea68e99023f0015053d1b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 KB (196139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be610c1314e52b1fca9d49b8da12ec182d97f376b3dee88ff924b4e32702911d`

```dockerfile
```

-	Layers:
	-	`sha256:730d0b870a5669e94b258110d49cca120f6c3d5616dbc2acb38343003b0ce6a2`  
		Last Modified: Wed, 08 Jan 2025 18:17:20 GMT  
		Size: 176.0 KB (175995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b22a8c0d3c0cc55bdcd7fe5b5a02d14a146ce48410618b73dca3f0d66250eef9`  
		Last Modified: Wed, 08 Jan 2025 18:17:20 GMT  
		Size: 20.1 KB (20144 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6-openssl` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:b80975a3fca709805ff045f95856208642213087ec9637f33e76b8ab3b2ab7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3868871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e88922f2e996585b7ef52a749919f5d831b4e16874848c1e7fb1492ad0bde4f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.18.11-s390x.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:552c3aaa08429935d8dfef69ca747244fe854badcb537563677169e2f2ebdde8`  
		Last Modified: Tue, 14 Jan 2025 20:44:17 GMT  
		Size: 3.2 MB (3231849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebead2477ddcafc90a9290540a04baacc10e99e9f1956b9a8a9d939cf725c65e`  
		Last Modified: Wed, 08 Jan 2025 18:15:19 GMT  
		Size: 636.8 KB (636782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b26b9b2d77a8a1873370b956d1dc0b3a9896f6f1687529b2461d8e3c52e654a`  
		Last Modified: Wed, 08 Jan 2025 18:15:18 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:e39a19ae83074131cef12d643d0a8118145de50baf9441e24c29c9a79b7e34e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 KB (196085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3467e1d6ca16a4af198539bf15bc22ffa45cb397fc9ea44d1119878d56dda3f`

```dockerfile
```

-	Layers:
	-	`sha256:9b875552fb1c001194e0eaee0a279d33f5f01ecbfe08e5e12ef73e18b6ebe2b9`  
		Last Modified: Wed, 08 Jan 2025 18:15:19 GMT  
		Size: 176.0 KB (175973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3790355df5358a733a64c7fec9ffac19c0cd8ad140c672ff471b0907d050cd1b`  
		Last Modified: Wed, 08 Jan 2025 18:15:18 GMT  
		Size: 20.1 KB (20112 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:1.6.15-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:a6e456ccc4685c5f0ab716cf70346ad44e729b3fa5b655c73d326b4d0085b207
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-mosquitto:1.6.15-openssl` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:ce8eb21f19fc0909608c9f53059beaba1420e898d4d7daa3371f9078c4c2e5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4058621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad05bd77f856d91b5fbc367b377b6ac53d7038e607f4856100966c8abd3a19b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:f54a5150a7602eaef3169b83e73d5927b20aef2fcaefcba18b532bd63b328fff`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3417974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f0d03dd32ee39939df7770bba7d904bd709a485e9cdb2dc1db7e78e70ff5f0`  
		Last Modified: Wed, 15 Jan 2025 06:00:08 GMT  
		Size: 640.4 KB (640407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb10d18cc52fc60af7a95dea4478ee169b57d8abd94e5a1719636178b52a6fb8`  
		Last Modified: Wed, 15 Jan 2025 06:00:07 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6.15-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:31651bc01c3ab90e3897b9a8d94353d1d4d54f5184e7f9f38838ce11add0230d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 KB (198034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5da65fe19663db58a36b88ca25cc3635a20d92bc4221178559c221f08552e2`

```dockerfile
```

-	Layers:
	-	`sha256:85d5faacd6311be7f2c516fb1877f94247b942f53d9e039ce28388a6ef10e0c5`  
		Last Modified: Wed, 08 Jan 2025 17:58:35 GMT  
		Size: 177.9 KB (177924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83ea76b909a5c737245e1d0ca151c39b98ea23c555b3737830930da751977328`  
		Last Modified: Wed, 08 Jan 2025 17:58:35 GMT  
		Size: 20.1 KB (20110 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6.15-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:92d1d26311297d03436e954ef1efc1bbd2e7e4508955a80654390e266d62bfb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd8e9df88f2dd19ad0ae3b7879d6b96abe99196d6a0742ae3a984c3ca0d0d82`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.18.11-armhf.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:803cf02755db9f4dbb0d52a3ff280052dd523cdfdb9e9be6494b4edd548d6dc6`  
		Last Modified: Tue, 14 Jan 2025 20:51:05 GMT  
		Size: 3.2 MB (3159977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982b4b3ea73f68baba7ae3131ab8972a5325a591cbf845eec376248bb0428fab`  
		Last Modified: Wed, 15 Jan 2025 13:20:37 GMT  
		Size: 614.1 KB (614120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2043f80c50b150209283a57636fd4e9d248e3ccaed373fc47209e8841e3d6f6e`  
		Last Modified: Tue, 07 Jan 2025 04:52:57 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6.15-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:597593beb9589da97bc89d16690a60845cc493d830190abbb99b208e42ad9333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (19957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a62bfb0802bf2a88e530f6ece44053a0f0ea2ad5975a3d921ebd306bfec733`

```dockerfile
```

-	Layers:
	-	`sha256:17a6401dfe8bb43f892c70a369a8cb56fc503096c24df8e1a5cbd30cd0956f69`  
		Last Modified: Wed, 08 Jan 2025 18:22:06 GMT  
		Size: 20.0 KB (19957 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6.15-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:563ea4312bdb4615ac4b61e862aaf54ea5e918fa057796b8576ece5cf5bf557c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3982582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27bbeac0200f02e2f4024e1c228a1a125e5b270d8fa7ff006b919658b42cae4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.18.11-aarch64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:f6b431426dd566e612639f03cd46e521b3133a043bb6b60edeeeef80d513e870`  
		Last Modified: Tue, 14 Jan 2025 20:34:06 GMT  
		Size: 3.3 MB (3341861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee833ac9acdbb04195dd00e61acb3c37feab6edbf90d860d24acb543ed2d4070`  
		Last Modified: Thu, 13 Feb 2025 17:13:01 GMT  
		Size: 640.5 KB (640482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13edf7e5f27c66f05853eb65be343799c26ca7694b868b439084f54afaa12475`  
		Last Modified: Sat, 08 Feb 2025 03:58:27 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6.15-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:507260262d65eb48c0c5ef9a52cd5b714c47f56243043f54efa58e8fe6c79c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 KB (198148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0624cec73ee6893372fa0ddaa6dec1ebc09480589cff94118b2e2b4e910ed1`

```dockerfile
```

-	Layers:
	-	`sha256:0d64989292eb0e6d1852a9cc2e725038f3f9656f5ca37fd7a524ef44e7d7a139`  
		Last Modified: Wed, 08 Jan 2025 18:23:38 GMT  
		Size: 178.0 KB (177956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df2ffb5d5d9066c4d21acfed7b025660c258980afe69f50fbb756b162c7268cc`  
		Last Modified: Wed, 08 Jan 2025 18:23:38 GMT  
		Size: 20.2 KB (20192 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6.15-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:f07bf2d484807d5d470c0931b2e83cfd290b603503ac2e4c2a6861cf340bfa35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3918594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2ed95744d43336d8d46d09d578bac60ae0eed85b20b808c53fc864cb34f1a6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.18.11-x86.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:bd5e0f642fd4fa0e53e323e5bdaa4e3ef6549fc49ad76da06114328d35f9e4ce`  
		Last Modified: Tue, 14 Jan 2025 21:24:43 GMT  
		Size: 3.3 MB (3251158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901be931a6394e45abeedbf57d2426812cc5be6fc578ef0948a3ed26f9255c80`  
		Last Modified: Wed, 08 Jan 2025 17:58:33 GMT  
		Size: 667.2 KB (667196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51dd60c5a4556ebe2cfb2a698d56eb62a8f7db4fe7fa68503df980e7eb07ed4`  
		Last Modified: Wed, 08 Jan 2025 17:58:33 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6.15-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:83087574c9443a61bb1500e509c1f496a73062a4f927c21aecf4d73b267c25b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 KB (197999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d317ac455c7e2a2a69021d3925fc3fbe6d0fb48befce649c1e05221b1caae54`

```dockerfile
```

-	Layers:
	-	`sha256:5ff6ccfb377f1fd5d43bb705e5b4b65ad391c6bfe19e697609372ef798d3fefd`  
		Last Modified: Wed, 08 Jan 2025 17:58:33 GMT  
		Size: 177.9 KB (177909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b34fb12ac3847333d72c1d665daa5a06526edaa8315cde4feb3085ae4eb4797c`  
		Last Modified: Wed, 08 Jan 2025 17:58:33 GMT  
		Size: 20.1 KB (20090 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6.15-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:1495752c821a478383534113a8b038089f20d95c0c053c9ed9c34f9353713b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4052404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d694e002c2926b3b7bafb4f4a542eaf984898c5749a8d75d7dc935adfa1913a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.18.11-ppc64le.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:6259f25643973acaf5182679ac24f10e7bcb8be462646ba81a87b013ec80c9ed`  
		Last Modified: Tue, 14 Jan 2025 20:33:51 GMT  
		Size: 3.4 MB (3359277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d88f4d5ff3aba0143ceeb4b35d96a14689b35da7dce37ffbde6802203077de`  
		Last Modified: Wed, 08 Jan 2025 18:17:21 GMT  
		Size: 692.9 KB (692887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc4ec82c8cb3a28d72fdf0ab9bd50c6db4c2df47918f40174b0120e8c07588c`  
		Last Modified: Wed, 08 Jan 2025 18:17:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6.15-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:a7fded12d01b0051e11539c0a47448b6b84352ea4dea68e99023f0015053d1b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 KB (196139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be610c1314e52b1fca9d49b8da12ec182d97f376b3dee88ff924b4e32702911d`

```dockerfile
```

-	Layers:
	-	`sha256:730d0b870a5669e94b258110d49cca120f6c3d5616dbc2acb38343003b0ce6a2`  
		Last Modified: Wed, 08 Jan 2025 18:17:20 GMT  
		Size: 176.0 KB (175995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b22a8c0d3c0cc55bdcd7fe5b5a02d14a146ce48410618b73dca3f0d66250eef9`  
		Last Modified: Wed, 08 Jan 2025 18:17:20 GMT  
		Size: 20.1 KB (20144 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6.15-openssl` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:b80975a3fca709805ff045f95856208642213087ec9637f33e76b8ab3b2ab7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3868871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e88922f2e996585b7ef52a749919f5d831b4e16874848c1e7fb1492ad0bde4f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.18.11-s390x.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:552c3aaa08429935d8dfef69ca747244fe854badcb537563677169e2f2ebdde8`  
		Last Modified: Tue, 14 Jan 2025 20:44:17 GMT  
		Size: 3.2 MB (3231849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebead2477ddcafc90a9290540a04baacc10e99e9f1956b9a8a9d939cf725c65e`  
		Last Modified: Wed, 08 Jan 2025 18:15:19 GMT  
		Size: 636.8 KB (636782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b26b9b2d77a8a1873370b956d1dc0b3a9896f6f1687529b2461d8e3c52e654a`  
		Last Modified: Wed, 08 Jan 2025 18:15:18 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6.15-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:e39a19ae83074131cef12d643d0a8118145de50baf9441e24c29c9a79b7e34e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 KB (196085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3467e1d6ca16a4af198539bf15bc22ffa45cb397fc9ea44d1119878d56dda3f`

```dockerfile
```

-	Layers:
	-	`sha256:9b875552fb1c001194e0eaee0a279d33f5f01ecbfe08e5e12ef73e18b6ebe2b9`  
		Last Modified: Wed, 08 Jan 2025 18:15:19 GMT  
		Size: 176.0 KB (175973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3790355df5358a733a64c7fec9ffac19c0cd8ad140c672ff471b0907d050cd1b`  
		Last Modified: Wed, 08 Jan 2025 18:15:18 GMT  
		Size: 20.1 KB (20112 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:2`

```console
$ docker pull eclipse-mosquitto@sha256:deae95623b9d5c6ca5e264380629db53b992106d436b56d42f7c8df46b41b96f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-mosquitto:2` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:7ee09b4dd85ea25f07922128f305585353c2834ab1cde8a69632cfe649fe7152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4373995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61843a2255ff7a0209cb452bc90af4a3af41df986808b50e2afe8df58a014336`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fe382c8a5ef350b25cf6bb57e83ab7fc2fd802c316d75e3129862fb03e5e4e`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 747.4 KB (747366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8fa0745f9b4cc560107aafbd512c9a4fad59d47e7f2a609088a75a97784041`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:8541bec48e97eea558b833c4251eca6f3f648b0730099962ef9848ae6de39567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 KB (201010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3476c032209b261f4619ec09d88769bff67dad4bf688eda0a3df8ef323b632`

```dockerfile
```

-	Layers:
	-	`sha256:1170e9102fecfd36e81bde2fbb5d0e71e74640051080213d95eb4ce970aab458`  
		Last Modified: Tue, 14 Jan 2025 22:39:47 GMT  
		Size: 177.9 KB (177856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba745a327008881921b67b12c0f52ae9955f1dc8a2c804100411d55bdcbe1ee7`  
		Last Modified: Tue, 14 Jan 2025 23:12:34 GMT  
		Size: 23.2 KB (23154 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:843c16811e277436b5c5acc57166556ff7667d1ab30e9dddb73f32fc931a297b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35381791854c245f7863716ef5582c6e4e38dd4796e715ef8ae035825930586`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Tue, 14 Jan 2025 20:34:27 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33741ccf332fedc54086f78955a7f7c062d68e9c570b54c2fcbd664d1e0be110`  
		Last Modified: Tue, 14 Jan 2025 20:34:23 GMT  
		Size: 719.9 KB (719862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4cfff44530c9bc96c46a403beaba77b56b5549a17d64fc090ff824c8ca302a`  
		Last Modified: Tue, 07 Jan 2025 04:54:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:53aa6f86240571ec82c49b6ae4b6db486ba3a3a86dc85aeda666281ce5fa8d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 KB (23046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56fef7fa9271a04f736a59aac8315c13f54c63ec8b813b33fae60bdbafbe8a7`

```dockerfile
```

-	Layers:
	-	`sha256:49577d947438769c75abf2585782b18e9d985c3cc0f1105707ff4f2481705ea3`  
		Last Modified: Fri, 07 Feb 2025 04:11:07 GMT  
		Size: 23.0 KB (23046 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:4705a440a3e5e3143f7c020c0f90833809b69fa325d8d2e0cc2fe4991b5b95bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4840552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cdb9a00077bbc2939b5e37241bf8b0da0a1ece3315f207d49b2fc765d488e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd3396764d5544adadcb96a804c10181b20cc0209495945ea8f4add1ab3c66c`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 749.4 KB (749413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c8deab35939b47ea7abcf3baf88258d9a3ca6ab8e188f8c4f2c73ee681f086`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:2ae224a4773e3bc1eb26d06a24ac62b8277dcf64ed99123453ce3e81c86eae64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 KB (201266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141e21516763808251a1e3845f81e43e7ab77fba34dba9ddaf9e2a71db76f0b4`

```dockerfile
```

-	Layers:
	-	`sha256:b224e0349955da5c177a7f07aeb6b38832fb75b88d6a631b0211cd59f5d18d94`  
		Last Modified: Tue, 14 Jan 2025 23:12:43 GMT  
		Size: 178.0 KB (177960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:198fa148210ff357d543bf58439890a01f268330be112f37cd8282098d3a112b`  
		Last Modified: Wed, 15 Jan 2025 10:06:47 GMT  
		Size: 23.3 KB (23306 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:0b323bfda696c5e714db988a73f5b2be6a80833470db3bb0965b181b2cda91d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4260337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845cf9cb3e2ae869796ae9ff1b80edb8cfd210fe67f16ab9c2cc11dbeb007026`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Tue, 14 Jan 2025 21:25:38 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936c1b63cf6e8cdeeea4b5d6033a46638313497f9b2a9c0f8d607a219d0e2e6c`  
		Last Modified: Tue, 14 Jan 2025 22:40:54 GMT  
		Size: 789.0 KB (788999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf9b7720cba29cd05912198bccbb71614e94b12d319af42d267d2ad4c51d61d`  
		Last Modified: Tue, 14 Jan 2025 22:41:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:25a05ba4caef99f524f8259740846431a514f2aedc5c3a0a9ff07938d809b51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 KB (200913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e0c91d29eed6106c83da1c6517bf9ff5ffcca6b2003a1f45ff7d00741c3c8b`

```dockerfile
```

-	Layers:
	-	`sha256:1ff7940e4598d1118a7f5e53ca6a755875bafdbc5a6677c198efcd82d2df121e`  
		Last Modified: Tue, 14 Jan 2025 22:39:59 GMT  
		Size: 177.8 KB (177811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:086d3237e5b048be94530403c08cfd8db9ef92faf3667fad8fe72482e07f0558`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 23.1 KB (23102 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:5fab56124ad7c1d854a5a212e280aa3bfd60ed668fd5415b551c42e5ea6644b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4394954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f167a42b5a1f7805744d4019f133f9e9ffc8e3817cb99ceeb23cf018ef7de9c6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bca7957551d2d47d18f0573ab65e77e7a0049808dfc8431dde2aad1dce1df7e`  
		Last Modified: Tue, 14 Jan 2025 23:12:50 GMT  
		Size: 820.2 KB (820180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2515d8b8efe0a20c199f560345325242482095029a59ed77ce90cf5b2ff7a078`  
		Last Modified: Tue, 14 Jan 2025 22:41:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:054a4fd52f0aa9ed530ea99a77a749042fa31ea3c9faa43b881b6dfe44945508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 KB (199184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b320ffadb3c981e8584604c7e5cda6629bcaff3fcec416587d2f9f260731696f`

```dockerfile
```

-	Layers:
	-	`sha256:edefd3739471fd1920f96937ecc474eb3193a4e02045ee18ab7037dfc75aa47b`  
		Last Modified: Tue, 14 Jan 2025 22:39:59 GMT  
		Size: 176.0 KB (175963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d333b77ae5d873e2408d01980c1296376a773498803fdf05daa366303e5e12`  
		Last Modified: Tue, 14 Jan 2025 23:12:53 GMT  
		Size: 23.2 KB (23221 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:6566e22afc536f5300c8723e4c312ca70b055193046d0ef65623c4e3452f9a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9930794d9d2da57ed64bd9ad82bcfd104d630760d8b24fd9eb00a8751a399cdf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Tue, 14 Jan 2025 21:25:41 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d61aecfc928aac1e86f36feab6688c31e6a97b32fe2a08c415adc81490ecf9`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 772.2 KB (772219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1414ddbc706e322cd9d926d7fcc42bebb5d75b4458410e1029a33beaca0e8e`  
		Last Modified: Tue, 14 Jan 2025 23:12:55 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:34a0e7319af5a8367bf45603fc7cc5e7620b7b216df88e9a92f65d2a63b46e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 KB (199059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff152e1055a34741555f319cc37e0b20fd52d4d55e115d485f427235b2f56397`

```dockerfile
```

-	Layers:
	-	`sha256:2ed494cc2bcc91abae48b391ab2f13c2e096b39c448c59f71a01aa637f35a26b`  
		Last Modified: Fri, 07 Feb 2025 04:11:13 GMT  
		Size: 175.9 KB (175905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f491631fd3f201aa258112eac820764ec18bcf824822cb6f9267e3c9bef8ec`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 23.2 KB (23154 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:2-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:deae95623b9d5c6ca5e264380629db53b992106d436b56d42f7c8df46b41b96f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-mosquitto:2-openssl` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:7ee09b4dd85ea25f07922128f305585353c2834ab1cde8a69632cfe649fe7152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4373995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61843a2255ff7a0209cb452bc90af4a3af41df986808b50e2afe8df58a014336`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fe382c8a5ef350b25cf6bb57e83ab7fc2fd802c316d75e3129862fb03e5e4e`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 747.4 KB (747366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8fa0745f9b4cc560107aafbd512c9a4fad59d47e7f2a609088a75a97784041`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:8541bec48e97eea558b833c4251eca6f3f648b0730099962ef9848ae6de39567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 KB (201010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3476c032209b261f4619ec09d88769bff67dad4bf688eda0a3df8ef323b632`

```dockerfile
```

-	Layers:
	-	`sha256:1170e9102fecfd36e81bde2fbb5d0e71e74640051080213d95eb4ce970aab458`  
		Last Modified: Tue, 14 Jan 2025 22:39:47 GMT  
		Size: 177.9 KB (177856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba745a327008881921b67b12c0f52ae9955f1dc8a2c804100411d55bdcbe1ee7`  
		Last Modified: Tue, 14 Jan 2025 23:12:34 GMT  
		Size: 23.2 KB (23154 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:843c16811e277436b5c5acc57166556ff7667d1ab30e9dddb73f32fc931a297b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35381791854c245f7863716ef5582c6e4e38dd4796e715ef8ae035825930586`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Tue, 14 Jan 2025 20:34:27 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33741ccf332fedc54086f78955a7f7c062d68e9c570b54c2fcbd664d1e0be110`  
		Last Modified: Tue, 14 Jan 2025 20:34:23 GMT  
		Size: 719.9 KB (719862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4cfff44530c9bc96c46a403beaba77b56b5549a17d64fc090ff824c8ca302a`  
		Last Modified: Tue, 07 Jan 2025 04:54:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:53aa6f86240571ec82c49b6ae4b6db486ba3a3a86dc85aeda666281ce5fa8d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 KB (23046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56fef7fa9271a04f736a59aac8315c13f54c63ec8b813b33fae60bdbafbe8a7`

```dockerfile
```

-	Layers:
	-	`sha256:49577d947438769c75abf2585782b18e9d985c3cc0f1105707ff4f2481705ea3`  
		Last Modified: Fri, 07 Feb 2025 04:11:07 GMT  
		Size: 23.0 KB (23046 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:4705a440a3e5e3143f7c020c0f90833809b69fa325d8d2e0cc2fe4991b5b95bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4840552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cdb9a00077bbc2939b5e37241bf8b0da0a1ece3315f207d49b2fc765d488e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd3396764d5544adadcb96a804c10181b20cc0209495945ea8f4add1ab3c66c`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 749.4 KB (749413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c8deab35939b47ea7abcf3baf88258d9a3ca6ab8e188f8c4f2c73ee681f086`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:2ae224a4773e3bc1eb26d06a24ac62b8277dcf64ed99123453ce3e81c86eae64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 KB (201266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141e21516763808251a1e3845f81e43e7ab77fba34dba9ddaf9e2a71db76f0b4`

```dockerfile
```

-	Layers:
	-	`sha256:b224e0349955da5c177a7f07aeb6b38832fb75b88d6a631b0211cd59f5d18d94`  
		Last Modified: Tue, 14 Jan 2025 23:12:43 GMT  
		Size: 178.0 KB (177960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:198fa148210ff357d543bf58439890a01f268330be112f37cd8282098d3a112b`  
		Last Modified: Wed, 15 Jan 2025 10:06:47 GMT  
		Size: 23.3 KB (23306 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:0b323bfda696c5e714db988a73f5b2be6a80833470db3bb0965b181b2cda91d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4260337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845cf9cb3e2ae869796ae9ff1b80edb8cfd210fe67f16ab9c2cc11dbeb007026`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Tue, 14 Jan 2025 21:25:38 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936c1b63cf6e8cdeeea4b5d6033a46638313497f9b2a9c0f8d607a219d0e2e6c`  
		Last Modified: Tue, 14 Jan 2025 22:40:54 GMT  
		Size: 789.0 KB (788999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf9b7720cba29cd05912198bccbb71614e94b12d319af42d267d2ad4c51d61d`  
		Last Modified: Tue, 14 Jan 2025 22:41:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:25a05ba4caef99f524f8259740846431a514f2aedc5c3a0a9ff07938d809b51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 KB (200913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e0c91d29eed6106c83da1c6517bf9ff5ffcca6b2003a1f45ff7d00741c3c8b`

```dockerfile
```

-	Layers:
	-	`sha256:1ff7940e4598d1118a7f5e53ca6a755875bafdbc5a6677c198efcd82d2df121e`  
		Last Modified: Tue, 14 Jan 2025 22:39:59 GMT  
		Size: 177.8 KB (177811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:086d3237e5b048be94530403c08cfd8db9ef92faf3667fad8fe72482e07f0558`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 23.1 KB (23102 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:5fab56124ad7c1d854a5a212e280aa3bfd60ed668fd5415b551c42e5ea6644b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4394954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f167a42b5a1f7805744d4019f133f9e9ffc8e3817cb99ceeb23cf018ef7de9c6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bca7957551d2d47d18f0573ab65e77e7a0049808dfc8431dde2aad1dce1df7e`  
		Last Modified: Tue, 14 Jan 2025 23:12:50 GMT  
		Size: 820.2 KB (820180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2515d8b8efe0a20c199f560345325242482095029a59ed77ce90cf5b2ff7a078`  
		Last Modified: Tue, 14 Jan 2025 22:41:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:054a4fd52f0aa9ed530ea99a77a749042fa31ea3c9faa43b881b6dfe44945508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 KB (199184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b320ffadb3c981e8584604c7e5cda6629bcaff3fcec416587d2f9f260731696f`

```dockerfile
```

-	Layers:
	-	`sha256:edefd3739471fd1920f96937ecc474eb3193a4e02045ee18ab7037dfc75aa47b`  
		Last Modified: Tue, 14 Jan 2025 22:39:59 GMT  
		Size: 176.0 KB (175963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d333b77ae5d873e2408d01980c1296376a773498803fdf05daa366303e5e12`  
		Last Modified: Tue, 14 Jan 2025 23:12:53 GMT  
		Size: 23.2 KB (23221 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2-openssl` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:6566e22afc536f5300c8723e4c312ca70b055193046d0ef65623c4e3452f9a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9930794d9d2da57ed64bd9ad82bcfd104d630760d8b24fd9eb00a8751a399cdf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Tue, 14 Jan 2025 21:25:41 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d61aecfc928aac1e86f36feab6688c31e6a97b32fe2a08c415adc81490ecf9`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 772.2 KB (772219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1414ddbc706e322cd9d926d7fcc42bebb5d75b4458410e1029a33beaca0e8e`  
		Last Modified: Tue, 14 Jan 2025 23:12:55 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:34a0e7319af5a8367bf45603fc7cc5e7620b7b216df88e9a92f65d2a63b46e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 KB (199059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff152e1055a34741555f319cc37e0b20fd52d4d55e115d485f427235b2f56397`

```dockerfile
```

-	Layers:
	-	`sha256:2ed494cc2bcc91abae48b391ab2f13c2e096b39c448c59f71a01aa637f35a26b`  
		Last Modified: Fri, 07 Feb 2025 04:11:13 GMT  
		Size: 175.9 KB (175905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f491631fd3f201aa258112eac820764ec18bcf824822cb6f9267e3c9bef8ec`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 23.2 KB (23154 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:2.0`

```console
$ docker pull eclipse-mosquitto@sha256:deae95623b9d5c6ca5e264380629db53b992106d436b56d42f7c8df46b41b96f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-mosquitto:2.0` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:7ee09b4dd85ea25f07922128f305585353c2834ab1cde8a69632cfe649fe7152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4373995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61843a2255ff7a0209cb452bc90af4a3af41df986808b50e2afe8df58a014336`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fe382c8a5ef350b25cf6bb57e83ab7fc2fd802c316d75e3129862fb03e5e4e`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 747.4 KB (747366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8fa0745f9b4cc560107aafbd512c9a4fad59d47e7f2a609088a75a97784041`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:8541bec48e97eea558b833c4251eca6f3f648b0730099962ef9848ae6de39567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 KB (201010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3476c032209b261f4619ec09d88769bff67dad4bf688eda0a3df8ef323b632`

```dockerfile
```

-	Layers:
	-	`sha256:1170e9102fecfd36e81bde2fbb5d0e71e74640051080213d95eb4ce970aab458`  
		Last Modified: Tue, 14 Jan 2025 22:39:47 GMT  
		Size: 177.9 KB (177856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba745a327008881921b67b12c0f52ae9955f1dc8a2c804100411d55bdcbe1ee7`  
		Last Modified: Tue, 14 Jan 2025 23:12:34 GMT  
		Size: 23.2 KB (23154 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:843c16811e277436b5c5acc57166556ff7667d1ab30e9dddb73f32fc931a297b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35381791854c245f7863716ef5582c6e4e38dd4796e715ef8ae035825930586`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Tue, 14 Jan 2025 20:34:27 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33741ccf332fedc54086f78955a7f7c062d68e9c570b54c2fcbd664d1e0be110`  
		Last Modified: Tue, 14 Jan 2025 20:34:23 GMT  
		Size: 719.9 KB (719862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4cfff44530c9bc96c46a403beaba77b56b5549a17d64fc090ff824c8ca302a`  
		Last Modified: Tue, 07 Jan 2025 04:54:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:53aa6f86240571ec82c49b6ae4b6db486ba3a3a86dc85aeda666281ce5fa8d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 KB (23046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56fef7fa9271a04f736a59aac8315c13f54c63ec8b813b33fae60bdbafbe8a7`

```dockerfile
```

-	Layers:
	-	`sha256:49577d947438769c75abf2585782b18e9d985c3cc0f1105707ff4f2481705ea3`  
		Last Modified: Fri, 07 Feb 2025 04:11:07 GMT  
		Size: 23.0 KB (23046 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:4705a440a3e5e3143f7c020c0f90833809b69fa325d8d2e0cc2fe4991b5b95bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4840552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cdb9a00077bbc2939b5e37241bf8b0da0a1ece3315f207d49b2fc765d488e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd3396764d5544adadcb96a804c10181b20cc0209495945ea8f4add1ab3c66c`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 749.4 KB (749413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c8deab35939b47ea7abcf3baf88258d9a3ca6ab8e188f8c4f2c73ee681f086`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:2ae224a4773e3bc1eb26d06a24ac62b8277dcf64ed99123453ce3e81c86eae64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 KB (201266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141e21516763808251a1e3845f81e43e7ab77fba34dba9ddaf9e2a71db76f0b4`

```dockerfile
```

-	Layers:
	-	`sha256:b224e0349955da5c177a7f07aeb6b38832fb75b88d6a631b0211cd59f5d18d94`  
		Last Modified: Tue, 14 Jan 2025 23:12:43 GMT  
		Size: 178.0 KB (177960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:198fa148210ff357d543bf58439890a01f268330be112f37cd8282098d3a112b`  
		Last Modified: Wed, 15 Jan 2025 10:06:47 GMT  
		Size: 23.3 KB (23306 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:0b323bfda696c5e714db988a73f5b2be6a80833470db3bb0965b181b2cda91d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4260337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845cf9cb3e2ae869796ae9ff1b80edb8cfd210fe67f16ab9c2cc11dbeb007026`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Tue, 14 Jan 2025 21:25:38 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936c1b63cf6e8cdeeea4b5d6033a46638313497f9b2a9c0f8d607a219d0e2e6c`  
		Last Modified: Tue, 14 Jan 2025 22:40:54 GMT  
		Size: 789.0 KB (788999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf9b7720cba29cd05912198bccbb71614e94b12d319af42d267d2ad4c51d61d`  
		Last Modified: Tue, 14 Jan 2025 22:41:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:25a05ba4caef99f524f8259740846431a514f2aedc5c3a0a9ff07938d809b51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 KB (200913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e0c91d29eed6106c83da1c6517bf9ff5ffcca6b2003a1f45ff7d00741c3c8b`

```dockerfile
```

-	Layers:
	-	`sha256:1ff7940e4598d1118a7f5e53ca6a755875bafdbc5a6677c198efcd82d2df121e`  
		Last Modified: Tue, 14 Jan 2025 22:39:59 GMT  
		Size: 177.8 KB (177811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:086d3237e5b048be94530403c08cfd8db9ef92faf3667fad8fe72482e07f0558`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 23.1 KB (23102 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:5fab56124ad7c1d854a5a212e280aa3bfd60ed668fd5415b551c42e5ea6644b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4394954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f167a42b5a1f7805744d4019f133f9e9ffc8e3817cb99ceeb23cf018ef7de9c6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bca7957551d2d47d18f0573ab65e77e7a0049808dfc8431dde2aad1dce1df7e`  
		Last Modified: Tue, 14 Jan 2025 23:12:50 GMT  
		Size: 820.2 KB (820180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2515d8b8efe0a20c199f560345325242482095029a59ed77ce90cf5b2ff7a078`  
		Last Modified: Tue, 14 Jan 2025 22:41:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:054a4fd52f0aa9ed530ea99a77a749042fa31ea3c9faa43b881b6dfe44945508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 KB (199184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b320ffadb3c981e8584604c7e5cda6629bcaff3fcec416587d2f9f260731696f`

```dockerfile
```

-	Layers:
	-	`sha256:edefd3739471fd1920f96937ecc474eb3193a4e02045ee18ab7037dfc75aa47b`  
		Last Modified: Tue, 14 Jan 2025 22:39:59 GMT  
		Size: 176.0 KB (175963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d333b77ae5d873e2408d01980c1296376a773498803fdf05daa366303e5e12`  
		Last Modified: Tue, 14 Jan 2025 23:12:53 GMT  
		Size: 23.2 KB (23221 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:6566e22afc536f5300c8723e4c312ca70b055193046d0ef65623c4e3452f9a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9930794d9d2da57ed64bd9ad82bcfd104d630760d8b24fd9eb00a8751a399cdf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Tue, 14 Jan 2025 21:25:41 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d61aecfc928aac1e86f36feab6688c31e6a97b32fe2a08c415adc81490ecf9`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 772.2 KB (772219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1414ddbc706e322cd9d926d7fcc42bebb5d75b4458410e1029a33beaca0e8e`  
		Last Modified: Tue, 14 Jan 2025 23:12:55 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:34a0e7319af5a8367bf45603fc7cc5e7620b7b216df88e9a92f65d2a63b46e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 KB (199059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff152e1055a34741555f319cc37e0b20fd52d4d55e115d485f427235b2f56397`

```dockerfile
```

-	Layers:
	-	`sha256:2ed494cc2bcc91abae48b391ab2f13c2e096b39c448c59f71a01aa637f35a26b`  
		Last Modified: Fri, 07 Feb 2025 04:11:13 GMT  
		Size: 175.9 KB (175905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f491631fd3f201aa258112eac820764ec18bcf824822cb6f9267e3c9bef8ec`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 23.2 KB (23154 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:2.0-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:deae95623b9d5c6ca5e264380629db53b992106d436b56d42f7c8df46b41b96f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-mosquitto:2.0-openssl` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:7ee09b4dd85ea25f07922128f305585353c2834ab1cde8a69632cfe649fe7152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4373995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61843a2255ff7a0209cb452bc90af4a3af41df986808b50e2afe8df58a014336`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fe382c8a5ef350b25cf6bb57e83ab7fc2fd802c316d75e3129862fb03e5e4e`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 747.4 KB (747366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8fa0745f9b4cc560107aafbd512c9a4fad59d47e7f2a609088a75a97784041`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:8541bec48e97eea558b833c4251eca6f3f648b0730099962ef9848ae6de39567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 KB (201010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3476c032209b261f4619ec09d88769bff67dad4bf688eda0a3df8ef323b632`

```dockerfile
```

-	Layers:
	-	`sha256:1170e9102fecfd36e81bde2fbb5d0e71e74640051080213d95eb4ce970aab458`  
		Last Modified: Tue, 14 Jan 2025 22:39:47 GMT  
		Size: 177.9 KB (177856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba745a327008881921b67b12c0f52ae9955f1dc8a2c804100411d55bdcbe1ee7`  
		Last Modified: Tue, 14 Jan 2025 23:12:34 GMT  
		Size: 23.2 KB (23154 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:843c16811e277436b5c5acc57166556ff7667d1ab30e9dddb73f32fc931a297b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35381791854c245f7863716ef5582c6e4e38dd4796e715ef8ae035825930586`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Tue, 14 Jan 2025 20:34:27 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33741ccf332fedc54086f78955a7f7c062d68e9c570b54c2fcbd664d1e0be110`  
		Last Modified: Tue, 14 Jan 2025 20:34:23 GMT  
		Size: 719.9 KB (719862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4cfff44530c9bc96c46a403beaba77b56b5549a17d64fc090ff824c8ca302a`  
		Last Modified: Tue, 07 Jan 2025 04:54:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:53aa6f86240571ec82c49b6ae4b6db486ba3a3a86dc85aeda666281ce5fa8d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 KB (23046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56fef7fa9271a04f736a59aac8315c13f54c63ec8b813b33fae60bdbafbe8a7`

```dockerfile
```

-	Layers:
	-	`sha256:49577d947438769c75abf2585782b18e9d985c3cc0f1105707ff4f2481705ea3`  
		Last Modified: Fri, 07 Feb 2025 04:11:07 GMT  
		Size: 23.0 KB (23046 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:4705a440a3e5e3143f7c020c0f90833809b69fa325d8d2e0cc2fe4991b5b95bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4840552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cdb9a00077bbc2939b5e37241bf8b0da0a1ece3315f207d49b2fc765d488e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd3396764d5544adadcb96a804c10181b20cc0209495945ea8f4add1ab3c66c`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 749.4 KB (749413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c8deab35939b47ea7abcf3baf88258d9a3ca6ab8e188f8c4f2c73ee681f086`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:2ae224a4773e3bc1eb26d06a24ac62b8277dcf64ed99123453ce3e81c86eae64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 KB (201266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141e21516763808251a1e3845f81e43e7ab77fba34dba9ddaf9e2a71db76f0b4`

```dockerfile
```

-	Layers:
	-	`sha256:b224e0349955da5c177a7f07aeb6b38832fb75b88d6a631b0211cd59f5d18d94`  
		Last Modified: Tue, 14 Jan 2025 23:12:43 GMT  
		Size: 178.0 KB (177960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:198fa148210ff357d543bf58439890a01f268330be112f37cd8282098d3a112b`  
		Last Modified: Wed, 15 Jan 2025 10:06:47 GMT  
		Size: 23.3 KB (23306 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:0b323bfda696c5e714db988a73f5b2be6a80833470db3bb0965b181b2cda91d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4260337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845cf9cb3e2ae869796ae9ff1b80edb8cfd210fe67f16ab9c2cc11dbeb007026`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Tue, 14 Jan 2025 21:25:38 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936c1b63cf6e8cdeeea4b5d6033a46638313497f9b2a9c0f8d607a219d0e2e6c`  
		Last Modified: Tue, 14 Jan 2025 22:40:54 GMT  
		Size: 789.0 KB (788999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf9b7720cba29cd05912198bccbb71614e94b12d319af42d267d2ad4c51d61d`  
		Last Modified: Tue, 14 Jan 2025 22:41:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:25a05ba4caef99f524f8259740846431a514f2aedc5c3a0a9ff07938d809b51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 KB (200913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e0c91d29eed6106c83da1c6517bf9ff5ffcca6b2003a1f45ff7d00741c3c8b`

```dockerfile
```

-	Layers:
	-	`sha256:1ff7940e4598d1118a7f5e53ca6a755875bafdbc5a6677c198efcd82d2df121e`  
		Last Modified: Tue, 14 Jan 2025 22:39:59 GMT  
		Size: 177.8 KB (177811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:086d3237e5b048be94530403c08cfd8db9ef92faf3667fad8fe72482e07f0558`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 23.1 KB (23102 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:5fab56124ad7c1d854a5a212e280aa3bfd60ed668fd5415b551c42e5ea6644b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4394954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f167a42b5a1f7805744d4019f133f9e9ffc8e3817cb99ceeb23cf018ef7de9c6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bca7957551d2d47d18f0573ab65e77e7a0049808dfc8431dde2aad1dce1df7e`  
		Last Modified: Tue, 14 Jan 2025 23:12:50 GMT  
		Size: 820.2 KB (820180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2515d8b8efe0a20c199f560345325242482095029a59ed77ce90cf5b2ff7a078`  
		Last Modified: Tue, 14 Jan 2025 22:41:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:054a4fd52f0aa9ed530ea99a77a749042fa31ea3c9faa43b881b6dfe44945508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 KB (199184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b320ffadb3c981e8584604c7e5cda6629bcaff3fcec416587d2f9f260731696f`

```dockerfile
```

-	Layers:
	-	`sha256:edefd3739471fd1920f96937ecc474eb3193a4e02045ee18ab7037dfc75aa47b`  
		Last Modified: Tue, 14 Jan 2025 22:39:59 GMT  
		Size: 176.0 KB (175963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d333b77ae5d873e2408d01980c1296376a773498803fdf05daa366303e5e12`  
		Last Modified: Tue, 14 Jan 2025 23:12:53 GMT  
		Size: 23.2 KB (23221 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0-openssl` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:6566e22afc536f5300c8723e4c312ca70b055193046d0ef65623c4e3452f9a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9930794d9d2da57ed64bd9ad82bcfd104d630760d8b24fd9eb00a8751a399cdf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Tue, 14 Jan 2025 21:25:41 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d61aecfc928aac1e86f36feab6688c31e6a97b32fe2a08c415adc81490ecf9`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 772.2 KB (772219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1414ddbc706e322cd9d926d7fcc42bebb5d75b4458410e1029a33beaca0e8e`  
		Last Modified: Tue, 14 Jan 2025 23:12:55 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:34a0e7319af5a8367bf45603fc7cc5e7620b7b216df88e9a92f65d2a63b46e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 KB (199059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff152e1055a34741555f319cc37e0b20fd52d4d55e115d485f427235b2f56397`

```dockerfile
```

-	Layers:
	-	`sha256:2ed494cc2bcc91abae48b391ab2f13c2e096b39c448c59f71a01aa637f35a26b`  
		Last Modified: Fri, 07 Feb 2025 04:11:13 GMT  
		Size: 175.9 KB (175905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f491631fd3f201aa258112eac820764ec18bcf824822cb6f9267e3c9bef8ec`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 23.2 KB (23154 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:2.0.20`

```console
$ docker pull eclipse-mosquitto@sha256:deae95623b9d5c6ca5e264380629db53b992106d436b56d42f7c8df46b41b96f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-mosquitto:2.0.20` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:7ee09b4dd85ea25f07922128f305585353c2834ab1cde8a69632cfe649fe7152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4373995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61843a2255ff7a0209cb452bc90af4a3af41df986808b50e2afe8df58a014336`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fe382c8a5ef350b25cf6bb57e83ab7fc2fd802c316d75e3129862fb03e5e4e`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 747.4 KB (747366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8fa0745f9b4cc560107aafbd512c9a4fad59d47e7f2a609088a75a97784041`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.20` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:8541bec48e97eea558b833c4251eca6f3f648b0730099962ef9848ae6de39567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 KB (201010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3476c032209b261f4619ec09d88769bff67dad4bf688eda0a3df8ef323b632`

```dockerfile
```

-	Layers:
	-	`sha256:1170e9102fecfd36e81bde2fbb5d0e71e74640051080213d95eb4ce970aab458`  
		Last Modified: Tue, 14 Jan 2025 22:39:47 GMT  
		Size: 177.9 KB (177856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba745a327008881921b67b12c0f52ae9955f1dc8a2c804100411d55bdcbe1ee7`  
		Last Modified: Tue, 14 Jan 2025 23:12:34 GMT  
		Size: 23.2 KB (23154 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.20` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:843c16811e277436b5c5acc57166556ff7667d1ab30e9dddb73f32fc931a297b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35381791854c245f7863716ef5582c6e4e38dd4796e715ef8ae035825930586`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Tue, 14 Jan 2025 20:34:27 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33741ccf332fedc54086f78955a7f7c062d68e9c570b54c2fcbd664d1e0be110`  
		Last Modified: Tue, 14 Jan 2025 20:34:23 GMT  
		Size: 719.9 KB (719862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4cfff44530c9bc96c46a403beaba77b56b5549a17d64fc090ff824c8ca302a`  
		Last Modified: Tue, 07 Jan 2025 04:54:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.20` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:53aa6f86240571ec82c49b6ae4b6db486ba3a3a86dc85aeda666281ce5fa8d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 KB (23046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56fef7fa9271a04f736a59aac8315c13f54c63ec8b813b33fae60bdbafbe8a7`

```dockerfile
```

-	Layers:
	-	`sha256:49577d947438769c75abf2585782b18e9d985c3cc0f1105707ff4f2481705ea3`  
		Last Modified: Fri, 07 Feb 2025 04:11:07 GMT  
		Size: 23.0 KB (23046 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.20` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:4705a440a3e5e3143f7c020c0f90833809b69fa325d8d2e0cc2fe4991b5b95bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4840552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cdb9a00077bbc2939b5e37241bf8b0da0a1ece3315f207d49b2fc765d488e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd3396764d5544adadcb96a804c10181b20cc0209495945ea8f4add1ab3c66c`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 749.4 KB (749413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c8deab35939b47ea7abcf3baf88258d9a3ca6ab8e188f8c4f2c73ee681f086`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.20` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:2ae224a4773e3bc1eb26d06a24ac62b8277dcf64ed99123453ce3e81c86eae64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 KB (201266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141e21516763808251a1e3845f81e43e7ab77fba34dba9ddaf9e2a71db76f0b4`

```dockerfile
```

-	Layers:
	-	`sha256:b224e0349955da5c177a7f07aeb6b38832fb75b88d6a631b0211cd59f5d18d94`  
		Last Modified: Tue, 14 Jan 2025 23:12:43 GMT  
		Size: 178.0 KB (177960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:198fa148210ff357d543bf58439890a01f268330be112f37cd8282098d3a112b`  
		Last Modified: Wed, 15 Jan 2025 10:06:47 GMT  
		Size: 23.3 KB (23306 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.20` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:0b323bfda696c5e714db988a73f5b2be6a80833470db3bb0965b181b2cda91d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4260337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845cf9cb3e2ae869796ae9ff1b80edb8cfd210fe67f16ab9c2cc11dbeb007026`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Tue, 14 Jan 2025 21:25:38 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936c1b63cf6e8cdeeea4b5d6033a46638313497f9b2a9c0f8d607a219d0e2e6c`  
		Last Modified: Tue, 14 Jan 2025 22:40:54 GMT  
		Size: 789.0 KB (788999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf9b7720cba29cd05912198bccbb71614e94b12d319af42d267d2ad4c51d61d`  
		Last Modified: Tue, 14 Jan 2025 22:41:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.20` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:25a05ba4caef99f524f8259740846431a514f2aedc5c3a0a9ff07938d809b51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 KB (200913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e0c91d29eed6106c83da1c6517bf9ff5ffcca6b2003a1f45ff7d00741c3c8b`

```dockerfile
```

-	Layers:
	-	`sha256:1ff7940e4598d1118a7f5e53ca6a755875bafdbc5a6677c198efcd82d2df121e`  
		Last Modified: Tue, 14 Jan 2025 22:39:59 GMT  
		Size: 177.8 KB (177811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:086d3237e5b048be94530403c08cfd8db9ef92faf3667fad8fe72482e07f0558`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 23.1 KB (23102 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.20` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:5fab56124ad7c1d854a5a212e280aa3bfd60ed668fd5415b551c42e5ea6644b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4394954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f167a42b5a1f7805744d4019f133f9e9ffc8e3817cb99ceeb23cf018ef7de9c6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bca7957551d2d47d18f0573ab65e77e7a0049808dfc8431dde2aad1dce1df7e`  
		Last Modified: Tue, 14 Jan 2025 23:12:50 GMT  
		Size: 820.2 KB (820180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2515d8b8efe0a20c199f560345325242482095029a59ed77ce90cf5b2ff7a078`  
		Last Modified: Tue, 14 Jan 2025 22:41:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.20` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:054a4fd52f0aa9ed530ea99a77a749042fa31ea3c9faa43b881b6dfe44945508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 KB (199184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b320ffadb3c981e8584604c7e5cda6629bcaff3fcec416587d2f9f260731696f`

```dockerfile
```

-	Layers:
	-	`sha256:edefd3739471fd1920f96937ecc474eb3193a4e02045ee18ab7037dfc75aa47b`  
		Last Modified: Tue, 14 Jan 2025 22:39:59 GMT  
		Size: 176.0 KB (175963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d333b77ae5d873e2408d01980c1296376a773498803fdf05daa366303e5e12`  
		Last Modified: Tue, 14 Jan 2025 23:12:53 GMT  
		Size: 23.2 KB (23221 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.20` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:6566e22afc536f5300c8723e4c312ca70b055193046d0ef65623c4e3452f9a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9930794d9d2da57ed64bd9ad82bcfd104d630760d8b24fd9eb00a8751a399cdf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Tue, 14 Jan 2025 21:25:41 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d61aecfc928aac1e86f36feab6688c31e6a97b32fe2a08c415adc81490ecf9`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 772.2 KB (772219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1414ddbc706e322cd9d926d7fcc42bebb5d75b4458410e1029a33beaca0e8e`  
		Last Modified: Tue, 14 Jan 2025 23:12:55 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.20` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:34a0e7319af5a8367bf45603fc7cc5e7620b7b216df88e9a92f65d2a63b46e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 KB (199059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff152e1055a34741555f319cc37e0b20fd52d4d55e115d485f427235b2f56397`

```dockerfile
```

-	Layers:
	-	`sha256:2ed494cc2bcc91abae48b391ab2f13c2e096b39c448c59f71a01aa637f35a26b`  
		Last Modified: Fri, 07 Feb 2025 04:11:13 GMT  
		Size: 175.9 KB (175905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f491631fd3f201aa258112eac820764ec18bcf824822cb6f9267e3c9bef8ec`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 23.2 KB (23154 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:2.0.20-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:deae95623b9d5c6ca5e264380629db53b992106d436b56d42f7c8df46b41b96f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-mosquitto:2.0.20-openssl` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:7ee09b4dd85ea25f07922128f305585353c2834ab1cde8a69632cfe649fe7152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4373995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61843a2255ff7a0209cb452bc90af4a3af41df986808b50e2afe8df58a014336`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fe382c8a5ef350b25cf6bb57e83ab7fc2fd802c316d75e3129862fb03e5e4e`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 747.4 KB (747366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8fa0745f9b4cc560107aafbd512c9a4fad59d47e7f2a609088a75a97784041`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.20-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:8541bec48e97eea558b833c4251eca6f3f648b0730099962ef9848ae6de39567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 KB (201010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3476c032209b261f4619ec09d88769bff67dad4bf688eda0a3df8ef323b632`

```dockerfile
```

-	Layers:
	-	`sha256:1170e9102fecfd36e81bde2fbb5d0e71e74640051080213d95eb4ce970aab458`  
		Last Modified: Tue, 14 Jan 2025 22:39:47 GMT  
		Size: 177.9 KB (177856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba745a327008881921b67b12c0f52ae9955f1dc8a2c804100411d55bdcbe1ee7`  
		Last Modified: Tue, 14 Jan 2025 23:12:34 GMT  
		Size: 23.2 KB (23154 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.20-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:843c16811e277436b5c5acc57166556ff7667d1ab30e9dddb73f32fc931a297b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35381791854c245f7863716ef5582c6e4e38dd4796e715ef8ae035825930586`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Tue, 14 Jan 2025 20:34:27 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33741ccf332fedc54086f78955a7f7c062d68e9c570b54c2fcbd664d1e0be110`  
		Last Modified: Tue, 14 Jan 2025 20:34:23 GMT  
		Size: 719.9 KB (719862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4cfff44530c9bc96c46a403beaba77b56b5549a17d64fc090ff824c8ca302a`  
		Last Modified: Tue, 07 Jan 2025 04:54:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.20-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:53aa6f86240571ec82c49b6ae4b6db486ba3a3a86dc85aeda666281ce5fa8d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 KB (23046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56fef7fa9271a04f736a59aac8315c13f54c63ec8b813b33fae60bdbafbe8a7`

```dockerfile
```

-	Layers:
	-	`sha256:49577d947438769c75abf2585782b18e9d985c3cc0f1105707ff4f2481705ea3`  
		Last Modified: Fri, 07 Feb 2025 04:11:07 GMT  
		Size: 23.0 KB (23046 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.20-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:4705a440a3e5e3143f7c020c0f90833809b69fa325d8d2e0cc2fe4991b5b95bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4840552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cdb9a00077bbc2939b5e37241bf8b0da0a1ece3315f207d49b2fc765d488e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd3396764d5544adadcb96a804c10181b20cc0209495945ea8f4add1ab3c66c`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 749.4 KB (749413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c8deab35939b47ea7abcf3baf88258d9a3ca6ab8e188f8c4f2c73ee681f086`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.20-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:2ae224a4773e3bc1eb26d06a24ac62b8277dcf64ed99123453ce3e81c86eae64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 KB (201266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141e21516763808251a1e3845f81e43e7ab77fba34dba9ddaf9e2a71db76f0b4`

```dockerfile
```

-	Layers:
	-	`sha256:b224e0349955da5c177a7f07aeb6b38832fb75b88d6a631b0211cd59f5d18d94`  
		Last Modified: Tue, 14 Jan 2025 23:12:43 GMT  
		Size: 178.0 KB (177960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:198fa148210ff357d543bf58439890a01f268330be112f37cd8282098d3a112b`  
		Last Modified: Wed, 15 Jan 2025 10:06:47 GMT  
		Size: 23.3 KB (23306 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.20-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:0b323bfda696c5e714db988a73f5b2be6a80833470db3bb0965b181b2cda91d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4260337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845cf9cb3e2ae869796ae9ff1b80edb8cfd210fe67f16ab9c2cc11dbeb007026`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Tue, 14 Jan 2025 21:25:38 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936c1b63cf6e8cdeeea4b5d6033a46638313497f9b2a9c0f8d607a219d0e2e6c`  
		Last Modified: Tue, 14 Jan 2025 22:40:54 GMT  
		Size: 789.0 KB (788999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf9b7720cba29cd05912198bccbb71614e94b12d319af42d267d2ad4c51d61d`  
		Last Modified: Tue, 14 Jan 2025 22:41:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.20-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:25a05ba4caef99f524f8259740846431a514f2aedc5c3a0a9ff07938d809b51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 KB (200913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e0c91d29eed6106c83da1c6517bf9ff5ffcca6b2003a1f45ff7d00741c3c8b`

```dockerfile
```

-	Layers:
	-	`sha256:1ff7940e4598d1118a7f5e53ca6a755875bafdbc5a6677c198efcd82d2df121e`  
		Last Modified: Tue, 14 Jan 2025 22:39:59 GMT  
		Size: 177.8 KB (177811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:086d3237e5b048be94530403c08cfd8db9ef92faf3667fad8fe72482e07f0558`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 23.1 KB (23102 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.20-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:5fab56124ad7c1d854a5a212e280aa3bfd60ed668fd5415b551c42e5ea6644b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4394954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f167a42b5a1f7805744d4019f133f9e9ffc8e3817cb99ceeb23cf018ef7de9c6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bca7957551d2d47d18f0573ab65e77e7a0049808dfc8431dde2aad1dce1df7e`  
		Last Modified: Tue, 14 Jan 2025 23:12:50 GMT  
		Size: 820.2 KB (820180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2515d8b8efe0a20c199f560345325242482095029a59ed77ce90cf5b2ff7a078`  
		Last Modified: Tue, 14 Jan 2025 22:41:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.20-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:054a4fd52f0aa9ed530ea99a77a749042fa31ea3c9faa43b881b6dfe44945508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 KB (199184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b320ffadb3c981e8584604c7e5cda6629bcaff3fcec416587d2f9f260731696f`

```dockerfile
```

-	Layers:
	-	`sha256:edefd3739471fd1920f96937ecc474eb3193a4e02045ee18ab7037dfc75aa47b`  
		Last Modified: Tue, 14 Jan 2025 22:39:59 GMT  
		Size: 176.0 KB (175963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d333b77ae5d873e2408d01980c1296376a773498803fdf05daa366303e5e12`  
		Last Modified: Tue, 14 Jan 2025 23:12:53 GMT  
		Size: 23.2 KB (23221 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.20-openssl` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:6566e22afc536f5300c8723e4c312ca70b055193046d0ef65623c4e3452f9a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9930794d9d2da57ed64bd9ad82bcfd104d630760d8b24fd9eb00a8751a399cdf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Tue, 14 Jan 2025 21:25:41 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d61aecfc928aac1e86f36feab6688c31e6a97b32fe2a08c415adc81490ecf9`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 772.2 KB (772219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1414ddbc706e322cd9d926d7fcc42bebb5d75b4458410e1029a33beaca0e8e`  
		Last Modified: Tue, 14 Jan 2025 23:12:55 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.20-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:34a0e7319af5a8367bf45603fc7cc5e7620b7b216df88e9a92f65d2a63b46e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 KB (199059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff152e1055a34741555f319cc37e0b20fd52d4d55e115d485f427235b2f56397`

```dockerfile
```

-	Layers:
	-	`sha256:2ed494cc2bcc91abae48b391ab2f13c2e096b39c448c59f71a01aa637f35a26b`  
		Last Modified: Fri, 07 Feb 2025 04:11:13 GMT  
		Size: 175.9 KB (175905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f491631fd3f201aa258112eac820764ec18bcf824822cb6f9267e3c9bef8ec`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 23.2 KB (23154 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:latest`

```console
$ docker pull eclipse-mosquitto@sha256:deae95623b9d5c6ca5e264380629db53b992106d436b56d42f7c8df46b41b96f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-mosquitto:latest` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:7ee09b4dd85ea25f07922128f305585353c2834ab1cde8a69632cfe649fe7152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4373995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61843a2255ff7a0209cb452bc90af4a3af41df986808b50e2afe8df58a014336`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fe382c8a5ef350b25cf6bb57e83ab7fc2fd802c316d75e3129862fb03e5e4e`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 747.4 KB (747366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8fa0745f9b4cc560107aafbd512c9a4fad59d47e7f2a609088a75a97784041`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:8541bec48e97eea558b833c4251eca6f3f648b0730099962ef9848ae6de39567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 KB (201010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3476c032209b261f4619ec09d88769bff67dad4bf688eda0a3df8ef323b632`

```dockerfile
```

-	Layers:
	-	`sha256:1170e9102fecfd36e81bde2fbb5d0e71e74640051080213d95eb4ce970aab458`  
		Last Modified: Tue, 14 Jan 2025 22:39:47 GMT  
		Size: 177.9 KB (177856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba745a327008881921b67b12c0f52ae9955f1dc8a2c804100411d55bdcbe1ee7`  
		Last Modified: Tue, 14 Jan 2025 23:12:34 GMT  
		Size: 23.2 KB (23154 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:latest` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:843c16811e277436b5c5acc57166556ff7667d1ab30e9dddb73f32fc931a297b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35381791854c245f7863716ef5582c6e4e38dd4796e715ef8ae035825930586`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Tue, 14 Jan 2025 20:34:27 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33741ccf332fedc54086f78955a7f7c062d68e9c570b54c2fcbd664d1e0be110`  
		Last Modified: Tue, 14 Jan 2025 20:34:23 GMT  
		Size: 719.9 KB (719862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4cfff44530c9bc96c46a403beaba77b56b5549a17d64fc090ff824c8ca302a`  
		Last Modified: Tue, 07 Jan 2025 04:54:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:53aa6f86240571ec82c49b6ae4b6db486ba3a3a86dc85aeda666281ce5fa8d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 KB (23046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56fef7fa9271a04f736a59aac8315c13f54c63ec8b813b33fae60bdbafbe8a7`

```dockerfile
```

-	Layers:
	-	`sha256:49577d947438769c75abf2585782b18e9d985c3cc0f1105707ff4f2481705ea3`  
		Last Modified: Fri, 07 Feb 2025 04:11:07 GMT  
		Size: 23.0 KB (23046 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:latest` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:4705a440a3e5e3143f7c020c0f90833809b69fa325d8d2e0cc2fe4991b5b95bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4840552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cdb9a00077bbc2939b5e37241bf8b0da0a1ece3315f207d49b2fc765d488e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd3396764d5544adadcb96a804c10181b20cc0209495945ea8f4add1ab3c66c`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 749.4 KB (749413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c8deab35939b47ea7abcf3baf88258d9a3ca6ab8e188f8c4f2c73ee681f086`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:2ae224a4773e3bc1eb26d06a24ac62b8277dcf64ed99123453ce3e81c86eae64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 KB (201266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141e21516763808251a1e3845f81e43e7ab77fba34dba9ddaf9e2a71db76f0b4`

```dockerfile
```

-	Layers:
	-	`sha256:b224e0349955da5c177a7f07aeb6b38832fb75b88d6a631b0211cd59f5d18d94`  
		Last Modified: Tue, 14 Jan 2025 23:12:43 GMT  
		Size: 178.0 KB (177960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:198fa148210ff357d543bf58439890a01f268330be112f37cd8282098d3a112b`  
		Last Modified: Wed, 15 Jan 2025 10:06:47 GMT  
		Size: 23.3 KB (23306 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:latest` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:0b323bfda696c5e714db988a73f5b2be6a80833470db3bb0965b181b2cda91d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4260337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845cf9cb3e2ae869796ae9ff1b80edb8cfd210fe67f16ab9c2cc11dbeb007026`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Tue, 14 Jan 2025 21:25:38 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936c1b63cf6e8cdeeea4b5d6033a46638313497f9b2a9c0f8d607a219d0e2e6c`  
		Last Modified: Tue, 14 Jan 2025 22:40:54 GMT  
		Size: 789.0 KB (788999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf9b7720cba29cd05912198bccbb71614e94b12d319af42d267d2ad4c51d61d`  
		Last Modified: Tue, 14 Jan 2025 22:41:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:25a05ba4caef99f524f8259740846431a514f2aedc5c3a0a9ff07938d809b51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 KB (200913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e0c91d29eed6106c83da1c6517bf9ff5ffcca6b2003a1f45ff7d00741c3c8b`

```dockerfile
```

-	Layers:
	-	`sha256:1ff7940e4598d1118a7f5e53ca6a755875bafdbc5a6677c198efcd82d2df121e`  
		Last Modified: Tue, 14 Jan 2025 22:39:59 GMT  
		Size: 177.8 KB (177811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:086d3237e5b048be94530403c08cfd8db9ef92faf3667fad8fe72482e07f0558`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 23.1 KB (23102 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:latest` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:5fab56124ad7c1d854a5a212e280aa3bfd60ed668fd5415b551c42e5ea6644b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4394954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f167a42b5a1f7805744d4019f133f9e9ffc8e3817cb99ceeb23cf018ef7de9c6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bca7957551d2d47d18f0573ab65e77e7a0049808dfc8431dde2aad1dce1df7e`  
		Last Modified: Tue, 14 Jan 2025 23:12:50 GMT  
		Size: 820.2 KB (820180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2515d8b8efe0a20c199f560345325242482095029a59ed77ce90cf5b2ff7a078`  
		Last Modified: Tue, 14 Jan 2025 22:41:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:054a4fd52f0aa9ed530ea99a77a749042fa31ea3c9faa43b881b6dfe44945508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 KB (199184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b320ffadb3c981e8584604c7e5cda6629bcaff3fcec416587d2f9f260731696f`

```dockerfile
```

-	Layers:
	-	`sha256:edefd3739471fd1920f96937ecc474eb3193a4e02045ee18ab7037dfc75aa47b`  
		Last Modified: Tue, 14 Jan 2025 22:39:59 GMT  
		Size: 176.0 KB (175963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d333b77ae5d873e2408d01980c1296376a773498803fdf05daa366303e5e12`  
		Last Modified: Tue, 14 Jan 2025 23:12:53 GMT  
		Size: 23.2 KB (23221 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:latest` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:6566e22afc536f5300c8723e4c312ca70b055193046d0ef65623c4e3452f9a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9930794d9d2da57ed64bd9ad82bcfd104d630760d8b24fd9eb00a8751a399cdf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Tue, 14 Jan 2025 21:25:41 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d61aecfc928aac1e86f36feab6688c31e6a97b32fe2a08c415adc81490ecf9`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 772.2 KB (772219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1414ddbc706e322cd9d926d7fcc42bebb5d75b4458410e1029a33beaca0e8e`  
		Last Modified: Tue, 14 Jan 2025 23:12:55 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:34a0e7319af5a8367bf45603fc7cc5e7620b7b216df88e9a92f65d2a63b46e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 KB (199059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff152e1055a34741555f319cc37e0b20fd52d4d55e115d485f427235b2f56397`

```dockerfile
```

-	Layers:
	-	`sha256:2ed494cc2bcc91abae48b391ab2f13c2e096b39c448c59f71a01aa637f35a26b`  
		Last Modified: Fri, 07 Feb 2025 04:11:13 GMT  
		Size: 175.9 KB (175905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f491631fd3f201aa258112eac820764ec18bcf824822cb6f9267e3c9bef8ec`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 23.2 KB (23154 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:openssl`

```console
$ docker pull eclipse-mosquitto@sha256:deae95623b9d5c6ca5e264380629db53b992106d436b56d42f7c8df46b41b96f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-mosquitto:openssl` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:7ee09b4dd85ea25f07922128f305585353c2834ab1cde8a69632cfe649fe7152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4373995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61843a2255ff7a0209cb452bc90af4a3af41df986808b50e2afe8df58a014336`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fe382c8a5ef350b25cf6bb57e83ab7fc2fd802c316d75e3129862fb03e5e4e`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 747.4 KB (747366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8fa0745f9b4cc560107aafbd512c9a4fad59d47e7f2a609088a75a97784041`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:8541bec48e97eea558b833c4251eca6f3f648b0730099962ef9848ae6de39567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 KB (201010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3476c032209b261f4619ec09d88769bff67dad4bf688eda0a3df8ef323b632`

```dockerfile
```

-	Layers:
	-	`sha256:1170e9102fecfd36e81bde2fbb5d0e71e74640051080213d95eb4ce970aab458`  
		Last Modified: Tue, 14 Jan 2025 22:39:47 GMT  
		Size: 177.9 KB (177856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba745a327008881921b67b12c0f52ae9955f1dc8a2c804100411d55bdcbe1ee7`  
		Last Modified: Tue, 14 Jan 2025 23:12:34 GMT  
		Size: 23.2 KB (23154 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:843c16811e277436b5c5acc57166556ff7667d1ab30e9dddb73f32fc931a297b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35381791854c245f7863716ef5582c6e4e38dd4796e715ef8ae035825930586`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Tue, 14 Jan 2025 20:34:27 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33741ccf332fedc54086f78955a7f7c062d68e9c570b54c2fcbd664d1e0be110`  
		Last Modified: Tue, 14 Jan 2025 20:34:23 GMT  
		Size: 719.9 KB (719862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4cfff44530c9bc96c46a403beaba77b56b5549a17d64fc090ff824c8ca302a`  
		Last Modified: Tue, 07 Jan 2025 04:54:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:53aa6f86240571ec82c49b6ae4b6db486ba3a3a86dc85aeda666281ce5fa8d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 KB (23046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56fef7fa9271a04f736a59aac8315c13f54c63ec8b813b33fae60bdbafbe8a7`

```dockerfile
```

-	Layers:
	-	`sha256:49577d947438769c75abf2585782b18e9d985c3cc0f1105707ff4f2481705ea3`  
		Last Modified: Fri, 07 Feb 2025 04:11:07 GMT  
		Size: 23.0 KB (23046 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:4705a440a3e5e3143f7c020c0f90833809b69fa325d8d2e0cc2fe4991b5b95bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4840552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cdb9a00077bbc2939b5e37241bf8b0da0a1ece3315f207d49b2fc765d488e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd3396764d5544adadcb96a804c10181b20cc0209495945ea8f4add1ab3c66c`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 749.4 KB (749413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c8deab35939b47ea7abcf3baf88258d9a3ca6ab8e188f8c4f2c73ee681f086`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:2ae224a4773e3bc1eb26d06a24ac62b8277dcf64ed99123453ce3e81c86eae64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 KB (201266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141e21516763808251a1e3845f81e43e7ab77fba34dba9ddaf9e2a71db76f0b4`

```dockerfile
```

-	Layers:
	-	`sha256:b224e0349955da5c177a7f07aeb6b38832fb75b88d6a631b0211cd59f5d18d94`  
		Last Modified: Tue, 14 Jan 2025 23:12:43 GMT  
		Size: 178.0 KB (177960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:198fa148210ff357d543bf58439890a01f268330be112f37cd8282098d3a112b`  
		Last Modified: Wed, 15 Jan 2025 10:06:47 GMT  
		Size: 23.3 KB (23306 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:0b323bfda696c5e714db988a73f5b2be6a80833470db3bb0965b181b2cda91d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4260337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845cf9cb3e2ae869796ae9ff1b80edb8cfd210fe67f16ab9c2cc11dbeb007026`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Tue, 14 Jan 2025 21:25:38 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936c1b63cf6e8cdeeea4b5d6033a46638313497f9b2a9c0f8d607a219d0e2e6c`  
		Last Modified: Tue, 14 Jan 2025 22:40:54 GMT  
		Size: 789.0 KB (788999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf9b7720cba29cd05912198bccbb71614e94b12d319af42d267d2ad4c51d61d`  
		Last Modified: Tue, 14 Jan 2025 22:41:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:25a05ba4caef99f524f8259740846431a514f2aedc5c3a0a9ff07938d809b51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 KB (200913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e0c91d29eed6106c83da1c6517bf9ff5ffcca6b2003a1f45ff7d00741c3c8b`

```dockerfile
```

-	Layers:
	-	`sha256:1ff7940e4598d1118a7f5e53ca6a755875bafdbc5a6677c198efcd82d2df121e`  
		Last Modified: Tue, 14 Jan 2025 22:39:59 GMT  
		Size: 177.8 KB (177811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:086d3237e5b048be94530403c08cfd8db9ef92faf3667fad8fe72482e07f0558`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 23.1 KB (23102 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:5fab56124ad7c1d854a5a212e280aa3bfd60ed668fd5415b551c42e5ea6644b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4394954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f167a42b5a1f7805744d4019f133f9e9ffc8e3817cb99ceeb23cf018ef7de9c6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bca7957551d2d47d18f0573ab65e77e7a0049808dfc8431dde2aad1dce1df7e`  
		Last Modified: Tue, 14 Jan 2025 23:12:50 GMT  
		Size: 820.2 KB (820180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2515d8b8efe0a20c199f560345325242482095029a59ed77ce90cf5b2ff7a078`  
		Last Modified: Tue, 14 Jan 2025 22:41:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:054a4fd52f0aa9ed530ea99a77a749042fa31ea3c9faa43b881b6dfe44945508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 KB (199184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b320ffadb3c981e8584604c7e5cda6629bcaff3fcec416587d2f9f260731696f`

```dockerfile
```

-	Layers:
	-	`sha256:edefd3739471fd1920f96937ecc474eb3193a4e02045ee18ab7037dfc75aa47b`  
		Last Modified: Tue, 14 Jan 2025 22:39:59 GMT  
		Size: 176.0 KB (175963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d333b77ae5d873e2408d01980c1296376a773498803fdf05daa366303e5e12`  
		Last Modified: Tue, 14 Jan 2025 23:12:53 GMT  
		Size: 23.2 KB (23221 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:openssl` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:6566e22afc536f5300c8723e4c312ca70b055193046d0ef65623c4e3452f9a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9930794d9d2da57ed64bd9ad82bcfd104d630760d8b24fd9eb00a8751a399cdf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 16 Oct 2024 19:28:05 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Wed, 16 Oct 2024 19:28:05 GMT
ENV VERSION=2.0.20 DOWNLOAD_SHA256=ebd07d89d2a446a7f74100ad51272e4a8bf300b61634a7812e19f068f2759de8 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Wed, 16 Oct 2024 19:28:05 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Wed, 16 Oct 2024 19:28:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Wed, 16 Oct 2024 19:28:05 GMT
EXPOSE map[1883/tcp:{}]
# Wed, 16 Oct 2024 19:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Oct 2024 19:28:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Tue, 14 Jan 2025 21:25:41 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d61aecfc928aac1e86f36feab6688c31e6a97b32fe2a08c415adc81490ecf9`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 772.2 KB (772219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1414ddbc706e322cd9d926d7fcc42bebb5d75b4458410e1029a33beaca0e8e`  
		Last Modified: Tue, 14 Jan 2025 23:12:55 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:34a0e7319af5a8367bf45603fc7cc5e7620b7b216df88e9a92f65d2a63b46e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 KB (199059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff152e1055a34741555f319cc37e0b20fd52d4d55e115d485f427235b2f56397`

```dockerfile
```

-	Layers:
	-	`sha256:2ed494cc2bcc91abae48b391ab2f13c2e096b39c448c59f71a01aa637f35a26b`  
		Last Modified: Fri, 07 Feb 2025 04:11:13 GMT  
		Size: 175.9 KB (175905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f491631fd3f201aa258112eac820764ec18bcf824822cb6f9267e3c9bef8ec`  
		Last Modified: Tue, 14 Jan 2025 22:41:03 GMT  
		Size: 23.2 KB (23154 bytes)  
		MIME: application/vnd.in-toto+json
