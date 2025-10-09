## `eclipse-temurin:25_36-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:791d5d532c81d02d16e93d34d8546d50a641222c2a40da5fc263c8a35ba773c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:25_36-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2e0d6ad6df7dd50ca5feaf2889591b0de4ab4a1cd13c67f36b4ddb51891bbbc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109316896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b513ba40147ffa8e772d6a0ab622f9607d117ce1bcaa35379482ba3d7c96bd8c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 25 Sep 2025 19:59:06 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='1f18ba69ca7d674724307a66928a9b80049748b4276c629450935543db2cdfb1';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25_36.tar.gz';          ;;        x86_64)          ESUM='637e47474d411ed86134f413af7d5fef4180ddb0bf556347b7e74a88cf8904c8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db03fa3ac16472a254962ebcd81ad021907bbad285d0f6cdc9a1502f80e25f71`  
		Last Modified: Wed, 08 Oct 2025 23:34:17 GMT  
		Size: 14.2 MB (14245319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a39bec576f64b4114bdea072e5b630129dd7815e2001b4fbdf0d8777eec25ab`  
		Last Modified: Wed, 08 Oct 2025 23:34:31 GMT  
		Size: 91.3 MB (91266716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c248d02cde76c58f066897343c950bf9da798d7213e690f2205a87b12de4da`  
		Last Modified: Wed, 08 Oct 2025 23:34:14 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0249b6ee0600ac5bf443cd0634e2ffa05dc60ee1940d165feab4071b10180121`  
		Last Modified: Wed, 08 Oct 2025 23:34:13 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25_36-jdk-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:587a43ed162504025c8a8fe2255f0131fe86480036edd76d0ffbafcdf6453613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **969.8 KB (969846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4e5703ddd2dd9289dd9fc4103c9e3e33a0bec98bb38aae8ff7cc1baef60e95`

```dockerfile
```

-	Layers:
	-	`sha256:133c4ce66998601449ac4d2104a05baba8d5514ee01b78adb6b333c78b3481ef`  
		Last Modified: Thu, 09 Oct 2025 00:16:56 GMT  
		Size: 948.3 KB (948340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:485dd808437d4b4f71e86a1a983491a09ab59da10c62877797536bac33e85e5a`  
		Last Modified: Thu, 09 Oct 2025 00:16:57 GMT  
		Size: 21.5 KB (21506 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25_36-jdk-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:a97c969dd1afc9336acf4d5860a812b14ffcbe4b6f79e8e8949e4ce9e91a1b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.7 MB (108663858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e64ebc12a594d8148223051e2aa57d5bf2af387fb3872c6d7b2f459a485cf8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 25 Sep 2025 19:59:06 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='1f18ba69ca7d674724307a66928a9b80049748b4276c629450935543db2cdfb1';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25_36.tar.gz';          ;;        x86_64)          ESUM='637e47474d411ed86134f413af7d5fef4180ddb0bf556347b7e74a88cf8904c8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ade06a7471c002bcf656675566f358b0a11940fe7d9e6ff2c531e329a39c893`  
		Last Modified: Wed, 08 Oct 2025 21:49:10 GMT  
		Size: 14.4 MB (14352503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f393f605afb3f2558c3e606e83caffd55f6d504cce6766329478332fa835e3`  
		Last Modified: Wed, 08 Oct 2025 21:49:13 GMT  
		Size: 90.2 MB (90170879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd42f05d849ba1bbf31d4c7de1e475760b5930603787e167ae5175e231af087`  
		Last Modified: Wed, 08 Oct 2025 21:49:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5157fd5631d15dfdd67c1e40b54fbdd30adf2eac3929ce9ac5cf21ac9c341a`  
		Last Modified: Wed, 08 Oct 2025 21:49:09 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25_36-jdk-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:68f50962521465a5cf804bf6b6f8687041acf9d6a822407adea4af5079f97997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1120037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b876d7341ab6b36ae54849a3769bb7e09818616f6ee3ed47828e9665903f5c7b`

```dockerfile
```

-	Layers:
	-	`sha256:961efc50c8c9e70c21c5c5ae71ebbf27ff60cb0bd79d64087e488586667739d2`  
		Last Modified: Wed, 08 Oct 2025 23:22:31 GMT  
		Size: 1.1 MB (1098375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d649537d39bf65f3472c892e81ccea1923b89814e127be8aeb5f2e57afffdb9f`  
		Last Modified: Wed, 08 Oct 2025 23:22:32 GMT  
		Size: 21.7 KB (21662 bytes)  
		MIME: application/vnd.in-toto+json
