## `eclipse-temurin:25-jdk-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:dfcc9a0b4cf16576ad4150509f6b1d45a92ae36eeb967c1c058c867f2990c442
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:25-jdk-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:54a6130328a3cf3fb3ff1dd4970df1dbcb63c45673bc6a46028b22eb8ced0e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109548482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ba8de8e7fba9bf3566fa1b14120c738d592ee9bbfd8cfc874bd6585721b811`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:24:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Apr 2026 00:24:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:24:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 17 Apr 2026 00:24:24 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 17 Apr 2026 00:24:24 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Fri, 17 Apr 2026 00:24:31 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e8d928fb018eabb31a148ebadaa5a5ec69273e6562afede21c426960a6a67143';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='961f13ba0ee1e18c41c50ab642361e4283dee5e7947a48ed6a72c8a661d0cca0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Fri, 17 Apr 2026 00:24:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 17 Apr 2026 00:24:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:24:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 17 Apr 2026 00:24:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9a4304e8a48fba448c7a88826137d13f50667177bb3bcc862310dd4d7beb20`  
		Last Modified: Fri, 17 Apr 2026 00:24:45 GMT  
		Size: 14.2 MB (14247169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d335f0e3c9de4832ee9bd559cdfcad73a4c0e3ad7571642db9a86b5ab0ff1c`  
		Last Modified: Fri, 17 Apr 2026 00:24:47 GMT  
		Size: 91.5 MB (91490714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bd0418708606afcc79fa59eef24ee848d1329d356f289e078fe66da74e2be3`  
		Last Modified: Fri, 17 Apr 2026 00:24:45 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abc48544626a870fb8f5b5d8c5c17a3d7d9596d850af0d8377fbe3ba7f534d0`  
		Last Modified: Fri, 17 Apr 2026 00:24:37 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:396af9f7db4da6c079b799e0d6af39def7ddfdec02c489a80beceee812fc1a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **985.2 KB (985209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e41519529984d87d006b600c3fb41a018f8a9623cd08cb504f218ad18df155`

```dockerfile
```

-	Layers:
	-	`sha256:12855e2a0a38e2427c577b130e27f4108ef1658308ee4b4810f0f816320dc9b4`  
		Last Modified: Fri, 17 Apr 2026 00:24:45 GMT  
		Size: 964.7 KB (964675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1ce3c6f1b967c3a5e6f6366219ecd1418b87e6d7b677cce1112b3bd2078ea4c`  
		Last Modified: Fri, 17 Apr 2026 00:24:45 GMT  
		Size: 20.5 KB (20534 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-alpine-3.22` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:4c3fbfe5bf33a9a1b0227c1342cdd3b69d58c26283819c0409c69db9bbbad757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.9 MB (108924732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c97a7714e720edcabb1044e13d3300999c6164a60a9037ac695eaf4f8ea1fc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:26:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Apr 2026 00:26:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:26:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 17 Apr 2026 00:26:06 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 17 Apr 2026 00:26:06 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Fri, 17 Apr 2026 00:26:14 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e8d928fb018eabb31a148ebadaa5a5ec69273e6562afede21c426960a6a67143';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='961f13ba0ee1e18c41c50ab642361e4283dee5e7947a48ed6a72c8a661d0cca0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Fri, 17 Apr 2026 00:26:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 17 Apr 2026 00:26:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:26:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 17 Apr 2026 00:26:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d8fcd891a93a00f3b5f8b048d31b82516b21bf6ff15987219dc8c7e5208c93`  
		Last Modified: Fri, 17 Apr 2026 00:26:31 GMT  
		Size: 14.4 MB (14352370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5c7a4461efc9a3d1b9429a254bfce22ea89759f990309833cda3d16bf9ccba`  
		Last Modified: Fri, 17 Apr 2026 00:26:36 GMT  
		Size: 90.4 MB (90428057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba91b29868067cc750d1b3aba718a6f93f99fb3af1f13adfa09f477cef99fe35`  
		Last Modified: Fri, 17 Apr 2026 00:26:30 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58050e5f61216745c5c8e31417c5030770f1f950f21d0175a55f79bdbf1cf9b4`  
		Last Modified: Fri, 17 Apr 2026 00:26:30 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:dfd03276753bc3c0fea70b95dd6baf775d5503f0b3f6f6be78bffe3fc595f607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1135331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9155f343ead411b1fa56a42cb92811b28d54c77e64a0daa7f154df4eb47a021`

```dockerfile
```

-	Layers:
	-	`sha256:43fecfd4dd0f3fa6520ca36a0d2d62bbfc6685c7cc1cb75e51d96e4ed6ffc59a`  
		Last Modified: Fri, 17 Apr 2026 00:26:30 GMT  
		Size: 1.1 MB (1114674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5efe47651794364f1ef464b424422c57d4279fb854c69df8fb6ebcb93f115490`  
		Last Modified: Fri, 17 Apr 2026 00:26:30 GMT  
		Size: 20.7 KB (20657 bytes)  
		MIME: application/vnd.in-toto+json
