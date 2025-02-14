## `eclipse-temurin:23-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:2d00ccc56113b30e804abc891c57acccdd7c619175bda8ab667ebce072a2b7e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:23-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:c5175ce144dd9cb47f40b4523061fac4eedd405c3b619a80d49d621ce98d8a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.8 MB (189839685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9d7f849b9d14a176a423eab947e341bc19b0c713086e80b842285e683b59d6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='b55c5c881a2fed17ec5a59feaa33d9263703b399d1bfae3a5eaed3f140aa4570';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='2c05c6dfea23a83fdbfaf5b03cc3cfd8d998c8069e930e0e585a39d4a99f3d99';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a8038a3635430b4356b637ba5217e43aa9092f439d625013f2586aae877ba7`  
		Last Modified: Fri, 14 Feb 2025 19:26:04 GMT  
		Size: 20.7 MB (20667778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417fce73674842da3c03bc4b7d12442e0652642c6ff060b1f00d11787ea28a3e`  
		Last Modified: Fri, 14 Feb 2025 19:26:06 GMT  
		Size: 165.5 MB (165542600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536b6638d847e4bcf24ac3a852580d2287ee2def73f04daf4003435b6d9352b0`  
		Last Modified: Fri, 14 Feb 2025 19:26:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006fbc486fe4d8f68d11ff236a1d909149390935a200bafdcc47349457461576`  
		Last Modified: Fri, 14 Feb 2025 19:26:03 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:267c0d15df783e6b006d59b7a7cf9648a62138095d2e8ba87c4833dfd112b48b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c70007e556e0c81b87afa3c3697ae49e5a15c8f397e3e9703bce868c6838f4d`

```dockerfile
```

-	Layers:
	-	`sha256:3bd975c7223532dd62b17b14e471e6bab107d595e9a11d9290ecaa641fdcaa98`  
		Last Modified: Fri, 14 Feb 2025 22:15:15 GMT  
		Size: 1.1 MB (1069127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f75ccb40cbe46ded9988a94d432bcda27222422ae1d22ac14efb4efb4022d3`  
		Last Modified: Fri, 14 Feb 2025 22:15:16 GMT  
		Size: 20.4 KB (20448 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-alpine-3.20` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:29fcce445790321a450369eec1de06472699e3ab16ef1d545ab1976a35b359b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.5 MB (188518759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14630b928750c66995e46ef157cbeec3492448a3075f6f1eaf02549e7c3c9ef8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='b55c5c881a2fed17ec5a59feaa33d9263703b399d1bfae3a5eaed3f140aa4570';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='2c05c6dfea23a83fdbfaf5b03cc3cfd8d998c8069e930e0e585a39d4a99f3d99';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b57795d9838d4ab7da718bb75c1aa894db71d000660f5159c42d40d07be61b`  
		Last Modified: Fri, 07 Feb 2025 08:23:42 GMT  
		Size: 21.0 MB (21045569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775fb9f1633c2b3c2b030315c73b798288d67d7a2fb41c078801ed6244df256`  
		Last Modified: Mon, 10 Feb 2025 10:58:15 GMT  
		Size: 163.4 MB (163380011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ec246ae6ae2360d6b0e9cd45a70a7c79aa742ab9842a68d176864104d7b196`  
		Last Modified: Mon, 10 Feb 2025 10:57:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40393c4f14ae3d0b1ad8d95d75aa4f10dbdaaf03bb4170abfa5fe39deeaad85`  
		Last Modified: Tue, 11 Feb 2025 22:22:49 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:374d34eb2a578b736c12d5de1a29735fffc29ef48192a8c1dd85033d8c830377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1193597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9eba391b07ccc6a4db88244dad18fd11180a70ea0e05f6f7c0520645e91acfc`

```dockerfile
```

-	Layers:
	-	`sha256:d57824b6732d964d858a90062aaa851352aaffe873a2d9637c64146174bd4ba7`  
		Last Modified: Fri, 14 Feb 2025 22:15:17 GMT  
		Size: 1.2 MB (1173026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5d02b406b3b5b14a75fbb2cc058bb7c0848f20b44168f227a1defdcd608a332`  
		Last Modified: Fri, 14 Feb 2025 22:15:17 GMT  
		Size: 20.6 KB (20571 bytes)  
		MIME: application/vnd.in-toto+json
