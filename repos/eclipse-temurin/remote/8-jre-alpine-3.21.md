## `eclipse-temurin:8-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:2bb8193b57d71e9600266e385c79536892989d8abde9183e098e4558e49e8807
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d0ee34be858514bc00b09cdfb7e3f6d858858e8ee3cb239a58cc15fff3ba3009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62077399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf83eca5982b5ca147476e8c08699be5316565cf1f136baa31e22d0f67b6bcc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:13:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:13:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:13:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:13:10 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:13:10 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:14:10 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='c1b64ab1d2c96ac0fd89c60377396cc4457f954ee7ce931f3a0e547f701e6595';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:14:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:14:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:14:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa92feb649a4fb8d7d1fb59d25aefc768eaf769fc0146084a45700bdcf747740`  
		Last Modified: Thu, 05 Feb 2026 22:13:26 GMT  
		Size: 16.2 MB (16174652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b56685e3410dbbc0a6e0ecaae226b10c6a7f4dc0319d4b0bbe4f99a6970df05`  
		Last Modified: Thu, 05 Feb 2026 22:14:21 GMT  
		Size: 42.3 MB (42256596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7481b2eb6a1ad9722914827fa74cac67af5427ebde45065641cdfb212c74248c`  
		Last Modified: Thu, 05 Feb 2026 22:14:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a6c873438ab36e111d6ae84fd1ef9dd7912053836ba773c48805e5faf1c66c`  
		Last Modified: Thu, 05 Feb 2026 22:14:20 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e668a6f6797535db1c24176ba65f36a15d79295b648f92e3a31112499d5ab49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.7 KB (945661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2000ac449e90d54bd28b14e39e797d1929d8862dd9000b6defac02c2554d6d2b`

```dockerfile
```

-	Layers:
	-	`sha256:66678c81829d0468379e07055b4bac9e62af3f5db9ecdf800ba639add460d61f`  
		Last Modified: Thu, 05 Feb 2026 22:14:19 GMT  
		Size: 927.5 KB (927474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:811c8ef0f1db64a1396349445dba13f42fbf80a2ea41e543eb67748503ca3269`  
		Last Modified: Thu, 05 Feb 2026 22:14:20 GMT  
		Size: 18.2 KB (18187 bytes)  
		MIME: application/vnd.in-toto+json
