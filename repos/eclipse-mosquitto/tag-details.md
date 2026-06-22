<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eclipse-mosquitto`

-	[`eclipse-mosquitto:1.6-openssl`](#eclipse-mosquitto16-openssl)
-	[`eclipse-mosquitto:1.6.15-openssl`](#eclipse-mosquitto1615-openssl)
-	[`eclipse-mosquitto:2`](#eclipse-mosquitto2)
-	[`eclipse-mosquitto:2-openssl`](#eclipse-mosquitto2-openssl)
-	[`eclipse-mosquitto:2.0`](#eclipse-mosquitto20)
-	[`eclipse-mosquitto:2.0-openssl`](#eclipse-mosquitto20-openssl)
-	[`eclipse-mosquitto:2.0.22`](#eclipse-mosquitto2022)
-	[`eclipse-mosquitto:2.0.22-openssl`](#eclipse-mosquitto2022-openssl)
-	[`eclipse-mosquitto:2.1-alpine`](#eclipse-mosquitto21-alpine)
-	[`eclipse-mosquitto:2.1.2-alpine`](#eclipse-mosquitto212-alpine)
-	[`eclipse-mosquitto:alpine`](#eclipse-mosquittoalpine)
-	[`eclipse-mosquitto:latest`](#eclipse-mosquittolatest)
-	[`eclipse-mosquitto:openssl`](#eclipse-mosquittoopenssl)

## `eclipse-mosquitto:1.6-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:1adce580ae335bc21562ab9cc352b43f0a3b757bfdba479cf3f8f3f01a242ae5
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
$ docker pull eclipse-mosquitto@sha256:50e1376db2d5ec17106a74a8c3447264567cc76e7402ef7607f432ed215817ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4685264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f69eb3570297edf6503a89411c28bea6a686cb597a6d0067fdb18dffabf2306`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:45:11 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:45:11 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=1.6.15
# Mon, 22 Jun 2026 19:45:11 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:45:11 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:45:12 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:45:12 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:45:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:45:12 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba9d7834049569e2aa9e565acc116ee27137af8912dea8c6a4cb9657146b0c8`  
		Last Modified: Mon, 22 Jun 2026 19:45:17 GMT  
		Size: 840.6 KB (840602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe44dc340094e6805bdd748dece39110f7ebd3eaec85025508638e4f63c65ba`  
		Last Modified: Mon, 22 Jun 2026 19:45:16 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:e0d914097b661a13d45c42d3dfb5da507b1278c0299f6e502f05f520a64e0803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.3 KB (554336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5538d2a891d24b811137a8f334fbf9bead96eef8f2625d89415ed17ebf09eb2e`

```dockerfile
```

-	Layers:
	-	`sha256:b551f2ebce254120abd52764680fced3b9ca41fac70bde02edcc098174b92d76`  
		Last Modified: Mon, 22 Jun 2026 19:45:17 GMT  
		Size: 536.8 KB (536849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27649cc7277039e0467aaf082d59749b7ce76c51ac9751a899b05cd8974cbd4b`  
		Last Modified: Mon, 22 Jun 2026 19:45:17 GMT  
		Size: 17.5 KB (17487 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:bd798d0c43117f06b1e316624e36da5015332e9964f67e7556cdc60f038df421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4368959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93906568d1624151127da37b6399c5e34ffbfe54d4823d96ab556c81dd65b7e7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:45:58 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:45:58 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=1.6.15
# Mon, 22 Jun 2026 19:45:58 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:45:58 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:45:58 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:45:58 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:45:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:45:58 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05176d51c7bf273617e4ed2893a650c0a0bd519d89f452d45e5a51199635599d`  
		Last Modified: Mon, 22 Jun 2026 19:46:02 GMT  
		Size: 816.1 KB (816124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d7cfda4761463a733410905f6159a1b3a2adc01e6eecbe523a065347b9ddc3`  
		Last Modified: Mon, 22 Jun 2026 19:46:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:36194e15b3d287d5aeb10e18245597e0d40e6aa4a6c47c77473532a41cf3b92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 KB (17337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5028580f674830dd0c32ec188a250380056cc7a0d626fa8a8ec1478362ccbbe`

```dockerfile
```

-	Layers:
	-	`sha256:832591a81e994cdef862ff5c225f9013239696a17e4f4c611977916561e642eb`  
		Last Modified: Mon, 22 Jun 2026 19:46:02 GMT  
		Size: 17.3 KB (17337 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:640cbe277d99d5d5b9de5f469b3e2ef37092f6a7811ba9ee46f12ec6ab59716e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5021907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:679310b000c2879ecdefdaebcdb6aaaebe79d125f0708d740d8251a02b30b945`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:56 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:56 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=1.6.15
# Mon, 22 Jun 2026 19:46:56 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:56 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:56 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:56 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abd2ce2a06c4aaf1c1fc2b9924e030fc6f15dc72fa2bc3f6d75413ad2e31f15`  
		Last Modified: Mon, 22 Jun 2026 19:47:01 GMT  
		Size: 839.8 KB (839809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1143820fc0d78fa94a1384340c8833031cf690c787d147b63bb67021515e14`  
		Last Modified: Mon, 22 Jun 2026 19:47:00 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:dcf07d18e18ce6fa3931209288f713d12324fd17f1ed3aa67546600f38f90444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.8 KB (553799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43db9f9fb168bca789cb5dd497bd9fbdd938c98425165a85f894afbb6268aa1`

```dockerfile
```

-	Layers:
	-	`sha256:373170d7e7333a5599de55927a119383be43a15d3f4367512417581641590c02`  
		Last Modified: Mon, 22 Jun 2026 19:47:01 GMT  
		Size: 536.2 KB (536231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73739d0010f522b7f683e8da525f193cbe1393e21f225b6f6b6ca7b979829bf4`  
		Last Modified: Mon, 22 Jun 2026 19:47:01 GMT  
		Size: 17.6 KB (17568 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:3ecc2241befe3f47651f8f235c53aee3917a65b4b98ce9b0b83a316ec36386e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4540845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6166b612e9865d26135039a6c07fb759d33d13e05f6aa1d39d309a5c1f0caa5d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:13 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:13 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=1.6.15
# Mon, 22 Jun 2026 19:46:13 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:13 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1638b99b23417f8ecfd8f34fb72ce73f0d145faa64777c46d54cb1aa0e72d31c`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 872.6 KB (872616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622c49a45e24c620d3e5c8a33995bc2441943cff8567036a16946b3633d29c61`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:6f486a3260f3a0074c2a7ddfffebed26132cb2763f335b583c4ac3cf1daac5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.3 KB (554300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3fe45bf417d77c924b54e7d4f3105c934b7491d23db321435aac0e52f5a4ed2`

```dockerfile
```

-	Layers:
	-	`sha256:ed92044992e0dd077d7b1f85d3ba39cbc7b97b4db43aeb854ab970c06ad5a97c`  
		Last Modified: Mon, 22 Jun 2026 19:46:18 GMT  
		Size: 536.8 KB (536834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41bb06a10d8d2025d479bf4e038ea985144f54a1d94275cc9be553871829bf5c`  
		Last Modified: Mon, 22 Jun 2026 19:46:18 GMT  
		Size: 17.5 KB (17466 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:d0f6baa28e1d7f0289c6b29a4713fd65bcf359be664dbd2fbd30fc8dbe716677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4712597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014dcc83c306d393f9637ad17c3a177b762213c70ced4c21d75e733acd465fb0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:52:33 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:52:33 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=1.6.15
# Mon, 22 Jun 2026 19:52:33 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:52:33 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:52:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:52:34 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:52:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:52:34 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540fb273c70c84ca32da2daaef3d960200c4c4b8622d9de6a33f3674b428349f`  
		Last Modified: Mon, 22 Jun 2026 19:52:42 GMT  
		Size: 900.1 KB (900057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4941a2d16d3be16d24eda725f535e951cf95cf500eb7e712bc03b0459efc23`  
		Last Modified: Mon, 22 Jun 2026 19:52:42 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:8886a13c94a66128165a1d15b280de785914b8a03fc922536f5908842d7e8545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.7 KB (553740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ed1a14876b625f97cb9855e2137c0c016a1db38692f26eb0f3d3267add687a`

```dockerfile
```

-	Layers:
	-	`sha256:65d6424586c2ebb480425ac78ca9615d21fd071a045a6ea40c9f484dde407537`  
		Last Modified: Mon, 22 Jun 2026 19:52:42 GMT  
		Size: 536.2 KB (536220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d086c0de2676efa89439effc2c91b816f128f5a2d4af0127353c7aa6b7033672`  
		Last Modified: Mon, 22 Jun 2026 19:52:42 GMT  
		Size: 17.5 KB (17520 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6-openssl` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:e515bb6c2c4c19c61d79480121828aec23d1c2b00966d36451e435b84ff940ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4564932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b821837688e606caf8679c2fba0d97517f2d1ba2ea3c49faf65607471964776`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:43 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:43 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=1.6.15
# Mon, 22 Jun 2026 19:46:43 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:43 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:43 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:43 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:43 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a27697664253e08e5f6c0e6aac7ed46b308971ed59e7ba238274dc1c5496ab`  
		Last Modified: Mon, 22 Jun 2026 19:46:52 GMT  
		Size: 857.4 KB (857445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670ee5bc86f9214563619a49fd0b51ffcfbe9d02f410c0e43116970dea7ebf82`  
		Last Modified: Mon, 22 Jun 2026 19:46:52 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:05e4f640f9b4d793141cec80e8f8eb1fb3f2129ce42c9110352ba612acc14b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.7 KB (553686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edeb8f9a0192527a3d1f00acd624180e256abdf696868641b96667e8ccd9e37a`

```dockerfile
```

-	Layers:
	-	`sha256:78e9e03b1afce16938fced2a6cf9f79c88a289cd4ebe9788ae78488dba866454`  
		Last Modified: Mon, 22 Jun 2026 19:46:52 GMT  
		Size: 536.2 KB (536198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c55ed38cfae6eb5ff94c489e6363c360310a6272ddae5baeef14b914ffad0930`  
		Last Modified: Mon, 22 Jun 2026 19:46:52 GMT  
		Size: 17.5 KB (17488 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:1.6.15-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:1adce580ae335bc21562ab9cc352b43f0a3b757bfdba479cf3f8f3f01a242ae5
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
$ docker pull eclipse-mosquitto@sha256:50e1376db2d5ec17106a74a8c3447264567cc76e7402ef7607f432ed215817ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4685264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f69eb3570297edf6503a89411c28bea6a686cb597a6d0067fdb18dffabf2306`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:45:11 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:45:11 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=1.6.15
# Mon, 22 Jun 2026 19:45:11 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:45:11 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:45:12 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:45:12 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:45:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:45:12 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba9d7834049569e2aa9e565acc116ee27137af8912dea8c6a4cb9657146b0c8`  
		Last Modified: Mon, 22 Jun 2026 19:45:17 GMT  
		Size: 840.6 KB (840602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe44dc340094e6805bdd748dece39110f7ebd3eaec85025508638e4f63c65ba`  
		Last Modified: Mon, 22 Jun 2026 19:45:16 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6.15-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:e0d914097b661a13d45c42d3dfb5da507b1278c0299f6e502f05f520a64e0803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.3 KB (554336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5538d2a891d24b811137a8f334fbf9bead96eef8f2625d89415ed17ebf09eb2e`

```dockerfile
```

-	Layers:
	-	`sha256:b551f2ebce254120abd52764680fced3b9ca41fac70bde02edcc098174b92d76`  
		Last Modified: Mon, 22 Jun 2026 19:45:17 GMT  
		Size: 536.8 KB (536849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27649cc7277039e0467aaf082d59749b7ce76c51ac9751a899b05cd8974cbd4b`  
		Last Modified: Mon, 22 Jun 2026 19:45:17 GMT  
		Size: 17.5 KB (17487 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6.15-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:bd798d0c43117f06b1e316624e36da5015332e9964f67e7556cdc60f038df421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4368959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93906568d1624151127da37b6399c5e34ffbfe54d4823d96ab556c81dd65b7e7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:45:58 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:45:58 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=1.6.15
# Mon, 22 Jun 2026 19:45:58 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:45:58 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:45:58 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:45:58 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:45:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:45:58 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05176d51c7bf273617e4ed2893a650c0a0bd519d89f452d45e5a51199635599d`  
		Last Modified: Mon, 22 Jun 2026 19:46:02 GMT  
		Size: 816.1 KB (816124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d7cfda4761463a733410905f6159a1b3a2adc01e6eecbe523a065347b9ddc3`  
		Last Modified: Mon, 22 Jun 2026 19:46:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6.15-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:36194e15b3d287d5aeb10e18245597e0d40e6aa4a6c47c77473532a41cf3b92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 KB (17337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5028580f674830dd0c32ec188a250380056cc7a0d626fa8a8ec1478362ccbbe`

```dockerfile
```

-	Layers:
	-	`sha256:832591a81e994cdef862ff5c225f9013239696a17e4f4c611977916561e642eb`  
		Last Modified: Mon, 22 Jun 2026 19:46:02 GMT  
		Size: 17.3 KB (17337 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6.15-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:640cbe277d99d5d5b9de5f469b3e2ef37092f6a7811ba9ee46f12ec6ab59716e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5021907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:679310b000c2879ecdefdaebcdb6aaaebe79d125f0708d740d8251a02b30b945`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:56 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:56 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=1.6.15
# Mon, 22 Jun 2026 19:46:56 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:56 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:56 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:56 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abd2ce2a06c4aaf1c1fc2b9924e030fc6f15dc72fa2bc3f6d75413ad2e31f15`  
		Last Modified: Mon, 22 Jun 2026 19:47:01 GMT  
		Size: 839.8 KB (839809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1143820fc0d78fa94a1384340c8833031cf690c787d147b63bb67021515e14`  
		Last Modified: Mon, 22 Jun 2026 19:47:00 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6.15-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:dcf07d18e18ce6fa3931209288f713d12324fd17f1ed3aa67546600f38f90444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.8 KB (553799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43db9f9fb168bca789cb5dd497bd9fbdd938c98425165a85f894afbb6268aa1`

```dockerfile
```

-	Layers:
	-	`sha256:373170d7e7333a5599de55927a119383be43a15d3f4367512417581641590c02`  
		Last Modified: Mon, 22 Jun 2026 19:47:01 GMT  
		Size: 536.2 KB (536231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73739d0010f522b7f683e8da525f193cbe1393e21f225b6f6b6ca7b979829bf4`  
		Last Modified: Mon, 22 Jun 2026 19:47:01 GMT  
		Size: 17.6 KB (17568 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6.15-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:3ecc2241befe3f47651f8f235c53aee3917a65b4b98ce9b0b83a316ec36386e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4540845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6166b612e9865d26135039a6c07fb759d33d13e05f6aa1d39d309a5c1f0caa5d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:13 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:13 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=1.6.15
# Mon, 22 Jun 2026 19:46:13 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:13 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1638b99b23417f8ecfd8f34fb72ce73f0d145faa64777c46d54cb1aa0e72d31c`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 872.6 KB (872616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622c49a45e24c620d3e5c8a33995bc2441943cff8567036a16946b3633d29c61`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6.15-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:6f486a3260f3a0074c2a7ddfffebed26132cb2763f335b583c4ac3cf1daac5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.3 KB (554300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3fe45bf417d77c924b54e7d4f3105c934b7491d23db321435aac0e52f5a4ed2`

```dockerfile
```

-	Layers:
	-	`sha256:ed92044992e0dd077d7b1f85d3ba39cbc7b97b4db43aeb854ab970c06ad5a97c`  
		Last Modified: Mon, 22 Jun 2026 19:46:18 GMT  
		Size: 536.8 KB (536834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41bb06a10d8d2025d479bf4e038ea985144f54a1d94275cc9be553871829bf5c`  
		Last Modified: Mon, 22 Jun 2026 19:46:18 GMT  
		Size: 17.5 KB (17466 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6.15-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:d0f6baa28e1d7f0289c6b29a4713fd65bcf359be664dbd2fbd30fc8dbe716677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4712597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014dcc83c306d393f9637ad17c3a177b762213c70ced4c21d75e733acd465fb0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:52:33 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:52:33 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=1.6.15
# Mon, 22 Jun 2026 19:52:33 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:52:33 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:52:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:52:34 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:52:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:52:34 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540fb273c70c84ca32da2daaef3d960200c4c4b8622d9de6a33f3674b428349f`  
		Last Modified: Mon, 22 Jun 2026 19:52:42 GMT  
		Size: 900.1 KB (900057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4941a2d16d3be16d24eda725f535e951cf95cf500eb7e712bc03b0459efc23`  
		Last Modified: Mon, 22 Jun 2026 19:52:42 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6.15-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:8886a13c94a66128165a1d15b280de785914b8a03fc922536f5908842d7e8545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.7 KB (553740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ed1a14876b625f97cb9855e2137c0c016a1db38692f26eb0f3d3267add687a`

```dockerfile
```

-	Layers:
	-	`sha256:65d6424586c2ebb480425ac78ca9615d21fd071a045a6ea40c9f484dde407537`  
		Last Modified: Mon, 22 Jun 2026 19:52:42 GMT  
		Size: 536.2 KB (536220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d086c0de2676efa89439effc2c91b816f128f5a2d4af0127353c7aa6b7033672`  
		Last Modified: Mon, 22 Jun 2026 19:52:42 GMT  
		Size: 17.5 KB (17520 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:1.6.15-openssl` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:e515bb6c2c4c19c61d79480121828aec23d1c2b00966d36451e435b84ff940ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4564932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b821837688e606caf8679c2fba0d97517f2d1ba2ea3c49faf65607471964776`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:43 GMT
ENV VERSION=1.6.15 DOWNLOAD_SHA256=5ff2271512f745bf1a451072cd3768a5daed71e90c5179fae12b049d6c02aa0f GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:43 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=1.6.15
# Mon, 22 Jun 2026 19:46:43 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/src/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v10 /usr/share/licenses/mosquitto/epl-v10 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:43 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:43 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:43 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:43 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a27697664253e08e5f6c0e6aac7ed46b308971ed59e7ba238274dc1c5496ab`  
		Last Modified: Mon, 22 Jun 2026 19:46:52 GMT  
		Size: 857.4 KB (857445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670ee5bc86f9214563619a49fd0b51ffcfbe9d02f410c0e43116970dea7ebf82`  
		Last Modified: Mon, 22 Jun 2026 19:46:52 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:1.6.15-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:05e4f640f9b4d793141cec80e8f8eb1fb3f2129ce42c9110352ba612acc14b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.7 KB (553686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edeb8f9a0192527a3d1f00acd624180e256abdf696868641b96667e8ccd9e37a`

```dockerfile
```

-	Layers:
	-	`sha256:78e9e03b1afce16938fced2a6cf9f79c88a289cd4ebe9788ae78488dba866454`  
		Last Modified: Mon, 22 Jun 2026 19:46:52 GMT  
		Size: 536.2 KB (536198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c55ed38cfae6eb5ff94c489e6363c360310a6272ddae5baeef14b914ffad0930`  
		Last Modified: Mon, 22 Jun 2026 19:46:52 GMT  
		Size: 17.5 KB (17488 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:2`

```console
$ docker pull eclipse-mosquitto@sha256:6f8d8a947c506f8a2290ec65cd4bd2bc7cb4d43fb5f6271f861cb013e2ef9797
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
$ docker pull eclipse-mosquitto@sha256:6dba0f1b2795ddcbe0d41bdfb8b8d56a423acca23ccde4342a4652be54639b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9981691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4725ea7590a578122675b1fdd242b94e5034885cfd0806045b25d700f5498ef5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:22 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:22 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:46:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386c64987679d3a8eaf9cc7d3698f3eda684e6126e8e0c50d4227add3552dc0b`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 6.1 MB (6136992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7cd47effe2f8c6a3d95385e470bd130bb232d0bc17a62da9d7962b34886f19`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:28c23f41929a7d171cd45d545b9388d0c9c629b893166e8a226c83ddce7b3d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.2 KB (627240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33542d63a1f237f0c21a384aa74f6bdf4e34d7c0f064d66eed04a871b6113478`

```dockerfile
```

-	Layers:
	-	`sha256:1917087cd3ac440379e06509ee4c2d6bd615681f4587a17f7444166c5ced4a69`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 605.0 KB (605022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f21e3636ba56436b5c6693d1018a7b61ddc9aa844105dd5e972352684f435719`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 22.2 KB (22218 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:da1de5d1a79d3032bee7127ed865bdbbe28d4ccc873cb334b7374277969cdd1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9642561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920d66bc8fbdfe05a3e40b8b02708647d7ad499e1d37857fd3ae1dc8ae4525fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:45:51 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:45:51 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:45:51 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:45:51 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:45:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:45:51 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:45:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:45:51 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453bacc80cbfdee4cc74a32087e8e19a6f269f7f39e6e444da5f408563657c0f`  
		Last Modified: Mon, 22 Jun 2026 19:45:55 GMT  
		Size: 6.1 MB (6089689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff7fb832e4d610a3298cdf645f4fd6eaaec0cece3e502ca7d31f4d1337a4fbe`  
		Last Modified: Mon, 22 Jun 2026 19:45:55 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:08d00d301f81a6c5d7eaae2fb85d9d0d457711cc15bbbdcd6d1029a39efadfd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 KB (22091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35a496ffcb07a95eedd2b0d1f484fdc653b67620f94021852c9c5a650f0d432`

```dockerfile
```

-	Layers:
	-	`sha256:be7999ce14dfc4dd8517c750c784f7c13382fd880933d403bb3a44d26b2fc822`  
		Last Modified: Mon, 22 Jun 2026 19:45:55 GMT  
		Size: 22.1 KB (22091 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:0cb9dcf861ada0efab0266b43a4e4c702c36df838a7b979c2820dc28bb61c5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10226398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db28dca6f113dc87797b9249d12841dc7877d1b31e8557d227785d9b832ff14`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:48 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:48 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:46:48 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:48 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:48 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:48 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8350ffc995a75ba3206aa4a315d75892c420a016b753a979c07dd3fc2f16c57`  
		Last Modified: Mon, 22 Jun 2026 19:46:54 GMT  
		Size: 6.0 MB (6044262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9176f981295ab62b1887ca5ed64e4d334ede3b22b5166cb76fc67e31a6abc98`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:46052b16b866868944158e91bbb792a6d496d04db9504523463a2f79a60db409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.0 KB (627975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93be1b726b3c16953c649a12dd9f0909098dc1037c667a2ba651112471180317`

```dockerfile
```

-	Layers:
	-	`sha256:7ccae809eccc5745ac1c839eb2d76b9fda108dea322cd508d9601a62947725d1`  
		Last Modified: Mon, 22 Jun 2026 19:46:54 GMT  
		Size: 605.6 KB (605642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:541f93da26ff0f69327c0ed923f7501f7fee41bcfc9e90534e63ca58efeee5db`  
		Last Modified: Mon, 22 Jun 2026 19:46:54 GMT  
		Size: 22.3 KB (22333 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:823a31d1ff413eda08b28ca557cfd13b585f13c3be294d6060ca5382ed329d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9833954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68250bf500236f1564e50ab5653d3449378e608daee25acfba0b69b5eb39cfe7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:03 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:03 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:46:03 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:03 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:03 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:03 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:03 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852582a4bb7b08bd18cce391c6dbf56c1cd9f5de2dda856b1c8504c6a21d433b`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 6.2 MB (6165688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a0b0392f2fb034eb43303fdeedc88881cc4ee9421396ba3122346f84ae0029`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:754444afb1844e80392fd4c5fc1421e8ef88f489bb2e898e50b619b6ea9f9e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.2 KB (627173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affcc33d5d770e8612897f32779a58d08a59555e975e943cee4c28541112ad9a`

```dockerfile
```

-	Layers:
	-	`sha256:9a8c0ab0b7a4a335e42fbd54c2a0d8c1f0dc21461b3fddac8a01ae595fc35a0f`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 605.0 KB (604992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17fa1b88eea5daf2377d8be2e0c9005e27efe364ba849dbf5bcbafe4652823af`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 22.2 KB (22181 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:5d49fb510e4d9895cc5dab57844c4c68579f5ba129b66854817376b903f29d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10257976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13160a70226f38c269d243a067a9587147f898fbce4c0199d737c6bf24077d04`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:50:56 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:50:56 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:50:56 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:50:56 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:50:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:50:57 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:50:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:50:57 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618cdef066c6a9a09b0c2a4aee15349a04cd31177d3997fafca499da8976d5ab`  
		Last Modified: Mon, 22 Jun 2026 19:51:06 GMT  
		Size: 6.4 MB (6445400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5acde757d31e48080fdfcb6e5c1bf404c71230cac28d5c03e0caf06c02a795`  
		Last Modified: Mon, 22 Jun 2026 19:51:06 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:e8c66806a39fb1e70b91db98208d1bc882200d6c8fa0ec0849c92724a1eb6839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.9 KB (627881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0358a54403d0468ce7c125024ae6c0c2f2f1ff41b2e4176f6b07084b24061`

```dockerfile
```

-	Layers:
	-	`sha256:94f54143d0237562f3306fbe851640841d9ce7b681f8d66b504bb129c9eb648e`  
		Last Modified: Mon, 22 Jun 2026 19:51:06 GMT  
		Size: 605.6 KB (605613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03aac17a30d49592d7421fdc30730da27b20586f56ab90a5d6f46e20b6e7be25`  
		Last Modified: Mon, 22 Jun 2026 19:51:06 GMT  
		Size: 22.3 KB (22268 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:47b319153cc2ab8676f2faa8937d5fc63ea05eb6102f4c9bb1466336de1431b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10160689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c3eca1970a7cfb70768f1f8d1707fe836c80b0deab83fe7743a683c88489a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:16 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:16 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:46:16 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:16 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:16 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:16 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbe88b35c8a00ec3bc79dd4909697496c000f13ab4d6fc4bf35b1ac8b214a54`  
		Last Modified: Mon, 22 Jun 2026 19:46:25 GMT  
		Size: 6.5 MB (6453164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32abab4338fe85a3a979fc0b6778c88ef609606420c071a3673e000f39f2753`  
		Last Modified: Mon, 22 Jun 2026 19:46:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:0966c1a39587a1a4d7ac80ccfbdba5f282dab50a7a84393ea8eb7b77bb6a28f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.8 KB (627791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f55fe1fd2faca2d5273f39b11cc50ad39c6c246258007fce6ef803db01ac96d`

```dockerfile
```

-	Layers:
	-	`sha256:74c907c2356d48291b7b5e33281a164b786c701bc9b485c6d1d4d849bc034d96`  
		Last Modified: Mon, 22 Jun 2026 19:46:25 GMT  
		Size: 605.6 KB (605573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eebc69820299f4a53de570c9877db46998254729af41ab08f1252f5db1de13e8`  
		Last Modified: Mon, 22 Jun 2026 19:46:25 GMT  
		Size: 22.2 KB (22218 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:2-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:212f89e1eaeb2c322d6441b64396e3346026674db8fa9c27beac293405c32b3c
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
$ docker pull eclipse-mosquitto@sha256:54c90ecc78645241b6aa272b2a5ac8fc20b0eaf02cc4dd431c0cc8d2fd4447dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4798168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a0bdfcbd9b7a86b36127cb81f54e1afd2019f12f39033458df405a027c03e3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:25 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:25 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:25 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:25 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:25 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:25 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:25 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abed10bdc2db7d274c50a4cf806f9566ba42ebfb000d0ffec9862fb098172ac8`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 953.4 KB (953378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a59d45fdd7a384bfb589d8b7f75f69a4ba3b8845a2a0a0e3b4f395c91920d`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:f6bc1b7a0f2d741ef94b00d3d3109c9920758ff8243031e2094b4483d229f951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.6 KB (559620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80077ef00de7f51499306941eeb1c247056b29b7e9834d164fd208422bb0b7e`

```dockerfile
```

-	Layers:
	-	`sha256:cab0c25086b76b1712462412d962835f93734826d0f9cfc402468651aeac6cd7`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 539.7 KB (539722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13c30b9ce05e160fa660946a7e0be9211d6b614cc4144f73183d0d2f11c59ffd`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 19.9 KB (19898 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:ddc6b11126fa606c4c1ba423a81ee51d2a5b07850c826355ee887ec6a873595f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4477726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60518e191159aa7f3ae234717b5b433e386b86069706876dc76355a64208499`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:45:53 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:45:53 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:45:53 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:45:53 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:45:53 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:45:53 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:45:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:45:53 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5bb9f7317cb1da71f85f62c209f1a302e6e2db9874abc40f14f08bb3ca51af`  
		Last Modified: Mon, 22 Jun 2026 19:45:57 GMT  
		Size: 924.8 KB (924762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179bffd599cea7ee712fcc9c8839562b01da6679cbfbf6d8e9181d58b441818b`  
		Last Modified: Mon, 22 Jun 2026 19:45:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:931aa3591a6745e21dbc60ddf88b1a14823e6d2da6c693b785e5424df5eb68a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbde73b387797107508fdea5f1f32bca05e2142b2063f86d0ae61155edffa664`

```dockerfile
```

-	Layers:
	-	`sha256:d582e92c2f7f154acde5bc9854bc93b9e1d785714f6b36b1d59a14e71a42a7ca`  
		Last Modified: Mon, 22 Jun 2026 19:45:57 GMT  
		Size: 19.8 KB (19779 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:823a8067cf2bb107250a26273b676c41bad11d009563725cae6827915182b6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fef2509a20f85341b1e5c4dd7864e1a4a15fba155b88afa025cbcd5b5611ce9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:58 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:58 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:58 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:58 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:58 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:58 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:58 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0ccfd3e7f198cb156c08ebfede0b1ac31c2e14d52897d7d38e0e47c832262a`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 952.9 KB (952918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf955ac443407760ad9c5b9e49b0b02ce123f0454f49d30a3da4a3fdb273b02`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:63cb223452e0d8dcccc0b484fcb752b54e079d4ea3782f95f7eb5e6566ecc50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.2 KB (559178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36eecea909bb485b58dc89b27f12e35afe8d885e66c7c6c74d2e64b2ba344583`

```dockerfile
```

-	Layers:
	-	`sha256:d0f53279c5fe22e98785439b0c674fdcb28ea743fda8c64becbe2eb5fbab80de`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 539.2 KB (539152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71cc56f198b718130f94d7be737a4b3f7c3853c5b8177f474eba0da069f0e43b`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 20.0 KB (20026 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:b35f5d5a4b7d48f99ff3da4095df17c3d1bdd109f988521a56e5727ac1a03221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4667013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698f9df0edb9197ffa085a50219bf6716622db889be70762077b2208f497b03c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:14 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:14 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:14 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e371fb2091bd005a8c10df16cbf331318c7cd510c16fc7eacfa4e0b73e8829b`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 998.7 KB (998654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7990a82e14d5db48cb51fa0eeea8e840d0bf653de1e7a511be5b7ea5498d14b4`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:3adb5fc84d1a4ec39fdf90d7fd33b39339febc88028d6e1ebccce51d905f1e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.5 KB (559543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4496ba50b795bf21ef6da808dae1428a8017996b0f46bcc3612af62f0800e3d0`

```dockerfile
```

-	Layers:
	-	`sha256:d4beb820ff3734973163d15b174a43020e9553cccba838c1baeb48d90fff0485`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 539.7 KB (539687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be1b408f71832cb70a583ae9a070b6f66545fd2dd4c610720d4aab960c26840d`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 19.9 KB (19856 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:42a2d20b7a2f9cd6d6de77c77cc28c0366f0a00a8e906b9516f5cc5434a0ad00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4850442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffc8a7066412f2c4b9dfa9fdfd16194b16dd912707d2c41161eb91ae062b381`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:51:54 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:51:54 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:51:54 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:51:54 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:51:55 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:51:55 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:51:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:51:55 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f43b806acd6e3376d7e9cdd47929717155662b6fac68ad61fc7ac0b2588f54e`  
		Last Modified: Mon, 22 Jun 2026 19:52:06 GMT  
		Size: 1.0 MB (1037774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad3fff5188760e18873d93d9d1dee307d9a074baffebf30cb95c80d0a57e170`  
		Last Modified: Mon, 22 Jun 2026 19:52:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:f0109e498fd903cc279d128151b7e4d3b4831d24d275bae5ae453b970a27302d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.1 KB (559073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7f18c58f65e26927c71739a3a5bce42f07205ae24bd73b7816b8534e93f32f`

```dockerfile
```

-	Layers:
	-	`sha256:210eb8c11173e7894356744b073f8c177d002ba08590e27c8ef676831cd8d220`  
		Last Modified: Mon, 22 Jun 2026 19:52:05 GMT  
		Size: 539.1 KB (539117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69bcee047f8db3db8bb831dae9e117417d7ad28e38559d21c5e8fa0050265cce`  
		Last Modified: Mon, 22 Jun 2026 19:52:05 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2-openssl` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:2fbbe1880a616caf41786ac6f859672630b92583fb65ef99df081d1c8d08ee84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ec81e53a587efde5d8b12de7c52bcf143c0e2792abc2fd42be969533f955ee`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:45 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:45 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:45 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:45 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:45 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:45 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:45 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26686a72838fb7d2ad73890a6d2ffd473d327de49376e0ceabd4541e4b319e92`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 980.3 KB (980301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0c73fe985dae6773fb042a636b35bd152cea4582e64e6164159dad6706459a`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:6e10004ca4d6cb1b33ec9db2c44c67e909ee3de58612b188cf560ee361f3388f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.0 KB (558969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b314313ca8e8616fcc4dcaf0873c99e4a66b2ebcd1db747891dbcdb80f9ab732`

```dockerfile
```

-	Layers:
	-	`sha256:0f1d0eacb44f2b78b81bdd84c04a62bb3e1c54d9e1303b0a7ab061699d679a28`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 539.1 KB (539071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35fa2e10b46228cc77da09d20158b0af1b330c10e8cfe16d5ca1dbf2a4920863`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 19.9 KB (19898 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:2.0`

```console
$ docker pull eclipse-mosquitto@sha256:212f89e1eaeb2c322d6441b64396e3346026674db8fa9c27beac293405c32b3c
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
$ docker pull eclipse-mosquitto@sha256:54c90ecc78645241b6aa272b2a5ac8fc20b0eaf02cc4dd431c0cc8d2fd4447dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4798168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a0bdfcbd9b7a86b36127cb81f54e1afd2019f12f39033458df405a027c03e3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:25 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:25 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:25 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:25 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:25 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:25 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:25 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abed10bdc2db7d274c50a4cf806f9566ba42ebfb000d0ffec9862fb098172ac8`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 953.4 KB (953378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a59d45fdd7a384bfb589d8b7f75f69a4ba3b8845a2a0a0e3b4f395c91920d`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:f6bc1b7a0f2d741ef94b00d3d3109c9920758ff8243031e2094b4483d229f951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.6 KB (559620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80077ef00de7f51499306941eeb1c247056b29b7e9834d164fd208422bb0b7e`

```dockerfile
```

-	Layers:
	-	`sha256:cab0c25086b76b1712462412d962835f93734826d0f9cfc402468651aeac6cd7`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 539.7 KB (539722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13c30b9ce05e160fa660946a7e0be9211d6b614cc4144f73183d0d2f11c59ffd`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 19.9 KB (19898 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:ddc6b11126fa606c4c1ba423a81ee51d2a5b07850c826355ee887ec6a873595f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4477726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60518e191159aa7f3ae234717b5b433e386b86069706876dc76355a64208499`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:45:53 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:45:53 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:45:53 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:45:53 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:45:53 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:45:53 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:45:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:45:53 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5bb9f7317cb1da71f85f62c209f1a302e6e2db9874abc40f14f08bb3ca51af`  
		Last Modified: Mon, 22 Jun 2026 19:45:57 GMT  
		Size: 924.8 KB (924762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179bffd599cea7ee712fcc9c8839562b01da6679cbfbf6d8e9181d58b441818b`  
		Last Modified: Mon, 22 Jun 2026 19:45:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:931aa3591a6745e21dbc60ddf88b1a14823e6d2da6c693b785e5424df5eb68a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbde73b387797107508fdea5f1f32bca05e2142b2063f86d0ae61155edffa664`

```dockerfile
```

-	Layers:
	-	`sha256:d582e92c2f7f154acde5bc9854bc93b9e1d785714f6b36b1d59a14e71a42a7ca`  
		Last Modified: Mon, 22 Jun 2026 19:45:57 GMT  
		Size: 19.8 KB (19779 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:823a8067cf2bb107250a26273b676c41bad11d009563725cae6827915182b6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fef2509a20f85341b1e5c4dd7864e1a4a15fba155b88afa025cbcd5b5611ce9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:58 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:58 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:58 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:58 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:58 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:58 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:58 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0ccfd3e7f198cb156c08ebfede0b1ac31c2e14d52897d7d38e0e47c832262a`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 952.9 KB (952918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf955ac443407760ad9c5b9e49b0b02ce123f0454f49d30a3da4a3fdb273b02`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:63cb223452e0d8dcccc0b484fcb752b54e079d4ea3782f95f7eb5e6566ecc50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.2 KB (559178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36eecea909bb485b58dc89b27f12e35afe8d885e66c7c6c74d2e64b2ba344583`

```dockerfile
```

-	Layers:
	-	`sha256:d0f53279c5fe22e98785439b0c674fdcb28ea743fda8c64becbe2eb5fbab80de`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 539.2 KB (539152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71cc56f198b718130f94d7be737a4b3f7c3853c5b8177f474eba0da069f0e43b`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 20.0 KB (20026 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:b35f5d5a4b7d48f99ff3da4095df17c3d1bdd109f988521a56e5727ac1a03221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4667013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698f9df0edb9197ffa085a50219bf6716622db889be70762077b2208f497b03c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:14 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:14 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:14 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e371fb2091bd005a8c10df16cbf331318c7cd510c16fc7eacfa4e0b73e8829b`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 998.7 KB (998654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7990a82e14d5db48cb51fa0eeea8e840d0bf653de1e7a511be5b7ea5498d14b4`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:3adb5fc84d1a4ec39fdf90d7fd33b39339febc88028d6e1ebccce51d905f1e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.5 KB (559543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4496ba50b795bf21ef6da808dae1428a8017996b0f46bcc3612af62f0800e3d0`

```dockerfile
```

-	Layers:
	-	`sha256:d4beb820ff3734973163d15b174a43020e9553cccba838c1baeb48d90fff0485`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 539.7 KB (539687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be1b408f71832cb70a583ae9a070b6f66545fd2dd4c610720d4aab960c26840d`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 19.9 KB (19856 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:42a2d20b7a2f9cd6d6de77c77cc28c0366f0a00a8e906b9516f5cc5434a0ad00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4850442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffc8a7066412f2c4b9dfa9fdfd16194b16dd912707d2c41161eb91ae062b381`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:51:54 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:51:54 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:51:54 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:51:54 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:51:55 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:51:55 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:51:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:51:55 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f43b806acd6e3376d7e9cdd47929717155662b6fac68ad61fc7ac0b2588f54e`  
		Last Modified: Mon, 22 Jun 2026 19:52:06 GMT  
		Size: 1.0 MB (1037774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad3fff5188760e18873d93d9d1dee307d9a074baffebf30cb95c80d0a57e170`  
		Last Modified: Mon, 22 Jun 2026 19:52:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:f0109e498fd903cc279d128151b7e4d3b4831d24d275bae5ae453b970a27302d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.1 KB (559073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7f18c58f65e26927c71739a3a5bce42f07205ae24bd73b7816b8534e93f32f`

```dockerfile
```

-	Layers:
	-	`sha256:210eb8c11173e7894356744b073f8c177d002ba08590e27c8ef676831cd8d220`  
		Last Modified: Mon, 22 Jun 2026 19:52:05 GMT  
		Size: 539.1 KB (539117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69bcee047f8db3db8bb831dae9e117417d7ad28e38559d21c5e8fa0050265cce`  
		Last Modified: Mon, 22 Jun 2026 19:52:05 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:2fbbe1880a616caf41786ac6f859672630b92583fb65ef99df081d1c8d08ee84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ec81e53a587efde5d8b12de7c52bcf143c0e2792abc2fd42be969533f955ee`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:45 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:45 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:45 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:45 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:45 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:45 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:45 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26686a72838fb7d2ad73890a6d2ffd473d327de49376e0ceabd4541e4b319e92`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 980.3 KB (980301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0c73fe985dae6773fb042a636b35bd152cea4582e64e6164159dad6706459a`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:6e10004ca4d6cb1b33ec9db2c44c67e909ee3de58612b188cf560ee361f3388f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.0 KB (558969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b314313ca8e8616fcc4dcaf0873c99e4a66b2ebcd1db747891dbcdb80f9ab732`

```dockerfile
```

-	Layers:
	-	`sha256:0f1d0eacb44f2b78b81bdd84c04a62bb3e1c54d9e1303b0a7ab061699d679a28`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 539.1 KB (539071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35fa2e10b46228cc77da09d20158b0af1b330c10e8cfe16d5ca1dbf2a4920863`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 19.9 KB (19898 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:2.0-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:212f89e1eaeb2c322d6441b64396e3346026674db8fa9c27beac293405c32b3c
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
$ docker pull eclipse-mosquitto@sha256:54c90ecc78645241b6aa272b2a5ac8fc20b0eaf02cc4dd431c0cc8d2fd4447dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4798168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a0bdfcbd9b7a86b36127cb81f54e1afd2019f12f39033458df405a027c03e3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:25 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:25 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:25 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:25 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:25 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:25 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:25 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abed10bdc2db7d274c50a4cf806f9566ba42ebfb000d0ffec9862fb098172ac8`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 953.4 KB (953378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a59d45fdd7a384bfb589d8b7f75f69a4ba3b8845a2a0a0e3b4f395c91920d`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:f6bc1b7a0f2d741ef94b00d3d3109c9920758ff8243031e2094b4483d229f951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.6 KB (559620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80077ef00de7f51499306941eeb1c247056b29b7e9834d164fd208422bb0b7e`

```dockerfile
```

-	Layers:
	-	`sha256:cab0c25086b76b1712462412d962835f93734826d0f9cfc402468651aeac6cd7`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 539.7 KB (539722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13c30b9ce05e160fa660946a7e0be9211d6b614cc4144f73183d0d2f11c59ffd`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 19.9 KB (19898 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:ddc6b11126fa606c4c1ba423a81ee51d2a5b07850c826355ee887ec6a873595f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4477726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60518e191159aa7f3ae234717b5b433e386b86069706876dc76355a64208499`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:45:53 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:45:53 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:45:53 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:45:53 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:45:53 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:45:53 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:45:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:45:53 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5bb9f7317cb1da71f85f62c209f1a302e6e2db9874abc40f14f08bb3ca51af`  
		Last Modified: Mon, 22 Jun 2026 19:45:57 GMT  
		Size: 924.8 KB (924762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179bffd599cea7ee712fcc9c8839562b01da6679cbfbf6d8e9181d58b441818b`  
		Last Modified: Mon, 22 Jun 2026 19:45:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:931aa3591a6745e21dbc60ddf88b1a14823e6d2da6c693b785e5424df5eb68a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbde73b387797107508fdea5f1f32bca05e2142b2063f86d0ae61155edffa664`

```dockerfile
```

-	Layers:
	-	`sha256:d582e92c2f7f154acde5bc9854bc93b9e1d785714f6b36b1d59a14e71a42a7ca`  
		Last Modified: Mon, 22 Jun 2026 19:45:57 GMT  
		Size: 19.8 KB (19779 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:823a8067cf2bb107250a26273b676c41bad11d009563725cae6827915182b6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fef2509a20f85341b1e5c4dd7864e1a4a15fba155b88afa025cbcd5b5611ce9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:58 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:58 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:58 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:58 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:58 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:58 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:58 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0ccfd3e7f198cb156c08ebfede0b1ac31c2e14d52897d7d38e0e47c832262a`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 952.9 KB (952918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf955ac443407760ad9c5b9e49b0b02ce123f0454f49d30a3da4a3fdb273b02`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:63cb223452e0d8dcccc0b484fcb752b54e079d4ea3782f95f7eb5e6566ecc50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.2 KB (559178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36eecea909bb485b58dc89b27f12e35afe8d885e66c7c6c74d2e64b2ba344583`

```dockerfile
```

-	Layers:
	-	`sha256:d0f53279c5fe22e98785439b0c674fdcb28ea743fda8c64becbe2eb5fbab80de`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 539.2 KB (539152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71cc56f198b718130f94d7be737a4b3f7c3853c5b8177f474eba0da069f0e43b`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 20.0 KB (20026 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:b35f5d5a4b7d48f99ff3da4095df17c3d1bdd109f988521a56e5727ac1a03221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4667013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698f9df0edb9197ffa085a50219bf6716622db889be70762077b2208f497b03c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:14 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:14 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:14 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e371fb2091bd005a8c10df16cbf331318c7cd510c16fc7eacfa4e0b73e8829b`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 998.7 KB (998654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7990a82e14d5db48cb51fa0eeea8e840d0bf653de1e7a511be5b7ea5498d14b4`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:3adb5fc84d1a4ec39fdf90d7fd33b39339febc88028d6e1ebccce51d905f1e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.5 KB (559543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4496ba50b795bf21ef6da808dae1428a8017996b0f46bcc3612af62f0800e3d0`

```dockerfile
```

-	Layers:
	-	`sha256:d4beb820ff3734973163d15b174a43020e9553cccba838c1baeb48d90fff0485`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 539.7 KB (539687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be1b408f71832cb70a583ae9a070b6f66545fd2dd4c610720d4aab960c26840d`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 19.9 KB (19856 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:42a2d20b7a2f9cd6d6de77c77cc28c0366f0a00a8e906b9516f5cc5434a0ad00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4850442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffc8a7066412f2c4b9dfa9fdfd16194b16dd912707d2c41161eb91ae062b381`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:51:54 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:51:54 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:51:54 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:51:54 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:51:55 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:51:55 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:51:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:51:55 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f43b806acd6e3376d7e9cdd47929717155662b6fac68ad61fc7ac0b2588f54e`  
		Last Modified: Mon, 22 Jun 2026 19:52:06 GMT  
		Size: 1.0 MB (1037774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad3fff5188760e18873d93d9d1dee307d9a074baffebf30cb95c80d0a57e170`  
		Last Modified: Mon, 22 Jun 2026 19:52:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:f0109e498fd903cc279d128151b7e4d3b4831d24d275bae5ae453b970a27302d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.1 KB (559073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7f18c58f65e26927c71739a3a5bce42f07205ae24bd73b7816b8534e93f32f`

```dockerfile
```

-	Layers:
	-	`sha256:210eb8c11173e7894356744b073f8c177d002ba08590e27c8ef676831cd8d220`  
		Last Modified: Mon, 22 Jun 2026 19:52:05 GMT  
		Size: 539.1 KB (539117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69bcee047f8db3db8bb831dae9e117417d7ad28e38559d21c5e8fa0050265cce`  
		Last Modified: Mon, 22 Jun 2026 19:52:05 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0-openssl` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:2fbbe1880a616caf41786ac6f859672630b92583fb65ef99df081d1c8d08ee84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ec81e53a587efde5d8b12de7c52bcf143c0e2792abc2fd42be969533f955ee`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:45 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:45 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:45 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:45 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:45 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:45 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:45 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26686a72838fb7d2ad73890a6d2ffd473d327de49376e0ceabd4541e4b319e92`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 980.3 KB (980301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0c73fe985dae6773fb042a636b35bd152cea4582e64e6164159dad6706459a`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:6e10004ca4d6cb1b33ec9db2c44c67e909ee3de58612b188cf560ee361f3388f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.0 KB (558969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b314313ca8e8616fcc4dcaf0873c99e4a66b2ebcd1db747891dbcdb80f9ab732`

```dockerfile
```

-	Layers:
	-	`sha256:0f1d0eacb44f2b78b81bdd84c04a62bb3e1c54d9e1303b0a7ab061699d679a28`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 539.1 KB (539071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35fa2e10b46228cc77da09d20158b0af1b330c10e8cfe16d5ca1dbf2a4920863`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 19.9 KB (19898 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:2.0.22`

```console
$ docker pull eclipse-mosquitto@sha256:212f89e1eaeb2c322d6441b64396e3346026674db8fa9c27beac293405c32b3c
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

### `eclipse-mosquitto:2.0.22` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:54c90ecc78645241b6aa272b2a5ac8fc20b0eaf02cc4dd431c0cc8d2fd4447dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4798168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a0bdfcbd9b7a86b36127cb81f54e1afd2019f12f39033458df405a027c03e3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:25 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:25 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:25 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:25 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:25 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:25 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:25 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abed10bdc2db7d274c50a4cf806f9566ba42ebfb000d0ffec9862fb098172ac8`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 953.4 KB (953378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a59d45fdd7a384bfb589d8b7f75f69a4ba3b8845a2a0a0e3b4f395c91920d`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.22` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:f6bc1b7a0f2d741ef94b00d3d3109c9920758ff8243031e2094b4483d229f951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.6 KB (559620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80077ef00de7f51499306941eeb1c247056b29b7e9834d164fd208422bb0b7e`

```dockerfile
```

-	Layers:
	-	`sha256:cab0c25086b76b1712462412d962835f93734826d0f9cfc402468651aeac6cd7`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 539.7 KB (539722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13c30b9ce05e160fa660946a7e0be9211d6b614cc4144f73183d0d2f11c59ffd`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 19.9 KB (19898 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.22` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:ddc6b11126fa606c4c1ba423a81ee51d2a5b07850c826355ee887ec6a873595f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4477726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60518e191159aa7f3ae234717b5b433e386b86069706876dc76355a64208499`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:45:53 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:45:53 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:45:53 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:45:53 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:45:53 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:45:53 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:45:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:45:53 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5bb9f7317cb1da71f85f62c209f1a302e6e2db9874abc40f14f08bb3ca51af`  
		Last Modified: Mon, 22 Jun 2026 19:45:57 GMT  
		Size: 924.8 KB (924762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179bffd599cea7ee712fcc9c8839562b01da6679cbfbf6d8e9181d58b441818b`  
		Last Modified: Mon, 22 Jun 2026 19:45:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.22` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:931aa3591a6745e21dbc60ddf88b1a14823e6d2da6c693b785e5424df5eb68a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbde73b387797107508fdea5f1f32bca05e2142b2063f86d0ae61155edffa664`

```dockerfile
```

-	Layers:
	-	`sha256:d582e92c2f7f154acde5bc9854bc93b9e1d785714f6b36b1d59a14e71a42a7ca`  
		Last Modified: Mon, 22 Jun 2026 19:45:57 GMT  
		Size: 19.8 KB (19779 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.22` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:823a8067cf2bb107250a26273b676c41bad11d009563725cae6827915182b6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fef2509a20f85341b1e5c4dd7864e1a4a15fba155b88afa025cbcd5b5611ce9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:58 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:58 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:58 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:58 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:58 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:58 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:58 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0ccfd3e7f198cb156c08ebfede0b1ac31c2e14d52897d7d38e0e47c832262a`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 952.9 KB (952918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf955ac443407760ad9c5b9e49b0b02ce123f0454f49d30a3da4a3fdb273b02`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.22` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:63cb223452e0d8dcccc0b484fcb752b54e079d4ea3782f95f7eb5e6566ecc50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.2 KB (559178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36eecea909bb485b58dc89b27f12e35afe8d885e66c7c6c74d2e64b2ba344583`

```dockerfile
```

-	Layers:
	-	`sha256:d0f53279c5fe22e98785439b0c674fdcb28ea743fda8c64becbe2eb5fbab80de`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 539.2 KB (539152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71cc56f198b718130f94d7be737a4b3f7c3853c5b8177f474eba0da069f0e43b`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 20.0 KB (20026 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.22` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:b35f5d5a4b7d48f99ff3da4095df17c3d1bdd109f988521a56e5727ac1a03221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4667013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698f9df0edb9197ffa085a50219bf6716622db889be70762077b2208f497b03c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:14 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:14 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:14 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e371fb2091bd005a8c10df16cbf331318c7cd510c16fc7eacfa4e0b73e8829b`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 998.7 KB (998654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7990a82e14d5db48cb51fa0eeea8e840d0bf653de1e7a511be5b7ea5498d14b4`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.22` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:3adb5fc84d1a4ec39fdf90d7fd33b39339febc88028d6e1ebccce51d905f1e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.5 KB (559543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4496ba50b795bf21ef6da808dae1428a8017996b0f46bcc3612af62f0800e3d0`

```dockerfile
```

-	Layers:
	-	`sha256:d4beb820ff3734973163d15b174a43020e9553cccba838c1baeb48d90fff0485`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 539.7 KB (539687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be1b408f71832cb70a583ae9a070b6f66545fd2dd4c610720d4aab960c26840d`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 19.9 KB (19856 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.22` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:42a2d20b7a2f9cd6d6de77c77cc28c0366f0a00a8e906b9516f5cc5434a0ad00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4850442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffc8a7066412f2c4b9dfa9fdfd16194b16dd912707d2c41161eb91ae062b381`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:51:54 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:51:54 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:51:54 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:51:54 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:51:55 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:51:55 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:51:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:51:55 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f43b806acd6e3376d7e9cdd47929717155662b6fac68ad61fc7ac0b2588f54e`  
		Last Modified: Mon, 22 Jun 2026 19:52:06 GMT  
		Size: 1.0 MB (1037774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad3fff5188760e18873d93d9d1dee307d9a074baffebf30cb95c80d0a57e170`  
		Last Modified: Mon, 22 Jun 2026 19:52:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.22` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:f0109e498fd903cc279d128151b7e4d3b4831d24d275bae5ae453b970a27302d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.1 KB (559073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7f18c58f65e26927c71739a3a5bce42f07205ae24bd73b7816b8534e93f32f`

```dockerfile
```

-	Layers:
	-	`sha256:210eb8c11173e7894356744b073f8c177d002ba08590e27c8ef676831cd8d220`  
		Last Modified: Mon, 22 Jun 2026 19:52:05 GMT  
		Size: 539.1 KB (539117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69bcee047f8db3db8bb831dae9e117417d7ad28e38559d21c5e8fa0050265cce`  
		Last Modified: Mon, 22 Jun 2026 19:52:05 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.22` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:2fbbe1880a616caf41786ac6f859672630b92583fb65ef99df081d1c8d08ee84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ec81e53a587efde5d8b12de7c52bcf143c0e2792abc2fd42be969533f955ee`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:45 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:45 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:45 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:45 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:45 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:45 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:45 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26686a72838fb7d2ad73890a6d2ffd473d327de49376e0ceabd4541e4b319e92`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 980.3 KB (980301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0c73fe985dae6773fb042a636b35bd152cea4582e64e6164159dad6706459a`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.22` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:6e10004ca4d6cb1b33ec9db2c44c67e909ee3de58612b188cf560ee361f3388f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.0 KB (558969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b314313ca8e8616fcc4dcaf0873c99e4a66b2ebcd1db747891dbcdb80f9ab732`

```dockerfile
```

-	Layers:
	-	`sha256:0f1d0eacb44f2b78b81bdd84c04a62bb3e1c54d9e1303b0a7ab061699d679a28`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 539.1 KB (539071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35fa2e10b46228cc77da09d20158b0af1b330c10e8cfe16d5ca1dbf2a4920863`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 19.9 KB (19898 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:2.0.22-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:212f89e1eaeb2c322d6441b64396e3346026674db8fa9c27beac293405c32b3c
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

### `eclipse-mosquitto:2.0.22-openssl` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:54c90ecc78645241b6aa272b2a5ac8fc20b0eaf02cc4dd431c0cc8d2fd4447dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4798168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a0bdfcbd9b7a86b36127cb81f54e1afd2019f12f39033458df405a027c03e3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:25 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:25 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:25 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:25 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:25 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:25 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:25 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abed10bdc2db7d274c50a4cf806f9566ba42ebfb000d0ffec9862fb098172ac8`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 953.4 KB (953378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a59d45fdd7a384bfb589d8b7f75f69a4ba3b8845a2a0a0e3b4f395c91920d`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.22-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:f6bc1b7a0f2d741ef94b00d3d3109c9920758ff8243031e2094b4483d229f951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.6 KB (559620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80077ef00de7f51499306941eeb1c247056b29b7e9834d164fd208422bb0b7e`

```dockerfile
```

-	Layers:
	-	`sha256:cab0c25086b76b1712462412d962835f93734826d0f9cfc402468651aeac6cd7`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 539.7 KB (539722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13c30b9ce05e160fa660946a7e0be9211d6b614cc4144f73183d0d2f11c59ffd`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 19.9 KB (19898 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.22-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:ddc6b11126fa606c4c1ba423a81ee51d2a5b07850c826355ee887ec6a873595f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4477726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60518e191159aa7f3ae234717b5b433e386b86069706876dc76355a64208499`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:45:53 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:45:53 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:45:53 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:45:53 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:45:53 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:45:53 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:45:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:45:53 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5bb9f7317cb1da71f85f62c209f1a302e6e2db9874abc40f14f08bb3ca51af`  
		Last Modified: Mon, 22 Jun 2026 19:45:57 GMT  
		Size: 924.8 KB (924762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179bffd599cea7ee712fcc9c8839562b01da6679cbfbf6d8e9181d58b441818b`  
		Last Modified: Mon, 22 Jun 2026 19:45:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.22-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:931aa3591a6745e21dbc60ddf88b1a14823e6d2da6c693b785e5424df5eb68a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbde73b387797107508fdea5f1f32bca05e2142b2063f86d0ae61155edffa664`

```dockerfile
```

-	Layers:
	-	`sha256:d582e92c2f7f154acde5bc9854bc93b9e1d785714f6b36b1d59a14e71a42a7ca`  
		Last Modified: Mon, 22 Jun 2026 19:45:57 GMT  
		Size: 19.8 KB (19779 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.22-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:823a8067cf2bb107250a26273b676c41bad11d009563725cae6827915182b6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fef2509a20f85341b1e5c4dd7864e1a4a15fba155b88afa025cbcd5b5611ce9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:58 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:58 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:58 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:58 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:58 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:58 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:58 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0ccfd3e7f198cb156c08ebfede0b1ac31c2e14d52897d7d38e0e47c832262a`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 952.9 KB (952918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf955ac443407760ad9c5b9e49b0b02ce123f0454f49d30a3da4a3fdb273b02`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.22-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:63cb223452e0d8dcccc0b484fcb752b54e079d4ea3782f95f7eb5e6566ecc50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.2 KB (559178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36eecea909bb485b58dc89b27f12e35afe8d885e66c7c6c74d2e64b2ba344583`

```dockerfile
```

-	Layers:
	-	`sha256:d0f53279c5fe22e98785439b0c674fdcb28ea743fda8c64becbe2eb5fbab80de`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 539.2 KB (539152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71cc56f198b718130f94d7be737a4b3f7c3853c5b8177f474eba0da069f0e43b`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 20.0 KB (20026 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.22-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:b35f5d5a4b7d48f99ff3da4095df17c3d1bdd109f988521a56e5727ac1a03221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4667013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698f9df0edb9197ffa085a50219bf6716622db889be70762077b2208f497b03c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:14 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:14 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:14 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e371fb2091bd005a8c10df16cbf331318c7cd510c16fc7eacfa4e0b73e8829b`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 998.7 KB (998654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7990a82e14d5db48cb51fa0eeea8e840d0bf653de1e7a511be5b7ea5498d14b4`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.22-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:3adb5fc84d1a4ec39fdf90d7fd33b39339febc88028d6e1ebccce51d905f1e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.5 KB (559543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4496ba50b795bf21ef6da808dae1428a8017996b0f46bcc3612af62f0800e3d0`

```dockerfile
```

-	Layers:
	-	`sha256:d4beb820ff3734973163d15b174a43020e9553cccba838c1baeb48d90fff0485`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 539.7 KB (539687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be1b408f71832cb70a583ae9a070b6f66545fd2dd4c610720d4aab960c26840d`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 19.9 KB (19856 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.22-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:42a2d20b7a2f9cd6d6de77c77cc28c0366f0a00a8e906b9516f5cc5434a0ad00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4850442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffc8a7066412f2c4b9dfa9fdfd16194b16dd912707d2c41161eb91ae062b381`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:51:54 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:51:54 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:51:54 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:51:54 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:51:55 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:51:55 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:51:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:51:55 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f43b806acd6e3376d7e9cdd47929717155662b6fac68ad61fc7ac0b2588f54e`  
		Last Modified: Mon, 22 Jun 2026 19:52:06 GMT  
		Size: 1.0 MB (1037774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad3fff5188760e18873d93d9d1dee307d9a074baffebf30cb95c80d0a57e170`  
		Last Modified: Mon, 22 Jun 2026 19:52:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.22-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:f0109e498fd903cc279d128151b7e4d3b4831d24d275bae5ae453b970a27302d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.1 KB (559073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7f18c58f65e26927c71739a3a5bce42f07205ae24bd73b7816b8534e93f32f`

```dockerfile
```

-	Layers:
	-	`sha256:210eb8c11173e7894356744b073f8c177d002ba08590e27c8ef676831cd8d220`  
		Last Modified: Mon, 22 Jun 2026 19:52:05 GMT  
		Size: 539.1 KB (539117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69bcee047f8db3db8bb831dae9e117417d7ad28e38559d21c5e8fa0050265cce`  
		Last Modified: Mon, 22 Jun 2026 19:52:05 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.0.22-openssl` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:2fbbe1880a616caf41786ac6f859672630b92583fb65ef99df081d1c8d08ee84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ec81e53a587efde5d8b12de7c52bcf143c0e2792abc2fd42be969533f955ee`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:45 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:45 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:45 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:45 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:45 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:45 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:45 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26686a72838fb7d2ad73890a6d2ffd473d327de49376e0ceabd4541e4b319e92`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 980.3 KB (980301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0c73fe985dae6773fb042a636b35bd152cea4582e64e6164159dad6706459a`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.0.22-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:6e10004ca4d6cb1b33ec9db2c44c67e909ee3de58612b188cf560ee361f3388f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.0 KB (558969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b314313ca8e8616fcc4dcaf0873c99e4a66b2ebcd1db747891dbcdb80f9ab732`

```dockerfile
```

-	Layers:
	-	`sha256:0f1d0eacb44f2b78b81bdd84c04a62bb3e1c54d9e1303b0a7ab061699d679a28`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 539.1 KB (539071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35fa2e10b46228cc77da09d20158b0af1b330c10e8cfe16d5ca1dbf2a4920863`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 19.9 KB (19898 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:2.1-alpine`

```console
$ docker pull eclipse-mosquitto@sha256:6f8d8a947c506f8a2290ec65cd4bd2bc7cb4d43fb5f6271f861cb013e2ef9797
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

### `eclipse-mosquitto:2.1-alpine` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:6dba0f1b2795ddcbe0d41bdfb8b8d56a423acca23ccde4342a4652be54639b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9981691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4725ea7590a578122675b1fdd242b94e5034885cfd0806045b25d700f5498ef5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:22 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:22 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:46:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386c64987679d3a8eaf9cc7d3698f3eda684e6126e8e0c50d4227add3552dc0b`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 6.1 MB (6136992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7cd47effe2f8c6a3d95385e470bd130bb232d0bc17a62da9d7962b34886f19`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.1-alpine` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:28c23f41929a7d171cd45d545b9388d0c9c629b893166e8a226c83ddce7b3d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.2 KB (627240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33542d63a1f237f0c21a384aa74f6bdf4e34d7c0f064d66eed04a871b6113478`

```dockerfile
```

-	Layers:
	-	`sha256:1917087cd3ac440379e06509ee4c2d6bd615681f4587a17f7444166c5ced4a69`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 605.0 KB (605022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f21e3636ba56436b5c6693d1018a7b61ddc9aa844105dd5e972352684f435719`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 22.2 KB (22218 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.1-alpine` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:da1de5d1a79d3032bee7127ed865bdbbe28d4ccc873cb334b7374277969cdd1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9642561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920d66bc8fbdfe05a3e40b8b02708647d7ad499e1d37857fd3ae1dc8ae4525fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:45:51 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:45:51 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:45:51 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:45:51 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:45:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:45:51 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:45:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:45:51 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453bacc80cbfdee4cc74a32087e8e19a6f269f7f39e6e444da5f408563657c0f`  
		Last Modified: Mon, 22 Jun 2026 19:45:55 GMT  
		Size: 6.1 MB (6089689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff7fb832e4d610a3298cdf645f4fd6eaaec0cece3e502ca7d31f4d1337a4fbe`  
		Last Modified: Mon, 22 Jun 2026 19:45:55 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.1-alpine` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:08d00d301f81a6c5d7eaae2fb85d9d0d457711cc15bbbdcd6d1029a39efadfd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 KB (22091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35a496ffcb07a95eedd2b0d1f484fdc653b67620f94021852c9c5a650f0d432`

```dockerfile
```

-	Layers:
	-	`sha256:be7999ce14dfc4dd8517c750c784f7c13382fd880933d403bb3a44d26b2fc822`  
		Last Modified: Mon, 22 Jun 2026 19:45:55 GMT  
		Size: 22.1 KB (22091 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.1-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:0cb9dcf861ada0efab0266b43a4e4c702c36df838a7b979c2820dc28bb61c5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10226398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db28dca6f113dc87797b9249d12841dc7877d1b31e8557d227785d9b832ff14`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:48 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:48 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:46:48 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:48 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:48 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:48 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8350ffc995a75ba3206aa4a315d75892c420a016b753a979c07dd3fc2f16c57`  
		Last Modified: Mon, 22 Jun 2026 19:46:54 GMT  
		Size: 6.0 MB (6044262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9176f981295ab62b1887ca5ed64e4d334ede3b22b5166cb76fc67e31a6abc98`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.1-alpine` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:46052b16b866868944158e91bbb792a6d496d04db9504523463a2f79a60db409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.0 KB (627975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93be1b726b3c16953c649a12dd9f0909098dc1037c667a2ba651112471180317`

```dockerfile
```

-	Layers:
	-	`sha256:7ccae809eccc5745ac1c839eb2d76b9fda108dea322cd508d9601a62947725d1`  
		Last Modified: Mon, 22 Jun 2026 19:46:54 GMT  
		Size: 605.6 KB (605642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:541f93da26ff0f69327c0ed923f7501f7fee41bcfc9e90534e63ca58efeee5db`  
		Last Modified: Mon, 22 Jun 2026 19:46:54 GMT  
		Size: 22.3 KB (22333 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.1-alpine` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:823a31d1ff413eda08b28ca557cfd13b585f13c3be294d6060ca5382ed329d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9833954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68250bf500236f1564e50ab5653d3449378e608daee25acfba0b69b5eb39cfe7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:03 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:03 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:46:03 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:03 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:03 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:03 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:03 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852582a4bb7b08bd18cce391c6dbf56c1cd9f5de2dda856b1c8504c6a21d433b`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 6.2 MB (6165688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a0b0392f2fb034eb43303fdeedc88881cc4ee9421396ba3122346f84ae0029`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.1-alpine` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:754444afb1844e80392fd4c5fc1421e8ef88f489bb2e898e50b619b6ea9f9e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.2 KB (627173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affcc33d5d770e8612897f32779a58d08a59555e975e943cee4c28541112ad9a`

```dockerfile
```

-	Layers:
	-	`sha256:9a8c0ab0b7a4a335e42fbd54c2a0d8c1f0dc21461b3fddac8a01ae595fc35a0f`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 605.0 KB (604992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17fa1b88eea5daf2377d8be2e0c9005e27efe364ba849dbf5bcbafe4652823af`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 22.2 KB (22181 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.1-alpine` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:5d49fb510e4d9895cc5dab57844c4c68579f5ba129b66854817376b903f29d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10257976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13160a70226f38c269d243a067a9587147f898fbce4c0199d737c6bf24077d04`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:50:56 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:50:56 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:50:56 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:50:56 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:50:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:50:57 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:50:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:50:57 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618cdef066c6a9a09b0c2a4aee15349a04cd31177d3997fafca499da8976d5ab`  
		Last Modified: Mon, 22 Jun 2026 19:51:06 GMT  
		Size: 6.4 MB (6445400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5acde757d31e48080fdfcb6e5c1bf404c71230cac28d5c03e0caf06c02a795`  
		Last Modified: Mon, 22 Jun 2026 19:51:06 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.1-alpine` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:e8c66806a39fb1e70b91db98208d1bc882200d6c8fa0ec0849c92724a1eb6839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.9 KB (627881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0358a54403d0468ce7c125024ae6c0c2f2f1ff41b2e4176f6b07084b24061`

```dockerfile
```

-	Layers:
	-	`sha256:94f54143d0237562f3306fbe851640841d9ce7b681f8d66b504bb129c9eb648e`  
		Last Modified: Mon, 22 Jun 2026 19:51:06 GMT  
		Size: 605.6 KB (605613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03aac17a30d49592d7421fdc30730da27b20586f56ab90a5d6f46e20b6e7be25`  
		Last Modified: Mon, 22 Jun 2026 19:51:06 GMT  
		Size: 22.3 KB (22268 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.1-alpine` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:47b319153cc2ab8676f2faa8937d5fc63ea05eb6102f4c9bb1466336de1431b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10160689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c3eca1970a7cfb70768f1f8d1707fe836c80b0deab83fe7743a683c88489a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:16 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:16 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:46:16 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:16 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:16 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:16 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbe88b35c8a00ec3bc79dd4909697496c000f13ab4d6fc4bf35b1ac8b214a54`  
		Last Modified: Mon, 22 Jun 2026 19:46:25 GMT  
		Size: 6.5 MB (6453164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32abab4338fe85a3a979fc0b6778c88ef609606420c071a3673e000f39f2753`  
		Last Modified: Mon, 22 Jun 2026 19:46:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.1-alpine` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:0966c1a39587a1a4d7ac80ccfbdba5f282dab50a7a84393ea8eb7b77bb6a28f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.8 KB (627791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f55fe1fd2faca2d5273f39b11cc50ad39c6c246258007fce6ef803db01ac96d`

```dockerfile
```

-	Layers:
	-	`sha256:74c907c2356d48291b7b5e33281a164b786c701bc9b485c6d1d4d849bc034d96`  
		Last Modified: Mon, 22 Jun 2026 19:46:25 GMT  
		Size: 605.6 KB (605573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eebc69820299f4a53de570c9877db46998254729af41ab08f1252f5db1de13e8`  
		Last Modified: Mon, 22 Jun 2026 19:46:25 GMT  
		Size: 22.2 KB (22218 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:2.1.2-alpine`

```console
$ docker pull eclipse-mosquitto@sha256:6f8d8a947c506f8a2290ec65cd4bd2bc7cb4d43fb5f6271f861cb013e2ef9797
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

### `eclipse-mosquitto:2.1.2-alpine` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:6dba0f1b2795ddcbe0d41bdfb8b8d56a423acca23ccde4342a4652be54639b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9981691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4725ea7590a578122675b1fdd242b94e5034885cfd0806045b25d700f5498ef5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:22 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:22 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:46:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386c64987679d3a8eaf9cc7d3698f3eda684e6126e8e0c50d4227add3552dc0b`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 6.1 MB (6136992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7cd47effe2f8c6a3d95385e470bd130bb232d0bc17a62da9d7962b34886f19`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.1.2-alpine` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:28c23f41929a7d171cd45d545b9388d0c9c629b893166e8a226c83ddce7b3d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.2 KB (627240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33542d63a1f237f0c21a384aa74f6bdf4e34d7c0f064d66eed04a871b6113478`

```dockerfile
```

-	Layers:
	-	`sha256:1917087cd3ac440379e06509ee4c2d6bd615681f4587a17f7444166c5ced4a69`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 605.0 KB (605022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f21e3636ba56436b5c6693d1018a7b61ddc9aa844105dd5e972352684f435719`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 22.2 KB (22218 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.1.2-alpine` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:da1de5d1a79d3032bee7127ed865bdbbe28d4ccc873cb334b7374277969cdd1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9642561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920d66bc8fbdfe05a3e40b8b02708647d7ad499e1d37857fd3ae1dc8ae4525fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:45:51 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:45:51 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:45:51 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:45:51 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:45:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:45:51 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:45:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:45:51 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453bacc80cbfdee4cc74a32087e8e19a6f269f7f39e6e444da5f408563657c0f`  
		Last Modified: Mon, 22 Jun 2026 19:45:55 GMT  
		Size: 6.1 MB (6089689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff7fb832e4d610a3298cdf645f4fd6eaaec0cece3e502ca7d31f4d1337a4fbe`  
		Last Modified: Mon, 22 Jun 2026 19:45:55 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.1.2-alpine` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:08d00d301f81a6c5d7eaae2fb85d9d0d457711cc15bbbdcd6d1029a39efadfd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 KB (22091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35a496ffcb07a95eedd2b0d1f484fdc653b67620f94021852c9c5a650f0d432`

```dockerfile
```

-	Layers:
	-	`sha256:be7999ce14dfc4dd8517c750c784f7c13382fd880933d403bb3a44d26b2fc822`  
		Last Modified: Mon, 22 Jun 2026 19:45:55 GMT  
		Size: 22.1 KB (22091 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.1.2-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:0cb9dcf861ada0efab0266b43a4e4c702c36df838a7b979c2820dc28bb61c5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10226398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db28dca6f113dc87797b9249d12841dc7877d1b31e8557d227785d9b832ff14`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:48 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:48 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:46:48 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:48 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:48 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:48 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8350ffc995a75ba3206aa4a315d75892c420a016b753a979c07dd3fc2f16c57`  
		Last Modified: Mon, 22 Jun 2026 19:46:54 GMT  
		Size: 6.0 MB (6044262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9176f981295ab62b1887ca5ed64e4d334ede3b22b5166cb76fc67e31a6abc98`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.1.2-alpine` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:46052b16b866868944158e91bbb792a6d496d04db9504523463a2f79a60db409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.0 KB (627975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93be1b726b3c16953c649a12dd9f0909098dc1037c667a2ba651112471180317`

```dockerfile
```

-	Layers:
	-	`sha256:7ccae809eccc5745ac1c839eb2d76b9fda108dea322cd508d9601a62947725d1`  
		Last Modified: Mon, 22 Jun 2026 19:46:54 GMT  
		Size: 605.6 KB (605642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:541f93da26ff0f69327c0ed923f7501f7fee41bcfc9e90534e63ca58efeee5db`  
		Last Modified: Mon, 22 Jun 2026 19:46:54 GMT  
		Size: 22.3 KB (22333 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.1.2-alpine` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:823a31d1ff413eda08b28ca557cfd13b585f13c3be294d6060ca5382ed329d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9833954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68250bf500236f1564e50ab5653d3449378e608daee25acfba0b69b5eb39cfe7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:03 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:03 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:46:03 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:03 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:03 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:03 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:03 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852582a4bb7b08bd18cce391c6dbf56c1cd9f5de2dda856b1c8504c6a21d433b`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 6.2 MB (6165688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a0b0392f2fb034eb43303fdeedc88881cc4ee9421396ba3122346f84ae0029`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.1.2-alpine` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:754444afb1844e80392fd4c5fc1421e8ef88f489bb2e898e50b619b6ea9f9e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.2 KB (627173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affcc33d5d770e8612897f32779a58d08a59555e975e943cee4c28541112ad9a`

```dockerfile
```

-	Layers:
	-	`sha256:9a8c0ab0b7a4a335e42fbd54c2a0d8c1f0dc21461b3fddac8a01ae595fc35a0f`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 605.0 KB (604992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17fa1b88eea5daf2377d8be2e0c9005e27efe364ba849dbf5bcbafe4652823af`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 22.2 KB (22181 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.1.2-alpine` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:5d49fb510e4d9895cc5dab57844c4c68579f5ba129b66854817376b903f29d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10257976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13160a70226f38c269d243a067a9587147f898fbce4c0199d737c6bf24077d04`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:50:56 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:50:56 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:50:56 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:50:56 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:50:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:50:57 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:50:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:50:57 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618cdef066c6a9a09b0c2a4aee15349a04cd31177d3997fafca499da8976d5ab`  
		Last Modified: Mon, 22 Jun 2026 19:51:06 GMT  
		Size: 6.4 MB (6445400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5acde757d31e48080fdfcb6e5c1bf404c71230cac28d5c03e0caf06c02a795`  
		Last Modified: Mon, 22 Jun 2026 19:51:06 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.1.2-alpine` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:e8c66806a39fb1e70b91db98208d1bc882200d6c8fa0ec0849c92724a1eb6839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.9 KB (627881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0358a54403d0468ce7c125024ae6c0c2f2f1ff41b2e4176f6b07084b24061`

```dockerfile
```

-	Layers:
	-	`sha256:94f54143d0237562f3306fbe851640841d9ce7b681f8d66b504bb129c9eb648e`  
		Last Modified: Mon, 22 Jun 2026 19:51:06 GMT  
		Size: 605.6 KB (605613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03aac17a30d49592d7421fdc30730da27b20586f56ab90a5d6f46e20b6e7be25`  
		Last Modified: Mon, 22 Jun 2026 19:51:06 GMT  
		Size: 22.3 KB (22268 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2.1.2-alpine` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:47b319153cc2ab8676f2faa8937d5fc63ea05eb6102f4c9bb1466336de1431b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10160689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c3eca1970a7cfb70768f1f8d1707fe836c80b0deab83fe7743a683c88489a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:16 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:16 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:46:16 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:16 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:16 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:16 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbe88b35c8a00ec3bc79dd4909697496c000f13ab4d6fc4bf35b1ac8b214a54`  
		Last Modified: Mon, 22 Jun 2026 19:46:25 GMT  
		Size: 6.5 MB (6453164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32abab4338fe85a3a979fc0b6778c88ef609606420c071a3673e000f39f2753`  
		Last Modified: Mon, 22 Jun 2026 19:46:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2.1.2-alpine` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:0966c1a39587a1a4d7ac80ccfbdba5f282dab50a7a84393ea8eb7b77bb6a28f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.8 KB (627791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f55fe1fd2faca2d5273f39b11cc50ad39c6c246258007fce6ef803db01ac96d`

```dockerfile
```

-	Layers:
	-	`sha256:74c907c2356d48291b7b5e33281a164b786c701bc9b485c6d1d4d849bc034d96`  
		Last Modified: Mon, 22 Jun 2026 19:46:25 GMT  
		Size: 605.6 KB (605573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eebc69820299f4a53de570c9877db46998254729af41ab08f1252f5db1de13e8`  
		Last Modified: Mon, 22 Jun 2026 19:46:25 GMT  
		Size: 22.2 KB (22218 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:alpine`

```console
$ docker pull eclipse-mosquitto@sha256:6f8d8a947c506f8a2290ec65cd4bd2bc7cb4d43fb5f6271f861cb013e2ef9797
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

### `eclipse-mosquitto:alpine` - linux; amd64

```console
$ docker pull eclipse-mosquitto@sha256:6dba0f1b2795ddcbe0d41bdfb8b8d56a423acca23ccde4342a4652be54639b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9981691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4725ea7590a578122675b1fdd242b94e5034885cfd0806045b25d700f5498ef5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:22 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:22 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:46:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386c64987679d3a8eaf9cc7d3698f3eda684e6126e8e0c50d4227add3552dc0b`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 6.1 MB (6136992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7cd47effe2f8c6a3d95385e470bd130bb232d0bc17a62da9d7962b34886f19`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:alpine` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:28c23f41929a7d171cd45d545b9388d0c9c629b893166e8a226c83ddce7b3d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.2 KB (627240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33542d63a1f237f0c21a384aa74f6bdf4e34d7c0f064d66eed04a871b6113478`

```dockerfile
```

-	Layers:
	-	`sha256:1917087cd3ac440379e06509ee4c2d6bd615681f4587a17f7444166c5ced4a69`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 605.0 KB (605022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f21e3636ba56436b5c6693d1018a7b61ddc9aa844105dd5e972352684f435719`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 22.2 KB (22218 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:alpine` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:da1de5d1a79d3032bee7127ed865bdbbe28d4ccc873cb334b7374277969cdd1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9642561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920d66bc8fbdfe05a3e40b8b02708647d7ad499e1d37857fd3ae1dc8ae4525fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:45:51 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:45:51 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:45:51 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:45:51 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:45:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:45:51 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:45:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:45:51 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453bacc80cbfdee4cc74a32087e8e19a6f269f7f39e6e444da5f408563657c0f`  
		Last Modified: Mon, 22 Jun 2026 19:45:55 GMT  
		Size: 6.1 MB (6089689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff7fb832e4d610a3298cdf645f4fd6eaaec0cece3e502ca7d31f4d1337a4fbe`  
		Last Modified: Mon, 22 Jun 2026 19:45:55 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:alpine` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:08d00d301f81a6c5d7eaae2fb85d9d0d457711cc15bbbdcd6d1029a39efadfd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 KB (22091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35a496ffcb07a95eedd2b0d1f484fdc653b67620f94021852c9c5a650f0d432`

```dockerfile
```

-	Layers:
	-	`sha256:be7999ce14dfc4dd8517c750c784f7c13382fd880933d403bb3a44d26b2fc822`  
		Last Modified: Mon, 22 Jun 2026 19:45:55 GMT  
		Size: 22.1 KB (22091 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:0cb9dcf861ada0efab0266b43a4e4c702c36df838a7b979c2820dc28bb61c5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10226398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db28dca6f113dc87797b9249d12841dc7877d1b31e8557d227785d9b832ff14`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:48 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:48 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:46:48 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:48 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:48 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:48 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8350ffc995a75ba3206aa4a315d75892c420a016b753a979c07dd3fc2f16c57`  
		Last Modified: Mon, 22 Jun 2026 19:46:54 GMT  
		Size: 6.0 MB (6044262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9176f981295ab62b1887ca5ed64e4d334ede3b22b5166cb76fc67e31a6abc98`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:alpine` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:46052b16b866868944158e91bbb792a6d496d04db9504523463a2f79a60db409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.0 KB (627975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93be1b726b3c16953c649a12dd9f0909098dc1037c667a2ba651112471180317`

```dockerfile
```

-	Layers:
	-	`sha256:7ccae809eccc5745ac1c839eb2d76b9fda108dea322cd508d9601a62947725d1`  
		Last Modified: Mon, 22 Jun 2026 19:46:54 GMT  
		Size: 605.6 KB (605642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:541f93da26ff0f69327c0ed923f7501f7fee41bcfc9e90534e63ca58efeee5db`  
		Last Modified: Mon, 22 Jun 2026 19:46:54 GMT  
		Size: 22.3 KB (22333 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:alpine` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:823a31d1ff413eda08b28ca557cfd13b585f13c3be294d6060ca5382ed329d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9833954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68250bf500236f1564e50ab5653d3449378e608daee25acfba0b69b5eb39cfe7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:03 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:03 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:46:03 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:03 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:03 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:03 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:03 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852582a4bb7b08bd18cce391c6dbf56c1cd9f5de2dda856b1c8504c6a21d433b`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 6.2 MB (6165688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a0b0392f2fb034eb43303fdeedc88881cc4ee9421396ba3122346f84ae0029`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:alpine` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:754444afb1844e80392fd4c5fc1421e8ef88f489bb2e898e50b619b6ea9f9e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.2 KB (627173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affcc33d5d770e8612897f32779a58d08a59555e975e943cee4c28541112ad9a`

```dockerfile
```

-	Layers:
	-	`sha256:9a8c0ab0b7a4a335e42fbd54c2a0d8c1f0dc21461b3fddac8a01ae595fc35a0f`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 605.0 KB (604992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17fa1b88eea5daf2377d8be2e0c9005e27efe364ba849dbf5bcbafe4652823af`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 22.2 KB (22181 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:alpine` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:5d49fb510e4d9895cc5dab57844c4c68579f5ba129b66854817376b903f29d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10257976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13160a70226f38c269d243a067a9587147f898fbce4c0199d737c6bf24077d04`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:50:56 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:50:56 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:50:56 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:50:56 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:50:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:50:57 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:50:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:50:57 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618cdef066c6a9a09b0c2a4aee15349a04cd31177d3997fafca499da8976d5ab`  
		Last Modified: Mon, 22 Jun 2026 19:51:06 GMT  
		Size: 6.4 MB (6445400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5acde757d31e48080fdfcb6e5c1bf404c71230cac28d5c03e0caf06c02a795`  
		Last Modified: Mon, 22 Jun 2026 19:51:06 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:alpine` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:e8c66806a39fb1e70b91db98208d1bc882200d6c8fa0ec0849c92724a1eb6839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.9 KB (627881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0358a54403d0468ce7c125024ae6c0c2f2f1ff41b2e4176f6b07084b24061`

```dockerfile
```

-	Layers:
	-	`sha256:94f54143d0237562f3306fbe851640841d9ce7b681f8d66b504bb129c9eb648e`  
		Last Modified: Mon, 22 Jun 2026 19:51:06 GMT  
		Size: 605.6 KB (605613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03aac17a30d49592d7421fdc30730da27b20586f56ab90a5d6f46e20b6e7be25`  
		Last Modified: Mon, 22 Jun 2026 19:51:06 GMT  
		Size: 22.3 KB (22268 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:alpine` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:47b319153cc2ab8676f2faa8937d5fc63ea05eb6102f4c9bb1466336de1431b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10160689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c3eca1970a7cfb70768f1f8d1707fe836c80b0deab83fe7743a683c88489a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:16 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:16 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:46:16 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:16 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:16 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:16 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbe88b35c8a00ec3bc79dd4909697496c000f13ab4d6fc4bf35b1ac8b214a54`  
		Last Modified: Mon, 22 Jun 2026 19:46:25 GMT  
		Size: 6.5 MB (6453164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32abab4338fe85a3a979fc0b6778c88ef609606420c071a3673e000f39f2753`  
		Last Modified: Mon, 22 Jun 2026 19:46:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:alpine` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:0966c1a39587a1a4d7ac80ccfbdba5f282dab50a7a84393ea8eb7b77bb6a28f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.8 KB (627791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f55fe1fd2faca2d5273f39b11cc50ad39c6c246258007fce6ef803db01ac96d`

```dockerfile
```

-	Layers:
	-	`sha256:74c907c2356d48291b7b5e33281a164b786c701bc9b485c6d1d4d849bc034d96`  
		Last Modified: Mon, 22 Jun 2026 19:46:25 GMT  
		Size: 605.6 KB (605573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eebc69820299f4a53de570c9877db46998254729af41ab08f1252f5db1de13e8`  
		Last Modified: Mon, 22 Jun 2026 19:46:25 GMT  
		Size: 22.2 KB (22218 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:latest`

```console
$ docker pull eclipse-mosquitto@sha256:6f8d8a947c506f8a2290ec65cd4bd2bc7cb4d43fb5f6271f861cb013e2ef9797
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
$ docker pull eclipse-mosquitto@sha256:6dba0f1b2795ddcbe0d41bdfb8b8d56a423acca23ccde4342a4652be54639b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9981691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4725ea7590a578122675b1fdd242b94e5034885cfd0806045b25d700f5498ef5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:22 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:22 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:46:22 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:22 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:22 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:22 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386c64987679d3a8eaf9cc7d3698f3eda684e6126e8e0c50d4227add3552dc0b`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 6.1 MB (6136992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7cd47effe2f8c6a3d95385e470bd130bb232d0bc17a62da9d7962b34886f19`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:28c23f41929a7d171cd45d545b9388d0c9c629b893166e8a226c83ddce7b3d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.2 KB (627240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33542d63a1f237f0c21a384aa74f6bdf4e34d7c0f064d66eed04a871b6113478`

```dockerfile
```

-	Layers:
	-	`sha256:1917087cd3ac440379e06509ee4c2d6bd615681f4587a17f7444166c5ced4a69`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 605.0 KB (605022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f21e3636ba56436b5c6693d1018a7b61ddc9aa844105dd5e972352684f435719`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 22.2 KB (22218 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:latest` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:da1de5d1a79d3032bee7127ed865bdbbe28d4ccc873cb334b7374277969cdd1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9642561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920d66bc8fbdfe05a3e40b8b02708647d7ad499e1d37857fd3ae1dc8ae4525fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:45:51 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:45:51 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:45:51 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:45:51 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:45:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:45:51 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:45:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:45:51 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453bacc80cbfdee4cc74a32087e8e19a6f269f7f39e6e444da5f408563657c0f`  
		Last Modified: Mon, 22 Jun 2026 19:45:55 GMT  
		Size: 6.1 MB (6089689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff7fb832e4d610a3298cdf645f4fd6eaaec0cece3e502ca7d31f4d1337a4fbe`  
		Last Modified: Mon, 22 Jun 2026 19:45:55 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:08d00d301f81a6c5d7eaae2fb85d9d0d457711cc15bbbdcd6d1029a39efadfd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 KB (22091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35a496ffcb07a95eedd2b0d1f484fdc653b67620f94021852c9c5a650f0d432`

```dockerfile
```

-	Layers:
	-	`sha256:be7999ce14dfc4dd8517c750c784f7c13382fd880933d403bb3a44d26b2fc822`  
		Last Modified: Mon, 22 Jun 2026 19:45:55 GMT  
		Size: 22.1 KB (22091 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:latest` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:0cb9dcf861ada0efab0266b43a4e4c702c36df838a7b979c2820dc28bb61c5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10226398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db28dca6f113dc87797b9249d12841dc7877d1b31e8557d227785d9b832ff14`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:48 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:48 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:46:48 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:48 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:48 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:48 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8350ffc995a75ba3206aa4a315d75892c420a016b753a979c07dd3fc2f16c57`  
		Last Modified: Mon, 22 Jun 2026 19:46:54 GMT  
		Size: 6.0 MB (6044262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9176f981295ab62b1887ca5ed64e4d334ede3b22b5166cb76fc67e31a6abc98`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:46052b16b866868944158e91bbb792a6d496d04db9504523463a2f79a60db409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.0 KB (627975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93be1b726b3c16953c649a12dd9f0909098dc1037c667a2ba651112471180317`

```dockerfile
```

-	Layers:
	-	`sha256:7ccae809eccc5745ac1c839eb2d76b9fda108dea322cd508d9601a62947725d1`  
		Last Modified: Mon, 22 Jun 2026 19:46:54 GMT  
		Size: 605.6 KB (605642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:541f93da26ff0f69327c0ed923f7501f7fee41bcfc9e90534e63ca58efeee5db`  
		Last Modified: Mon, 22 Jun 2026 19:46:54 GMT  
		Size: 22.3 KB (22333 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:latest` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:823a31d1ff413eda08b28ca557cfd13b585f13c3be294d6060ca5382ed329d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9833954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68250bf500236f1564e50ab5653d3449378e608daee25acfba0b69b5eb39cfe7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:03 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:03 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:46:03 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:03 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:03 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:03 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:03 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852582a4bb7b08bd18cce391c6dbf56c1cd9f5de2dda856b1c8504c6a21d433b`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 6.2 MB (6165688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a0b0392f2fb034eb43303fdeedc88881cc4ee9421396ba3122346f84ae0029`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:754444afb1844e80392fd4c5fc1421e8ef88f489bb2e898e50b619b6ea9f9e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.2 KB (627173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affcc33d5d770e8612897f32779a58d08a59555e975e943cee4c28541112ad9a`

```dockerfile
```

-	Layers:
	-	`sha256:9a8c0ab0b7a4a335e42fbd54c2a0d8c1f0dc21461b3fddac8a01ae595fc35a0f`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 605.0 KB (604992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17fa1b88eea5daf2377d8be2e0c9005e27efe364ba849dbf5bcbafe4652823af`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 22.2 KB (22181 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:latest` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:5d49fb510e4d9895cc5dab57844c4c68579f5ba129b66854817376b903f29d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10257976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13160a70226f38c269d243a067a9587147f898fbce4c0199d737c6bf24077d04`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:50:56 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:50:56 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:50:56 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:50:56 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:50:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:50:57 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:50:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:50:57 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618cdef066c6a9a09b0c2a4aee15349a04cd31177d3997fafca499da8976d5ab`  
		Last Modified: Mon, 22 Jun 2026 19:51:06 GMT  
		Size: 6.4 MB (6445400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5acde757d31e48080fdfcb6e5c1bf404c71230cac28d5c03e0caf06c02a795`  
		Last Modified: Mon, 22 Jun 2026 19:51:06 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:e8c66806a39fb1e70b91db98208d1bc882200d6c8fa0ec0849c92724a1eb6839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.9 KB (627881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0358a54403d0468ce7c125024ae6c0c2f2f1ff41b2e4176f6b07084b24061`

```dockerfile
```

-	Layers:
	-	`sha256:94f54143d0237562f3306fbe851640841d9ce7b681f8d66b504bb129c9eb648e`  
		Last Modified: Mon, 22 Jun 2026 19:51:06 GMT  
		Size: 605.6 KB (605613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03aac17a30d49592d7421fdc30730da27b20586f56ab90a5d6f46e20b6e7be25`  
		Last Modified: Mon, 22 Jun 2026 19:51:06 GMT  
		Size: 22.3 KB (22268 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:latest` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:47b319153cc2ab8676f2faa8937d5fc63ea05eb6102f4c9bb1466336de1431b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10160689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c3eca1970a7cfb70768f1f8d1707fe836c80b0deab83fe7743a683c88489a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:16 GMT
ENV VERSION=2.1.2 DOWNLOAD_SHA256=fd905380691ac65ea5a93779e8214941829e3d6e038d5edff9eac5fd74cbed02 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:16 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.1.2
# Mon, 22 Jun 2026 19:46:16 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         argon2-dev         build-base         cjson-dev         cmake         gnupg         libedit-dev         libmicrohttpd-dev         linux-headers         openssl-dev         sqlite-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build -DHTTP_API_DIR=\\\"/usr/share/mosquitto/dashboard\\\""         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/apps/mosquitto_signal/mosquitto_signal /usr/bin/mosquitto_signal &&     install -s -m755 /build/mosq/plugins/acl-file/mosquitto_acl_file.so /usr/lib/mosquitto_acl_file.so &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -s -m755 /build/mosq/plugins/password-file/mosquitto_password_file.so /usr/lib/mosquitto_password_file.so &&     install -s -m755 /build/mosq/plugins/persist-sqlite/mosquitto_persist_sqlite.so /usr/lib/mosquitto_persist_sqlite.so &&     install -s -m755 /build/mosq/plugins/sparkplug-aware/mosquitto_sparkplug_aware.so /usr/lib/mosquitto_sparkplug_aware.so &&     install -m644 /build/mosq/docker/2.1-alpine/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -m644 /build/mosq/docker/2.1-ubuntu/mosquitto.conf /mosquitto-no-auth.conf &&     install -d /usr/share/mosquitto &&     cp -r /build/mosq/dashboard/src /usr/share/mosquitto/dashboard &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         argon2-libs         ca-certificates         cjson         libedit         libmicrohttpd         sqlite-libs         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:16 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:16 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:16 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbe88b35c8a00ec3bc79dd4909697496c000f13ab4d6fc4bf35b1ac8b214a54`  
		Last Modified: Mon, 22 Jun 2026 19:46:25 GMT  
		Size: 6.5 MB (6453164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32abab4338fe85a3a979fc0b6778c88ef609606420c071a3673e000f39f2753`  
		Last Modified: Mon, 22 Jun 2026 19:46:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:latest` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:0966c1a39587a1a4d7ac80ccfbdba5f282dab50a7a84393ea8eb7b77bb6a28f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.8 KB (627791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f55fe1fd2faca2d5273f39b11cc50ad39c6c246258007fce6ef803db01ac96d`

```dockerfile
```

-	Layers:
	-	`sha256:74c907c2356d48291b7b5e33281a164b786c701bc9b485c6d1d4d849bc034d96`  
		Last Modified: Mon, 22 Jun 2026 19:46:25 GMT  
		Size: 605.6 KB (605573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eebc69820299f4a53de570c9877db46998254729af41ab08f1252f5db1de13e8`  
		Last Modified: Mon, 22 Jun 2026 19:46:25 GMT  
		Size: 22.2 KB (22218 bytes)  
		MIME: application/vnd.in-toto+json

## `eclipse-mosquitto:openssl`

```console
$ docker pull eclipse-mosquitto@sha256:212f89e1eaeb2c322d6441b64396e3346026674db8fa9c27beac293405c32b3c
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
$ docker pull eclipse-mosquitto@sha256:54c90ecc78645241b6aa272b2a5ac8fc20b0eaf02cc4dd431c0cc8d2fd4447dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4798168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a0bdfcbd9b7a86b36127cb81f54e1afd2019f12f39033458df405a027c03e3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:25 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:25 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:25 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:25 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:25 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:25 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:25 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abed10bdc2db7d274c50a4cf806f9566ba42ebfb000d0ffec9862fb098172ac8`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 953.4 KB (953378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a59d45fdd7a384bfb589d8b7f75f69a4ba3b8845a2a0a0e3b4f395c91920d`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:f6bc1b7a0f2d741ef94b00d3d3109c9920758ff8243031e2094b4483d229f951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.6 KB (559620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80077ef00de7f51499306941eeb1c247056b29b7e9834d164fd208422bb0b7e`

```dockerfile
```

-	Layers:
	-	`sha256:cab0c25086b76b1712462412d962835f93734826d0f9cfc402468651aeac6cd7`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 539.7 KB (539722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13c30b9ce05e160fa660946a7e0be9211d6b614cc4144f73183d0d2f11c59ffd`  
		Last Modified: Mon, 22 Jun 2026 19:46:30 GMT  
		Size: 19.9 KB (19898 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:ddc6b11126fa606c4c1ba423a81ee51d2a5b07850c826355ee887ec6a873595f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4477726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60518e191159aa7f3ae234717b5b433e386b86069706876dc76355a64208499`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:45:53 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:45:53 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:45:53 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:45:53 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:45:53 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:45:53 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:45:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:45:53 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5bb9f7317cb1da71f85f62c209f1a302e6e2db9874abc40f14f08bb3ca51af`  
		Last Modified: Mon, 22 Jun 2026 19:45:57 GMT  
		Size: 924.8 KB (924762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179bffd599cea7ee712fcc9c8839562b01da6679cbfbf6d8e9181d58b441818b`  
		Last Modified: Mon, 22 Jun 2026 19:45:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:931aa3591a6745e21dbc60ddf88b1a14823e6d2da6c693b785e5424df5eb68a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbde73b387797107508fdea5f1f32bca05e2142b2063f86d0ae61155edffa664`

```dockerfile
```

-	Layers:
	-	`sha256:d582e92c2f7f154acde5bc9854bc93b9e1d785714f6b36b1d59a14e71a42a7ca`  
		Last Modified: Mon, 22 Jun 2026 19:45:57 GMT  
		Size: 19.8 KB (19779 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:823a8067cf2bb107250a26273b676c41bad11d009563725cae6827915182b6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fef2509a20f85341b1e5c4dd7864e1a4a15fba155b88afa025cbcd5b5611ce9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:58 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:58 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:58 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:58 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:58 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:58 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:58 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0ccfd3e7f198cb156c08ebfede0b1ac31c2e14d52897d7d38e0e47c832262a`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 952.9 KB (952918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf955ac443407760ad9c5b9e49b0b02ce123f0454f49d30a3da4a3fdb273b02`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:63cb223452e0d8dcccc0b484fcb752b54e079d4ea3782f95f7eb5e6566ecc50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.2 KB (559178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36eecea909bb485b58dc89b27f12e35afe8d885e66c7c6c74d2e64b2ba344583`

```dockerfile
```

-	Layers:
	-	`sha256:d0f53279c5fe22e98785439b0c674fdcb28ea743fda8c64becbe2eb5fbab80de`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 539.2 KB (539152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71cc56f198b718130f94d7be737a4b3f7c3853c5b8177f474eba0da069f0e43b`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 20.0 KB (20026 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:b35f5d5a4b7d48f99ff3da4095df17c3d1bdd109f988521a56e5727ac1a03221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4667013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698f9df0edb9197ffa085a50219bf6716622db889be70762077b2208f497b03c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:14 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:14 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:14 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e371fb2091bd005a8c10df16cbf331318c7cd510c16fc7eacfa4e0b73e8829b`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 998.7 KB (998654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7990a82e14d5db48cb51fa0eeea8e840d0bf653de1e7a511be5b7ea5498d14b4`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:3adb5fc84d1a4ec39fdf90d7fd33b39339febc88028d6e1ebccce51d905f1e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.5 KB (559543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4496ba50b795bf21ef6da808dae1428a8017996b0f46bcc3612af62f0800e3d0`

```dockerfile
```

-	Layers:
	-	`sha256:d4beb820ff3734973163d15b174a43020e9553cccba838c1baeb48d90fff0485`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 539.7 KB (539687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be1b408f71832cb70a583ae9a070b6f66545fd2dd4c610720d4aab960c26840d`  
		Last Modified: Mon, 22 Jun 2026 19:46:19 GMT  
		Size: 19.9 KB (19856 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:42a2d20b7a2f9cd6d6de77c77cc28c0366f0a00a8e906b9516f5cc5434a0ad00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4850442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffc8a7066412f2c4b9dfa9fdfd16194b16dd912707d2c41161eb91ae062b381`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:51:54 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:51:54 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:51:54 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:51:54 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:51:55 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:51:55 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:51:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:51:55 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f43b806acd6e3376d7e9cdd47929717155662b6fac68ad61fc7ac0b2588f54e`  
		Last Modified: Mon, 22 Jun 2026 19:52:06 GMT  
		Size: 1.0 MB (1037774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad3fff5188760e18873d93d9d1dee307d9a074baffebf30cb95c80d0a57e170`  
		Last Modified: Mon, 22 Jun 2026 19:52:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:f0109e498fd903cc279d128151b7e4d3b4831d24d275bae5ae453b970a27302d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.1 KB (559073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7f18c58f65e26927c71739a3a5bce42f07205ae24bd73b7816b8534e93f32f`

```dockerfile
```

-	Layers:
	-	`sha256:210eb8c11173e7894356744b073f8c177d002ba08590e27c8ef676831cd8d220`  
		Last Modified: Mon, 22 Jun 2026 19:52:05 GMT  
		Size: 539.1 KB (539117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69bcee047f8db3db8bb831dae9e117417d7ad28e38559d21c5e8fa0050265cce`  
		Last Modified: Mon, 22 Jun 2026 19:52:05 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:openssl` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:2fbbe1880a616caf41786ac6f859672630b92583fb65ef99df081d1c8d08ee84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ec81e53a587efde5d8b12de7c52bcf143c0e2792abc2fd42be969533f955ee`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:45 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Mon, 22 Jun 2026 19:46:45 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Mon, 22 Jun 2026 19:46:45 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Mon, 22 Jun 2026 19:46:45 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Mon, 22 Jun 2026 19:46:45 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Mon, 22 Jun 2026 19:46:45 GMT
EXPOSE map[1883/tcp:{}]
# Mon, 22 Jun 2026 19:46:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:45 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26686a72838fb7d2ad73890a6d2ffd473d327de49376e0ceabd4541e4b319e92`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 980.3 KB (980301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0c73fe985dae6773fb042a636b35bd152cea4582e64e6164159dad6706459a`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:6e10004ca4d6cb1b33ec9db2c44c67e909ee3de58612b188cf560ee361f3388f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.0 KB (558969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b314313ca8e8616fcc4dcaf0873c99e4a66b2ebcd1db747891dbcdb80f9ab732`

```dockerfile
```

-	Layers:
	-	`sha256:0f1d0eacb44f2b78b81bdd84c04a62bb3e1c54d9e1303b0a7ab061699d679a28`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 539.1 KB (539071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35fa2e10b46228cc77da09d20158b0af1b330c10e8cfe16d5ca1dbf2a4920863`  
		Last Modified: Mon, 22 Jun 2026 19:46:53 GMT  
		Size: 19.9 KB (19898 bytes)  
		MIME: application/vnd.in-toto+json
