## `eclipse-temurin:11-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:e763ac96a3deaada17b197bc253f3b8cbda63ed5bad91f93b1428001c9148a2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:878b7d9c348a100e71e1fe4ef7ab851f0366eb6bf467ce83f5f771ccb0bb6f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160196875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c1e2a7b3f46834dbb9abb0e220a8f2c9f16896db55439a93c4a6ce8417fb31`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:57:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:13 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:57:13 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 17:57:18 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='c7b58655ffde7b5e6fce4a32fdcd21be5745b3bb64ee2bc723fcf55eae720ebe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:57:19 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:57:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974df0e0eb67fd6fa35aefb5620f2d84f013b3e0b11b4c38737099a86303d60b`  
		Last Modified: Sat, 08 Nov 2025 17:57:33 GMT  
		Size: 16.3 MB (16289652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b829ff2503da3447968682832d5a69ea284ba1d657a4f8e58d4c799c8c348e`  
		Last Modified: Wed, 07 Jan 2026 18:59:59 GMT  
		Size: 140.1 MB (140102363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a217f6eeaed3b8ab583b886e8495c9ca0664bb21717752475480bc1453bb07d2`  
		Last Modified: Wed, 07 Jan 2026 18:59:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea81eccc49bc152ef173ac2d3a5ac97163278251fda36902720deae5aa454418`  
		Last Modified: Wed, 07 Jan 2026 18:59:54 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8db41665b2ecbb938fb8a65bf3013278c192d492fd2de872ad7c06ed6736cea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1022204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71bd1f42b9151d3999eb925cfba8895bad1abdd52d2ca64c3ba546f23830fdbd`

```dockerfile
```

-	Layers:
	-	`sha256:0d075c5aba7483b4209b5afa15876f7cb1fb305aed573a4365bc4b21a0287f9c`  
		Last Modified: Sat, 08 Nov 2025 17:57:33 GMT  
		Size: 1.0 MB (1002038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a54db5119cf5a518050a99d673a02aa317dd98cd6707b556978ab476f46a6174`  
		Last Modified: Sat, 08 Nov 2025 17:57:33 GMT  
		Size: 20.2 KB (20166 bytes)  
		MIME: application/vnd.in-toto+json
