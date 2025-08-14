## `eclipse-temurin:17-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:6a4c08c0125d587116b8b4402b73e9d1dd3a1b3cfecc8af6c55a67e378b79ca3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d3cf704da989710e58b5e4f58b709257c346d2a92421c7a8159d5b60d8c3ee4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168431985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabe576a8e7d20d74fcf8aa11838d00f3f2fe7a8c8a2d3453e0e0f50c4479f78`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='2e83ac152fb315db0d667761f2120b64504800f641a513044e834a1a41f29bc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9090e086acaf5ff2144d8bf4beb01a4656ef6fb0a515c1944ad9b433815e67`  
		Last Modified: Mon, 04 Aug 2025 19:11:30 GMT  
		Size: 20.9 MB (20942685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8738e994d69cdf5c12f3ed52f534ccb6338c6c11e6afc80f1983ada90f39a3`  
		Last Modified: Mon, 04 Aug 2025 21:16:45 GMT  
		Size: 143.8 MB (143849322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165031445dc40ffe66a39645b37c6ec6893e26598e8733ddbc98c6e5f5d76d98`  
		Last Modified: Mon, 04 Aug 2025 19:11:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ad722bed61bc77d1d5b5149c4909bca01ae3d92c63bdbc6d1bdce96fcad352`  
		Last Modified: Mon, 04 Aug 2025 19:11:20 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:442b694853c91b999f5df386b92605c57ce96c7607123ef24328bff2b299bfbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1118259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68a5f346fc459300d52fd5387c3713c3248ced5d90fc9af644d550ddd73f3a7`

```dockerfile
```

-	Layers:
	-	`sha256:6835ca95b971b504e0c3ca5d0c14dcc530f5fb72d1a077b73c29e537fcda3cb7`  
		Last Modified: Mon, 04 Aug 2025 21:16:33 GMT  
		Size: 1.1 MB (1098605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da40e0659738e511ba2d921c2ae1f37a37169fdcbcdae3d5a06f6f315b983872`  
		Last Modified: Mon, 04 Aug 2025 21:16:34 GMT  
		Size: 19.7 KB (19654 bytes)  
		MIME: application/vnd.in-toto+json
