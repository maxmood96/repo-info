<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eclipse-mosquitto`

-	[`eclipse-mosquitto:1.6-openssl`](#eclipse-mosquitto16-openssl)
-	[`eclipse-mosquitto:1.6.15-openssl`](#eclipse-mosquitto1615-openssl)
-	[`eclipse-mosquitto:2`](#eclipse-mosquitto2)
-	[`eclipse-mosquitto:2-openssl`](#eclipse-mosquitto2-openssl)
-	[`eclipse-mosquitto:2.0`](#eclipse-mosquitto20)
-	[`eclipse-mosquitto:2.0-openssl`](#eclipse-mosquitto20-openssl)
-	[`eclipse-mosquitto:2.0.18`](#eclipse-mosquitto2018)
-	[`eclipse-mosquitto:2.0.18-openssl`](#eclipse-mosquitto2018-openssl)
-	[`eclipse-mosquitto:latest`](#eclipse-mosquittolatest)
-	[`eclipse-mosquitto:openssl`](#eclipse-mosquittoopenssl)

## `eclipse-mosquitto:1.6-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:5a5f89edddbdaeb2d6b461863566b85c3a6a171f7a44bb1e011b15df3cabf7ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `eclipse-mosquitto:1.6-openssl` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:2d134c62403d1a6536d61534ee6febcc74fd4f46e5ce189935ea07e20a0b0ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4054795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388124001d53954e20dc550a455a95e9287272cc594f73f1cf79da67c40e7a79`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431feea909ee856aaeddc133940b5513cfb7691b2137340392d790d8c15be727`  
		Last Modified: Fri, 06 Sep 2024 23:15:45 GMT  
		Size: 638.2 KB (638243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631498fd7117e346606da1e1dc17c4723bd2ca35978f3dacdf6a7374304de25d`  
		Last Modified: Fri, 06 Sep 2024 23:15:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:a53c8c3dc6bbd087ad8c63afaf5fc9c3474953017a9e023f4e05f34e6d95ea91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 KB (196549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487304b199d940f4fc8d23101145b3f7733ec117e174579468f459eedcb2cfb4`

```dockerfile
```

-	Layers:
	-	`sha256:05397da2afd3e70790123056952f83d2daead28961214ed880731cc35fb22de2`  
		Last Modified: Fri, 06 Sep 2024 23:15:45 GMT  
		Size: 176.7 KB (176677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f42abafbd7d6022f275a25e0f94acd65ea0b4ca9659554309ca9047ef194629`  
		Last Modified: Fri, 06 Sep 2024 23:15:45 GMT  
		Size: 19.9 KB (19872 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:498bdb15f94fe7212d58cca19d6124b5cec9b54a67d9ae791e5fe396b30f5b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3770479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a77a0a0c78b22c4d007078d3722f681678b24ea9a332eac08a12a4be1e233a4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:563fdf5092d9904eba8b5f0f0e881bed7eab326ea811d934e3bf5d1a2032f54d in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:7dda9a44ae82b876e897d397270585fb4961cf54d8b9a6ca9cbfd5b57a7621ea`  
		Last Modified: Mon, 22 Jul 2024 21:50:01 GMT  
		Size: 3.2 MB (3158088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1b80841e4d010e2a76e39d5ec29bbaa2c7ebedfc211deb50af61723146b1b9`  
		Last Modified: Tue, 23 Jul 2024 02:50:48 GMT  
		Size: 612.2 KB (612152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7645380a0efc07599b340cde8cd89748668896bb4dd72fbbbfb7cde36a1c3b`  
		Last Modified: Mon, 22 Jul 2024 22:13:39 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:3159ef2f4c8040a578cac1284bd589e04965461f15dbbed762e3edb7d8b6401b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1410597f8f5b59780a579f74a692221861cfb4e23783d5f14ea1dc4bf721784`

```dockerfile
```

-	Layers:
	-	`sha256:63312b91f27f8e762214d5bd78a86e603bd97dbb9a646033b7d4e2f225f625e8`  
		Last Modified: Tue, 23 Jul 2024 02:50:48 GMT  
		Size: 19.7 KB (19708 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:00b9b5e5deaf19090f22765da8cc9fa4a10c37599ab163c16229462776eb2a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3978282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f273ce74faf95909531ad74e331c6b4f7ab60ad289774c795386f84696eff77e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1078d190f0939c7d559bc06b5a418570e872247251f2c6f1692b99d9b4dc0384`  
		Last Modified: Tue, 23 Jul 2024 13:59:43 GMT  
		Size: 638.5 KB (638548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79978cc6db87bb4e804d103427299c59bc184b908533784109b19d2621f4e0a`  
		Last Modified: Tue, 23 Jul 2024 13:59:42 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:a4c2d7b5d4166fcbb8cb31f5a4ea7583747acae91014f081246ff185e804aecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 KB (196858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b55024a3312064c75d1558fadbf37a89667ba1d00af375ecb78c8aebf87737`

```dockerfile
```

-	Layers:
	-	`sha256:cacaf07c3296b2b3c1c1eb46c46c5404e8d3b0f240317ea642f8eda1352fc73a`  
		Last Modified: Tue, 23 Jul 2024 13:59:43 GMT  
		Size: 176.7 KB (176709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f456982e5c58a24886183358e3926a9013cd4039f95ebe3c6f2b4153d011fb1`  
		Last Modified: Tue, 23 Jul 2024 13:59:43 GMT  
		Size: 20.1 KB (20149 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:f41980098e1857bdcaf79da464327de5b3f5b5abf1ca06e8603d12682c49b7f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563d5f0c96a84f6bb0cf6086fad195435a00cf5d30833ce03aa0a5caf3a8bb0b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:3f9375bc94d18fade7e783bc4d3373e87c738a044bd90802cada5ca164406383 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:174906c4031bcf6ff94e454d6ab4eb615c17d7526cb059d51b364fb429bfc6a7`  
		Last Modified: Fri, 06 Sep 2024 22:42:07 GMT  
		Size: 3.3 MB (3250469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adba5e4b86672c546911fd74572f0bacbea0b0ed90571ff9c34187dd6db23dd1`  
		Last Modified: Fri, 06 Sep 2024 23:15:49 GMT  
		Size: 665.7 KB (665655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ce2548e94a033aab39119553b64bae2304294b30382aa8f8e1657094f1f9a`  
		Last Modified: Fri, 06 Sep 2024 23:15:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:44df3c4c55639f6215b6b459c62990e757bc4bee9f905365a9189dfdf3f0ee26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 KB (196515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a2d8e37b19ca7712c71a9a3f30b82d2e7799bec3a5aa269b9c0689d3717afe`

```dockerfile
```

-	Layers:
	-	`sha256:2e618218157481c4791bcbdf49dd3d5a0dcecc334adda80d747f8d47c39587aa`  
		Last Modified: Fri, 06 Sep 2024 23:15:49 GMT  
		Size: 176.7 KB (176662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7997f8a6dcb77a6aa99bbab2a910f47eee9d31fb9f686b6ddd1753b7236c57a7`  
		Last Modified: Fri, 06 Sep 2024 23:15:49 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:f0ecfbcf488f34c7baf7bb0e399318485e7c2cefe33514058a86f9d016c9f5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4049603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d888bcbf9ab20575974e228749f02740f41d4c2ed575d9e48e6c1bb944b3f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:39fb75dfdfdb9dd435f3c590aab65b7ba2e1633e7fb84509706e3eeb59f2c5a5 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:248e3c27daa6f506dd6946aadf071230265e194056aefeb63e0bcddc4087e672`  
		Last Modified: Mon, 22 Jul 2024 21:27:13 GMT  
		Size: 3.4 MB (3358632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb89a3fae3ee04136ee11811e90dd514b302f47e5f64ce78c963e8a0e614278`  
		Last Modified: Tue, 23 Jul 2024 12:21:09 GMT  
		Size: 690.7 KB (690732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43869f098b6ace751b151543513bc55b7389b28ecd7d0e9056e5af2abc36f689`  
		Last Modified: Tue, 23 Jul 2024 12:21:08 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:5ef01bf574bd25f14835570950f0062ec7e21458eda3b92dd9497f5974450a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 KB (194644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac6d7eec6a4ac279763d9f7ff0f6b2566541063f9aa2dca1ede9dd3b8e729eb`

```dockerfile
```

-	Layers:
	-	`sha256:f11857330bc4b0e9a81cb86b8958fc494a656dd98cd0cee581753b65a4cf163b`  
		Last Modified: Tue, 23 Jul 2024 12:21:09 GMT  
		Size: 174.7 KB (174745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78e9d3868f0c189a34164b1b4d9518f231252c6461acddcea369daa2c68eb4b0`  
		Last Modified: Tue, 23 Jul 2024 12:21:08 GMT  
		Size: 19.9 KB (19899 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:1.6.15-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:5a5f89edddbdaeb2d6b461863566b85c3a6a171f7a44bb1e011b15df3cabf7ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `eclipse-mosquitto:1.6.15-openssl` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:2d134c62403d1a6536d61534ee6febcc74fd4f46e5ce189935ea07e20a0b0ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4054795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388124001d53954e20dc550a455a95e9287272cc594f73f1cf79da67c40e7a79`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431feea909ee856aaeddc133940b5513cfb7691b2137340392d790d8c15be727`  
		Last Modified: Fri, 06 Sep 2024 23:15:45 GMT  
		Size: 638.2 KB (638243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631498fd7117e346606da1e1dc17c4723bd2ca35978f3dacdf6a7374304de25d`  
		Last Modified: Fri, 06 Sep 2024 23:15:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6.15-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:a53c8c3dc6bbd087ad8c63afaf5fc9c3474953017a9e023f4e05f34e6d95ea91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 KB (196549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487304b199d940f4fc8d23101145b3f7733ec117e174579468f459eedcb2cfb4`

```dockerfile
```

-	Layers:
	-	`sha256:05397da2afd3e70790123056952f83d2daead28961214ed880731cc35fb22de2`  
		Last Modified: Fri, 06 Sep 2024 23:15:45 GMT  
		Size: 176.7 KB (176677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f42abafbd7d6022f275a25e0f94acd65ea0b4ca9659554309ca9047ef194629`  
		Last Modified: Fri, 06 Sep 2024 23:15:45 GMT  
		Size: 19.9 KB (19872 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6.15-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:498bdb15f94fe7212d58cca19d6124b5cec9b54a67d9ae791e5fe396b30f5b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3770479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a77a0a0c78b22c4d007078d3722f681678b24ea9a332eac08a12a4be1e233a4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:563fdf5092d9904eba8b5f0f0e881bed7eab326ea811d934e3bf5d1a2032f54d in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:7dda9a44ae82b876e897d397270585fb4961cf54d8b9a6ca9cbfd5b57a7621ea`  
		Last Modified: Mon, 22 Jul 2024 21:50:01 GMT  
		Size: 3.2 MB (3158088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1b80841e4d010e2a76e39d5ec29bbaa2c7ebedfc211deb50af61723146b1b9`  
		Last Modified: Tue, 23 Jul 2024 02:50:48 GMT  
		Size: 612.2 KB (612152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7645380a0efc07599b340cde8cd89748668896bb4dd72fbbbfb7cde36a1c3b`  
		Last Modified: Mon, 22 Jul 2024 22:13:39 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6.15-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:3159ef2f4c8040a578cac1284bd589e04965461f15dbbed762e3edb7d8b6401b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1410597f8f5b59780a579f74a692221861cfb4e23783d5f14ea1dc4bf721784`

```dockerfile
```

-	Layers:
	-	`sha256:63312b91f27f8e762214d5bd78a86e603bd97dbb9a646033b7d4e2f225f625e8`  
		Last Modified: Tue, 23 Jul 2024 02:50:48 GMT  
		Size: 19.7 KB (19708 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6.15-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:00b9b5e5deaf19090f22765da8cc9fa4a10c37599ab163c16229462776eb2a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3978282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f273ce74faf95909531ad74e331c6b4f7ab60ad289774c795386f84696eff77e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1078d190f0939c7d559bc06b5a418570e872247251f2c6f1692b99d9b4dc0384`  
		Last Modified: Tue, 23 Jul 2024 13:59:43 GMT  
		Size: 638.5 KB (638548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79978cc6db87bb4e804d103427299c59bc184b908533784109b19d2621f4e0a`  
		Last Modified: Tue, 23 Jul 2024 13:59:42 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6.15-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:a4c2d7b5d4166fcbb8cb31f5a4ea7583747acae91014f081246ff185e804aecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 KB (196858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b55024a3312064c75d1558fadbf37a89667ba1d00af375ecb78c8aebf87737`

```dockerfile
```

-	Layers:
	-	`sha256:cacaf07c3296b2b3c1c1eb46c46c5404e8d3b0f240317ea642f8eda1352fc73a`  
		Last Modified: Tue, 23 Jul 2024 13:59:43 GMT  
		Size: 176.7 KB (176709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f456982e5c58a24886183358e3926a9013cd4039f95ebe3c6f2b4153d011fb1`  
		Last Modified: Tue, 23 Jul 2024 13:59:43 GMT  
		Size: 20.1 KB (20149 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6.15-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:f41980098e1857bdcaf79da464327de5b3f5b5abf1ca06e8603d12682c49b7f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563d5f0c96a84f6bb0cf6086fad195435a00cf5d30833ce03aa0a5caf3a8bb0b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:3f9375bc94d18fade7e783bc4d3373e87c738a044bd90802cada5ca164406383 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:174906c4031bcf6ff94e454d6ab4eb615c17d7526cb059d51b364fb429bfc6a7`  
		Last Modified: Fri, 06 Sep 2024 22:42:07 GMT  
		Size: 3.3 MB (3250469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adba5e4b86672c546911fd74572f0bacbea0b0ed90571ff9c34187dd6db23dd1`  
		Last Modified: Fri, 06 Sep 2024 23:15:49 GMT  
		Size: 665.7 KB (665655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ce2548e94a033aab39119553b64bae2304294b30382aa8f8e1657094f1f9a`  
		Last Modified: Fri, 06 Sep 2024 23:15:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6.15-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:44df3c4c55639f6215b6b459c62990e757bc4bee9f905365a9189dfdf3f0ee26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 KB (196515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a2d8e37b19ca7712c71a9a3f30b82d2e7799bec3a5aa269b9c0689d3717afe`

```dockerfile
```

-	Layers:
	-	`sha256:2e618218157481c4791bcbdf49dd3d5a0dcecc334adda80d747f8d47c39587aa`  
		Last Modified: Fri, 06 Sep 2024 23:15:49 GMT  
		Size: 176.7 KB (176662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7997f8a6dcb77a6aa99bbab2a910f47eee9d31fb9f686b6ddd1753b7236c57a7`  
		Last Modified: Fri, 06 Sep 2024 23:15:49 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6.15-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:f0ecfbcf488f34c7baf7bb0e399318485e7c2cefe33514058a86f9d016c9f5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4049603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d888bcbf9ab20575974e228749f02740f41d4c2ed575d9e48e6c1bb944b3f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:39fb75dfdfdb9dd435f3c590aab65b7ba2e1633e7fb84509706e3eeb59f2c5a5 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:248e3c27daa6f506dd6946aadf071230265e194056aefeb63e0bcddc4087e672`  
		Last Modified: Mon, 22 Jul 2024 21:27:13 GMT  
		Size: 3.4 MB (3358632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb89a3fae3ee04136ee11811e90dd514b302f47e5f64ce78c963e8a0e614278`  
		Last Modified: Tue, 23 Jul 2024 12:21:09 GMT  
		Size: 690.7 KB (690732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43869f098b6ace751b151543513bc55b7389b28ecd7d0e9056e5af2abc36f689`  
		Last Modified: Tue, 23 Jul 2024 12:21:08 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6.15-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:5ef01bf574bd25f14835570950f0062ec7e21458eda3b92dd9497f5974450a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 KB (194644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac6d7eec6a4ac279763d9f7ff0f6b2566541063f9aa2dca1ede9dd3b8e729eb`

```dockerfile
```

-	Layers:
	-	`sha256:f11857330bc4b0e9a81cb86b8958fc494a656dd98cd0cee581753b65a4cf163b`  
		Last Modified: Tue, 23 Jul 2024 12:21:09 GMT  
		Size: 174.7 KB (174745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78e9d3868f0c189a34164b1b4d9518f231252c6461acddcea369daa2c68eb4b0`  
		Last Modified: Tue, 23 Jul 2024 12:21:08 GMT  
		Size: 19.9 KB (19899 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:2`

```console
$ docker pull eclipse-mosquitto@sha256:bf778f6dd52e69af25402ab3312bc1bd35ea2ffc3b03213894b0b4090478d80e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `eclipse-mosquitto:2` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:f43889926d948c1146751bce701373b71c16a81e5de9b2986b7589221fa4d9e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6209916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25945831d6b8935b016caacc6f612ad4876ba124601b240e64953886cf264b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fe766d1a323e90061758aa0d500abdc36868baa794b5b26c0142fed0fca8bb`  
		Last Modified: Fri, 06 Sep 2024 23:15:50 GMT  
		Size: 2.8 MB (2793234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ee472cb1771785cb71689fce0ec1bae78b4139360a5974729096e1611876fa`  
		Last Modified: Fri, 06 Sep 2024 23:15:49 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:3917c40d375a8d918c950d2e867c97b9c110e22ee55042dc3d5c65efa43327be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 KB (209682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09514bf674b91278d23964f683857002be5770169f24cce668607e4bfa4123c`

```dockerfile
```

-	Layers:
	-	`sha256:2066bfe6f7a9cdd145db61271fefe03780dd537b227060eeedc8eb373cee83c0`  
		Last Modified: Fri, 06 Sep 2024 23:15:49 GMT  
		Size: 187.9 KB (187921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:301335fa3e73be614d994bfdd11a5f495780e76742688ff819fd9f5d82046017`  
		Last Modified: Fri, 06 Sep 2024 23:15:49 GMT  
		Size: 21.8 KB (21761 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:b6e7c33bbd3eeb289e3af56003351c94df9f9ea6d29bc557f22732dd1975f509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1371cae20bd96aa936a572d5cefe34dd2285d3b75df7e4b9688b5e7b06c4c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:563fdf5092d9904eba8b5f0f0e881bed7eab326ea811d934e3bf5d1a2032f54d in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:7dda9a44ae82b876e897d397270585fb4961cf54d8b9a6ca9cbfd5b57a7621ea`  
		Last Modified: Mon, 22 Jul 2024 21:50:01 GMT  
		Size: 3.2 MB (3158088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbf10fe87b3e1231172f5e54a81380131a1556a2cdc225dee021475ba56a72b`  
		Last Modified: Tue, 23 Jul 2024 02:49:12 GMT  
		Size: 2.6 MB (2589823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48b2fcfe02e215e7b532ad64c85a18036203bfee6d623e2b5adc51037b768cf`  
		Last Modified: Mon, 22 Jul 2024 22:06:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:0b3a320289e84f0ad5b23675b44448d0c379b97dde03eb338922cea8664cd20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 KB (21611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff949287204ead763af17bed1d00d66dadb53c4ab4946a72434d661119e512ef`

```dockerfile
```

-	Layers:
	-	`sha256:c70b0d38ea51321e9347e1416443c763b4908cb64b4fa6b2e43d24732ccc4372`  
		Last Modified: Tue, 23 Jul 2024 02:49:11 GMT  
		Size: 21.6 KB (21611 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:3f625cfb5e98c947520bf04d6457009163d48f9343a1ce7b21fbb404e8bc9e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6170422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e7357637ceafcebd9b8ed11a95bb84d79e97e3a41080eec4752a0a82efec9e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745ec8c47d1a7c8204d5272d7587860eb413e22ce8b151c226cd5d6976fd449a`  
		Last Modified: Tue, 23 Jul 2024 13:57:16 GMT  
		Size: 2.8 MB (2830559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d00374516dcf52c340d2b05af721607e4217950c1ae072c7bf942fa3ee8be7`  
		Last Modified: Tue, 23 Jul 2024 13:57:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:08362ad441678846283baf956b8fc5d9a5f5d2a149b8a834fd5c7b575544cae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 KB (210037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5462b6963ef8d12f6820904fd8de6a83814b3d2f603a5452a4a9043b5dc564ae`

```dockerfile
```

-	Layers:
	-	`sha256:6c3fbd00a7ccbf399fc984c97207da3d0829d94b18bd026df3e8b840212aa5dc`  
		Last Modified: Tue, 23 Jul 2024 13:57:16 GMT  
		Size: 188.0 KB (187977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a02934a8317aae5d9ece070a3b284f618222be9784c7ad6f4abcd530b1a1473d`  
		Last Modified: Tue, 23 Jul 2024 13:57:15 GMT  
		Size: 22.1 KB (22060 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:8797816fa05b369f8c5a7b10319908ba8e8d85920a1a9857b87a20accade59d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6107784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d27d1f5c308e0f7bdaaed6665545dfc86edc2b518d00bdaa4865588a53f645f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:3f9375bc94d18fade7e783bc4d3373e87c738a044bd90802cada5ca164406383 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:174906c4031bcf6ff94e454d6ab4eb615c17d7526cb059d51b364fb429bfc6a7`  
		Last Modified: Fri, 06 Sep 2024 22:42:07 GMT  
		Size: 3.3 MB (3250469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f2493b42b67852663c5b9fc6f5e284654ff31837c6f272ed0556b4c431b131`  
		Last Modified: Fri, 06 Sep 2024 23:16:10 GMT  
		Size: 2.9 MB (2856946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d490bed0dcb3e3596af91a2336a9919ea4a20a84d042b905fafc8840522fc0`  
		Last Modified: Fri, 06 Sep 2024 23:16:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:064fa02624768ff1b44e3f54fe6975910b4e8674024152b5cb30500c7964ca1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 KB (209628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6528c702537dcce465598af7e80a66b4a611f4c7a106ba5a5167a0a80f87b59b`

```dockerfile
```

-	Layers:
	-	`sha256:8d155c70527ea776802f205108e02234f7bad15293c78f2912329a6341c66112`  
		Last Modified: Fri, 06 Sep 2024 23:16:10 GMT  
		Size: 187.9 KB (187896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38b7c516ad4f1e69e909df730d5d744bd8ebe47485c656cfb9fd2c7f44a596c4`  
		Last Modified: Fri, 06 Sep 2024 23:16:10 GMT  
		Size: 21.7 KB (21732 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:4cc6300ff0389af76399b795a0bd4034a0128eac8bea750c71cb55f735b61fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6302399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14bb37d5bc7419ac207f1044804a8047f4430d079569d1867756f242029cb2c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:39fb75dfdfdb9dd435f3c590aab65b7ba2e1633e7fb84509706e3eeb59f2c5a5 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:248e3c27daa6f506dd6946aadf071230265e194056aefeb63e0bcddc4087e672`  
		Last Modified: Mon, 22 Jul 2024 21:27:13 GMT  
		Size: 3.4 MB (3358632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae86363d8c7496c27c5c388d66f0a3ede78bfa045b678476c112117ed8de6d`  
		Last Modified: Tue, 23 Jul 2024 12:19:04 GMT  
		Size: 2.9 MB (2943398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724468a62583a04e50cb89bb529e5c7e964af48fdfb169f84639df19a967768a`  
		Last Modified: Tue, 23 Jul 2024 12:19:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:1879f2610937a751b98b19bc8a0e52c9b8dd607777dc2f6f9334a8de8e7b4ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 KB (207800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c25fab00821c66f6f7b079393d19cfa3102cff1c968bb8052eca6375551a3ff`

```dockerfile
```

-	Layers:
	-	`sha256:ad304861205a9eb8ab717becb33e63f80fb7e3a1e735e8368f3c7077bb80163a`  
		Last Modified: Tue, 23 Jul 2024 12:19:04 GMT  
		Size: 186.0 KB (186001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8728c9ca0cdd74a13dbd13675c08324d9201ed5c62b52b1075ea10685b1cdb85`  
		Last Modified: Tue, 23 Jul 2024 12:19:04 GMT  
		Size: 21.8 KB (21799 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:2-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:eb4404a75a4fe8c8fb2ccb39feb1ac77f081267d73d1d228265e4a3178207710
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `eclipse-mosquitto:2-openssl` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:c3db24f40dc7c60f861e71760a784122817ed305cd2d1a129d9da61df043579c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4161776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee9db88b1f9debbf9502b18bd351421e3d121ca50c73bfe9362e3624c96d4ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0258921abac7826cf0e1dbb48575ca770cfabce949293c1c271c57f1db63e4`  
		Last Modified: Fri, 06 Sep 2024 23:15:54 GMT  
		Size: 745.1 KB (745094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62991dde98b33ebdb538de04546bd3402d8c64369a7d28a5cd19a9312135da5`  
		Last Modified: Fri, 06 Sep 2024 23:15:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:96ec401c176c3317d31b2104697b538ac13c3544734b9ebf3160e2fe53ee5bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.6 KB (200569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c508c8bd40873530fbb930a5f81e31271a55b1067049e290ffa19f7c6380698`

```dockerfile
```

-	Layers:
	-	`sha256:8d389339b17129d4a115ddb808ff9862c967bff91dbd7fe5070e7173f234d654`  
		Last Modified: Fri, 06 Sep 2024 23:15:54 GMT  
		Size: 178.9 KB (178918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bd8962577860df38019837c937130791111a9a9f0ded558e4dd1c9c33e18cb8`  
		Last Modified: Fri, 06 Sep 2024 23:15:54 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:ddab224d00101de50e5e76ca39ef4b1b75d2453bd8837a83298c6d30ca8d7578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3874811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c758a772c613be51580e98af86e89b15bb727b87895d283a5a187b4899b44a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:563fdf5092d9904eba8b5f0f0e881bed7eab326ea811d934e3bf5d1a2032f54d in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:7dda9a44ae82b876e897d397270585fb4961cf54d8b9a6ca9cbfd5b57a7621ea`  
		Last Modified: Mon, 22 Jul 2024 21:50:01 GMT  
		Size: 3.2 MB (3158088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a87cd28e50d46d0e69f0c3588ef4a427dae40c0e6c3466f5dea163cd41bf9de`  
		Last Modified: Tue, 23 Jul 2024 02:49:59 GMT  
		Size: 716.4 KB (716354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518ee7ee7663ffd12d77d968bbc115e2522168048a3a7542e9a4ab88f7f5fac`  
		Last Modified: Mon, 22 Jul 2024 22:11:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:95f34900d87604e805080eefa0314b190f45e3d90ceec56d85b3ff9f7b286f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 KB (21501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f333621c1e91bbdd5ceeb526c278674daf6cdcc136205ea00c9c4dcd12caba`

```dockerfile
```

-	Layers:
	-	`sha256:f3f841657d82a561e6681048551b15a5341b2b14084308a8093462df90c87dff`  
		Last Modified: Tue, 23 Jul 2024 02:49:59 GMT  
		Size: 21.5 KB (21501 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:749b46719b5147bf4caec7119c5ebd3a82b7239ad6b7bf676acf533992ca2356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7715ae3d8b17de372215488eaacb5250acd4d68694fcf307afca9b4395ee795`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620123aecb3fe261f9268cc5397fa49d06d9af0a07ae41a38161e8227076520`  
		Last Modified: Tue, 23 Jul 2024 13:58:56 GMT  
		Size: 743.8 KB (743784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afefc64540d22ad906eb124e94d1006f87e21b7aed96cffbbedca609602554d4`  
		Last Modified: Tue, 23 Jul 2024 13:58:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:b593205aa714de8eebef52941fa7de996f9c081a2994d5daeb5d73ad1d2c2319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 KB (200924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bf945ad86ebc794bb561244a77fb477b0803632e7b83fb339cf5ccd9986f0b`

```dockerfile
```

-	Layers:
	-	`sha256:e06a00efbfae8d412a6bc19421b5b985121b66e87a626bef4e79cbb6100b26e3`  
		Last Modified: Tue, 23 Jul 2024 13:58:56 GMT  
		Size: 179.0 KB (178974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34409f83afcffce4d27b25eab370dea86ec37e1e05092593ef6b80f77e2f5438`  
		Last Modified: Tue, 23 Jul 2024 13:58:56 GMT  
		Size: 21.9 KB (21950 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:e4a2ac6ebb8a9f6ae6186df062df578f64a0a354d9dfb9b3063f98fb02701ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4035659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f2fd1fbcc6312c4e757ce897ee9c8547c0646df3cb62f82ffd8595083fb750`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:3f9375bc94d18fade7e783bc4d3373e87c738a044bd90802cada5ca164406383 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:174906c4031bcf6ff94e454d6ab4eb615c17d7526cb059d51b364fb429bfc6a7`  
		Last Modified: Fri, 06 Sep 2024 22:42:07 GMT  
		Size: 3.3 MB (3250469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2cf3c0cbd97dc6eddac667954ded2d69d6f155ae69b0a5cbbbe7b61d02ddd2`  
		Last Modified: Fri, 06 Sep 2024 23:15:58 GMT  
		Size: 784.8 KB (784821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916331651422e7893b875e564887b929b6bf5ca74649dc87317d3eaa3992b300`  
		Last Modified: Fri, 06 Sep 2024 23:15:58 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:a9888ff523cd3b226f55d3bcd5a890fda30141c137e1c660791a7722fbbf7452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.5 KB (200515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8a0a9b517e37ef9e433583b012c8fbc7237d1c5a5005aee05fd768c3f95ce7`

```dockerfile
```

-	Layers:
	-	`sha256:fef60d27d23316b212d7cc882d63789094986e62d5cc3ff9930005e15197abb1`  
		Last Modified: Fri, 06 Sep 2024 23:15:58 GMT  
		Size: 178.9 KB (178893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4994f43e0d44d0c4de5083f39fe20d84f1d07175f602ed51d9e330ed267c21e0`  
		Last Modified: Fri, 06 Sep 2024 23:15:58 GMT  
		Size: 21.6 KB (21622 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:eb5cfb2410a625d842dd4238f61dd858ff090ec04708abc7eb8da7444858f6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a746bd7254f91f279dea5b14f49fe3c76935b117e5d870283835deca2245fee6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:39fb75dfdfdb9dd435f3c590aab65b7ba2e1633e7fb84509706e3eeb59f2c5a5 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:248e3c27daa6f506dd6946aadf071230265e194056aefeb63e0bcddc4087e672`  
		Last Modified: Mon, 22 Jul 2024 21:27:13 GMT  
		Size: 3.4 MB (3358632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9a51acd7c6d249fb46c6ae1b500fbc19d5a6d7a719d7c888efbb2362cc6b3d`  
		Last Modified: Tue, 23 Jul 2024 12:20:09 GMT  
		Size: 816.2 KB (816177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee8f9840a34ca1a60da92700049967990ccd5b02696be9668a3accedfbd2f6c`  
		Last Modified: Tue, 23 Jul 2024 12:20:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:b765721e578f62b6174e82e6b41e57074f0ae55957546166b9298f42cadd890b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0f1aaa72cc4e90be7648216ce33c19855d85eccc18547de3f729b30cba27bb`

```dockerfile
```

-	Layers:
	-	`sha256:1a0fb6d52ff6ee2559c96919aff2b61ad1ad37c2e7ca07e39533950c76e8d5ec`  
		Last Modified: Tue, 23 Jul 2024 12:20:09 GMT  
		Size: 177.0 KB (176998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7054ee224ee0cf4af92e12a5049bf8f838a654721bf45b883ce27156366c4d81`  
		Last Modified: Tue, 23 Jul 2024 12:20:08 GMT  
		Size: 21.7 KB (21689 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:2.0`

```console
$ docker pull eclipse-mosquitto@sha256:bf778f6dd52e69af25402ab3312bc1bd35ea2ffc3b03213894b0b4090478d80e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `eclipse-mosquitto:2.0` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:f43889926d948c1146751bce701373b71c16a81e5de9b2986b7589221fa4d9e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6209916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25945831d6b8935b016caacc6f612ad4876ba124601b240e64953886cf264b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fe766d1a323e90061758aa0d500abdc36868baa794b5b26c0142fed0fca8bb`  
		Last Modified: Fri, 06 Sep 2024 23:15:50 GMT  
		Size: 2.8 MB (2793234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ee472cb1771785cb71689fce0ec1bae78b4139360a5974729096e1611876fa`  
		Last Modified: Fri, 06 Sep 2024 23:15:49 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:3917c40d375a8d918c950d2e867c97b9c110e22ee55042dc3d5c65efa43327be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 KB (209682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09514bf674b91278d23964f683857002be5770169f24cce668607e4bfa4123c`

```dockerfile
```

-	Layers:
	-	`sha256:2066bfe6f7a9cdd145db61271fefe03780dd537b227060eeedc8eb373cee83c0`  
		Last Modified: Fri, 06 Sep 2024 23:15:49 GMT  
		Size: 187.9 KB (187921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:301335fa3e73be614d994bfdd11a5f495780e76742688ff819fd9f5d82046017`  
		Last Modified: Fri, 06 Sep 2024 23:15:49 GMT  
		Size: 21.8 KB (21761 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:b6e7c33bbd3eeb289e3af56003351c94df9f9ea6d29bc557f22732dd1975f509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1371cae20bd96aa936a572d5cefe34dd2285d3b75df7e4b9688b5e7b06c4c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:563fdf5092d9904eba8b5f0f0e881bed7eab326ea811d934e3bf5d1a2032f54d in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:7dda9a44ae82b876e897d397270585fb4961cf54d8b9a6ca9cbfd5b57a7621ea`  
		Last Modified: Mon, 22 Jul 2024 21:50:01 GMT  
		Size: 3.2 MB (3158088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbf10fe87b3e1231172f5e54a81380131a1556a2cdc225dee021475ba56a72b`  
		Last Modified: Tue, 23 Jul 2024 02:49:12 GMT  
		Size: 2.6 MB (2589823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48b2fcfe02e215e7b532ad64c85a18036203bfee6d623e2b5adc51037b768cf`  
		Last Modified: Mon, 22 Jul 2024 22:06:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:0b3a320289e84f0ad5b23675b44448d0c379b97dde03eb338922cea8664cd20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 KB (21611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff949287204ead763af17bed1d00d66dadb53c4ab4946a72434d661119e512ef`

```dockerfile
```

-	Layers:
	-	`sha256:c70b0d38ea51321e9347e1416443c763b4908cb64b4fa6b2e43d24732ccc4372`  
		Last Modified: Tue, 23 Jul 2024 02:49:11 GMT  
		Size: 21.6 KB (21611 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:3f625cfb5e98c947520bf04d6457009163d48f9343a1ce7b21fbb404e8bc9e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6170422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e7357637ceafcebd9b8ed11a95bb84d79e97e3a41080eec4752a0a82efec9e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745ec8c47d1a7c8204d5272d7587860eb413e22ce8b151c226cd5d6976fd449a`  
		Last Modified: Tue, 23 Jul 2024 13:57:16 GMT  
		Size: 2.8 MB (2830559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d00374516dcf52c340d2b05af721607e4217950c1ae072c7bf942fa3ee8be7`  
		Last Modified: Tue, 23 Jul 2024 13:57:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:08362ad441678846283baf956b8fc5d9a5f5d2a149b8a834fd5c7b575544cae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 KB (210037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5462b6963ef8d12f6820904fd8de6a83814b3d2f603a5452a4a9043b5dc564ae`

```dockerfile
```

-	Layers:
	-	`sha256:6c3fbd00a7ccbf399fc984c97207da3d0829d94b18bd026df3e8b840212aa5dc`  
		Last Modified: Tue, 23 Jul 2024 13:57:16 GMT  
		Size: 188.0 KB (187977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a02934a8317aae5d9ece070a3b284f618222be9784c7ad6f4abcd530b1a1473d`  
		Last Modified: Tue, 23 Jul 2024 13:57:15 GMT  
		Size: 22.1 KB (22060 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:8797816fa05b369f8c5a7b10319908ba8e8d85920a1a9857b87a20accade59d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6107784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d27d1f5c308e0f7bdaaed6665545dfc86edc2b518d00bdaa4865588a53f645f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:3f9375bc94d18fade7e783bc4d3373e87c738a044bd90802cada5ca164406383 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:174906c4031bcf6ff94e454d6ab4eb615c17d7526cb059d51b364fb429bfc6a7`  
		Last Modified: Fri, 06 Sep 2024 22:42:07 GMT  
		Size: 3.3 MB (3250469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f2493b42b67852663c5b9fc6f5e284654ff31837c6f272ed0556b4c431b131`  
		Last Modified: Fri, 06 Sep 2024 23:16:10 GMT  
		Size: 2.9 MB (2856946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d490bed0dcb3e3596af91a2336a9919ea4a20a84d042b905fafc8840522fc0`  
		Last Modified: Fri, 06 Sep 2024 23:16:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:064fa02624768ff1b44e3f54fe6975910b4e8674024152b5cb30500c7964ca1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 KB (209628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6528c702537dcce465598af7e80a66b4a611f4c7a106ba5a5167a0a80f87b59b`

```dockerfile
```

-	Layers:
	-	`sha256:8d155c70527ea776802f205108e02234f7bad15293c78f2912329a6341c66112`  
		Last Modified: Fri, 06 Sep 2024 23:16:10 GMT  
		Size: 187.9 KB (187896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38b7c516ad4f1e69e909df730d5d744bd8ebe47485c656cfb9fd2c7f44a596c4`  
		Last Modified: Fri, 06 Sep 2024 23:16:10 GMT  
		Size: 21.7 KB (21732 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:4cc6300ff0389af76399b795a0bd4034a0128eac8bea750c71cb55f735b61fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6302399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14bb37d5bc7419ac207f1044804a8047f4430d079569d1867756f242029cb2c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:39fb75dfdfdb9dd435f3c590aab65b7ba2e1633e7fb84509706e3eeb59f2c5a5 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:248e3c27daa6f506dd6946aadf071230265e194056aefeb63e0bcddc4087e672`  
		Last Modified: Mon, 22 Jul 2024 21:27:13 GMT  
		Size: 3.4 MB (3358632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae86363d8c7496c27c5c388d66f0a3ede78bfa045b678476c112117ed8de6d`  
		Last Modified: Tue, 23 Jul 2024 12:19:04 GMT  
		Size: 2.9 MB (2943398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724468a62583a04e50cb89bb529e5c7e964af48fdfb169f84639df19a967768a`  
		Last Modified: Tue, 23 Jul 2024 12:19:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:1879f2610937a751b98b19bc8a0e52c9b8dd607777dc2f6f9334a8de8e7b4ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 KB (207800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c25fab00821c66f6f7b079393d19cfa3102cff1c968bb8052eca6375551a3ff`

```dockerfile
```

-	Layers:
	-	`sha256:ad304861205a9eb8ab717becb33e63f80fb7e3a1e735e8368f3c7077bb80163a`  
		Last Modified: Tue, 23 Jul 2024 12:19:04 GMT  
		Size: 186.0 KB (186001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8728c9ca0cdd74a13dbd13675c08324d9201ed5c62b52b1075ea10685b1cdb85`  
		Last Modified: Tue, 23 Jul 2024 12:19:04 GMT  
		Size: 21.8 KB (21799 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:2.0-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:eb4404a75a4fe8c8fb2ccb39feb1ac77f081267d73d1d228265e4a3178207710
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `eclipse-mosquitto:2.0-openssl` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:c3db24f40dc7c60f861e71760a784122817ed305cd2d1a129d9da61df043579c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4161776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee9db88b1f9debbf9502b18bd351421e3d121ca50c73bfe9362e3624c96d4ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0258921abac7826cf0e1dbb48575ca770cfabce949293c1c271c57f1db63e4`  
		Last Modified: Fri, 06 Sep 2024 23:15:54 GMT  
		Size: 745.1 KB (745094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62991dde98b33ebdb538de04546bd3402d8c64369a7d28a5cd19a9312135da5`  
		Last Modified: Fri, 06 Sep 2024 23:15:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:96ec401c176c3317d31b2104697b538ac13c3544734b9ebf3160e2fe53ee5bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.6 KB (200569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c508c8bd40873530fbb930a5f81e31271a55b1067049e290ffa19f7c6380698`

```dockerfile
```

-	Layers:
	-	`sha256:8d389339b17129d4a115ddb808ff9862c967bff91dbd7fe5070e7173f234d654`  
		Last Modified: Fri, 06 Sep 2024 23:15:54 GMT  
		Size: 178.9 KB (178918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bd8962577860df38019837c937130791111a9a9f0ded558e4dd1c9c33e18cb8`  
		Last Modified: Fri, 06 Sep 2024 23:15:54 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:ddab224d00101de50e5e76ca39ef4b1b75d2453bd8837a83298c6d30ca8d7578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3874811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c758a772c613be51580e98af86e89b15bb727b87895d283a5a187b4899b44a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:563fdf5092d9904eba8b5f0f0e881bed7eab326ea811d934e3bf5d1a2032f54d in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:7dda9a44ae82b876e897d397270585fb4961cf54d8b9a6ca9cbfd5b57a7621ea`  
		Last Modified: Mon, 22 Jul 2024 21:50:01 GMT  
		Size: 3.2 MB (3158088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a87cd28e50d46d0e69f0c3588ef4a427dae40c0e6c3466f5dea163cd41bf9de`  
		Last Modified: Tue, 23 Jul 2024 02:49:59 GMT  
		Size: 716.4 KB (716354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518ee7ee7663ffd12d77d968bbc115e2522168048a3a7542e9a4ab88f7f5fac`  
		Last Modified: Mon, 22 Jul 2024 22:11:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:95f34900d87604e805080eefa0314b190f45e3d90ceec56d85b3ff9f7b286f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 KB (21501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f333621c1e91bbdd5ceeb526c278674daf6cdcc136205ea00c9c4dcd12caba`

```dockerfile
```

-	Layers:
	-	`sha256:f3f841657d82a561e6681048551b15a5341b2b14084308a8093462df90c87dff`  
		Last Modified: Tue, 23 Jul 2024 02:49:59 GMT  
		Size: 21.5 KB (21501 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:749b46719b5147bf4caec7119c5ebd3a82b7239ad6b7bf676acf533992ca2356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7715ae3d8b17de372215488eaacb5250acd4d68694fcf307afca9b4395ee795`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620123aecb3fe261f9268cc5397fa49d06d9af0a07ae41a38161e8227076520`  
		Last Modified: Tue, 23 Jul 2024 13:58:56 GMT  
		Size: 743.8 KB (743784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afefc64540d22ad906eb124e94d1006f87e21b7aed96cffbbedca609602554d4`  
		Last Modified: Tue, 23 Jul 2024 13:58:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:b593205aa714de8eebef52941fa7de996f9c081a2994d5daeb5d73ad1d2c2319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 KB (200924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bf945ad86ebc794bb561244a77fb477b0803632e7b83fb339cf5ccd9986f0b`

```dockerfile
```

-	Layers:
	-	`sha256:e06a00efbfae8d412a6bc19421b5b985121b66e87a626bef4e79cbb6100b26e3`  
		Last Modified: Tue, 23 Jul 2024 13:58:56 GMT  
		Size: 179.0 KB (178974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34409f83afcffce4d27b25eab370dea86ec37e1e05092593ef6b80f77e2f5438`  
		Last Modified: Tue, 23 Jul 2024 13:58:56 GMT  
		Size: 21.9 KB (21950 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:e4a2ac6ebb8a9f6ae6186df062df578f64a0a354d9dfb9b3063f98fb02701ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4035659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f2fd1fbcc6312c4e757ce897ee9c8547c0646df3cb62f82ffd8595083fb750`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:3f9375bc94d18fade7e783bc4d3373e87c738a044bd90802cada5ca164406383 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:174906c4031bcf6ff94e454d6ab4eb615c17d7526cb059d51b364fb429bfc6a7`  
		Last Modified: Fri, 06 Sep 2024 22:42:07 GMT  
		Size: 3.3 MB (3250469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2cf3c0cbd97dc6eddac667954ded2d69d6f155ae69b0a5cbbbe7b61d02ddd2`  
		Last Modified: Fri, 06 Sep 2024 23:15:58 GMT  
		Size: 784.8 KB (784821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916331651422e7893b875e564887b929b6bf5ca74649dc87317d3eaa3992b300`  
		Last Modified: Fri, 06 Sep 2024 23:15:58 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:a9888ff523cd3b226f55d3bcd5a890fda30141c137e1c660791a7722fbbf7452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.5 KB (200515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8a0a9b517e37ef9e433583b012c8fbc7237d1c5a5005aee05fd768c3f95ce7`

```dockerfile
```

-	Layers:
	-	`sha256:fef60d27d23316b212d7cc882d63789094986e62d5cc3ff9930005e15197abb1`  
		Last Modified: Fri, 06 Sep 2024 23:15:58 GMT  
		Size: 178.9 KB (178893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4994f43e0d44d0c4de5083f39fe20d84f1d07175f602ed51d9e330ed267c21e0`  
		Last Modified: Fri, 06 Sep 2024 23:15:58 GMT  
		Size: 21.6 KB (21622 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:eb5cfb2410a625d842dd4238f61dd858ff090ec04708abc7eb8da7444858f6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a746bd7254f91f279dea5b14f49fe3c76935b117e5d870283835deca2245fee6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:39fb75dfdfdb9dd435f3c590aab65b7ba2e1633e7fb84509706e3eeb59f2c5a5 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:248e3c27daa6f506dd6946aadf071230265e194056aefeb63e0bcddc4087e672`  
		Last Modified: Mon, 22 Jul 2024 21:27:13 GMT  
		Size: 3.4 MB (3358632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9a51acd7c6d249fb46c6ae1b500fbc19d5a6d7a719d7c888efbb2362cc6b3d`  
		Last Modified: Tue, 23 Jul 2024 12:20:09 GMT  
		Size: 816.2 KB (816177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee8f9840a34ca1a60da92700049967990ccd5b02696be9668a3accedfbd2f6c`  
		Last Modified: Tue, 23 Jul 2024 12:20:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:b765721e578f62b6174e82e6b41e57074f0ae55957546166b9298f42cadd890b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0f1aaa72cc4e90be7648216ce33c19855d85eccc18547de3f729b30cba27bb`

```dockerfile
```

-	Layers:
	-	`sha256:1a0fb6d52ff6ee2559c96919aff2b61ad1ad37c2e7ca07e39533950c76e8d5ec`  
		Last Modified: Tue, 23 Jul 2024 12:20:09 GMT  
		Size: 177.0 KB (176998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7054ee224ee0cf4af92e12a5049bf8f838a654721bf45b883ce27156366c4d81`  
		Last Modified: Tue, 23 Jul 2024 12:20:08 GMT  
		Size: 21.7 KB (21689 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:2.0.18`

```console
$ docker pull eclipse-mosquitto@sha256:bf778f6dd52e69af25402ab3312bc1bd35ea2ffc3b03213894b0b4090478d80e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `eclipse-mosquitto:2.0.18` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:f43889926d948c1146751bce701373b71c16a81e5de9b2986b7589221fa4d9e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6209916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25945831d6b8935b016caacc6f612ad4876ba124601b240e64953886cf264b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fe766d1a323e90061758aa0d500abdc36868baa794b5b26c0142fed0fca8bb`  
		Last Modified: Fri, 06 Sep 2024 23:15:50 GMT  
		Size: 2.8 MB (2793234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ee472cb1771785cb71689fce0ec1bae78b4139360a5974729096e1611876fa`  
		Last Modified: Fri, 06 Sep 2024 23:15:49 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.18` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:3917c40d375a8d918c950d2e867c97b9c110e22ee55042dc3d5c65efa43327be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 KB (209682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09514bf674b91278d23964f683857002be5770169f24cce668607e4bfa4123c`

```dockerfile
```

-	Layers:
	-	`sha256:2066bfe6f7a9cdd145db61271fefe03780dd537b227060eeedc8eb373cee83c0`  
		Last Modified: Fri, 06 Sep 2024 23:15:49 GMT  
		Size: 187.9 KB (187921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:301335fa3e73be614d994bfdd11a5f495780e76742688ff819fd9f5d82046017`  
		Last Modified: Fri, 06 Sep 2024 23:15:49 GMT  
		Size: 21.8 KB (21761 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.18` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:b6e7c33bbd3eeb289e3af56003351c94df9f9ea6d29bc557f22732dd1975f509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1371cae20bd96aa936a572d5cefe34dd2285d3b75df7e4b9688b5e7b06c4c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:563fdf5092d9904eba8b5f0f0e881bed7eab326ea811d934e3bf5d1a2032f54d in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:7dda9a44ae82b876e897d397270585fb4961cf54d8b9a6ca9cbfd5b57a7621ea`  
		Last Modified: Mon, 22 Jul 2024 21:50:01 GMT  
		Size: 3.2 MB (3158088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbf10fe87b3e1231172f5e54a81380131a1556a2cdc225dee021475ba56a72b`  
		Last Modified: Tue, 23 Jul 2024 02:49:12 GMT  
		Size: 2.6 MB (2589823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48b2fcfe02e215e7b532ad64c85a18036203bfee6d623e2b5adc51037b768cf`  
		Last Modified: Mon, 22 Jul 2024 22:06:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.18` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:0b3a320289e84f0ad5b23675b44448d0c379b97dde03eb338922cea8664cd20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 KB (21611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff949287204ead763af17bed1d00d66dadb53c4ab4946a72434d661119e512ef`

```dockerfile
```

-	Layers:
	-	`sha256:c70b0d38ea51321e9347e1416443c763b4908cb64b4fa6b2e43d24732ccc4372`  
		Last Modified: Tue, 23 Jul 2024 02:49:11 GMT  
		Size: 21.6 KB (21611 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.18` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:3f625cfb5e98c947520bf04d6457009163d48f9343a1ce7b21fbb404e8bc9e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6170422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e7357637ceafcebd9b8ed11a95bb84d79e97e3a41080eec4752a0a82efec9e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745ec8c47d1a7c8204d5272d7587860eb413e22ce8b151c226cd5d6976fd449a`  
		Last Modified: Tue, 23 Jul 2024 13:57:16 GMT  
		Size: 2.8 MB (2830559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d00374516dcf52c340d2b05af721607e4217950c1ae072c7bf942fa3ee8be7`  
		Last Modified: Tue, 23 Jul 2024 13:57:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.18` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:08362ad441678846283baf956b8fc5d9a5f5d2a149b8a834fd5c7b575544cae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 KB (210037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5462b6963ef8d12f6820904fd8de6a83814b3d2f603a5452a4a9043b5dc564ae`

```dockerfile
```

-	Layers:
	-	`sha256:6c3fbd00a7ccbf399fc984c97207da3d0829d94b18bd026df3e8b840212aa5dc`  
		Last Modified: Tue, 23 Jul 2024 13:57:16 GMT  
		Size: 188.0 KB (187977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a02934a8317aae5d9ece070a3b284f618222be9784c7ad6f4abcd530b1a1473d`  
		Last Modified: Tue, 23 Jul 2024 13:57:15 GMT  
		Size: 22.1 KB (22060 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.18` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:8797816fa05b369f8c5a7b10319908ba8e8d85920a1a9857b87a20accade59d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6107784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d27d1f5c308e0f7bdaaed6665545dfc86edc2b518d00bdaa4865588a53f645f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:3f9375bc94d18fade7e783bc4d3373e87c738a044bd90802cada5ca164406383 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:174906c4031bcf6ff94e454d6ab4eb615c17d7526cb059d51b364fb429bfc6a7`  
		Last Modified: Fri, 06 Sep 2024 22:42:07 GMT  
		Size: 3.3 MB (3250469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f2493b42b67852663c5b9fc6f5e284654ff31837c6f272ed0556b4c431b131`  
		Last Modified: Fri, 06 Sep 2024 23:16:10 GMT  
		Size: 2.9 MB (2856946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d490bed0dcb3e3596af91a2336a9919ea4a20a84d042b905fafc8840522fc0`  
		Last Modified: Fri, 06 Sep 2024 23:16:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.18` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:064fa02624768ff1b44e3f54fe6975910b4e8674024152b5cb30500c7964ca1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 KB (209628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6528c702537dcce465598af7e80a66b4a611f4c7a106ba5a5167a0a80f87b59b`

```dockerfile
```

-	Layers:
	-	`sha256:8d155c70527ea776802f205108e02234f7bad15293c78f2912329a6341c66112`  
		Last Modified: Fri, 06 Sep 2024 23:16:10 GMT  
		Size: 187.9 KB (187896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38b7c516ad4f1e69e909df730d5d744bd8ebe47485c656cfb9fd2c7f44a596c4`  
		Last Modified: Fri, 06 Sep 2024 23:16:10 GMT  
		Size: 21.7 KB (21732 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.18` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:4cc6300ff0389af76399b795a0bd4034a0128eac8bea750c71cb55f735b61fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6302399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14bb37d5bc7419ac207f1044804a8047f4430d079569d1867756f242029cb2c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:39fb75dfdfdb9dd435f3c590aab65b7ba2e1633e7fb84509706e3eeb59f2c5a5 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:248e3c27daa6f506dd6946aadf071230265e194056aefeb63e0bcddc4087e672`  
		Last Modified: Mon, 22 Jul 2024 21:27:13 GMT  
		Size: 3.4 MB (3358632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae86363d8c7496c27c5c388d66f0a3ede78bfa045b678476c112117ed8de6d`  
		Last Modified: Tue, 23 Jul 2024 12:19:04 GMT  
		Size: 2.9 MB (2943398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724468a62583a04e50cb89bb529e5c7e964af48fdfb169f84639df19a967768a`  
		Last Modified: Tue, 23 Jul 2024 12:19:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.18` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:1879f2610937a751b98b19bc8a0e52c9b8dd607777dc2f6f9334a8de8e7b4ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 KB (207800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c25fab00821c66f6f7b079393d19cfa3102cff1c968bb8052eca6375551a3ff`

```dockerfile
```

-	Layers:
	-	`sha256:ad304861205a9eb8ab717becb33e63f80fb7e3a1e735e8368f3c7077bb80163a`  
		Last Modified: Tue, 23 Jul 2024 12:19:04 GMT  
		Size: 186.0 KB (186001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8728c9ca0cdd74a13dbd13675c08324d9201ed5c62b52b1075ea10685b1cdb85`  
		Last Modified: Tue, 23 Jul 2024 12:19:04 GMT  
		Size: 21.8 KB (21799 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:2.0.18-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:eb4404a75a4fe8c8fb2ccb39feb1ac77f081267d73d1d228265e4a3178207710
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `eclipse-mosquitto:2.0.18-openssl` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:c3db24f40dc7c60f861e71760a784122817ed305cd2d1a129d9da61df043579c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4161776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee9db88b1f9debbf9502b18bd351421e3d121ca50c73bfe9362e3624c96d4ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0258921abac7826cf0e1dbb48575ca770cfabce949293c1c271c57f1db63e4`  
		Last Modified: Fri, 06 Sep 2024 23:15:54 GMT  
		Size: 745.1 KB (745094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62991dde98b33ebdb538de04546bd3402d8c64369a7d28a5cd19a9312135da5`  
		Last Modified: Fri, 06 Sep 2024 23:15:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.18-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:96ec401c176c3317d31b2104697b538ac13c3544734b9ebf3160e2fe53ee5bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.6 KB (200569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c508c8bd40873530fbb930a5f81e31271a55b1067049e290ffa19f7c6380698`

```dockerfile
```

-	Layers:
	-	`sha256:8d389339b17129d4a115ddb808ff9862c967bff91dbd7fe5070e7173f234d654`  
		Last Modified: Fri, 06 Sep 2024 23:15:54 GMT  
		Size: 178.9 KB (178918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bd8962577860df38019837c937130791111a9a9f0ded558e4dd1c9c33e18cb8`  
		Last Modified: Fri, 06 Sep 2024 23:15:54 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.18-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:ddab224d00101de50e5e76ca39ef4b1b75d2453bd8837a83298c6d30ca8d7578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3874811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c758a772c613be51580e98af86e89b15bb727b87895d283a5a187b4899b44a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:563fdf5092d9904eba8b5f0f0e881bed7eab326ea811d934e3bf5d1a2032f54d in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:7dda9a44ae82b876e897d397270585fb4961cf54d8b9a6ca9cbfd5b57a7621ea`  
		Last Modified: Mon, 22 Jul 2024 21:50:01 GMT  
		Size: 3.2 MB (3158088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a87cd28e50d46d0e69f0c3588ef4a427dae40c0e6c3466f5dea163cd41bf9de`  
		Last Modified: Tue, 23 Jul 2024 02:49:59 GMT  
		Size: 716.4 KB (716354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518ee7ee7663ffd12d77d968bbc115e2522168048a3a7542e9a4ab88f7f5fac`  
		Last Modified: Mon, 22 Jul 2024 22:11:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.18-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:95f34900d87604e805080eefa0314b190f45e3d90ceec56d85b3ff9f7b286f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 KB (21501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f333621c1e91bbdd5ceeb526c278674daf6cdcc136205ea00c9c4dcd12caba`

```dockerfile
```

-	Layers:
	-	`sha256:f3f841657d82a561e6681048551b15a5341b2b14084308a8093462df90c87dff`  
		Last Modified: Tue, 23 Jul 2024 02:49:59 GMT  
		Size: 21.5 KB (21501 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.18-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:749b46719b5147bf4caec7119c5ebd3a82b7239ad6b7bf676acf533992ca2356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7715ae3d8b17de372215488eaacb5250acd4d68694fcf307afca9b4395ee795`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620123aecb3fe261f9268cc5397fa49d06d9af0a07ae41a38161e8227076520`  
		Last Modified: Tue, 23 Jul 2024 13:58:56 GMT  
		Size: 743.8 KB (743784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afefc64540d22ad906eb124e94d1006f87e21b7aed96cffbbedca609602554d4`  
		Last Modified: Tue, 23 Jul 2024 13:58:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.18-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:b593205aa714de8eebef52941fa7de996f9c081a2994d5daeb5d73ad1d2c2319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 KB (200924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bf945ad86ebc794bb561244a77fb477b0803632e7b83fb339cf5ccd9986f0b`

```dockerfile
```

-	Layers:
	-	`sha256:e06a00efbfae8d412a6bc19421b5b985121b66e87a626bef4e79cbb6100b26e3`  
		Last Modified: Tue, 23 Jul 2024 13:58:56 GMT  
		Size: 179.0 KB (178974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34409f83afcffce4d27b25eab370dea86ec37e1e05092593ef6b80f77e2f5438`  
		Last Modified: Tue, 23 Jul 2024 13:58:56 GMT  
		Size: 21.9 KB (21950 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.18-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:e4a2ac6ebb8a9f6ae6186df062df578f64a0a354d9dfb9b3063f98fb02701ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4035659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f2fd1fbcc6312c4e757ce897ee9c8547c0646df3cb62f82ffd8595083fb750`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:3f9375bc94d18fade7e783bc4d3373e87c738a044bd90802cada5ca164406383 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:174906c4031bcf6ff94e454d6ab4eb615c17d7526cb059d51b364fb429bfc6a7`  
		Last Modified: Fri, 06 Sep 2024 22:42:07 GMT  
		Size: 3.3 MB (3250469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2cf3c0cbd97dc6eddac667954ded2d69d6f155ae69b0a5cbbbe7b61d02ddd2`  
		Last Modified: Fri, 06 Sep 2024 23:15:58 GMT  
		Size: 784.8 KB (784821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916331651422e7893b875e564887b929b6bf5ca74649dc87317d3eaa3992b300`  
		Last Modified: Fri, 06 Sep 2024 23:15:58 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.18-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:a9888ff523cd3b226f55d3bcd5a890fda30141c137e1c660791a7722fbbf7452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.5 KB (200515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8a0a9b517e37ef9e433583b012c8fbc7237d1c5a5005aee05fd768c3f95ce7`

```dockerfile
```

-	Layers:
	-	`sha256:fef60d27d23316b212d7cc882d63789094986e62d5cc3ff9930005e15197abb1`  
		Last Modified: Fri, 06 Sep 2024 23:15:58 GMT  
		Size: 178.9 KB (178893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4994f43e0d44d0c4de5083f39fe20d84f1d07175f602ed51d9e330ed267c21e0`  
		Last Modified: Fri, 06 Sep 2024 23:15:58 GMT  
		Size: 21.6 KB (21622 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.18-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:eb5cfb2410a625d842dd4238f61dd858ff090ec04708abc7eb8da7444858f6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a746bd7254f91f279dea5b14f49fe3c76935b117e5d870283835deca2245fee6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:39fb75dfdfdb9dd435f3c590aab65b7ba2e1633e7fb84509706e3eeb59f2c5a5 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:248e3c27daa6f506dd6946aadf071230265e194056aefeb63e0bcddc4087e672`  
		Last Modified: Mon, 22 Jul 2024 21:27:13 GMT  
		Size: 3.4 MB (3358632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9a51acd7c6d249fb46c6ae1b500fbc19d5a6d7a719d7c888efbb2362cc6b3d`  
		Last Modified: Tue, 23 Jul 2024 12:20:09 GMT  
		Size: 816.2 KB (816177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee8f9840a34ca1a60da92700049967990ccd5b02696be9668a3accedfbd2f6c`  
		Last Modified: Tue, 23 Jul 2024 12:20:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.18-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:b765721e578f62b6174e82e6b41e57074f0ae55957546166b9298f42cadd890b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0f1aaa72cc4e90be7648216ce33c19855d85eccc18547de3f729b30cba27bb`

```dockerfile
```

-	Layers:
	-	`sha256:1a0fb6d52ff6ee2559c96919aff2b61ad1ad37c2e7ca07e39533950c76e8d5ec`  
		Last Modified: Tue, 23 Jul 2024 12:20:09 GMT  
		Size: 177.0 KB (176998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7054ee224ee0cf4af92e12a5049bf8f838a654721bf45b883ce27156366c4d81`  
		Last Modified: Tue, 23 Jul 2024 12:20:08 GMT  
		Size: 21.7 KB (21689 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:latest`

```console
$ docker pull eclipse-mosquitto@sha256:bf778f6dd52e69af25402ab3312bc1bd35ea2ffc3b03213894b0b4090478d80e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `eclipse-mosquitto:latest` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:f43889926d948c1146751bce701373b71c16a81e5de9b2986b7589221fa4d9e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6209916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25945831d6b8935b016caacc6f612ad4876ba124601b240e64953886cf264b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fe766d1a323e90061758aa0d500abdc36868baa794b5b26c0142fed0fca8bb`  
		Last Modified: Fri, 06 Sep 2024 23:15:50 GMT  
		Size: 2.8 MB (2793234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ee472cb1771785cb71689fce0ec1bae78b4139360a5974729096e1611876fa`  
		Last Modified: Fri, 06 Sep 2024 23:15:49 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:3917c40d375a8d918c950d2e867c97b9c110e22ee55042dc3d5c65efa43327be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 KB (209682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09514bf674b91278d23964f683857002be5770169f24cce668607e4bfa4123c`

```dockerfile
```

-	Layers:
	-	`sha256:2066bfe6f7a9cdd145db61271fefe03780dd537b227060eeedc8eb373cee83c0`  
		Last Modified: Fri, 06 Sep 2024 23:15:49 GMT  
		Size: 187.9 KB (187921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:301335fa3e73be614d994bfdd11a5f495780e76742688ff819fd9f5d82046017`  
		Last Modified: Fri, 06 Sep 2024 23:15:49 GMT  
		Size: 21.8 KB (21761 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:latest` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:b6e7c33bbd3eeb289e3af56003351c94df9f9ea6d29bc557f22732dd1975f509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1371cae20bd96aa936a572d5cefe34dd2285d3b75df7e4b9688b5e7b06c4c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:563fdf5092d9904eba8b5f0f0e881bed7eab326ea811d934e3bf5d1a2032f54d in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:7dda9a44ae82b876e897d397270585fb4961cf54d8b9a6ca9cbfd5b57a7621ea`  
		Last Modified: Mon, 22 Jul 2024 21:50:01 GMT  
		Size: 3.2 MB (3158088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbf10fe87b3e1231172f5e54a81380131a1556a2cdc225dee021475ba56a72b`  
		Last Modified: Tue, 23 Jul 2024 02:49:12 GMT  
		Size: 2.6 MB (2589823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48b2fcfe02e215e7b532ad64c85a18036203bfee6d623e2b5adc51037b768cf`  
		Last Modified: Mon, 22 Jul 2024 22:06:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:0b3a320289e84f0ad5b23675b44448d0c379b97dde03eb338922cea8664cd20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 KB (21611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff949287204ead763af17bed1d00d66dadb53c4ab4946a72434d661119e512ef`

```dockerfile
```

-	Layers:
	-	`sha256:c70b0d38ea51321e9347e1416443c763b4908cb64b4fa6b2e43d24732ccc4372`  
		Last Modified: Tue, 23 Jul 2024 02:49:11 GMT  
		Size: 21.6 KB (21611 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:latest` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:3f625cfb5e98c947520bf04d6457009163d48f9343a1ce7b21fbb404e8bc9e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6170422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e7357637ceafcebd9b8ed11a95bb84d79e97e3a41080eec4752a0a82efec9e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745ec8c47d1a7c8204d5272d7587860eb413e22ce8b151c226cd5d6976fd449a`  
		Last Modified: Tue, 23 Jul 2024 13:57:16 GMT  
		Size: 2.8 MB (2830559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d00374516dcf52c340d2b05af721607e4217950c1ae072c7bf942fa3ee8be7`  
		Last Modified: Tue, 23 Jul 2024 13:57:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:08362ad441678846283baf956b8fc5d9a5f5d2a149b8a834fd5c7b575544cae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 KB (210037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5462b6963ef8d12f6820904fd8de6a83814b3d2f603a5452a4a9043b5dc564ae`

```dockerfile
```

-	Layers:
	-	`sha256:6c3fbd00a7ccbf399fc984c97207da3d0829d94b18bd026df3e8b840212aa5dc`  
		Last Modified: Tue, 23 Jul 2024 13:57:16 GMT  
		Size: 188.0 KB (187977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a02934a8317aae5d9ece070a3b284f618222be9784c7ad6f4abcd530b1a1473d`  
		Last Modified: Tue, 23 Jul 2024 13:57:15 GMT  
		Size: 22.1 KB (22060 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:latest` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:8797816fa05b369f8c5a7b10319908ba8e8d85920a1a9857b87a20accade59d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6107784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d27d1f5c308e0f7bdaaed6665545dfc86edc2b518d00bdaa4865588a53f645f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:3f9375bc94d18fade7e783bc4d3373e87c738a044bd90802cada5ca164406383 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:174906c4031bcf6ff94e454d6ab4eb615c17d7526cb059d51b364fb429bfc6a7`  
		Last Modified: Fri, 06 Sep 2024 22:42:07 GMT  
		Size: 3.3 MB (3250469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f2493b42b67852663c5b9fc6f5e284654ff31837c6f272ed0556b4c431b131`  
		Last Modified: Fri, 06 Sep 2024 23:16:10 GMT  
		Size: 2.9 MB (2856946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d490bed0dcb3e3596af91a2336a9919ea4a20a84d042b905fafc8840522fc0`  
		Last Modified: Fri, 06 Sep 2024 23:16:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:064fa02624768ff1b44e3f54fe6975910b4e8674024152b5cb30500c7964ca1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 KB (209628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6528c702537dcce465598af7e80a66b4a611f4c7a106ba5a5167a0a80f87b59b`

```dockerfile
```

-	Layers:
	-	`sha256:8d155c70527ea776802f205108e02234f7bad15293c78f2912329a6341c66112`  
		Last Modified: Fri, 06 Sep 2024 23:16:10 GMT  
		Size: 187.9 KB (187896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38b7c516ad4f1e69e909df730d5d744bd8ebe47485c656cfb9fd2c7f44a596c4`  
		Last Modified: Fri, 06 Sep 2024 23:16:10 GMT  
		Size: 21.7 KB (21732 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:latest` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:4cc6300ff0389af76399b795a0bd4034a0128eac8bea750c71cb55f735b61fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6302399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14bb37d5bc7419ac207f1044804a8047f4430d079569d1867756f242029cb2c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:39fb75dfdfdb9dd435f3c590aab65b7ba2e1633e7fb84509706e3eeb59f2c5a5 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libressl-dev         linux-headers         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_TLS_PSK=no         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libressl &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:248e3c27daa6f506dd6946aadf071230265e194056aefeb63e0bcddc4087e672`  
		Last Modified: Mon, 22 Jul 2024 21:27:13 GMT  
		Size: 3.4 MB (3358632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae86363d8c7496c27c5c388d66f0a3ede78bfa045b678476c112117ed8de6d`  
		Last Modified: Tue, 23 Jul 2024 12:19:04 GMT  
		Size: 2.9 MB (2943398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724468a62583a04e50cb89bb529e5c7e964af48fdfb169f84639df19a967768a`  
		Last Modified: Tue, 23 Jul 2024 12:19:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:1879f2610937a751b98b19bc8a0e52c9b8dd607777dc2f6f9334a8de8e7b4ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 KB (207800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c25fab00821c66f6f7b079393d19cfa3102cff1c968bb8052eca6375551a3ff`

```dockerfile
```

-	Layers:
	-	`sha256:ad304861205a9eb8ab717becb33e63f80fb7e3a1e735e8368f3c7077bb80163a`  
		Last Modified: Tue, 23 Jul 2024 12:19:04 GMT  
		Size: 186.0 KB (186001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8728c9ca0cdd74a13dbd13675c08324d9201ed5c62b52b1075ea10685b1cdb85`  
		Last Modified: Tue, 23 Jul 2024 12:19:04 GMT  
		Size: 21.8 KB (21799 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:openssl`

```console
$ docker pull eclipse-mosquitto@sha256:eb4404a75a4fe8c8fb2ccb39feb1ac77f081267d73d1d228265e4a3178207710
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `eclipse-mosquitto:openssl` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:c3db24f40dc7c60f861e71760a784122817ed305cd2d1a129d9da61df043579c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4161776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee9db88b1f9debbf9502b18bd351421e3d121ca50c73bfe9362e3624c96d4ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0258921abac7826cf0e1dbb48575ca770cfabce949293c1c271c57f1db63e4`  
		Last Modified: Fri, 06 Sep 2024 23:15:54 GMT  
		Size: 745.1 KB (745094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62991dde98b33ebdb538de04546bd3402d8c64369a7d28a5cd19a9312135da5`  
		Last Modified: Fri, 06 Sep 2024 23:15:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:96ec401c176c3317d31b2104697b538ac13c3544734b9ebf3160e2fe53ee5bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.6 KB (200569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c508c8bd40873530fbb930a5f81e31271a55b1067049e290ffa19f7c6380698`

```dockerfile
```

-	Layers:
	-	`sha256:8d389339b17129d4a115ddb808ff9862c967bff91dbd7fe5070e7173f234d654`  
		Last Modified: Fri, 06 Sep 2024 23:15:54 GMT  
		Size: 178.9 KB (178918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bd8962577860df38019837c937130791111a9a9f0ded558e4dd1c9c33e18cb8`  
		Last Modified: Fri, 06 Sep 2024 23:15:54 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:ddab224d00101de50e5e76ca39ef4b1b75d2453bd8837a83298c6d30ca8d7578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3874811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c758a772c613be51580e98af86e89b15bb727b87895d283a5a187b4899b44a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:563fdf5092d9904eba8b5f0f0e881bed7eab326ea811d934e3bf5d1a2032f54d in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:7dda9a44ae82b876e897d397270585fb4961cf54d8b9a6ca9cbfd5b57a7621ea`  
		Last Modified: Mon, 22 Jul 2024 21:50:01 GMT  
		Size: 3.2 MB (3158088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a87cd28e50d46d0e69f0c3588ef4a427dae40c0e6c3466f5dea163cd41bf9de`  
		Last Modified: Tue, 23 Jul 2024 02:49:59 GMT  
		Size: 716.4 KB (716354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518ee7ee7663ffd12d77d968bbc115e2522168048a3a7542e9a4ab88f7f5fac`  
		Last Modified: Mon, 22 Jul 2024 22:11:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:95f34900d87604e805080eefa0314b190f45e3d90ceec56d85b3ff9f7b286f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 KB (21501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f333621c1e91bbdd5ceeb526c278674daf6cdcc136205ea00c9c4dcd12caba`

```dockerfile
```

-	Layers:
	-	`sha256:f3f841657d82a561e6681048551b15a5341b2b14084308a8093462df90c87dff`  
		Last Modified: Tue, 23 Jul 2024 02:49:59 GMT  
		Size: 21.5 KB (21501 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:749b46719b5147bf4caec7119c5ebd3a82b7239ad6b7bf676acf533992ca2356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7715ae3d8b17de372215488eaacb5250acd4d68694fcf307afca9b4395ee795`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620123aecb3fe261f9268cc5397fa49d06d9af0a07ae41a38161e8227076520`  
		Last Modified: Tue, 23 Jul 2024 13:58:56 GMT  
		Size: 743.8 KB (743784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afefc64540d22ad906eb124e94d1006f87e21b7aed96cffbbedca609602554d4`  
		Last Modified: Tue, 23 Jul 2024 13:58:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:b593205aa714de8eebef52941fa7de996f9c081a2994d5daeb5d73ad1d2c2319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 KB (200924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bf945ad86ebc794bb561244a77fb477b0803632e7b83fb339cf5ccd9986f0b`

```dockerfile
```

-	Layers:
	-	`sha256:e06a00efbfae8d412a6bc19421b5b985121b66e87a626bef4e79cbb6100b26e3`  
		Last Modified: Tue, 23 Jul 2024 13:58:56 GMT  
		Size: 179.0 KB (178974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34409f83afcffce4d27b25eab370dea86ec37e1e05092593ef6b80f77e2f5438`  
		Last Modified: Tue, 23 Jul 2024 13:58:56 GMT  
		Size: 21.9 KB (21950 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:e4a2ac6ebb8a9f6ae6186df062df578f64a0a354d9dfb9b3063f98fb02701ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4035659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f2fd1fbcc6312c4e757ce897ee9c8547c0646df3cb62f82ffd8595083fb750`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:3f9375bc94d18fade7e783bc4d3373e87c738a044bd90802cada5ca164406383 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:174906c4031bcf6ff94e454d6ab4eb615c17d7526cb059d51b364fb429bfc6a7`  
		Last Modified: Fri, 06 Sep 2024 22:42:07 GMT  
		Size: 3.3 MB (3250469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2cf3c0cbd97dc6eddac667954ded2d69d6f155ae69b0a5cbbbe7b61d02ddd2`  
		Last Modified: Fri, 06 Sep 2024 23:15:58 GMT  
		Size: 784.8 KB (784821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916331651422e7893b875e564887b929b6bf5ca74649dc87317d3eaa3992b300`  
		Last Modified: Fri, 06 Sep 2024 23:15:58 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:a9888ff523cd3b226f55d3bcd5a890fda30141c137e1c660791a7722fbbf7452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.5 KB (200515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8a0a9b517e37ef9e433583b012c8fbc7237d1c5a5005aee05fd768c3f95ce7`

```dockerfile
```

-	Layers:
	-	`sha256:fef60d27d23316b212d7cc882d63789094986e62d5cc3ff9930005e15197abb1`  
		Last Modified: Fri, 06 Sep 2024 23:15:58 GMT  
		Size: 178.9 KB (178893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4994f43e0d44d0c4de5083f39fe20d84f1d07175f602ed51d9e330ed267c21e0`  
		Last Modified: Fri, 06 Sep 2024 23:15:58 GMT  
		Size: 21.6 KB (21622 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:eb5cfb2410a625d842dd4238f61dd858ff090ec04708abc7eb8da7444858f6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a746bd7254f91f279dea5b14f49fe3c76935b117e5d870283835deca2245fee6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 18 Sep 2023 21:32:22 GMT
ADD file:39fb75dfdfdb9dd435f3c590aab65b7ba2e1633e7fb84509706e3eeb59f2c5a5 in / 
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
LABEL maintainer=Roger Light <roger@atchoo.org> description=Eclipse Mosquitto MQTT Broker
# Mon, 18 Sep 2023 21:32:22 GMT
ENV VERSION=2.0.18 DOWNLOAD_SHA256=d665fe7d0032881b1371a47f34169ee4edab67903b2cd2b4c083822823f4448a GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7 LWS_VERSION=4.2.1 LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51
# Mon, 18 Sep 2023 21:32:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         linux-headers         openssl-dev         util-linux-dev &&     wget https://github.com/warmcat/libwebsockets/archive/v${LWS_VERSION}.tar.gz -O /tmp/lws.tar.gz &&     echo "$LWS_SHA256  /tmp/lws.tar.gz" | sha256sum -c - &&     mkdir -p /build/lws &&     tar --strip=1 -xf /tmp/lws.tar.gz -C /build/lws &&     rm /tmp/lws.tar.gz &&     cd /build/lws &&     cmake .         -DCMAKE_BUILD_TYPE=MinSizeRel         -DCMAKE_INSTALL_PREFIX=/usr         -DDISABLE_WERROR=ON         -DLWS_IPV6=ON         -DLWS_WITHOUT_BUILTIN_GETIFADDRS=ON         -DLWS_WITHOUT_CLIENT=ON         -DLWS_WITHOUT_EXTENSIONS=ON         -DLWS_WITHOUT_TESTAPPS=ON         -DLWS_WITH_EXTERNAL_POLL=ON         -DLWS_WITH_HTTP2=OFF         -DLWS_WITH_SHARED=OFF         -DLWS_WITH_ZIP_FOPS=OFF         -DLWS_WITH_ZLIB=OFF &&     make -j "$(nproc)" &&     rm -rf /root/.cmake &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build/lws/include -I/build"         LDFLAGS="-L/build/lws/lib"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/lws/LICENSE /usr/share/licenses/libwebsockets/LICENSE &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 18 Sep 2023 21:32:22 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 18 Sep 2023 21:32:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 18 Sep 2023 21:32:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Sep 2023 21:32:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:248e3c27daa6f506dd6946aadf071230265e194056aefeb63e0bcddc4087e672`  
		Last Modified: Mon, 22 Jul 2024 21:27:13 GMT  
		Size: 3.4 MB (3358632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9a51acd7c6d249fb46c6ae1b500fbc19d5a6d7a719d7c888efbb2362cc6b3d`  
		Last Modified: Tue, 23 Jul 2024 12:20:09 GMT  
		Size: 816.2 KB (816177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee8f9840a34ca1a60da92700049967990ccd5b02696be9668a3accedfbd2f6c`  
		Last Modified: Tue, 23 Jul 2024 12:20:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:b765721e578f62b6174e82e6b41e57074f0ae55957546166b9298f42cadd890b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0f1aaa72cc4e90be7648216ce33c19855d85eccc18547de3f729b30cba27bb`

```dockerfile
```

-	Layers:
	-	`sha256:1a0fb6d52ff6ee2559c96919aff2b61ad1ad37c2e7ca07e39533950c76e8d5ec`  
		Last Modified: Tue, 23 Jul 2024 12:20:09 GMT  
		Size: 177.0 KB (176998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7054ee224ee0cf4af92e12a5049bf8f838a654721bf45b883ce27156366c4d81`  
		Last Modified: Tue, 23 Jul 2024 12:20:08 GMT  
		Size: 21.7 KB (21689 bytes)  
		MIME: application/vnd.in-toto+json
