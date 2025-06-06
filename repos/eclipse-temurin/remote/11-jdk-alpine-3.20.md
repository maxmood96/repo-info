## `eclipse-temurin:11-jdk-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:b9c69c6b9bdd7b5169e3371cc41e13156b8a72b8ed923ff9711b809710fdbb19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jdk-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:ecea92df6c53b8a0ff5d0b69d8a2d2e91fce459c3a69290ff76f7ee1b0160c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160455226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7bdc26b8ac46fbbd95fcbfc450f90f5ea86db0f001353d8152e4843333a6f9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='5defac0a735690b04bc1bbe9d7e3b5faed6dd54f946858349ba114394f8fb386';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f747efddd95ea6660a628fdaa1212e7b1d2619c85558d9375d4baa6cc696bc`  
		Last Modified: Fri, 09 May 2025 12:29:35 GMT  
		Size: 16.0 MB (16025916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20b3378bb09b92cc165ac80fd50ae776b2e9869e7b01179ff92a36a6df992b6`  
		Last Modified: Fri, 09 May 2025 12:29:44 GMT  
		Size: 140.8 MB (140800006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d588f757ad04fc5c3dfa490ef06d284c48f338eb3608da7f83f91a6c0613ed32`  
		Last Modified: Fri, 09 May 2025 12:29:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881f8e1531ad37ac2ffebb68457ec3af357c536feb22d2a86af5a70ada600404`  
		Last Modified: Fri, 09 May 2025 12:29:34 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b076a6adb2a77b809a7f35973d05106d37fde48fb7a10be1daf4dfc34cff0040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1007181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727717bfdded74110213418989160fba6aa3ca2b201094b4333e92692a04bee1`

```dockerfile
```

-	Layers:
	-	`sha256:be5439fb1eff25372f803bc375cdbc737f48b8f98160c11f68ed9cbc9754f6c1`  
		Last Modified: Fri, 06 Jun 2025 02:13:14 GMT  
		Size: 988.0 KB (987968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e4d1d571957ce3b68a7f8413b2276d83c53b55f6b9a5cc12f91f12272279d43`  
		Last Modified: Fri, 06 Jun 2025 02:13:15 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json
