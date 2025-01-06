## `eclipse-mosquitto:latest`

```console
$ docker pull eclipse-mosquitto@sha256:8b396cec28cd5e8e1a3aba1d9abdbddd42c454c80f703e77c1bec56e152fa54e
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
$ docker pull eclipse-mosquitto@sha256:c16ebb350bd1509a33ee09edb5bafe4579fe53ae189b756362701bfdc2c0f931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc6f47a31a7d2f6996c82a7dd5e1256bfe4e678ec575424fb26d709020a76ee`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de46c2114acad22444684ef8cdefc1bdad3d32d491cf1c24d163295de016d878`  
		Last Modified: Tue, 12 Nov 2024 02:05:27 GMT  
		Size: 3.0 MB (3024519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da74935a2317a95fd13a230d45431c93931bbe3c9bbddb97590eee18804c9b61`  
		Last Modified: Tue, 12 Nov 2024 02:05:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:469d5b50c92c05a77a532d92057a863db1a75b20d754dd442fc752144e81786d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.0 KB (199988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfcd5ea387d4181a0152193121514c853cf3465d448284ca8810ae4586328a3d`

```dockerfile
```

-	Layers:
	-	`sha256:59a3e7d547b9ff513498b76f77f92edba946db7a7b4cf8b6c34dfad6e9a486e1`  
		Last Modified: Tue, 12 Nov 2024 02:05:27 GMT  
		Size: 176.8 KB (176833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d99bea79b5860e5162ba0b2c7f3db20bcf0b531479352bafff48acd95ae6c00a`  
		Last Modified: Tue, 12 Nov 2024 02:05:27 GMT  
		Size: 23.2 KB (23155 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:latest` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:6e5b912cf0befc4e0c092f6913d727146f087423c20b8cd25443a30444ae3477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b083df720357a98cb55fd9d537b528d994b81c3bd63f74d1379f22d2f1bac93c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51829d5d43c089a8246942341deefa2c8242b7442d478b64fbacc1179473edbf`  
		Last Modified: Tue, 12 Nov 2024 02:20:23 GMT  
		Size: 2.7 MB (2666385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5a146154c2093a1f0b751e8133ffd4f62c4e594b4b92865cdf991540d9b592`  
		Last Modified: Tue, 12 Nov 2024 02:20:22 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:0751f50e246544497d5f06ada5552a8dfa8781a50d8c002a7d8aa3a48305dee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 KB (23049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c060c49370824abfd6bb6aa2d9a7bb800ace1c0568978ee7a0f88066f6718a`

```dockerfile
```

-	Layers:
	-	`sha256:f5e2402ec4bb78640292ff820b5e5ca80b621bddd1bb50eddf70bc81ab68971d`  
		Size: 23.0 KB (23049 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:latest` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:8f93133e92a8f78397937f8e54ee82fc63d7d353c24ad5b4fb5d9171ccfca052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7527977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4372cc18130828529587cde9f1b17628e192c805c0ab21210f19b5492642f9f7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbe2020af9b0df3f8387377d437050df39ffa0a2ab721b4b3ae1d492222d099`  
		Last Modified: Tue, 12 Nov 2024 02:26:09 GMT  
		Size: 3.4 MB (3439881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41b8d2861724b73f190bd8f89c63a007f9c9ae3d23340333a89c784eb5b8fad`  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:aa930d4769436b4a215f8701a9cc01c490d01172a2705c0763a2dea2dedfa4dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 KB (200245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939c70bc400f1e9b0a2979d5cf597402c86636e8fbf8174ca2af9f5ef2869fc7`

```dockerfile
```

-	Layers:
	-	`sha256:6f7be0b98d62a82d51e83a143bf36063582e320ed137f306c3579b240fc85112`  
		Size: 176.9 KB (176937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8df825c897ff6577736a2b75ed5958b9291a45f31898d326082b6bfb8399086`  
		Last Modified: Tue, 12 Nov 2024 02:26:08 GMT  
		Size: 23.3 KB (23308 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:latest` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:bade7465a128bc618d2f53e24f100c285c587a3b4b4b4e1cde056afdd4767a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6370022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d925c7838d3675dcf05c124acccb167d0ae220c730075bf613fb871789d354`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3911662d97405ffe3ae632666c240ec4e9e5495469d0235d25f6b49090c7ed`  
		Last Modified: Tue, 12 Nov 2024 02:05:46 GMT  
		Size: 2.9 MB (2900434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4778340c31b80249ef6f320083fac7d58717d64127b1841bce106b2be4cb46b`  
		Last Modified: Tue, 12 Nov 2024 02:05:46 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:5e0a14f7a122166fc11d5c64902eb0076a5604df53218ed882f61d328ff235a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.9 KB (199892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bee7c776e6dbcd2f6981a0e33d596d4194f98687e35d98a69a08b94e8c06866`

```dockerfile
```

-	Layers:
	-	`sha256:2787d7312df2d74d9f534ddff5f2d19fe6bf9561baefe239d4b1494f19a2abdd`  
		Last Modified: Tue, 12 Nov 2024 02:05:46 GMT  
		Size: 176.8 KB (176788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acde177525fba6fae189205728c91217c4ffadc8b81f269ad0fafc33e60bea2f`  
		Last Modified: Tue, 12 Nov 2024 02:05:46 GMT  
		Size: 23.1 KB (23104 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:latest` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:314becd05a4bba484a44c93b1d6d1238637d05c6b1e603da061678af1bb77e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6533483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d6496ee5d513adf97cc857dd3ff7c3a4065886755e8528facf94756554bafb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5b082e88a57f7ac9413e7d78a1377d687b2c66a87d06a9fa5848386760bf01`  
		Last Modified: Tue, 12 Nov 2024 02:28:07 GMT  
		Size: 3.0 MB (2960655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46bd6a1997c02f498555470761daeb808d8396b1097f119c8ef84c4dd61a842`  
		Last Modified: Tue, 12 Nov 2024 02:28:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:e11dc28e3bfee2ca14b90b7b55b31eb61e59488731affe8cf197367b29a35094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 KB (198161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb98e92976879e9588fca57ea9fe84e98ef8b6ec858e87f636842449e4f4fc1e`

```dockerfile
```

-	Layers:
	-	`sha256:4025f483daf2ad478fd6b5123476971aa76f1c10c17239b0f0d9eec43e93cabf`  
		Last Modified: Tue, 12 Nov 2024 02:28:07 GMT  
		Size: 174.9 KB (174937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e7755b053da6716443a5cc0ada529682bf926bf11b7db31f2f93d8e29a5bd45`  
		Last Modified: Tue, 12 Nov 2024 02:28:07 GMT  
		Size: 23.2 KB (23224 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:latest` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:b466b7f89bef0b07e0a716892d2b457b860f86f1eac5b79ebc8810fe0d1f7530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6264506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791ed7bb8d74ad4fb59ab4e7555074c410320f65567dacafc699d6d6da259089`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a690ba9ee080706875646c1512b7e26b45a3f03cea61b4c73042002f185e8e02`  
		Last Modified: Tue, 12 Nov 2024 02:25:51 GMT  
		Size: 2.8 MB (2802530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b2f7f5a2fe6a31d16fda3ebecdbc7a0beaabf0ff10dd94766e06c1c0800c08`  
		Last Modified: Tue, 12 Nov 2024 02:25:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:d8db37861e3ce8b62c5b8ebadd45374ab2ebd349894001ee1d8c8906dda0752c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 KB (198035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dfb15f98db83becc29a54e5b91d2a32f8181559fccf4c52e933cecb17ef8d2a`

```dockerfile
```

-	Layers:
	-	`sha256:2fac6091b54264a4de5de80f8d66033cb757f3cf8740d6902364cff267f7e9ab`  
		Last Modified: Tue, 12 Nov 2024 02:25:51 GMT  
		Size: 174.9 KB (174879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9b05c6161202ed93bbfe13cbe794f9cc32072531e707d972261710af153aabd`  
		Size: 23.2 KB (23156 bytes)  
		MIME: application/vnd.in-toto+json
