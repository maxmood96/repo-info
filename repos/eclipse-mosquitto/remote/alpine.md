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
