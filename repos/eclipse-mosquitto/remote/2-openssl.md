## `eclipse-mosquitto:2-openssl`

```console
$ docker pull eclipse-mosquitto@sha256:6852da90a65dfff7aa3a1c8b249e92bb83c17ea8bbcce56bedff8707332a1a29
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
$ docker pull eclipse-mosquitto@sha256:10b94cc46bad579465e423e6979709f9cee9a778fca9ee0ee12c8590711eec6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4866294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f982bd980b9739fe55e5f637fa716555b765621c541adcdd033b139a94d70e09`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 17:54:43 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Thu, 05 Feb 2026 17:54:43 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Thu, 05 Feb 2026 17:54:43 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Thu, 05 Feb 2026 17:54:43 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Thu, 05 Feb 2026 17:54:43 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Thu, 05 Feb 2026 17:54:43 GMT
EXPOSE map[1883/tcp:{}]
# Thu, 05 Feb 2026 17:54:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 17:54:43 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1b9700f7054a1b784fecc93db3f15464633fdf78a5cbd305febeb61545a20b`  
		Last Modified: Thu, 05 Feb 2026 17:54:48 GMT  
		Size: 1.0 MB (1004104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af742c5b8dd7ef4e251288bc96d21c242cabe87f395a3b07262008619fb1b4cd`  
		Last Modified: Thu, 05 Feb 2026 17:54:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:3d8427a9075c1083b8ad6bd9507a51598797a34b9543d2739adb78b2df9e4808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.5 KB (578469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af5da09a47e3026a4e9305d90566414645b433f7b7646b313a4f8b5c5d43802`

```dockerfile
```

-	Layers:
	-	`sha256:56d31fc23121fd27360edbe9461be64aed634aaf9e2cf38783b2e6dc0493d429`  
		Last Modified: Thu, 05 Feb 2026 17:54:47 GMT  
		Size: 558.6 KB (558569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0523736a0d65286fbb576ca77681ff3b12807c4641e84bec9838c56c0af8f9be`  
		Last Modified: Thu, 05 Feb 2026 17:54:48 GMT  
		Size: 19.9 KB (19900 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2-openssl` - linux; arm variant v6

```console
$ docker pull eclipse-mosquitto@sha256:f50f166481e3fd5f6aebd676b0150bd889cc2504cdff3520eb05f4d883bec5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4546424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63cf38893cf4697d36405890ec9dc5bc2285bd2adbd9d2cb47e26ee54edb382c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 17:56:40 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Thu, 05 Feb 2026 17:56:40 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Thu, 05 Feb 2026 17:56:40 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Thu, 05 Feb 2026 17:56:40 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Thu, 05 Feb 2026 17:56:40 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Thu, 05 Feb 2026 17:56:40 GMT
EXPOSE map[1883/tcp:{}]
# Thu, 05 Feb 2026 17:56:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 17:56:40 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0b65ea4643f4403f3ea953ffb68c247236a38c4a877af711fcb7b7f9a96375`  
		Last Modified: Thu, 05 Feb 2026 17:56:44 GMT  
		Size: 976.2 KB (976233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d195c6f9736f216e7d997b35f7c92314571d8a2a2e4642b8a9aa5194249cc2`  
		Last Modified: Thu, 05 Feb 2026 17:56:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:497f3a404a43b94127cf79b0cab58e01609d0af38c6eb9db716b0af286f903dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b34e81186db08e2b5af83d168f3b2c951332ccb00edbdc792a525360b34eba3`

```dockerfile
```

-	Layers:
	-	`sha256:701769c681dcc27321a91fb6e187e367e06bde22dd2450233c60b6f04b18df5d`  
		Last Modified: Thu, 05 Feb 2026 17:56:44 GMT  
		Size: 19.8 KB (19779 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2-openssl` - linux; arm64 variant v8

```console
$ docker pull eclipse-mosquitto@sha256:092b2db87a7b65b9e8f70652c94267a3fa4f062048368ba3794327a1e5626d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5201073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8768a43ef7fd48767606827c79290870281c8d443a9a1821d6fd09074f3b636`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 17:54:54 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Thu, 05 Feb 2026 17:54:54 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Thu, 05 Feb 2026 17:54:54 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Thu, 05 Feb 2026 17:54:54 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Thu, 05 Feb 2026 17:54:54 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Thu, 05 Feb 2026 17:54:54 GMT
EXPOSE map[1883/tcp:{}]
# Thu, 05 Feb 2026 17:54:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 17:54:54 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabeb73a27a81b54b09d1f1f1a7fa3a623710f33b198c36715f91bd7249ce406`  
		Last Modified: Thu, 05 Feb 2026 17:54:59 GMT  
		Size: 1.0 MB (1003613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236a1c18a67ceffce175a689d4ceb5392e29f8a958ed6fd299c415a3d6b4013e`  
		Last Modified: Thu, 05 Feb 2026 17:54:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:4207dee325f5cc9a78ba554f5fce627aad02ce2a119d46ab68f483eb4f1329fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.0 KB (578027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e06913a7c1cc49a9d33eea3eae1bc3411deac5b18be493f0d39507217ebf47`

```dockerfile
```

-	Layers:
	-	`sha256:0d21f781a87f656e62220b272df6f9d0d3bed4a200234daa106c0b37790ef22a`  
		Last Modified: Thu, 05 Feb 2026 17:54:59 GMT  
		Size: 558.0 KB (557999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e703652d14c0d532c6a40f8975225dd6d88e09bc65ead2724175baa2455508`  
		Last Modified: Thu, 05 Feb 2026 17:54:59 GMT  
		Size: 20.0 KB (20028 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2-openssl` - linux; 386

```console
$ docker pull eclipse-mosquitto@sha256:76b7afc957708ffed13d183f39c4760b8da5e899529f666bb17d10d1615cc8ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4737518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bbf455e383b31fea4469f56e317e95840db6cef5a662b5aadf7ab55ba42203`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 17:56:13 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Thu, 05 Feb 2026 17:56:13 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Thu, 05 Feb 2026 17:56:13 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Thu, 05 Feb 2026 17:56:13 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Thu, 05 Feb 2026 17:56:13 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Thu, 05 Feb 2026 17:56:13 GMT
EXPOSE map[1883/tcp:{}]
# Thu, 05 Feb 2026 17:56:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 17:56:13 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0294a6fe8cf568af298a5b70f38de734c16140f2bffbf90a2bd885acc609be`  
		Last Modified: Thu, 05 Feb 2026 17:56:18 GMT  
		Size: 1.1 MB (1050151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4efdb725f7e6a6a4455c37d8e2073426952662017f707ef52309d27233ffb4`  
		Last Modified: Thu, 05 Feb 2026 17:56:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:4a71d24317fe1ee357deb7e264b9db1378d3d93841d2a8ba10ee694cd4134269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.4 KB (578392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6af0f9d86dabcd4b3ae60aad240fcb0a3d14c6e9a631ee22f16847e84858c7`

```dockerfile
```

-	Layers:
	-	`sha256:a178d7aa020c2a4a7f1d9cbdadb1684300132a66519c51dcde452e1ea139b0c5`  
		Last Modified: Thu, 05 Feb 2026 17:56:18 GMT  
		Size: 558.5 KB (558534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:692c354bfd19ed4b7d787195bf251e1feac19b75e242e07b295c9aa73444c2ee`  
		Last Modified: Thu, 05 Feb 2026 17:56:18 GMT  
		Size: 19.9 KB (19858 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2-openssl` - linux; ppc64le

```console
$ docker pull eclipse-mosquitto@sha256:0fb7355975af164848c5df20e18ecd20bb7e3ba06369d00e3dc4347de4c4cbc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4918484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d173337fa7a90b627c1c5df78db4524099de6b8b7de0bd0ea5b7e5073dddaa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 17:55:03 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Thu, 05 Feb 2026 17:55:03 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Thu, 05 Feb 2026 17:55:03 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Thu, 05 Feb 2026 17:55:03 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Thu, 05 Feb 2026 17:55:05 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Thu, 05 Feb 2026 17:55:05 GMT
EXPOSE map[1883/tcp:{}]
# Thu, 05 Feb 2026 17:55:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 17:55:05 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b52729248767e648902ba56bfc030c54497f3f01e41125fb1e2b5b444362ff1`  
		Last Modified: Thu, 05 Feb 2026 17:55:15 GMT  
		Size: 1.1 MB (1088472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a3e4f4da24fa875217f578bd5e1898c9a83d2c66a43195b054b4b9625f4b09`  
		Last Modified: Thu, 05 Feb 2026 17:55:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:b224bb98f8b1484ff42eb2e8274a8a6acf9ee922fe94012baef8f518e1fa8ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.9 KB (577920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f559ae53d509c321883e9080299f862d7ed05f2dd66732554b00558b5615441`

```dockerfile
```

-	Layers:
	-	`sha256:a06d3db005a14ba9f326fc014ae40f080a7e728397d02bcc8d9e1c6ddda585bb`  
		Last Modified: Thu, 05 Feb 2026 17:55:15 GMT  
		Size: 558.0 KB (557964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12ba2b210ee94c2c12de10d03b6bde2138cc920fb4afcf1439e244dc54d1c3f`  
		Last Modified: Thu, 05 Feb 2026 17:55:15 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-mosquitto:2-openssl` - linux; s390x

```console
$ docker pull eclipse-mosquitto@sha256:ad4c680f1d441a08bbe036fdf03cfdb25ee36b4c889ffd9bc9b108e1bcb57fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4757950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6fdea098e0e65aa4d47ad071e09bd8eb152902d9e356e535e6012676a445ac7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/sbin\/mosquitto","-c","\/mosquitto\/config\/mosquitto.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 17:55:46 GMT
ENV VERSION=2.0.22 DOWNLOAD_SHA256=2f752589ef7db40260b633fbdb536e9a04b446a315138d64a7ff3c14e2de6b68 GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7
# Thu, 05 Feb 2026 17:55:46 GMT
LABEL org.opencontainers.image.authors=Roger Light <roger@atchoo.org> org.opencontainers.image.title=eclipse-mosquitto org.opencontainers.image.description=Eclipse Mosquitto MQTT Broker org.opencontainers.image.url=https://mosquitto.org/ org.opencontainers.image.documentation=https://mosquitto.org/documentation/ org.opencontainers.image.source=https://github.com/eclipse-mosquitto/mosquitto org.opencontainers.image.licenses=EPL-2.0 OR BSD-3-Clause org.opencontainers.image.version=2.0.22
# Thu, 05 Feb 2026 17:55:46 GMT
RUN set -x &&     apk --no-cache add --virtual build-deps         build-base         cmake         cjson-dev         gnupg         libwebsockets-dev         linux-headers         openssl-dev         util-linux-dev &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz -O /tmp/mosq.tar.gz &&     echo "$DOWNLOAD_SHA256  /tmp/mosq.tar.gz" | sha256sum -c - &&     wget https://mosquitto.org/files/source/mosquitto-${VERSION}.tar.gz.asc -O /tmp/mosq.tar.gz.asc &&     export GNUPGHOME="$(mktemp -d)" &&     found='';     for server in         hkps://keys.openpgp.org         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $GPG_KEYS from $server";         gpg --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$GPG_KEYS" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $GPG_KEYS" && exit 1;     gpg --batch --verify /tmp/mosq.tar.gz.asc /tmp/mosq.tar.gz &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /tmp/mosq.tar.gz.asc &&     mkdir -p /build/mosq &&     tar --strip=1 -xf /tmp/mosq.tar.gz -C /build/mosq &&     rm /tmp/mosq.tar.gz &&     make -C /build/mosq -j "$(nproc)"         CFLAGS="-Wall -O2 -I/build"         WITH_ADNS=no         WITH_DOCS=no         WITH_SHARED_LIBRARIES=yes         WITH_SRV=no         WITH_STRIP=yes         WITH_WEBSOCKETS=yes         prefix=/usr         binary &&     addgroup -S -g 1883 mosquitto 2>/dev/null &&     adduser -S -u 1883 -D -H -h /var/empty -s /sbin/nologin -G mosquitto -g mosquitto mosquitto 2>/dev/null &&     mkdir -p /mosquitto/config /mosquitto/data /mosquitto/log &&     install -d /usr/sbin/ &&     install -s -m755 /build/mosq/client/mosquitto_pub /usr/bin/mosquitto_pub &&     install -s -m755 /build/mosq/client/mosquitto_rr /usr/bin/mosquitto_rr &&     install -s -m755 /build/mosq/client/mosquitto_sub /usr/bin/mosquitto_sub &&     install -s -m644 /build/mosq/lib/libmosquitto.so.1 /usr/lib/libmosquitto.so.1 &&     install -s -m755 /build/mosq/src/mosquitto /usr/sbin/mosquitto &&     install -s -m755 /build/mosq/apps/mosquitto_ctrl/mosquitto_ctrl /usr/bin/mosquitto_ctrl &&     install -s -m755 /build/mosq/apps/mosquitto_passwd/mosquitto_passwd /usr/bin/mosquitto_passwd &&     install -s -m755 /build/mosq/plugins/dynamic-security/mosquitto_dynamic_security.so /usr/lib/mosquitto_dynamic_security.so &&     install -m644 /build/mosq/mosquitto.conf /mosquitto/config/mosquitto.conf &&     install -Dm644 /build/mosq/epl-v20 /usr/share/licenses/mosquitto/epl-v20 &&     install -Dm644 /build/mosq/edl-v10 /usr/share/licenses/mosquitto/edl-v10 &&     chown -R mosquitto:mosquitto /mosquitto &&     apk --no-cache add         ca-certificates         cjson         libwebsockets         tzdata &&     apk del build-deps &&     rm -rf /build # buildkit
# Thu, 05 Feb 2026 17:55:46 GMT
VOLUME [/mosquitto/data /mosquitto/log]
# Thu, 05 Feb 2026 17:55:46 GMT
COPY docker-entrypoint.sh mosquitto-no-auth.conf / # buildkit
# Thu, 05 Feb 2026 17:55:46 GMT
EXPOSE map[1883/tcp:{}]
# Thu, 05 Feb 2026 17:55:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 17:55:46 GMT
CMD ["/usr/sbin/mosquitto" "-c" "/mosquitto/config/mosquitto.conf"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e12c27ceec11f44ba4fd413cae23f306bdd72741bd7eb267f3009a4008a265`  
		Last Modified: Thu, 05 Feb 2026 17:55:57 GMT  
		Size: 1.0 MB (1032248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb051da8107edefa089eb415ab0ea20c72f6ed975e606cb66f2db8518ff3025`  
		Last Modified: Thu, 05 Feb 2026 17:55:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-mosquitto:2-openssl` - unknown; unknown

```console
$ docker pull eclipse-mosquitto@sha256:7198943eabe0e7748521a445edbc9d7c3d0b7b011d04061b64a2416e50b87894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.8 KB (577818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab816a212d72637c20aed3312e73e1ef2b73e5619bbf49a3a151f42b8d147e0`

```dockerfile
```

-	Layers:
	-	`sha256:df1a59e04bc9e947443764231372dcd0be74883dc44c85be78f726caa5ef7e7a`  
		Last Modified: Thu, 05 Feb 2026 17:55:57 GMT  
		Size: 557.9 KB (557918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf8d176f1ee52055e438e04d50d58d5e9ecbfc7aa820c00100e9616d943ff9b5`  
		Last Modified: Thu, 05 Feb 2026 17:55:57 GMT  
		Size: 19.9 KB (19900 bytes)  
		MIME: application/vnd.in-toto+json
