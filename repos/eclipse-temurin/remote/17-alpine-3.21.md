## `eclipse-temurin:17-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:7a234db051cecf40070dd9e71d93b6dc68457a21f7820f3225c0e63549c9eb02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:3b0f1879bbd8d2b180d5c89514bd74859f4da925a7e71db00616afc2dd3b8ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169358408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaed5fa451f5332167977130feca4d84df7757ef932168e845c7b746eb075b92`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:17:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:17:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:17:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:17:06 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:17:06 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 05 Feb 2026 22:17:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='3246fb1834d21c22ed717db9f8ba3f07e0f562bbeeebdc44a7499d5eb6df47bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:17:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:17:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:17:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:17:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acae424759de4516cca72198cc9bf78e47217aa2a04fd41da1836173c06d893`  
		Last Modified: Thu, 05 Feb 2026 22:17:28 GMT  
		Size: 20.9 MB (20949982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db91cb32bc772d6f7fa4272d517f3a9bd35db0b756290342286cb803194da166`  
		Last Modified: Thu, 05 Feb 2026 22:17:30 GMT  
		Size: 144.8 MB (144762273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2789367b7ae5ea9817db534473fb07cc267fd1f6e0dbfc0e5a39dfe514a0ccb4`  
		Last Modified: Thu, 05 Feb 2026 22:17:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9814d1b2085ef65a9f6d69e4efddd0d2d62c792e7438e60baba1f93c9e117697`  
		Last Modified: Thu, 05 Feb 2026 22:17:27 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f939629fcf91dc67532f82185fdb2e5a3ee472212d910f089098015d9d659315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1122083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8d2378372e8e55d9d17e1d0a45e8c5d3980be749c193dfc632ac32171f7ae8`

```dockerfile
```

-	Layers:
	-	`sha256:b21a59350ee89ebfe6cd086a909516d34cd1e66baf73d4521ba147e082a24b9f`  
		Last Modified: Thu, 05 Feb 2026 22:17:27 GMT  
		Size: 1.1 MB (1102472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01703cb4be38f5c2dc590717f6ff100b033538163c6a586adc104fea2f4fb20f`  
		Last Modified: Thu, 05 Feb 2026 22:17:26 GMT  
		Size: 19.6 KB (19611 bytes)  
		MIME: application/vnd.in-toto+json
