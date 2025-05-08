## `eclipse-temurin:21-jdk-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:2cb1938e5350b68e139848c06dd910335c90c3373b0e8ea005ec34cbea68e153
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jdk-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:aa6c2fa73db636789d67e1d96d20e224602ac21a22b9795752ed89d19136afbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.2 MB (182156382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d53ffbb1ce6fd6541e78141fd51b7316bbc184d8ae3d91c621fd928b736bfc`
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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='76dbb5152f15e509a5fc965936b2b912f806bb977853ab028c362c5340b1c4e9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.7_6.tar.gz';          ;;        x86_64)          ESUM='79ecc4b213d21ae5c389bea13c6ed23ca4804a45b7b076983356c28105580013';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:33789da93344c5e1792da30d9a6201f8a99e3ebfa85118f1704ee006ae7191cc`  
		Last Modified: Thu, 08 May 2025 17:05:34 GMT  
		Size: 20.7 MB (20670516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eeee6191536431da42f8e89e5f4b28ba8f7b0e6509b8d95cf95683edb7441f`  
		Last Modified: Thu, 08 May 2025 19:23:19 GMT  
		Size: 157.9 MB (157856559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59aa0412022c98a2c167e25e2e72f12328eb745f09a90498ab08c2190e5b4ed`  
		Last Modified: Thu, 08 May 2025 17:05:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b569345297c1c19003fe6a46cef1211acc8cf66042ab47db8ce8eafa757da`  
		Last Modified: Thu, 08 May 2025 17:05:33 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e0f34ba3e99ae2743a3cffb6ce735d812a1e87667d7f24f9e96079e2c2e33154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1088295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8139901b8e1d7b7d5d54edcecc001a4ea8b3c3c28afbd3aaaa32c3140d5180`

```dockerfile
```

-	Layers:
	-	`sha256:c032562e286c3b95db79f977100cd28788993abe163ad67dcbbe4b8ee44d0bb3`  
		Last Modified: Wed, 23 Apr 2025 16:32:02 GMT  
		Size: 1.1 MB (1067846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc26a899b1db0af27ab3ba8b7367b3ab918835ecca71da871f09235559b27946`  
		Last Modified: Wed, 23 Apr 2025 16:32:02 GMT  
		Size: 20.4 KB (20449 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-alpine-3.20` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:ba36378aae9d9b5d0ede37744cdaececec383b816cbfa4b17a1bd40b3493b850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (180999799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bedb9276a6f2cc9a1fb71e5f01abe4faf44fd9dba87c27de3068de71fab93bcc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='76dbb5152f15e509a5fc965936b2b912f806bb977853ab028c362c5340b1c4e9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.7_6.tar.gz';          ;;        x86_64)          ESUM='79ecc4b213d21ae5c389bea13c6ed23ca4804a45b7b076983356c28105580013';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96809c65b6feb2ccad22cb977f4f7d6f7c15255ddfdcc2d8c53d4b3495147ce5`  
		Last Modified: Wed, 23 Apr 2025 16:39:40 GMT  
		Size: 21.0 MB (21048653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c488fe7e8ebbc726507923e4a6c6bcb36981cb81067c248717ee06c79992bf`  
		Last Modified: Wed, 23 Apr 2025 16:39:44 GMT  
		Size: 155.9 MB (155857571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8778263a60feee70c47443b600857bb0f0596b373978007d5f8c52236be1c6b`  
		Last Modified: Wed, 23 Apr 2025 16:39:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57db443888e3c96ddce3fc7b35b5ee1a5f6f655638a2ef4f84e7346ea019ef51`  
		Last Modified: Wed, 23 Apr 2025 16:39:39 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a4747eecaf94757d306ae731b2bc9f850a12525edde51f6ccfb68995895a61fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1192936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b00c0bf27ad03ecb8adff55fac160ce77451f3839b3bef357e881fb4b1b618`

```dockerfile
```

-	Layers:
	-	`sha256:b7a727b2b1ef3f49321c88fc74ae691a83c2ccc10602b697c8119dd8f7527eff`  
		Last Modified: Wed, 23 Apr 2025 16:39:39 GMT  
		Size: 1.2 MB (1172366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:742e4ad556a7df2e7fcb6d22092e70308076f23bfb3742f93ecab4ee6122e68d`  
		Last Modified: Wed, 23 Apr 2025 16:39:38 GMT  
		Size: 20.6 KB (20570 bytes)  
		MIME: application/vnd.in-toto+json
