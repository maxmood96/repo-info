<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eclipse-mosquitto`

-	[`eclipse-mosquitto:1.5`](#eclipse-mosquitto15)
-	[`eclipse-mosquitto:1.5.11`](#eclipse-mosquitto1511)
-	[`eclipse-mosquitto:1.6`](#eclipse-mosquitto16)
-	[`eclipse-mosquitto:1.6-openssl`](#eclipse-mosquitto16-openssl)
-	[`eclipse-mosquitto:1.6.15`](#eclipse-mosquitto1615)
-	[`eclipse-mosquitto:1.6.15-openssl`](#eclipse-mosquitto1615-openssl)
-	[`eclipse-mosquitto:2`](#eclipse-mosquitto2)
-	[`eclipse-mosquitto:2-openssl`](#eclipse-mosquitto2-openssl)
-	[`eclipse-mosquitto:2.0`](#eclipse-mosquitto20)
-	[`eclipse-mosquitto:2.0-openssl`](#eclipse-mosquitto20-openssl)
-	[`eclipse-mosquitto:2.0.15`](#eclipse-mosquitto2015)
-	[`eclipse-mosquitto:2.0.15-openssl`](#eclipse-mosquitto2015-openssl)
-	[`eclipse-mosquitto:latest`](#eclipse-mosquittolatest)
-	[`eclipse-mosquitto:openssl`](#eclipse-mosquittoopenssl)

## `eclipse-mosquitto:1.5`

```console
$ docker pull eclipse-mosquitto@sha256:e456f54793842f1a30af0596987d5c88639bb4af81e53f503127d4baf7cb595a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-mosquitto:1.5` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:1f5718aa533673e3e0dde3ee08ce44fdfa028085f5565cb843bb8529180442c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5392446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7231c892ef20f7cf3762b9c7fcb9a6eec65dbfdc717685f7c7279ccbc43a7c5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:59 GMT
ADD file:a41bb436701fd0adf99a3157d19f172b3e54ea033f5c617009e2d1bdeac206d7 in / 
# Sat, 11 Feb 2023 04:46:59 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:44:59 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 07:46:02 GMT
ENV VERSION=1.5.11 DOWNLOAD_SHA256=4a3b8a8f5505d27a7a966dd68bfd76f1e69feb51796d1b46b7271d1bb5a1a299 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=2.4.2 LWS_SHA256=73012d7fcf428dedccc816e83a63a01462e27819d5537b8e0d0c7264bfacfad6
# Sat, 11 Feb 2023 07:46:21 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -flto"         LDFLAGS="-L/build/lws/lib -flto"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl         libuuid &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 07:46:21 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 07:46:21 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Sat, 11 Feb 2023 07:46:22 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 07:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 07:46:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:d261077062b2aebb9ca8dc61f2b00e7e2b4e44179d3cfbe526c4ee0c5e41b26f`  
		Last Modified: Sat, 11 Feb 2023 04:47:49 GMT  
		Size: 2.8 MB (2829633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0285e9a4fb6514fc01428187b2ed72340dac83162f65627d85ce2c7115084dd5`  
		Last Modified: Sat, 11 Feb 2023 07:47:23 GMT  
		Size: 2.6 MB (2562575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c73f79be7f6f0025aa5c102dac93fd45f0e4f9eb0290e57de1f63e90200d5e6`  
		Last Modified: Sat, 11 Feb 2023 07:47:23 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.5` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:ab8d03511c387ea58a80ad393b6742597e55d45a68ba7b4c858a913a4bdf1ea5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5345350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc33917d5759f6dd51bd22c70ce699687e0adc47a8aa5cbae995f1c5a662e8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:54 GMT
ADD file:767f6566ea2c075838c0a86ca644a37e446f309f68952f5f921970f046abd252 in / 
# Mon, 13 Mar 2023 16:12:54 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 16:41:53 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 13 Mar 2023 16:43:03 GMT
ENV VERSION=1.5.11 DOWNLOAD_SHA256=4a3b8a8f5505d27a7a966dd68bfd76f1e69feb51796d1b46b7271d1bb5a1a299 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=2.4.2 LWS_SHA256=73012d7fcf428dedccc816e83a63a01462e27819d5537b8e0d0c7264bfacfad6
# Mon, 13 Mar 2023 16:43:23 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -flto"         LDFLAGS="-L/build/lws/lib -flto"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl         libuuid &&     apk del build-deps &&     rm -rf /build
# Mon, 13 Mar 2023 16:43:23 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 13 Mar 2023 16:43:23 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Mon, 13 Mar 2023 16:43:23 GMT
EXPOSE 1883
# Mon, 13 Mar 2023 16:43:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 13 Mar 2023 16:43:23 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:7616dd32f4bf5fddffb2543afaac2355a5fc495348c01060cd67181e36343e96`  
		Last Modified: Fri, 10 Feb 2023 20:51:02 GMT  
		Size: 2.6 MB (2638152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e8cb489ee6c2ce6d47206c24813015bac05de67dbdcae88c241bffc77f1d78`  
		Last Modified: Mon, 13 Mar 2023 16:44:56 GMT  
		Size: 2.7 MB (2706959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660c705d4fc05ae522fbb3020212ff8a87e44bf23b2d5649a06a924909323784`  
		Last Modified: Mon, 13 Mar 2023 16:44:56 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.5` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:75d4eede796149a3f897493aaaaf13a382136d102113abefe537444823b7d487
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5242661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c880468dfa908e6416d1739266ebf1dd211b81da9155b7e72af2b10a33c4bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:19 GMT
ADD file:50a841463966858f1c3ca87143cf96145d1d52f7349ef516adfbf21cdd5684fe in / 
# Fri, 10 Feb 2023 21:24:19 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:08:27 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:09:19 GMT
ENV VERSION=1.5.11 DOWNLOAD_SHA256=4a3b8a8f5505d27a7a966dd68bfd76f1e69feb51796d1b46b7271d1bb5a1a299 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=2.4.2 LWS_SHA256=73012d7fcf428dedccc816e83a63a01462e27819d5537b8e0d0c7264bfacfad6
# Fri, 10 Feb 2023 22:09:35 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -flto"         LDFLAGS="-L/build/lws/lib -flto"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl         libuuid &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:09:36 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:09:36 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Fri, 10 Feb 2023 22:09:36 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:09:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:09:36 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:6f0e733d82e26042c603e231c39b56abbabdad66673a736ec71c69c65be95f41`  
		Last Modified: Fri, 10 Feb 2023 21:25:10 GMT  
		Size: 2.7 MB (2725026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30c11874bdb67ffaf9ed11bb043195c49a69fec15665a1cc115cf87a062dfbe`  
		Last Modified: Fri, 10 Feb 2023 22:10:37 GMT  
		Size: 2.5 MB (2517395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3204aac963a34196ab9da42aa0abf9e5ed44746d02c77f4fdd102e55f8c05a`  
		Last Modified: Fri, 10 Feb 2023 22:10:37 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.5` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:058286143380c992868d1ca6ca8ece6eb27b0e31959b40d92d6a0b3d44d41c58
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5559153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad03eb3ed10e11e12ceaaeb2ae9381ec91c7dd95711df1b9b2ca777ae5d0b5f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:39 GMT
ADD file:d88c188553d983f16407f891790a4e553fda681fa265d89ec12a70ba2f41b0da in / 
# Fri, 10 Feb 2023 21:24:39 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:06:55 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:08:16 GMT
ENV VERSION=1.5.11 DOWNLOAD_SHA256=4a3b8a8f5505d27a7a966dd68bfd76f1e69feb51796d1b46b7271d1bb5a1a299 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=2.4.2 LWS_SHA256=73012d7fcf428dedccc816e83a63a01462e27819d5537b8e0d0c7264bfacfad6
# Fri, 10 Feb 2023 22:08:35 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -flto"         LDFLAGS="-L/build/lws/lib -flto"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl         libuuid &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:08:36 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:08:38 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Fri, 10 Feb 2023 22:08:38 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:08:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:08:40 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:84644bcd984e34c8b3bc44d8040b7017495e31100c1f4d726c92b40cf6cf7351`  
		Last Modified: Fri, 10 Feb 2023 21:25:51 GMT  
		Size: 2.8 MB (2835110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914b134f1e595c14151e4c5ea194938c314046a37a40f32fb71521196ba20eeb`  
		Last Modified: Fri, 10 Feb 2023 22:10:10 GMT  
		Size: 2.7 MB (2723804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668b9faae0100f446e829110cf3b68b56c1f27e083fccdb379eeca0da3731b7d`  
		Last Modified: Fri, 10 Feb 2023 22:10:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.5` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:6f3f6d42555279609d8feffd4bc677619137d354fcde262e7f41fae78d2ffd24
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5475329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f070a5773f614133df063c9c03def9ff5beb06a8e79a6284627fb391fe77fb70`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:21:00 GMT
ADD file:99507b43b1818a9e49705772be1d12eb9519e137ba653d9d569700b6f6d36523 in / 
# Fri, 10 Feb 2023 21:21:01 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:16:55 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:18:46 GMT
ENV VERSION=1.5.11 DOWNLOAD_SHA256=4a3b8a8f5505d27a7a966dd68bfd76f1e69feb51796d1b46b7271d1bb5a1a299 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=2.4.2 LWS_SHA256=73012d7fcf428dedccc816e83a63a01462e27819d5537b8e0d0c7264bfacfad6
# Fri, 10 Feb 2023 22:19:20 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -flto"         LDFLAGS="-L/build/lws/lib -flto"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl         libuuid &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:19:21 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:19:22 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Fri, 10 Feb 2023 22:19:22 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:19:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:19:23 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:443774f2f57bdbe836e7f8ee0ccfb6fc2c2f7f258030154416ae5c1c4528e756`  
		Last Modified: Fri, 10 Feb 2023 21:22:15 GMT  
		Size: 2.8 MB (2816405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52739073396e02c51243f3e67bfc0fe9a4deebd381345f992623da381f263d6e`  
		Last Modified: Fri, 10 Feb 2023 22:20:57 GMT  
		Size: 2.7 MB (2658685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3da093e50a17455dc252268016e2d9947afe02b8c52b2b956607b2578e2624`  
		Last Modified: Fri, 10 Feb 2023 22:20:56 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.5` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:f7715b263c9d7b55231b214da4819d62fa3349c1b8e2924f38fe5b7a8f42dc8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8294ec4ab1a85de9fe6c34a013995666bf296faf08530577d7db86dfdf936cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:43 GMT
ADD file:3590370451e8df75d0fe22ac6cb669c667358fd514c69df4be770a687f378871 in / 
# Fri, 10 Feb 2023 21:41:43 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:43:38 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 05:44:41 GMT
ENV VERSION=1.5.11 DOWNLOAD_SHA256=4a3b8a8f5505d27a7a966dd68bfd76f1e69feb51796d1b46b7271d1bb5a1a299 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=2.4.2 LWS_SHA256=73012d7fcf428dedccc816e83a63a01462e27819d5537b8e0d0c7264bfacfad6
# Sat, 11 Feb 2023 05:44:56 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -flto"         LDFLAGS="-L/build/lws/lib -flto"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl         libuuid &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 05:44:57 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 05:44:57 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Sat, 11 Feb 2023 05:44:57 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 05:44:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 05:44:57 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:ce265ad7528283161562836d2f4c84efa75654b4e39eab9bd3c332c7d288afda`  
		Last Modified: Fri, 10 Feb 2023 21:42:40 GMT  
		Size: 2.6 MB (2614244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039930bc6de76596c455b8a402595c31d76ccefa936d9d3b404cfa9e1764570f`  
		Last Modified: Sat, 11 Feb 2023 05:46:05 GMT  
		Size: 2.6 MB (2605882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373fbc16fcb42c50a466daf74c22548fcbcb9a3afe99bc3ba86a6bb603d65d7a`  
		Last Modified: Sat, 11 Feb 2023 05:46:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eclipse-mosquitto:1.5.11`

```console
$ docker pull eclipse-mosquitto@sha256:e456f54793842f1a30af0596987d5c88639bb4af81e53f503127d4baf7cb595a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-mosquitto:1.5.11` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:1f5718aa533673e3e0dde3ee08ce44fdfa028085f5565cb843bb8529180442c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5392446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7231c892ef20f7cf3762b9c7fcb9a6eec65dbfdc717685f7c7279ccbc43a7c5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:59 GMT
ADD file:a41bb436701fd0adf99a3157d19f172b3e54ea033f5c617009e2d1bdeac206d7 in / 
# Sat, 11 Feb 2023 04:46:59 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:44:59 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 07:46:02 GMT
ENV VERSION=1.5.11 DOWNLOAD_SHA256=4a3b8a8f5505d27a7a966dd68bfd76f1e69feb51796d1b46b7271d1bb5a1a299 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=2.4.2 LWS_SHA256=73012d7fcf428dedccc816e83a63a01462e27819d5537b8e0d0c7264bfacfad6
# Sat, 11 Feb 2023 07:46:21 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -flto"         LDFLAGS="-L/build/lws/lib -flto"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl         libuuid &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 07:46:21 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 07:46:21 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Sat, 11 Feb 2023 07:46:22 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 07:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 07:46:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:d261077062b2aebb9ca8dc61f2b00e7e2b4e44179d3cfbe526c4ee0c5e41b26f`  
		Last Modified: Sat, 11 Feb 2023 04:47:49 GMT  
		Size: 2.8 MB (2829633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0285e9a4fb6514fc01428187b2ed72340dac83162f65627d85ce2c7115084dd5`  
		Last Modified: Sat, 11 Feb 2023 07:47:23 GMT  
		Size: 2.6 MB (2562575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c73f79be7f6f0025aa5c102dac93fd45f0e4f9eb0290e57de1f63e90200d5e6`  
		Last Modified: Sat, 11 Feb 2023 07:47:23 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.5.11` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:ab8d03511c387ea58a80ad393b6742597e55d45a68ba7b4c858a913a4bdf1ea5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5345350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc33917d5759f6dd51bd22c70ce699687e0adc47a8aa5cbae995f1c5a662e8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:54 GMT
ADD file:767f6566ea2c075838c0a86ca644a37e446f309f68952f5f921970f046abd252 in / 
# Mon, 13 Mar 2023 16:12:54 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 16:41:53 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 13 Mar 2023 16:43:03 GMT
ENV VERSION=1.5.11 DOWNLOAD_SHA256=4a3b8a8f5505d27a7a966dd68bfd76f1e69feb51796d1b46b7271d1bb5a1a299 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=2.4.2 LWS_SHA256=73012d7fcf428dedccc816e83a63a01462e27819d5537b8e0d0c7264bfacfad6
# Mon, 13 Mar 2023 16:43:23 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -flto"         LDFLAGS="-L/build/lws/lib -flto"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl         libuuid &&     apk del build-deps &&     rm -rf /build
# Mon, 13 Mar 2023 16:43:23 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 13 Mar 2023 16:43:23 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Mon, 13 Mar 2023 16:43:23 GMT
EXPOSE 1883
# Mon, 13 Mar 2023 16:43:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 13 Mar 2023 16:43:23 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:7616dd32f4bf5fddffb2543afaac2355a5fc495348c01060cd67181e36343e96`  
		Last Modified: Fri, 10 Feb 2023 20:51:02 GMT  
		Size: 2.6 MB (2638152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e8cb489ee6c2ce6d47206c24813015bac05de67dbdcae88c241bffc77f1d78`  
		Last Modified: Mon, 13 Mar 2023 16:44:56 GMT  
		Size: 2.7 MB (2706959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660c705d4fc05ae522fbb3020212ff8a87e44bf23b2d5649a06a924909323784`  
		Last Modified: Mon, 13 Mar 2023 16:44:56 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.5.11` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:75d4eede796149a3f897493aaaaf13a382136d102113abefe537444823b7d487
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5242661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c880468dfa908e6416d1739266ebf1dd211b81da9155b7e72af2b10a33c4bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:19 GMT
ADD file:50a841463966858f1c3ca87143cf96145d1d52f7349ef516adfbf21cdd5684fe in / 
# Fri, 10 Feb 2023 21:24:19 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:08:27 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:09:19 GMT
ENV VERSION=1.5.11 DOWNLOAD_SHA256=4a3b8a8f5505d27a7a966dd68bfd76f1e69feb51796d1b46b7271d1bb5a1a299 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=2.4.2 LWS_SHA256=73012d7fcf428dedccc816e83a63a01462e27819d5537b8e0d0c7264bfacfad6
# Fri, 10 Feb 2023 22:09:35 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -flto"         LDFLAGS="-L/build/lws/lib -flto"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl         libuuid &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:09:36 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:09:36 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Fri, 10 Feb 2023 22:09:36 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:09:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:09:36 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:6f0e733d82e26042c603e231c39b56abbabdad66673a736ec71c69c65be95f41`  
		Last Modified: Fri, 10 Feb 2023 21:25:10 GMT  
		Size: 2.7 MB (2725026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30c11874bdb67ffaf9ed11bb043195c49a69fec15665a1cc115cf87a062dfbe`  
		Last Modified: Fri, 10 Feb 2023 22:10:37 GMT  
		Size: 2.5 MB (2517395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3204aac963a34196ab9da42aa0abf9e5ed44746d02c77f4fdd102e55f8c05a`  
		Last Modified: Fri, 10 Feb 2023 22:10:37 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.5.11` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:058286143380c992868d1ca6ca8ece6eb27b0e31959b40d92d6a0b3d44d41c58
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5559153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad03eb3ed10e11e12ceaaeb2ae9381ec91c7dd95711df1b9b2ca777ae5d0b5f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:39 GMT
ADD file:d88c188553d983f16407f891790a4e553fda681fa265d89ec12a70ba2f41b0da in / 
# Fri, 10 Feb 2023 21:24:39 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:06:55 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:08:16 GMT
ENV VERSION=1.5.11 DOWNLOAD_SHA256=4a3b8a8f5505d27a7a966dd68bfd76f1e69feb51796d1b46b7271d1bb5a1a299 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=2.4.2 LWS_SHA256=73012d7fcf428dedccc816e83a63a01462e27819d5537b8e0d0c7264bfacfad6
# Fri, 10 Feb 2023 22:08:35 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -flto"         LDFLAGS="-L/build/lws/lib -flto"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl         libuuid &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:08:36 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:08:38 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Fri, 10 Feb 2023 22:08:38 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:08:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:08:40 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:84644bcd984e34c8b3bc44d8040b7017495e31100c1f4d726c92b40cf6cf7351`  
		Last Modified: Fri, 10 Feb 2023 21:25:51 GMT  
		Size: 2.8 MB (2835110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914b134f1e595c14151e4c5ea194938c314046a37a40f32fb71521196ba20eeb`  
		Last Modified: Fri, 10 Feb 2023 22:10:10 GMT  
		Size: 2.7 MB (2723804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668b9faae0100f446e829110cf3b68b56c1f27e083fccdb379eeca0da3731b7d`  
		Last Modified: Fri, 10 Feb 2023 22:10:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.5.11` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:6f3f6d42555279609d8feffd4bc677619137d354fcde262e7f41fae78d2ffd24
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5475329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f070a5773f614133df063c9c03def9ff5beb06a8e79a6284627fb391fe77fb70`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:21:00 GMT
ADD file:99507b43b1818a9e49705772be1d12eb9519e137ba653d9d569700b6f6d36523 in / 
# Fri, 10 Feb 2023 21:21:01 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:16:55 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:18:46 GMT
ENV VERSION=1.5.11 DOWNLOAD_SHA256=4a3b8a8f5505d27a7a966dd68bfd76f1e69feb51796d1b46b7271d1bb5a1a299 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=2.4.2 LWS_SHA256=73012d7fcf428dedccc816e83a63a01462e27819d5537b8e0d0c7264bfacfad6
# Fri, 10 Feb 2023 22:19:20 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -flto"         LDFLAGS="-L/build/lws/lib -flto"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl         libuuid &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:19:21 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:19:22 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Fri, 10 Feb 2023 22:19:22 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:19:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:19:23 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:443774f2f57bdbe836e7f8ee0ccfb6fc2c2f7f258030154416ae5c1c4528e756`  
		Last Modified: Fri, 10 Feb 2023 21:22:15 GMT  
		Size: 2.8 MB (2816405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52739073396e02c51243f3e67bfc0fe9a4deebd381345f992623da381f263d6e`  
		Last Modified: Fri, 10 Feb 2023 22:20:57 GMT  
		Size: 2.7 MB (2658685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3da093e50a17455dc252268016e2d9947afe02b8c52b2b956607b2578e2624`  
		Last Modified: Fri, 10 Feb 2023 22:20:56 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.5.11` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:f7715b263c9d7b55231b214da4819d62fa3349c1b8e2924f38fe5b7a8f42dc8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8294ec4ab1a85de9fe6c34a013995666bf296faf08530577d7db86dfdf936cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:43 GMT
ADD file:3590370451e8df75d0fe22ac6cb669c667358fd514c69df4be770a687f378871 in / 
# Fri, 10 Feb 2023 21:41:43 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:43:38 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 05:44:41 GMT
ENV VERSION=1.5.11 DOWNLOAD_SHA256=4a3b8a8f5505d27a7a966dd68bfd76f1e69feb51796d1b46b7271d1bb5a1a299 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=2.4.2 LWS_SHA256=73012d7fcf428dedccc816e83a63a01462e27819d5537b8e0d0c7264bfacfad6
# Sat, 11 Feb 2023 05:44:56 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -flto"         LDFLAGS="-L/build/lws/lib -flto"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl         libuuid &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 05:44:57 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 05:44:57 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Sat, 11 Feb 2023 05:44:57 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 05:44:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 05:44:57 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:ce265ad7528283161562836d2f4c84efa75654b4e39eab9bd3c332c7d288afda`  
		Last Modified: Fri, 10 Feb 2023 21:42:40 GMT  
		Size: 2.6 MB (2614244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039930bc6de76596c455b8a402595c31d76ccefa936d9d3b404cfa9e1764570f`  
		Last Modified: Sat, 11 Feb 2023 05:46:05 GMT  
		Size: 2.6 MB (2605882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373fbc16fcb42c50a466daf74c22548fcbcb9a3afe99bc3ba86a6bb603d65d7a`  
		Last Modified: Sat, 11 Feb 2023 05:46:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eclipse-mosquitto:1.6`

```console
$ docker pull eclipse-mosquitto@sha256:bba4c72b43df4333ec7cd800e8e7278c674cbf2adc907f3405f7076e297c8e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-mosquitto:1.6` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:98cdafca37391270aa5e16362fac52fb21e606be2d6cee65d16965418d6dabb6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5513791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b338ee795ed5ed29e780661f54f05bfc644bd5d637d4397d76a4fa6736e77d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:59 GMT
ADD file:a41bb436701fd0adf99a3157d19f172b3e54ea033f5c617009e2d1bdeac206d7 in / 
# Sat, 11 Feb 2023 04:46:59 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:44:59 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 07:44:59 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 07:45:24 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 07:45:25 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 07:45:25 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Sat, 11 Feb 2023 07:45:25 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 07:45:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 07:45:25 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:d261077062b2aebb9ca8dc61f2b00e7e2b4e44179d3cfbe526c4ee0c5e41b26f`  
		Last Modified: Sat, 11 Feb 2023 04:47:49 GMT  
		Size: 2.8 MB (2829633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f56c2911bae1aa250f342877a41f78a69467dae9b01c62d5a8799c6f333a4e`  
		Last Modified: Sat, 11 Feb 2023 07:47:07 GMT  
		Size: 2.7 MB (2683919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206b090db03726760c8e2b19fb53530465e2b5e58ea30cb6478526f9440098cc`  
		Last Modified: Sat, 11 Feb 2023 07:47:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.6` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:04dae7fd9ecde738e95c42ccfe1906ff26f46aa7bf5eb77672f91ad44db4b795
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a378677ab03401ef33b4c4193c99d1898c7bfae5f25637db66133ca3637b3e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:54 GMT
ADD file:767f6566ea2c075838c0a86ca644a37e446f309f68952f5f921970f046abd252 in / 
# Mon, 13 Mar 2023 16:12:54 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 16:41:53 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 13 Mar 2023 16:41:53 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 13 Mar 2023 16:42:20 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl &&     apk del build-deps &&     rm -rf /build
# Mon, 13 Mar 2023 16:42:20 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 13 Mar 2023 16:42:20 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Mon, 13 Mar 2023 16:42:20 GMT
EXPOSE 1883
# Mon, 13 Mar 2023 16:42:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 13 Mar 2023 16:42:21 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:7616dd32f4bf5fddffb2543afaac2355a5fc495348c01060cd67181e36343e96`  
		Last Modified: Fri, 10 Feb 2023 20:51:02 GMT  
		Size: 2.6 MB (2638152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721ffab73c5d57ae9c7ff5136eb178e1308e4349ae1cf62b9504076c25b9a020`  
		Last Modified: Mon, 13 Mar 2023 16:44:36 GMT  
		Size: 2.8 MB (2811609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a3fb247065a772fcb0e1918c3f30efcd19156d2729d67d43a2e456c5e9796b`  
		Last Modified: Mon, 13 Mar 2023 16:44:36 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.6` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:d45682996a512b5a7faa0a1b25421119b0480ff772859505d635fa903ebd548b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5361737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fab828837071573a96e62b067c3969f8a987e2c45c6b9fcc1f8c8fac1bfa23`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:19 GMT
ADD file:50a841463966858f1c3ca87143cf96145d1d52f7349ef516adfbf21cdd5684fe in / 
# Fri, 10 Feb 2023 21:24:19 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:08:27 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:08:27 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:08:49 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:08:49 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:08:49 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Fri, 10 Feb 2023 22:08:49 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:08:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:08:49 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:6f0e733d82e26042c603e231c39b56abbabdad66673a736ec71c69c65be95f41`  
		Last Modified: Fri, 10 Feb 2023 21:25:10 GMT  
		Size: 2.7 MB (2725026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d0a544b126f253e231f49f2449b3e90c6f53bae60d068f33ae67e5d8e011e2`  
		Last Modified: Fri, 10 Feb 2023 22:10:21 GMT  
		Size: 2.6 MB (2636472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847b297767b219f1e402cae285521ca609148ecd35db885afb1be3cc61a788dd`  
		Last Modified: Fri, 10 Feb 2023 22:10:20 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.6` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:c88077c15a29f2a2abc0ef5e2549ab9d7fe0da48f6c3670769df14dd773f4e7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5691916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1875a844d84d614811f4adcc238eaef75c03b7ac8fd5c247fb27b66a913ebc8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:39 GMT
ADD file:d88c188553d983f16407f891790a4e553fda681fa265d89ec12a70ba2f41b0da in / 
# Fri, 10 Feb 2023 21:24:39 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:06:55 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:06:56 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:07:25 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:07:26 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:07:28 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Fri, 10 Feb 2023 22:07:28 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:07:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:07:30 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:84644bcd984e34c8b3bc44d8040b7017495e31100c1f4d726c92b40cf6cf7351`  
		Last Modified: Fri, 10 Feb 2023 21:25:51 GMT  
		Size: 2.8 MB (2835110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a540208296e52bc68ac3012039efe40ab7fb4421bf1f2ebfc06b780d5c2960`  
		Last Modified: Fri, 10 Feb 2023 22:09:49 GMT  
		Size: 2.9 MB (2856567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a944dfae6d082118039136e4ec1916ff6dc652a8423fdb96646c97d49776c09`  
		Last Modified: Fri, 10 Feb 2023 22:09:48 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.6` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:b7b50586040f3a0d158eea12f94bdb992f126228fe099fc5ac9b708979452765
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782d3fe21ec87f311b4a24b93b9d2bfb96df15b5fa936eb6e8f336d98718f319`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:21:00 GMT
ADD file:99507b43b1818a9e49705772be1d12eb9519e137ba653d9d569700b6f6d36523 in / 
# Fri, 10 Feb 2023 21:21:01 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:16:55 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:16:56 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:17:48 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:17:49 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:17:49 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Fri, 10 Feb 2023 22:17:50 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:17:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:17:51 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:443774f2f57bdbe836e7f8ee0ccfb6fc2c2f7f258030154416ae5c1c4528e756`  
		Last Modified: Fri, 10 Feb 2023 21:22:15 GMT  
		Size: 2.8 MB (2816405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e750287a787c89330386cf3e719c731a3c78b9c7e5bb8eb1889c0e29718010`  
		Last Modified: Fri, 10 Feb 2023 22:20:36 GMT  
		Size: 2.8 MB (2794656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a3125202bee750214c598e4a41e017a1e2e5895bbd703aa86a66376d15bbaa`  
		Last Modified: Fri, 10 Feb 2023 22:20:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.6` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:3f286207641c5c9e862bb73fa9f840a84b27fd31227126ea5330b3b2935c232b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5341194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fa2a41e266098253ef7a9e41efd21412078eb1d8650ecb04306d58b2196ef6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:43 GMT
ADD file:3590370451e8df75d0fe22ac6cb669c667358fd514c69df4be770a687f378871 in / 
# Fri, 10 Feb 2023 21:41:43 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:43:38 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 05:43:38 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 05:44:04 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 05:44:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 05:44:05 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Sat, 11 Feb 2023 05:44:05 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 05:44:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 05:44:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:ce265ad7528283161562836d2f4c84efa75654b4e39eab9bd3c332c7d288afda`  
		Last Modified: Fri, 10 Feb 2023 21:42:40 GMT  
		Size: 2.6 MB (2614244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc094062e65aeae7064da7c7d9a0bed8096aa1d339e8351ee887ba8c7a6a4599`  
		Last Modified: Sat, 11 Feb 2023 05:45:53 GMT  
		Size: 2.7 MB (2726711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abd18395b95c2f3f8538f859a13840028db467551c20bc3e61def7c259aead8`  
		Last Modified: Sat, 11 Feb 2023 05:45:53 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eclipse-mosquitto:1.6-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:6d51a71252793a188ae42e12182666813e581c8ad63c50de5cc3fbc7b180be72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-mosquitto:1.6-openssl` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:1ac7f25c9c9a58bf7db67841f953d9d33e98c7f89b93fd2825462095b33ded53
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3462341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe766e8a1a8cb072083275be56f282363c509144c776dba3e65f821bca67cb05`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:59 GMT
ADD file:a41bb436701fd0adf99a3157d19f172b3e54ea033f5c617009e2d1bdeac206d7 in / 
# Sat, 11 Feb 2023 04:46:59 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:44:59 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 07:44:59 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 07:45:54 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 07:45:54 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 07:45:54 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Sat, 11 Feb 2023 07:45:54 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 07:45:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 07:45:54 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:d261077062b2aebb9ca8dc61f2b00e7e2b4e44179d3cfbe526c4ee0c5e41b26f`  
		Last Modified: Sat, 11 Feb 2023 04:47:49 GMT  
		Size: 2.8 MB (2829633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c922d605245e7205d56068935a92ba0e394f9a30066aaa4539da7724b9ff35d1`  
		Last Modified: Sat, 11 Feb 2023 07:47:15 GMT  
		Size: 632.5 KB (632468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ddf14bb7e22b47e57414c8da70362d07eb82ed0259ee5061948ca419221b779`  
		Last Modified: Sat, 11 Feb 2023 07:47:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.6-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:9d137fde9c54c69e7b99fdca7bcd85f672e77e33a26ad089a902be96e5e5d420
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a62338d6d68ba26e8e4bf64e705cc4485ba35e7645a47e1d11c654d19d1d0e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:54 GMT
ADD file:767f6566ea2c075838c0a86ca644a37e446f309f68952f5f921970f046abd252 in / 
# Mon, 13 Mar 2023 16:12:54 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 16:41:53 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 13 Mar 2023 16:41:53 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 13 Mar 2023 16:42:54 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build
# Mon, 13 Mar 2023 16:42:54 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 13 Mar 2023 16:42:54 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Mon, 13 Mar 2023 16:42:54 GMT
EXPOSE 1883
# Mon, 13 Mar 2023 16:42:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 13 Mar 2023 16:42:54 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:7616dd32f4bf5fddffb2543afaac2355a5fc495348c01060cd67181e36343e96`  
		Last Modified: Fri, 10 Feb 2023 20:51:02 GMT  
		Size: 2.6 MB (2638152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72acd984f03c8327db04b5b14950c1a1ae0aaf1928e0dfb4bb4b7400bded24d4`  
		Last Modified: Mon, 13 Mar 2023 16:44:46 GMT  
		Size: 996.5 KB (996507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ba27f0521195a9dfb7e417711c2500754332f225e2edeea87c1288cf66593a`  
		Last Modified: Mon, 13 Mar 2023 16:44:46 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.6-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:c0fc66f7a9bbe7730276005029911867ef3cf66d68269a2db449298168554cab
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7c14cb6e5c4e1560588c4e14ba48b516fd28e67226f072e6561020f80b4d4a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:19 GMT
ADD file:50a841463966858f1c3ca87143cf96145d1d52f7349ef516adfbf21cdd5684fe in / 
# Fri, 10 Feb 2023 21:24:19 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:08:27 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:08:27 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:09:16 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:09:16 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:09:16 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Fri, 10 Feb 2023 22:09:16 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:09:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:09:17 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:6f0e733d82e26042c603e231c39b56abbabdad66673a736ec71c69c65be95f41`  
		Last Modified: Fri, 10 Feb 2023 21:25:10 GMT  
		Size: 2.7 MB (2725026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01001996eae7f51fd87e44f9d8bd3c872ab3c3aaa07c430c487f7149fdcf9e5a`  
		Last Modified: Fri, 10 Feb 2023 22:10:29 GMT  
		Size: 628.9 KB (628869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2225ea1b0166229f7d10f78ee8f11f3873f63beadffa8bcc070539d42e10e7`  
		Last Modified: Fri, 10 Feb 2023 22:10:29 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.6-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:06c08d096982b8e404306fb2fa2f057f9af55309f2973967ab556ce72e9f98a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3494506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018f9d828b5715da05f5e8f3582d7568acee95e5147ba185df9e36b7b8e123a1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:39 GMT
ADD file:d88c188553d983f16407f891790a4e553fda681fa265d89ec12a70ba2f41b0da in / 
# Fri, 10 Feb 2023 21:24:39 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:06:55 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:06:56 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:08:04 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:08:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:08:07 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Fri, 10 Feb 2023 22:08:07 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:08:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:08:09 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:84644bcd984e34c8b3bc44d8040b7017495e31100c1f4d726c92b40cf6cf7351`  
		Last Modified: Fri, 10 Feb 2023 21:25:51 GMT  
		Size: 2.8 MB (2835110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9e92ef986b6523d6b5a8397fab7dd8fb405847d418536f10531c66fd457df`  
		Last Modified: Fri, 10 Feb 2023 22:10:00 GMT  
		Size: 659.2 KB (659158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0db72468618e8e0a71538db2ee35d49189691731af9dcded1fbc9a072075975`  
		Last Modified: Fri, 10 Feb 2023 22:09:59 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.6-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:3cde172ad56a3b3f735eb1b082f706f35944a1d5c7cf3403055fb057743a8bab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3499780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222c9396c848897f8f50e97096c93897cb0b95cc28b6d0466be3f69d70d03d61`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:21:00 GMT
ADD file:99507b43b1818a9e49705772be1d12eb9519e137ba653d9d569700b6f6d36523 in / 
# Fri, 10 Feb 2023 21:21:01 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:16:55 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:16:56 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:18:35 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:18:35 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:18:36 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Fri, 10 Feb 2023 22:18:36 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:18:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:18:37 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:443774f2f57bdbe836e7f8ee0ccfb6fc2c2f7f258030154416ae5c1c4528e756`  
		Last Modified: Fri, 10 Feb 2023 21:22:15 GMT  
		Size: 2.8 MB (2816405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2ee184396036c4be678f8b7eac9bd5f565771797d8dfb194ec6a6994f483fe`  
		Last Modified: Fri, 10 Feb 2023 22:20:46 GMT  
		Size: 683.1 KB (683137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd27fa78fc2a93605b3f862cd9c4b0f7969e86c057703dc498ec968f6edc177b`  
		Last Modified: Fri, 10 Feb 2023 22:20:46 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.6-openssl` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:d812d7a64e5903610f5bb31211b4508b502e8e041c83abd065639e8006bfc18d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3243784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63397e8c1b35e624914f80f580737a04d4233a1d9a34b6d69c15649283695c8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:43 GMT
ADD file:3590370451e8df75d0fe22ac6cb669c667358fd514c69df4be770a687f378871 in / 
# Fri, 10 Feb 2023 21:41:43 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:43:38 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 05:43:38 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 05:44:36 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 05:44:36 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 05:44:36 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Sat, 11 Feb 2023 05:44:36 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 05:44:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 05:44:36 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:ce265ad7528283161562836d2f4c84efa75654b4e39eab9bd3c332c7d288afda`  
		Last Modified: Fri, 10 Feb 2023 21:42:40 GMT  
		Size: 2.6 MB (2614244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4487bf5b8ae6f37167136514042ef74d4284c4b28caf90968ac5731c759ed21d`  
		Last Modified: Sat, 11 Feb 2023 05:45:59 GMT  
		Size: 629.3 KB (629301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17972b98d1b3054053ccd3f0c33a247efc3bc177597faf05002f33386e8293e9`  
		Last Modified: Sat, 11 Feb 2023 05:45:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eclipse-mosquitto:1.6.15`

```console
$ docker pull eclipse-mosquitto@sha256:bba4c72b43df4333ec7cd800e8e7278c674cbf2adc907f3405f7076e297c8e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-mosquitto:1.6.15` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:98cdafca37391270aa5e16362fac52fb21e606be2d6cee65d16965418d6dabb6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5513791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b338ee795ed5ed29e780661f54f05bfc644bd5d637d4397d76a4fa6736e77d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:59 GMT
ADD file:a41bb436701fd0adf99a3157d19f172b3e54ea033f5c617009e2d1bdeac206d7 in / 
# Sat, 11 Feb 2023 04:46:59 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:44:59 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 07:44:59 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 07:45:24 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 07:45:25 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 07:45:25 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Sat, 11 Feb 2023 07:45:25 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 07:45:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 07:45:25 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:d261077062b2aebb9ca8dc61f2b00e7e2b4e44179d3cfbe526c4ee0c5e41b26f`  
		Last Modified: Sat, 11 Feb 2023 04:47:49 GMT  
		Size: 2.8 MB (2829633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f56c2911bae1aa250f342877a41f78a69467dae9b01c62d5a8799c6f333a4e`  
		Last Modified: Sat, 11 Feb 2023 07:47:07 GMT  
		Size: 2.7 MB (2683919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206b090db03726760c8e2b19fb53530465e2b5e58ea30cb6478526f9440098cc`  
		Last Modified: Sat, 11 Feb 2023 07:47:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.6.15` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:04dae7fd9ecde738e95c42ccfe1906ff26f46aa7bf5eb77672f91ad44db4b795
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a378677ab03401ef33b4c4193c99d1898c7bfae5f25637db66133ca3637b3e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:54 GMT
ADD file:767f6566ea2c075838c0a86ca644a37e446f309f68952f5f921970f046abd252 in / 
# Mon, 13 Mar 2023 16:12:54 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 16:41:53 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 13 Mar 2023 16:41:53 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 13 Mar 2023 16:42:20 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl &&     apk del build-deps &&     rm -rf /build
# Mon, 13 Mar 2023 16:42:20 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 13 Mar 2023 16:42:20 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Mon, 13 Mar 2023 16:42:20 GMT
EXPOSE 1883
# Mon, 13 Mar 2023 16:42:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 13 Mar 2023 16:42:21 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:7616dd32f4bf5fddffb2543afaac2355a5fc495348c01060cd67181e36343e96`  
		Last Modified: Fri, 10 Feb 2023 20:51:02 GMT  
		Size: 2.6 MB (2638152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721ffab73c5d57ae9c7ff5136eb178e1308e4349ae1cf62b9504076c25b9a020`  
		Last Modified: Mon, 13 Mar 2023 16:44:36 GMT  
		Size: 2.8 MB (2811609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a3fb247065a772fcb0e1918c3f30efcd19156d2729d67d43a2e456c5e9796b`  
		Last Modified: Mon, 13 Mar 2023 16:44:36 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.6.15` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:d45682996a512b5a7faa0a1b25421119b0480ff772859505d635fa903ebd548b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5361737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fab828837071573a96e62b067c3969f8a987e2c45c6b9fcc1f8c8fac1bfa23`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:19 GMT
ADD file:50a841463966858f1c3ca87143cf96145d1d52f7349ef516adfbf21cdd5684fe in / 
# Fri, 10 Feb 2023 21:24:19 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:08:27 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:08:27 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:08:49 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:08:49 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:08:49 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Fri, 10 Feb 2023 22:08:49 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:08:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:08:49 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:6f0e733d82e26042c603e231c39b56abbabdad66673a736ec71c69c65be95f41`  
		Last Modified: Fri, 10 Feb 2023 21:25:10 GMT  
		Size: 2.7 MB (2725026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d0a544b126f253e231f49f2449b3e90c6f53bae60d068f33ae67e5d8e011e2`  
		Last Modified: Fri, 10 Feb 2023 22:10:21 GMT  
		Size: 2.6 MB (2636472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847b297767b219f1e402cae285521ca609148ecd35db885afb1be3cc61a788dd`  
		Last Modified: Fri, 10 Feb 2023 22:10:20 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.6.15` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:c88077c15a29f2a2abc0ef5e2549ab9d7fe0da48f6c3670769df14dd773f4e7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5691916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1875a844d84d614811f4adcc238eaef75c03b7ac8fd5c247fb27b66a913ebc8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:39 GMT
ADD file:d88c188553d983f16407f891790a4e553fda681fa265d89ec12a70ba2f41b0da in / 
# Fri, 10 Feb 2023 21:24:39 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:06:55 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:06:56 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:07:25 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:07:26 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:07:28 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Fri, 10 Feb 2023 22:07:28 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:07:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:07:30 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:84644bcd984e34c8b3bc44d8040b7017495e31100c1f4d726c92b40cf6cf7351`  
		Last Modified: Fri, 10 Feb 2023 21:25:51 GMT  
		Size: 2.8 MB (2835110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a540208296e52bc68ac3012039efe40ab7fb4421bf1f2ebfc06b780d5c2960`  
		Last Modified: Fri, 10 Feb 2023 22:09:49 GMT  
		Size: 2.9 MB (2856567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a944dfae6d082118039136e4ec1916ff6dc652a8423fdb96646c97d49776c09`  
		Last Modified: Fri, 10 Feb 2023 22:09:48 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.6.15` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:b7b50586040f3a0d158eea12f94bdb992f126228fe099fc5ac9b708979452765
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782d3fe21ec87f311b4a24b93b9d2bfb96df15b5fa936eb6e8f336d98718f319`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:21:00 GMT
ADD file:99507b43b1818a9e49705772be1d12eb9519e137ba653d9d569700b6f6d36523 in / 
# Fri, 10 Feb 2023 21:21:01 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:16:55 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:16:56 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:17:48 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:17:49 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:17:49 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Fri, 10 Feb 2023 22:17:50 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:17:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:17:51 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:443774f2f57bdbe836e7f8ee0ccfb6fc2c2f7f258030154416ae5c1c4528e756`  
		Last Modified: Fri, 10 Feb 2023 21:22:15 GMT  
		Size: 2.8 MB (2816405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e750287a787c89330386cf3e719c731a3c78b9c7e5bb8eb1889c0e29718010`  
		Last Modified: Fri, 10 Feb 2023 22:20:36 GMT  
		Size: 2.8 MB (2794656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a3125202bee750214c598e4a41e017a1e2e5895bbd703aa86a66376d15bbaa`  
		Last Modified: Fri, 10 Feb 2023 22:20:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.6.15` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:3f286207641c5c9e862bb73fa9f840a84b27fd31227126ea5330b3b2935c232b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5341194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fa2a41e266098253ef7a9e41efd21412078eb1d8650ecb04306d58b2196ef6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:43 GMT
ADD file:3590370451e8df75d0fe22ac6cb669c667358fd514c69df4be770a687f378871 in / 
# Fri, 10 Feb 2023 21:41:43 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:43:38 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 05:43:38 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 05:44:04 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libressl &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 05:44:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 05:44:05 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Sat, 11 Feb 2023 05:44:05 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 05:44:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 05:44:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:ce265ad7528283161562836d2f4c84efa75654b4e39eab9bd3c332c7d288afda`  
		Last Modified: Fri, 10 Feb 2023 21:42:40 GMT  
		Size: 2.6 MB (2614244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc094062e65aeae7064da7c7d9a0bed8096aa1d339e8351ee887ba8c7a6a4599`  
		Last Modified: Sat, 11 Feb 2023 05:45:53 GMT  
		Size: 2.7 MB (2726711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abd18395b95c2f3f8538f859a13840028db467551c20bc3e61def7c259aead8`  
		Last Modified: Sat, 11 Feb 2023 05:45:53 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eclipse-mosquitto:1.6.15-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:6d51a71252793a188ae42e12182666813e581c8ad63c50de5cc3fbc7b180be72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-mosquitto:1.6.15-openssl` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:1ac7f25c9c9a58bf7db67841f953d9d33e98c7f89b93fd2825462095b33ded53
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3462341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe766e8a1a8cb072083275be56f282363c509144c776dba3e65f821bca67cb05`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:59 GMT
ADD file:a41bb436701fd0adf99a3157d19f172b3e54ea033f5c617009e2d1bdeac206d7 in / 
# Sat, 11 Feb 2023 04:46:59 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:44:59 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 07:44:59 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 07:45:54 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 07:45:54 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 07:45:54 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Sat, 11 Feb 2023 07:45:54 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 07:45:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 07:45:54 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:d261077062b2aebb9ca8dc61f2b00e7e2b4e44179d3cfbe526c4ee0c5e41b26f`  
		Last Modified: Sat, 11 Feb 2023 04:47:49 GMT  
		Size: 2.8 MB (2829633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c922d605245e7205d56068935a92ba0e394f9a30066aaa4539da7724b9ff35d1`  
		Last Modified: Sat, 11 Feb 2023 07:47:15 GMT  
		Size: 632.5 KB (632468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ddf14bb7e22b47e57414c8da70362d07eb82ed0259ee5061948ca419221b779`  
		Last Modified: Sat, 11 Feb 2023 07:47:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.6.15-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:9d137fde9c54c69e7b99fdca7bcd85f672e77e33a26ad089a902be96e5e5d420
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a62338d6d68ba26e8e4bf64e705cc4485ba35e7645a47e1d11c654d19d1d0e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:54 GMT
ADD file:767f6566ea2c075838c0a86ca644a37e446f309f68952f5f921970f046abd252 in / 
# Mon, 13 Mar 2023 16:12:54 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 16:41:53 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 13 Mar 2023 16:41:53 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 13 Mar 2023 16:42:54 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build
# Mon, 13 Mar 2023 16:42:54 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 13 Mar 2023 16:42:54 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Mon, 13 Mar 2023 16:42:54 GMT
EXPOSE 1883
# Mon, 13 Mar 2023 16:42:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 13 Mar 2023 16:42:54 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:7616dd32f4bf5fddffb2543afaac2355a5fc495348c01060cd67181e36343e96`  
		Last Modified: Fri, 10 Feb 2023 20:51:02 GMT  
		Size: 2.6 MB (2638152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72acd984f03c8327db04b5b14950c1a1ae0aaf1928e0dfb4bb4b7400bded24d4`  
		Last Modified: Mon, 13 Mar 2023 16:44:46 GMT  
		Size: 996.5 KB (996507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ba27f0521195a9dfb7e417711c2500754332f225e2edeea87c1288cf66593a`  
		Last Modified: Mon, 13 Mar 2023 16:44:46 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.6.15-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:c0fc66f7a9bbe7730276005029911867ef3cf66d68269a2db449298168554cab
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3354133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7c14cb6e5c4e1560588c4e14ba48b516fd28e67226f072e6561020f80b4d4a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:19 GMT
ADD file:50a841463966858f1c3ca87143cf96145d1d52f7349ef516adfbf21cdd5684fe in / 
# Fri, 10 Feb 2023 21:24:19 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:08:27 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:08:27 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:09:16 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:09:16 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:09:16 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Fri, 10 Feb 2023 22:09:16 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:09:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:09:17 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:6f0e733d82e26042c603e231c39b56abbabdad66673a736ec71c69c65be95f41`  
		Last Modified: Fri, 10 Feb 2023 21:25:10 GMT  
		Size: 2.7 MB (2725026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01001996eae7f51fd87e44f9d8bd3c872ab3c3aaa07c430c487f7149fdcf9e5a`  
		Last Modified: Fri, 10 Feb 2023 22:10:29 GMT  
		Size: 628.9 KB (628869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2225ea1b0166229f7d10f78ee8f11f3873f63beadffa8bcc070539d42e10e7`  
		Last Modified: Fri, 10 Feb 2023 22:10:29 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.6.15-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:06c08d096982b8e404306fb2fa2f057f9af55309f2973967ab556ce72e9f98a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3494506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018f9d828b5715da05f5e8f3582d7568acee95e5147ba185df9e36b7b8e123a1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:39 GMT
ADD file:d88c188553d983f16407f891790a4e553fda681fa265d89ec12a70ba2f41b0da in / 
# Fri, 10 Feb 2023 21:24:39 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:06:55 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:06:56 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:08:04 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:08:05 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:08:07 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Fri, 10 Feb 2023 22:08:07 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:08:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:08:09 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:84644bcd984e34c8b3bc44d8040b7017495e31100c1f4d726c92b40cf6cf7351`  
		Last Modified: Fri, 10 Feb 2023 21:25:51 GMT  
		Size: 2.8 MB (2835110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9e92ef986b6523d6b5a8397fab7dd8fb405847d418536f10531c66fd457df`  
		Last Modified: Fri, 10 Feb 2023 22:10:00 GMT  
		Size: 659.2 KB (659158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0db72468618e8e0a71538db2ee35d49189691731af9dcded1fbc9a072075975`  
		Last Modified: Fri, 10 Feb 2023 22:09:59 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.6.15-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:3cde172ad56a3b3f735eb1b082f706f35944a1d5c7cf3403055fb057743a8bab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3499780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222c9396c848897f8f50e97096c93897cb0b95cc28b6d0466be3f69d70d03d61`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:21:00 GMT
ADD file:99507b43b1818a9e49705772be1d12eb9519e137ba653d9d569700b6f6d36523 in / 
# Fri, 10 Feb 2023 21:21:01 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:16:55 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:16:56 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:18:35 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:18:35 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:18:36 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Fri, 10 Feb 2023 22:18:36 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:18:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:18:37 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:443774f2f57bdbe836e7f8ee0ccfb6fc2c2f7f258030154416ae5c1c4528e756`  
		Last Modified: Fri, 10 Feb 2023 21:22:15 GMT  
		Size: 2.8 MB (2816405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2ee184396036c4be678f8b7eac9bd5f565771797d8dfb194ec6a6994f483fe`  
		Last Modified: Fri, 10 Feb 2023 22:20:46 GMT  
		Size: 683.1 KB (683137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd27fa78fc2a93605b3f862cd9c4b0f7969e86c057703dc498ec968f6edc177b`  
		Last Modified: Fri, 10 Feb 2023 22:20:46 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:1.6.15-openssl` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:d812d7a64e5903610f5bb31211b4508b502e8e041c83abd065639e8006bfc18d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3243784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63397e8c1b35e624914f80f580737a04d4233a1d9a34b6d69c15649283695c8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:43 GMT
ADD file:3590370451e8df75d0fe22ac6cb669c667358fd514c69df4be770a687f378871 in / 
# Fri, 10 Feb 2023 21:41:43 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:43:38 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 05:43:38 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 05:44:36 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 05:44:36 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 05:44:36 GMT
COPY file:232de3a06de79606b9743327f59defda56818d50c1027dd2f0f1c5fb7917db2e in / 
# Sat, 11 Feb 2023 05:44:36 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 05:44:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 05:44:36 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:ce265ad7528283161562836d2f4c84efa75654b4e39eab9bd3c332c7d288afda`  
		Last Modified: Fri, 10 Feb 2023 21:42:40 GMT  
		Size: 2.6 MB (2614244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4487bf5b8ae6f37167136514042ef74d4284c4b28caf90968ac5731c759ed21d`  
		Last Modified: Sat, 11 Feb 2023 05:45:59 GMT  
		Size: 629.3 KB (629301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17972b98d1b3054053ccd3f0c33a247efc3bc177597faf05002f33386e8293e9`  
		Last Modified: Sat, 11 Feb 2023 05:45:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eclipse-mosquitto:2`

```console
$ docker pull eclipse-mosquitto@sha256:c043073ba24de67a1728a4e0755ebd8ef68ae9dd60d0d9886b15c955df5558b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-mosquitto:2` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:49d65691fd5d80a4d03a3dc3677550f7e3520276e055b1f1be3277087a2805fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5636957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57b79223a14bb804aee595864b3247c6c6ac8af270386f047b03fc18af100aa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:43:51 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 07:43:51 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 07:44:19 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 07:44:20 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 07:44:20 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Sat, 11 Feb 2023 07:44:20 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 07:44:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 07:44:20 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ca8a06e1f901d18efa8d3fe2ca4757aaf27008eb7609b39831cb52a4e2ec26`  
		Last Modified: Sat, 11 Feb 2023 07:46:42 GMT  
		Size: 2.8 MB (2828827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02910b6532bf997ae559423cae25e3c0baec9e36cc34b5da51f434fc2fb7fd3`  
		Last Modified: Sat, 11 Feb 2023 07:46:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:32480f5de1ca2dafaf2f71abed8a99939a552a49b6699e98491945028d8d04ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5164699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb35cdc2111999b40fabd0c01fac1bb26b61d1fcad23ea88837c8f3d03fbb3ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:48 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Mon, 13 Mar 2023 16:12:48 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 16:40:43 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 13 Mar 2023 16:40:44 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 13 Mar 2023 16:41:14 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Mon, 13 Mar 2023 16:41:14 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 13 Mar 2023 16:41:14 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Mon, 13 Mar 2023 16:41:14 GMT
EXPOSE 1883
# Mon, 13 Mar 2023 16:41:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 13 Mar 2023 16:41:14 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2688bb5fb53d62559f686ff80f564656790c072761df2b0cd0632d5ca1a74821`  
		Last Modified: Mon, 13 Mar 2023 16:44:04 GMT  
		Size: 2.5 MB (2547553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb02dd1e319a73a1cf2b520e3690f38fe825f6c9532f1344d03fa95ca208311`  
		Last Modified: Mon, 13 Mar 2023 16:44:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:ddce1f6d49b11163493f62b90fc40e71bd6ed639bc6f3fff98fa3cee6f498dad
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5491314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8daf179f68972469d14a519efcf3c52db5e61e5485a5ac7dcc23a468f9d608`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:07:31 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:07:31 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:07:54 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:07:54 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:07:54 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:07:54 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:07:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:07:54 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77a461c4d88d75f9a69a8e4033572e699ab571d80dccf891b979ae576579838`  
		Last Modified: Fri, 10 Feb 2023 22:09:56 GMT  
		Size: 2.8 MB (2781444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b32410a4d525fd2d51a6cbc02e9691094a6a0287e535ec48f7571a78c9d14a6`  
		Last Modified: Fri, 10 Feb 2023 22:09:55 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:9bc6355d2a26b1eb61f69a1f5a4a677768fe2e53d47c8e63a0c06b2424c7ecc6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5834155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd168e362dd65b4e7cb0d3d385b5a4052e6e64fbcfd880dbdcd99cd26ce3fd1c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:29 GMT
ADD file:59ac1f8f33f9b9727892b7e45b33f54ef3c20d9d876c49d6a4c057641821d68f in / 
# Fri, 10 Feb 2023 21:24:29 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:05:28 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:05:28 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:06:02 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:06:03 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:06:05 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:06:05 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:06:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:06:07 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:0987f51cd58a7d03bc7d6ff0a3a0a843c1a3fefcd41e3c8adc3999ddde7441e8`  
		Last Modified: Fri, 10 Feb 2023 21:25:30 GMT  
		Size: 2.8 MB (2810653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb82171ce97e635508647afd36cb51535e73c4ba55505f031c2a4150e106dfa`  
		Last Modified: Fri, 10 Feb 2023 22:09:19 GMT  
		Size: 3.0 MB (3023134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd80c78bc5b1e927f589fba7087fb88c88b96af1408f3ed133ebef74026998e`  
		Last Modified: Fri, 10 Feb 2023 22:09:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:c0254398acb53c465928f60c50188ce972e6254d27ca6bb55c76dbe8aa84f729
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5783777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bd2e415f3f60f13e6ab84f0499d7c249493ce7b7a14885115aa8853794690b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:14:54 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:14:55 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:15:42 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:15:43 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:15:43 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:15:44 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:15:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:15:45 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7c889150f13b6a972a46fec0e8c57d16d703566231e5862298780a512b35c4`  
		Last Modified: Fri, 10 Feb 2023 22:20:01 GMT  
		Size: 3.0 MB (2978781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c164929fbd4148d64d33f236254eca5b4fea8579e1c6c70deebd7e3af51afdc`  
		Last Modified: Fri, 10 Feb 2023 22:20:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:fd1b5435aa3551071d77e1e6eac1369abc49d336bf5ca61a75e8726959584364
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5477196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b716e3aa3e34f067f9fdbf772643f6dfe92b3b2946e6704de5b4c996517851`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:42:31 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 05:42:31 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 05:42:56 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 05:42:56 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 05:42:57 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Sat, 11 Feb 2023 05:42:57 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 05:42:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 05:42:57 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19510dbb190fdaa6cb6c7bacee2f3c507d025fb879639a76a12e3ea91b7464c`  
		Last Modified: Sat, 11 Feb 2023 05:45:34 GMT  
		Size: 2.9 MB (2883247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c1971b8cbe81a094691022fe2d71072d92a9df1080d2c75cd9e5389332eb0f`  
		Last Modified: Sat, 11 Feb 2023 05:45:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eclipse-mosquitto:2-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:f568dfb10fe2753c7f304d0f2a923697bb3128147717af98aa4a98b3cf7a027f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-mosquitto:2-openssl` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:0b663899d60c0d4d8a237b3ef733bef3d9fa0941bb1cd9b8686c058385fff4e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3540405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cca5da912eda578d9bb66977ccb08bf096a984df263d824183487de5ccec87`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:43:51 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 07:43:51 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 07:44:56 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 07:44:56 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 07:44:56 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Sat, 11 Feb 2023 07:44:56 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 07:44:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 07:44:56 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9518cf6acf001caa503f17af2421d28fc215ae21dfb49331a381b0eedcc29a`  
		Last Modified: Sat, 11 Feb 2023 07:46:55 GMT  
		Size: 732.3 KB (732275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636eec3ce25ff2474f7302d9751b4d437a600c359a0f56aea878b1973e6fbae7`  
		Last Modified: Sat, 11 Feb 2023 07:46:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:290b601f1c6f77fb628eb4b8f16a7eec901e651cba4e6a2d6c451f03e04f0f11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3322395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd67b8d3caa67ad94b91684c9e7c6db8bfe0413b54aefd7ae1b9cffc776b1c1c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:48 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Mon, 13 Mar 2023 16:12:48 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 16:40:43 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 13 Mar 2023 16:40:44 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 13 Mar 2023 16:41:46 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Mon, 13 Mar 2023 16:41:46 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 13 Mar 2023 16:41:46 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Mon, 13 Mar 2023 16:41:46 GMT
EXPOSE 1883
# Mon, 13 Mar 2023 16:41:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 13 Mar 2023 16:41:47 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e43ba4189456762d09d63c8cbb8098f4b836812fd484442354da99eff8c1107`  
		Last Modified: Mon, 13 Mar 2023 16:44:20 GMT  
		Size: 705.2 KB (705249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c5edd1a21ac19b677053e9a7bb2c9ce82efae5b004b606070371444d7fd5d5`  
		Last Modified: Mon, 13 Mar 2023 16:44:20 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:086fb1a2ece8d09a0671ce773f62a7c5def27c135f62ed27f5490f3348c7404b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3438408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fdb0f92572af0c7c221e0e7efa6049896ea1aed10094267873b10b2efa98d5c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:07:31 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:07:31 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:08:23 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:08:23 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:08:23 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:08:23 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:08:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:08:23 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f67f324a02d8067a8a845f37492ed48cc36046f8a90718d410444915c4335c`  
		Last Modified: Fri, 10 Feb 2023 22:10:08 GMT  
		Size: 728.5 KB (728538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200923fc339d37fa57f5874d7d6459f32f151b1d246c062fcf30914ae18669c4`  
		Last Modified: Fri, 10 Feb 2023 22:10:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:b01177297a8b35263996f8683c58770ff10f4bb9ced7348d605f388fa294921d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3581864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8928e629b4eea91158d8acec61972228566dedd61fbcf796311f752d15ce0be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:29 GMT
ADD file:59ac1f8f33f9b9727892b7e45b33f54ef3c20d9d876c49d6a4c057641821d68f in / 
# Fri, 10 Feb 2023 21:24:29 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:05:28 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:05:28 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:06:41 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:06:42 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:06:44 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:06:44 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:06:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:06:46 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:0987f51cd58a7d03bc7d6ff0a3a0a843c1a3fefcd41e3c8adc3999ddde7441e8`  
		Last Modified: Fri, 10 Feb 2023 21:25:30 GMT  
		Size: 2.8 MB (2810653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0239c398f7dca62942b948c87f89d0d6db3b896c29b6c6965408cf2c4b30891f`  
		Last Modified: Fri, 10 Feb 2023 22:09:33 GMT  
		Size: 770.8 KB (770843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b7c0f6bf5e8120976a6a05b4661b117816ec2a79cc7cf5f9fec2d66835a528`  
		Last Modified: Fri, 10 Feb 2023 22:09:33 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:82bffee113fc9888acd0f61fc3ac20cee6e4dff0d7b3c6f0cbac42171e6c3de8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3612946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f3629c1e91e31e314e61bc2649a5af669b7c5f16dea85b969d8719773d58fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:14:54 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:14:55 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:16:40 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:16:40 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:16:41 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:16:41 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:16:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:16:42 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3db7e03886dd824bd80f7adde75b0579208c52e94da12595a2ae65da0ecfd3`  
		Last Modified: Fri, 10 Feb 2023 22:20:19 GMT  
		Size: 808.0 KB (807950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c066243dadde9843e1a3d4eabca0bc3378e9ccbc9428326bb3696f125627da`  
		Last Modified: Fri, 10 Feb 2023 22:20:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2-openssl` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:473b1cacea2f5e76456da7a799493daa788718882a123e967c7dcd7c5a9a5a7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3326338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e72578573bbf50f48321bff45c77f00c9611161450fee0d9c275be41d1721d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:42:31 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 05:42:31 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 05:43:31 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 05:43:31 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 05:43:31 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Sat, 11 Feb 2023 05:43:31 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 05:43:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 05:43:32 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd2deda8b5a7b241e0b35f7a38fe475ab0d704d3f68d5ada981777c3b249c96`  
		Last Modified: Sat, 11 Feb 2023 05:45:43 GMT  
		Size: 732.4 KB (732389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5693fa66abc0c21b245889af4785c5747a307add6a7f8b959e0341bfec739965`  
		Last Modified: Sat, 11 Feb 2023 05:45:43 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eclipse-mosquitto:2.0`

```console
$ docker pull eclipse-mosquitto@sha256:c043073ba24de67a1728a4e0755ebd8ef68ae9dd60d0d9886b15c955df5558b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-mosquitto:2.0` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:49d65691fd5d80a4d03a3dc3677550f7e3520276e055b1f1be3277087a2805fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5636957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57b79223a14bb804aee595864b3247c6c6ac8af270386f047b03fc18af100aa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:43:51 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 07:43:51 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 07:44:19 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 07:44:20 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 07:44:20 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Sat, 11 Feb 2023 07:44:20 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 07:44:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 07:44:20 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ca8a06e1f901d18efa8d3fe2ca4757aaf27008eb7609b39831cb52a4e2ec26`  
		Last Modified: Sat, 11 Feb 2023 07:46:42 GMT  
		Size: 2.8 MB (2828827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02910b6532bf997ae559423cae25e3c0baec9e36cc34b5da51f434fc2fb7fd3`  
		Last Modified: Sat, 11 Feb 2023 07:46:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2.0` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:32480f5de1ca2dafaf2f71abed8a99939a552a49b6699e98491945028d8d04ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5164699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb35cdc2111999b40fabd0c01fac1bb26b61d1fcad23ea88837c8f3d03fbb3ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:48 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Mon, 13 Mar 2023 16:12:48 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 16:40:43 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 13 Mar 2023 16:40:44 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 13 Mar 2023 16:41:14 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Mon, 13 Mar 2023 16:41:14 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 13 Mar 2023 16:41:14 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Mon, 13 Mar 2023 16:41:14 GMT
EXPOSE 1883
# Mon, 13 Mar 2023 16:41:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 13 Mar 2023 16:41:14 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2688bb5fb53d62559f686ff80f564656790c072761df2b0cd0632d5ca1a74821`  
		Last Modified: Mon, 13 Mar 2023 16:44:04 GMT  
		Size: 2.5 MB (2547553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb02dd1e319a73a1cf2b520e3690f38fe825f6c9532f1344d03fa95ca208311`  
		Last Modified: Mon, 13 Mar 2023 16:44:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2.0` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:ddce1f6d49b11163493f62b90fc40e71bd6ed639bc6f3fff98fa3cee6f498dad
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5491314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8daf179f68972469d14a519efcf3c52db5e61e5485a5ac7dcc23a468f9d608`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:07:31 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:07:31 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:07:54 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:07:54 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:07:54 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:07:54 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:07:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:07:54 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77a461c4d88d75f9a69a8e4033572e699ab571d80dccf891b979ae576579838`  
		Last Modified: Fri, 10 Feb 2023 22:09:56 GMT  
		Size: 2.8 MB (2781444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b32410a4d525fd2d51a6cbc02e9691094a6a0287e535ec48f7571a78c9d14a6`  
		Last Modified: Fri, 10 Feb 2023 22:09:55 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2.0` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:9bc6355d2a26b1eb61f69a1f5a4a677768fe2e53d47c8e63a0c06b2424c7ecc6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5834155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd168e362dd65b4e7cb0d3d385b5a4052e6e64fbcfd880dbdcd99cd26ce3fd1c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:29 GMT
ADD file:59ac1f8f33f9b9727892b7e45b33f54ef3c20d9d876c49d6a4c057641821d68f in / 
# Fri, 10 Feb 2023 21:24:29 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:05:28 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:05:28 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:06:02 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:06:03 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:06:05 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:06:05 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:06:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:06:07 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:0987f51cd58a7d03bc7d6ff0a3a0a843c1a3fefcd41e3c8adc3999ddde7441e8`  
		Last Modified: Fri, 10 Feb 2023 21:25:30 GMT  
		Size: 2.8 MB (2810653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb82171ce97e635508647afd36cb51535e73c4ba55505f031c2a4150e106dfa`  
		Last Modified: Fri, 10 Feb 2023 22:09:19 GMT  
		Size: 3.0 MB (3023134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd80c78bc5b1e927f589fba7087fb88c88b96af1408f3ed133ebef74026998e`  
		Last Modified: Fri, 10 Feb 2023 22:09:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2.0` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:c0254398acb53c465928f60c50188ce972e6254d27ca6bb55c76dbe8aa84f729
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5783777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bd2e415f3f60f13e6ab84f0499d7c249493ce7b7a14885115aa8853794690b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:14:54 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:14:55 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:15:42 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:15:43 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:15:43 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:15:44 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:15:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:15:45 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7c889150f13b6a972a46fec0e8c57d16d703566231e5862298780a512b35c4`  
		Last Modified: Fri, 10 Feb 2023 22:20:01 GMT  
		Size: 3.0 MB (2978781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c164929fbd4148d64d33f236254eca5b4fea8579e1c6c70deebd7e3af51afdc`  
		Last Modified: Fri, 10 Feb 2023 22:20:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2.0` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:fd1b5435aa3551071d77e1e6eac1369abc49d336bf5ca61a75e8726959584364
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5477196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b716e3aa3e34f067f9fdbf772643f6dfe92b3b2946e6704de5b4c996517851`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:42:31 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 05:42:31 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 05:42:56 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 05:42:56 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 05:42:57 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Sat, 11 Feb 2023 05:42:57 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 05:42:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 05:42:57 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19510dbb190fdaa6cb6c7bacee2f3c507d025fb879639a76a12e3ea91b7464c`  
		Last Modified: Sat, 11 Feb 2023 05:45:34 GMT  
		Size: 2.9 MB (2883247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c1971b8cbe81a094691022fe2d71072d92a9df1080d2c75cd9e5389332eb0f`  
		Last Modified: Sat, 11 Feb 2023 05:45:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eclipse-mosquitto:2.0-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:f568dfb10fe2753c7f304d0f2a923697bb3128147717af98aa4a98b3cf7a027f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-mosquitto:2.0-openssl` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:0b663899d60c0d4d8a237b3ef733bef3d9fa0941bb1cd9b8686c058385fff4e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3540405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cca5da912eda578d9bb66977ccb08bf096a984df263d824183487de5ccec87`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:43:51 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 07:43:51 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 07:44:56 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 07:44:56 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 07:44:56 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Sat, 11 Feb 2023 07:44:56 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 07:44:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 07:44:56 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9518cf6acf001caa503f17af2421d28fc215ae21dfb49331a381b0eedcc29a`  
		Last Modified: Sat, 11 Feb 2023 07:46:55 GMT  
		Size: 732.3 KB (732275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636eec3ce25ff2474f7302d9751b4d437a600c359a0f56aea878b1973e6fbae7`  
		Last Modified: Sat, 11 Feb 2023 07:46:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2.0-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:290b601f1c6f77fb628eb4b8f16a7eec901e651cba4e6a2d6c451f03e04f0f11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3322395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd67b8d3caa67ad94b91684c9e7c6db8bfe0413b54aefd7ae1b9cffc776b1c1c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:48 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Mon, 13 Mar 2023 16:12:48 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 16:40:43 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 13 Mar 2023 16:40:44 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 13 Mar 2023 16:41:46 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Mon, 13 Mar 2023 16:41:46 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 13 Mar 2023 16:41:46 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Mon, 13 Mar 2023 16:41:46 GMT
EXPOSE 1883
# Mon, 13 Mar 2023 16:41:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 13 Mar 2023 16:41:47 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e43ba4189456762d09d63c8cbb8098f4b836812fd484442354da99eff8c1107`  
		Last Modified: Mon, 13 Mar 2023 16:44:20 GMT  
		Size: 705.2 KB (705249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c5edd1a21ac19b677053e9a7bb2c9ce82efae5b004b606070371444d7fd5d5`  
		Last Modified: Mon, 13 Mar 2023 16:44:20 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2.0-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:086fb1a2ece8d09a0671ce773f62a7c5def27c135f62ed27f5490f3348c7404b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3438408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fdb0f92572af0c7c221e0e7efa6049896ea1aed10094267873b10b2efa98d5c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:07:31 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:07:31 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:08:23 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:08:23 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:08:23 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:08:23 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:08:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:08:23 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f67f324a02d8067a8a845f37492ed48cc36046f8a90718d410444915c4335c`  
		Last Modified: Fri, 10 Feb 2023 22:10:08 GMT  
		Size: 728.5 KB (728538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200923fc339d37fa57f5874d7d6459f32f151b1d246c062fcf30914ae18669c4`  
		Last Modified: Fri, 10 Feb 2023 22:10:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2.0-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:b01177297a8b35263996f8683c58770ff10f4bb9ced7348d605f388fa294921d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3581864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8928e629b4eea91158d8acec61972228566dedd61fbcf796311f752d15ce0be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:29 GMT
ADD file:59ac1f8f33f9b9727892b7e45b33f54ef3c20d9d876c49d6a4c057641821d68f in / 
# Fri, 10 Feb 2023 21:24:29 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:05:28 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:05:28 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:06:41 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:06:42 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:06:44 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:06:44 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:06:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:06:46 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:0987f51cd58a7d03bc7d6ff0a3a0a843c1a3fefcd41e3c8adc3999ddde7441e8`  
		Last Modified: Fri, 10 Feb 2023 21:25:30 GMT  
		Size: 2.8 MB (2810653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0239c398f7dca62942b948c87f89d0d6db3b896c29b6c6965408cf2c4b30891f`  
		Last Modified: Fri, 10 Feb 2023 22:09:33 GMT  
		Size: 770.8 KB (770843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b7c0f6bf5e8120976a6a05b4661b117816ec2a79cc7cf5f9fec2d66835a528`  
		Last Modified: Fri, 10 Feb 2023 22:09:33 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2.0-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:82bffee113fc9888acd0f61fc3ac20cee6e4dff0d7b3c6f0cbac42171e6c3de8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3612946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f3629c1e91e31e314e61bc2649a5af669b7c5f16dea85b969d8719773d58fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:14:54 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:14:55 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:16:40 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:16:40 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:16:41 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:16:41 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:16:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:16:42 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3db7e03886dd824bd80f7adde75b0579208c52e94da12595a2ae65da0ecfd3`  
		Last Modified: Fri, 10 Feb 2023 22:20:19 GMT  
		Size: 808.0 KB (807950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c066243dadde9843e1a3d4eabca0bc3378e9ccbc9428326bb3696f125627da`  
		Last Modified: Fri, 10 Feb 2023 22:20:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2.0-openssl` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:473b1cacea2f5e76456da7a799493daa788718882a123e967c7dcd7c5a9a5a7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3326338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e72578573bbf50f48321bff45c77f00c9611161450fee0d9c275be41d1721d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:42:31 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 05:42:31 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 05:43:31 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 05:43:31 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 05:43:31 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Sat, 11 Feb 2023 05:43:31 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 05:43:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 05:43:32 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd2deda8b5a7b241e0b35f7a38fe475ab0d704d3f68d5ada981777c3b249c96`  
		Last Modified: Sat, 11 Feb 2023 05:45:43 GMT  
		Size: 732.4 KB (732389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5693fa66abc0c21b245889af4785c5747a307add6a7f8b959e0341bfec739965`  
		Last Modified: Sat, 11 Feb 2023 05:45:43 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eclipse-mosquitto:2.0.15`

```console
$ docker pull eclipse-mosquitto@sha256:c043073ba24de67a1728a4e0755ebd8ef68ae9dd60d0d9886b15c955df5558b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-mosquitto:2.0.15` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:49d65691fd5d80a4d03a3dc3677550f7e3520276e055b1f1be3277087a2805fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5636957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57b79223a14bb804aee595864b3247c6c6ac8af270386f047b03fc18af100aa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:43:51 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 07:43:51 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 07:44:19 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 07:44:20 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 07:44:20 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Sat, 11 Feb 2023 07:44:20 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 07:44:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 07:44:20 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ca8a06e1f901d18efa8d3fe2ca4757aaf27008eb7609b39831cb52a4e2ec26`  
		Last Modified: Sat, 11 Feb 2023 07:46:42 GMT  
		Size: 2.8 MB (2828827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02910b6532bf997ae559423cae25e3c0baec9e36cc34b5da51f434fc2fb7fd3`  
		Last Modified: Sat, 11 Feb 2023 07:46:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2.0.15` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:32480f5de1ca2dafaf2f71abed8a99939a552a49b6699e98491945028d8d04ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5164699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb35cdc2111999b40fabd0c01fac1bb26b61d1fcad23ea88837c8f3d03fbb3ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:48 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Mon, 13 Mar 2023 16:12:48 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 16:40:43 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 13 Mar 2023 16:40:44 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 13 Mar 2023 16:41:14 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Mon, 13 Mar 2023 16:41:14 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 13 Mar 2023 16:41:14 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Mon, 13 Mar 2023 16:41:14 GMT
EXPOSE 1883
# Mon, 13 Mar 2023 16:41:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 13 Mar 2023 16:41:14 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2688bb5fb53d62559f686ff80f564656790c072761df2b0cd0632d5ca1a74821`  
		Last Modified: Mon, 13 Mar 2023 16:44:04 GMT  
		Size: 2.5 MB (2547553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb02dd1e319a73a1cf2b520e3690f38fe825f6c9532f1344d03fa95ca208311`  
		Last Modified: Mon, 13 Mar 2023 16:44:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2.0.15` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:ddce1f6d49b11163493f62b90fc40e71bd6ed639bc6f3fff98fa3cee6f498dad
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5491314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8daf179f68972469d14a519efcf3c52db5e61e5485a5ac7dcc23a468f9d608`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:07:31 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:07:31 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:07:54 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:07:54 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:07:54 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:07:54 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:07:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:07:54 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77a461c4d88d75f9a69a8e4033572e699ab571d80dccf891b979ae576579838`  
		Last Modified: Fri, 10 Feb 2023 22:09:56 GMT  
		Size: 2.8 MB (2781444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b32410a4d525fd2d51a6cbc02e9691094a6a0287e535ec48f7571a78c9d14a6`  
		Last Modified: Fri, 10 Feb 2023 22:09:55 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2.0.15` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:9bc6355d2a26b1eb61f69a1f5a4a677768fe2e53d47c8e63a0c06b2424c7ecc6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5834155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd168e362dd65b4e7cb0d3d385b5a4052e6e64fbcfd880dbdcd99cd26ce3fd1c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:29 GMT
ADD file:59ac1f8f33f9b9727892b7e45b33f54ef3c20d9d876c49d6a4c057641821d68f in / 
# Fri, 10 Feb 2023 21:24:29 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:05:28 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:05:28 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:06:02 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:06:03 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:06:05 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:06:05 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:06:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:06:07 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:0987f51cd58a7d03bc7d6ff0a3a0a843c1a3fefcd41e3c8adc3999ddde7441e8`  
		Last Modified: Fri, 10 Feb 2023 21:25:30 GMT  
		Size: 2.8 MB (2810653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb82171ce97e635508647afd36cb51535e73c4ba55505f031c2a4150e106dfa`  
		Last Modified: Fri, 10 Feb 2023 22:09:19 GMT  
		Size: 3.0 MB (3023134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd80c78bc5b1e927f589fba7087fb88c88b96af1408f3ed133ebef74026998e`  
		Last Modified: Fri, 10 Feb 2023 22:09:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2.0.15` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:c0254398acb53c465928f60c50188ce972e6254d27ca6bb55c76dbe8aa84f729
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5783777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bd2e415f3f60f13e6ab84f0499d7c249493ce7b7a14885115aa8853794690b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:14:54 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:14:55 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:15:42 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:15:43 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:15:43 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:15:44 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:15:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:15:45 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7c889150f13b6a972a46fec0e8c57d16d703566231e5862298780a512b35c4`  
		Last Modified: Fri, 10 Feb 2023 22:20:01 GMT  
		Size: 3.0 MB (2978781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c164929fbd4148d64d33f236254eca5b4fea8579e1c6c70deebd7e3af51afdc`  
		Last Modified: Fri, 10 Feb 2023 22:20:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2.0.15` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:fd1b5435aa3551071d77e1e6eac1369abc49d336bf5ca61a75e8726959584364
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5477196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b716e3aa3e34f067f9fdbf772643f6dfe92b3b2946e6704de5b4c996517851`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:42:31 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 05:42:31 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 05:42:56 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 05:42:56 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 05:42:57 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Sat, 11 Feb 2023 05:42:57 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 05:42:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 05:42:57 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19510dbb190fdaa6cb6c7bacee2f3c507d025fb879639a76a12e3ea91b7464c`  
		Last Modified: Sat, 11 Feb 2023 05:45:34 GMT  
		Size: 2.9 MB (2883247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c1971b8cbe81a094691022fe2d71072d92a9df1080d2c75cd9e5389332eb0f`  
		Last Modified: Sat, 11 Feb 2023 05:45:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eclipse-mosquitto:2.0.15-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:f568dfb10fe2753c7f304d0f2a923697bb3128147717af98aa4a98b3cf7a027f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-mosquitto:2.0.15-openssl` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:0b663899d60c0d4d8a237b3ef733bef3d9fa0941bb1cd9b8686c058385fff4e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3540405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cca5da912eda578d9bb66977ccb08bf096a984df263d824183487de5ccec87`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:43:51 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 07:43:51 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 07:44:56 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 07:44:56 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 07:44:56 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Sat, 11 Feb 2023 07:44:56 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 07:44:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 07:44:56 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9518cf6acf001caa503f17af2421d28fc215ae21dfb49331a381b0eedcc29a`  
		Last Modified: Sat, 11 Feb 2023 07:46:55 GMT  
		Size: 732.3 KB (732275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636eec3ce25ff2474f7302d9751b4d437a600c359a0f56aea878b1973e6fbae7`  
		Last Modified: Sat, 11 Feb 2023 07:46:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2.0.15-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:290b601f1c6f77fb628eb4b8f16a7eec901e651cba4e6a2d6c451f03e04f0f11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3322395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd67b8d3caa67ad94b91684c9e7c6db8bfe0413b54aefd7ae1b9cffc776b1c1c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:48 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Mon, 13 Mar 2023 16:12:48 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 16:40:43 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 13 Mar 2023 16:40:44 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 13 Mar 2023 16:41:46 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Mon, 13 Mar 2023 16:41:46 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 13 Mar 2023 16:41:46 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Mon, 13 Mar 2023 16:41:46 GMT
EXPOSE 1883
# Mon, 13 Mar 2023 16:41:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 13 Mar 2023 16:41:47 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e43ba4189456762d09d63c8cbb8098f4b836812fd484442354da99eff8c1107`  
		Last Modified: Mon, 13 Mar 2023 16:44:20 GMT  
		Size: 705.2 KB (705249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c5edd1a21ac19b677053e9a7bb2c9ce82efae5b004b606070371444d7fd5d5`  
		Last Modified: Mon, 13 Mar 2023 16:44:20 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2.0.15-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:086fb1a2ece8d09a0671ce773f62a7c5def27c135f62ed27f5490f3348c7404b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3438408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fdb0f92572af0c7c221e0e7efa6049896ea1aed10094267873b10b2efa98d5c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:07:31 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:07:31 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:08:23 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:08:23 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:08:23 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:08:23 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:08:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:08:23 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f67f324a02d8067a8a845f37492ed48cc36046f8a90718d410444915c4335c`  
		Last Modified: Fri, 10 Feb 2023 22:10:08 GMT  
		Size: 728.5 KB (728538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200923fc339d37fa57f5874d7d6459f32f151b1d246c062fcf30914ae18669c4`  
		Last Modified: Fri, 10 Feb 2023 22:10:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2.0.15-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:b01177297a8b35263996f8683c58770ff10f4bb9ced7348d605f388fa294921d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3581864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8928e629b4eea91158d8acec61972228566dedd61fbcf796311f752d15ce0be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:29 GMT
ADD file:59ac1f8f33f9b9727892b7e45b33f54ef3c20d9d876c49d6a4c057641821d68f in / 
# Fri, 10 Feb 2023 21:24:29 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:05:28 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:05:28 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:06:41 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:06:42 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:06:44 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:06:44 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:06:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:06:46 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:0987f51cd58a7d03bc7d6ff0a3a0a843c1a3fefcd41e3c8adc3999ddde7441e8`  
		Last Modified: Fri, 10 Feb 2023 21:25:30 GMT  
		Size: 2.8 MB (2810653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0239c398f7dca62942b948c87f89d0d6db3b896c29b6c6965408cf2c4b30891f`  
		Last Modified: Fri, 10 Feb 2023 22:09:33 GMT  
		Size: 770.8 KB (770843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b7c0f6bf5e8120976a6a05b4661b117816ec2a79cc7cf5f9fec2d66835a528`  
		Last Modified: Fri, 10 Feb 2023 22:09:33 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2.0.15-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:82bffee113fc9888acd0f61fc3ac20cee6e4dff0d7b3c6f0cbac42171e6c3de8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3612946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f3629c1e91e31e314e61bc2649a5af669b7c5f16dea85b969d8719773d58fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:14:54 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:14:55 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:16:40 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:16:40 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:16:41 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:16:41 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:16:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:16:42 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3db7e03886dd824bd80f7adde75b0579208c52e94da12595a2ae65da0ecfd3`  
		Last Modified: Fri, 10 Feb 2023 22:20:19 GMT  
		Size: 808.0 KB (807950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c066243dadde9843e1a3d4eabca0bc3378e9ccbc9428326bb3696f125627da`  
		Last Modified: Fri, 10 Feb 2023 22:20:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:2.0.15-openssl` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:473b1cacea2f5e76456da7a799493daa788718882a123e967c7dcd7c5a9a5a7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3326338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e72578573bbf50f48321bff45c77f00c9611161450fee0d9c275be41d1721d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:42:31 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 05:42:31 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 05:43:31 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 05:43:31 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 05:43:31 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Sat, 11 Feb 2023 05:43:31 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 05:43:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 05:43:32 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd2deda8b5a7b241e0b35f7a38fe475ab0d704d3f68d5ada981777c3b249c96`  
		Last Modified: Sat, 11 Feb 2023 05:45:43 GMT  
		Size: 732.4 KB (732389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5693fa66abc0c21b245889af4785c5747a307add6a7f8b959e0341bfec739965`  
		Last Modified: Sat, 11 Feb 2023 05:45:43 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eclipse-mosquitto:latest`

```console
$ docker pull eclipse-mosquitto@sha256:c043073ba24de67a1728a4e0755ebd8ef68ae9dd60d0d9886b15c955df5558b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-mosquitto:latest` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:49d65691fd5d80a4d03a3dc3677550f7e3520276e055b1f1be3277087a2805fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5636957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57b79223a14bb804aee595864b3247c6c6ac8af270386f047b03fc18af100aa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:43:51 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 07:43:51 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 07:44:19 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 07:44:20 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 07:44:20 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Sat, 11 Feb 2023 07:44:20 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 07:44:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 07:44:20 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ca8a06e1f901d18efa8d3fe2ca4757aaf27008eb7609b39831cb52a4e2ec26`  
		Last Modified: Sat, 11 Feb 2023 07:46:42 GMT  
		Size: 2.8 MB (2828827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02910b6532bf997ae559423cae25e3c0baec9e36cc34b5da51f434fc2fb7fd3`  
		Last Modified: Sat, 11 Feb 2023 07:46:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:latest` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:32480f5de1ca2dafaf2f71abed8a99939a552a49b6699e98491945028d8d04ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5164699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb35cdc2111999b40fabd0c01fac1bb26b61d1fcad23ea88837c8f3d03fbb3ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:48 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Mon, 13 Mar 2023 16:12:48 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 16:40:43 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 13 Mar 2023 16:40:44 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 13 Mar 2023 16:41:14 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Mon, 13 Mar 2023 16:41:14 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 13 Mar 2023 16:41:14 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Mon, 13 Mar 2023 16:41:14 GMT
EXPOSE 1883
# Mon, 13 Mar 2023 16:41:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 13 Mar 2023 16:41:14 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2688bb5fb53d62559f686ff80f564656790c072761df2b0cd0632d5ca1a74821`  
		Last Modified: Mon, 13 Mar 2023 16:44:04 GMT  
		Size: 2.5 MB (2547553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb02dd1e319a73a1cf2b520e3690f38fe825f6c9532f1344d03fa95ca208311`  
		Last Modified: Mon, 13 Mar 2023 16:44:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:latest` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:ddce1f6d49b11163493f62b90fc40e71bd6ed639bc6f3fff98fa3cee6f498dad
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5491314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8daf179f68972469d14a519efcf3c52db5e61e5485a5ac7dcc23a468f9d608`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:07:31 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:07:31 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:07:54 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:07:54 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:07:54 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:07:54 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:07:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:07:54 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77a461c4d88d75f9a69a8e4033572e699ab571d80dccf891b979ae576579838`  
		Last Modified: Fri, 10 Feb 2023 22:09:56 GMT  
		Size: 2.8 MB (2781444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b32410a4d525fd2d51a6cbc02e9691094a6a0287e535ec48f7571a78c9d14a6`  
		Last Modified: Fri, 10 Feb 2023 22:09:55 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:latest` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:9bc6355d2a26b1eb61f69a1f5a4a677768fe2e53d47c8e63a0c06b2424c7ecc6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5834155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd168e362dd65b4e7cb0d3d385b5a4052e6e64fbcfd880dbdcd99cd26ce3fd1c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:29 GMT
ADD file:59ac1f8f33f9b9727892b7e45b33f54ef3c20d9d876c49d6a4c057641821d68f in / 
# Fri, 10 Feb 2023 21:24:29 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:05:28 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:05:28 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:06:02 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:06:03 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:06:05 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:06:05 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:06:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:06:07 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:0987f51cd58a7d03bc7d6ff0a3a0a843c1a3fefcd41e3c8adc3999ddde7441e8`  
		Last Modified: Fri, 10 Feb 2023 21:25:30 GMT  
		Size: 2.8 MB (2810653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb82171ce97e635508647afd36cb51535e73c4ba55505f031c2a4150e106dfa`  
		Last Modified: Fri, 10 Feb 2023 22:09:19 GMT  
		Size: 3.0 MB (3023134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd80c78bc5b1e927f589fba7087fb88c88b96af1408f3ed133ebef74026998e`  
		Last Modified: Fri, 10 Feb 2023 22:09:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:latest` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:c0254398acb53c465928f60c50188ce972e6254d27ca6bb55c76dbe8aa84f729
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5783777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bd2e415f3f60f13e6ab84f0499d7c249493ce7b7a14885115aa8853794690b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:14:54 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:14:55 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:15:42 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:15:43 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:15:43 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:15:44 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:15:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:15:45 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7c889150f13b6a972a46fec0e8c57d16d703566231e5862298780a512b35c4`  
		Last Modified: Fri, 10 Feb 2023 22:20:01 GMT  
		Size: 3.0 MB (2978781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c164929fbd4148d64d33f236254eca5b4fea8579e1c6c70deebd7e3af51afdc`  
		Last Modified: Fri, 10 Feb 2023 22:20:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:latest` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:fd1b5435aa3551071d77e1e6eac1369abc49d336bf5ca61a75e8726959584364
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5477196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b716e3aa3e34f067f9fdbf772643f6dfe92b3b2946e6704de5b4c996517851`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:42:31 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 05:42:31 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 05:42:56 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 05:42:56 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 05:42:57 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Sat, 11 Feb 2023 05:42:57 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 05:42:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 05:42:57 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19510dbb190fdaa6cb6c7bacee2f3c507d025fb879639a76a12e3ea91b7464c`  
		Last Modified: Sat, 11 Feb 2023 05:45:34 GMT  
		Size: 2.9 MB (2883247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c1971b8cbe81a094691022fe2d71072d92a9df1080d2c75cd9e5389332eb0f`  
		Last Modified: Sat, 11 Feb 2023 05:45:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eclipse-mosquitto:openssl`

```console
$ docker pull eclipse-mosquitto@sha256:f568dfb10fe2753c7f304d0f2a923697bb3128147717af98aa4a98b3cf7a027f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-mosquitto:openssl` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:0b663899d60c0d4d8a237b3ef733bef3d9fa0941bb1cd9b8686c058385fff4e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3540405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cca5da912eda578d9bb66977ccb08bf096a984df263d824183487de5ccec87`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:43:51 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 07:43:51 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 07:44:56 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 07:44:56 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 07:44:56 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Sat, 11 Feb 2023 07:44:56 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 07:44:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 07:44:56 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9518cf6acf001caa503f17af2421d28fc215ae21dfb49331a381b0eedcc29a`  
		Last Modified: Sat, 11 Feb 2023 07:46:55 GMT  
		Size: 732.3 KB (732275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636eec3ce25ff2474f7302d9751b4d437a600c359a0f56aea878b1973e6fbae7`  
		Last Modified: Sat, 11 Feb 2023 07:46:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:290b601f1c6f77fb628eb4b8f16a7eec901e651cba4e6a2d6c451f03e04f0f11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3322395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd67b8d3caa67ad94b91684c9e7c6db8bfe0413b54aefd7ae1b9cffc776b1c1c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:48 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Mon, 13 Mar 2023 16:12:48 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 16:40:43 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 13 Mar 2023 16:40:44 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 13 Mar 2023 16:41:46 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Mon, 13 Mar 2023 16:41:46 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 13 Mar 2023 16:41:46 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Mon, 13 Mar 2023 16:41:46 GMT
EXPOSE 1883
# Mon, 13 Mar 2023 16:41:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 13 Mar 2023 16:41:47 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e43ba4189456762d09d63c8cbb8098f4b836812fd484442354da99eff8c1107`  
		Last Modified: Mon, 13 Mar 2023 16:44:20 GMT  
		Size: 705.2 KB (705249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c5edd1a21ac19b677053e9a7bb2c9ce82efae5b004b606070371444d7fd5d5`  
		Last Modified: Mon, 13 Mar 2023 16:44:20 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:086fb1a2ece8d09a0671ce773f62a7c5def27c135f62ed27f5490f3348c7404b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3438408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fdb0f92572af0c7c221e0e7efa6049896ea1aed10094267873b10b2efa98d5c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:07:31 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:07:31 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:08:23 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:08:23 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:08:23 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:08:23 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:08:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:08:23 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f67f324a02d8067a8a845f37492ed48cc36046f8a90718d410444915c4335c`  
		Last Modified: Fri, 10 Feb 2023 22:10:08 GMT  
		Size: 728.5 KB (728538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200923fc339d37fa57f5874d7d6459f32f151b1d246c062fcf30914ae18669c4`  
		Last Modified: Fri, 10 Feb 2023 22:10:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:b01177297a8b35263996f8683c58770ff10f4bb9ced7348d605f388fa294921d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3581864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8928e629b4eea91158d8acec61972228566dedd61fbcf796311f752d15ce0be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:29 GMT
ADD file:59ac1f8f33f9b9727892b7e45b33f54ef3c20d9d876c49d6a4c057641821d68f in / 
# Fri, 10 Feb 2023 21:24:29 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:05:28 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:05:28 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:06:41 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:06:42 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:06:44 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:06:44 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:06:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:06:46 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:0987f51cd58a7d03bc7d6ff0a3a0a843c1a3fefcd41e3c8adc3999ddde7441e8`  
		Last Modified: Fri, 10 Feb 2023 21:25:30 GMT  
		Size: 2.8 MB (2810653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0239c398f7dca62942b948c87f89d0d6db3b896c29b6c6965408cf2c4b30891f`  
		Last Modified: Fri, 10 Feb 2023 22:09:33 GMT  
		Size: 770.8 KB (770843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b7c0f6bf5e8120976a6a05b4661b117816ec2a79cc7cf5f9fec2d66835a528`  
		Last Modified: Fri, 10 Feb 2023 22:09:33 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:82bffee113fc9888acd0f61fc3ac20cee6e4dff0d7b3c6f0cbac42171e6c3de8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3612946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f3629c1e91e31e314e61bc2649a5af669b7c5f16dea85b969d8719773d58fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:14:54 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Fri, 10 Feb 2023 22:14:55 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Fri, 10 Feb 2023 22:16:40 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Fri, 10 Feb 2023 22:16:40 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Fri, 10 Feb 2023 22:16:41 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Fri, 10 Feb 2023 22:16:41 GMT
EXPOSE 1883
# Fri, 10 Feb 2023 22:16:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:16:42 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3db7e03886dd824bd80f7adde75b0579208c52e94da12595a2ae65da0ecfd3`  
		Last Modified: Fri, 10 Feb 2023 22:20:19 GMT  
		Size: 808.0 KB (807950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c066243dadde9843e1a3d4eabca0bc3378e9ccbc9428326bb3696f125627da`  
		Last Modified: Fri, 10 Feb 2023 22:20:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-mosquitto:openssl` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:473b1cacea2f5e76456da7a799493daa788718882a123e967c7dcd7c5a9a5a7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3326338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e72578573bbf50f48321bff45c77f00c9611161450fee0d9c275be41d1721d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:42:31 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Sat, 11 Feb 2023 05:42:31 GMT
ENV VERSION=2.0.15 DOWNLOAD_SHA256=4735b1d32e3f91c7a8896741d88a3022e89730a1ee897946decfa0df27039ac6 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Sat, 11 Feb 2023 05:43:31 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build
# Sat, 11 Feb 2023 05:43:31 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Sat, 11 Feb 2023 05:43:31 GMT
COPY multi:f828fb0704e6f46a450b717895e8dada966524fb8a3bd947f3ac0bd7ae28f571 in / 
# Sat, 11 Feb 2023 05:43:31 GMT
EXPOSE 1883
# Sat, 11 Feb 2023 05:43:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 05:43:32 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd2deda8b5a7b241e0b35f7a38fe475ab0d704d3f68d5ada981777c3b249c96`  
		Last Modified: Sat, 11 Feb 2023 05:45:43 GMT  
		Size: 732.4 KB (732389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5693fa66abc0c21b245889af4785c5747a307add6a7f8b959e0341bfec739965`  
		Last Modified: Sat, 11 Feb 2023 05:45:43 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
