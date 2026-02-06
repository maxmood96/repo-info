## `eclipse-temurin:25-jdk-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:fb9c47f1870b3c014dcec393ff65aa4c193303b582f89399d6dab125bd6ebdb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:25-jdk-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e29db8bdebbb40d5dba683da436c150c8b79de16bff106929702af43694e0680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109544303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab036d9f997d9e2d4d09cd925b4974a87649f6691ce28d893d81162712fdd74`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:20:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:20:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:20:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:20:35 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:20:35 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:20:42 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e8d928fb018eabb31a148ebadaa5a5ec69273e6562afede21c426960a6a67143';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='961f13ba0ee1e18c41c50ab642361e4283dee5e7947a48ed6a72c8a661d0cca0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 05 Feb 2026 22:20:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:20:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:20:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:20:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cef8c07632c7232fce24c50d8b3f78d558647eb596ddc8bc47c220d8be4b0f2`  
		Last Modified: Thu, 05 Feb 2026 22:20:57 GMT  
		Size: 14.2 MB (14246476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502b2d4a8166984ca8ac7bb8b48be9a6b6ad327467982c5b0e002dbaf93cce3a`  
		Last Modified: Thu, 05 Feb 2026 22:20:58 GMT  
		Size: 91.5 MB (91490543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e905fa06555d1fa0c6884a1ac1fca9410f3bdc9f2bd21854474f60d4ed5471c`  
		Last Modified: Thu, 05 Feb 2026 22:20:56 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e334bc02a6d6619304b34b0aada0ca7fe84c7a44e7897ff083aa4873d3d4054f`  
		Last Modified: Thu, 05 Feb 2026 22:20:56 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c970003aa1d9ef767efb4f98992da44fd13219218b2d6a6297c2aac680350a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **985.9 KB (985897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe24445ba90ca1ad077a88d3d6732a4c0c6ba7efd01a37d9ed4edb9acfbce64`

```dockerfile
```

-	Layers:
	-	`sha256:c25b6ab789bb0085d59da435a026b21bc3d351912903687f631a95bde0aa1bf4`  
		Last Modified: Thu, 05 Feb 2026 22:20:56 GMT  
		Size: 965.4 KB (965362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3de526b4cdf9411d6f2d0ce253a7692cc45f581d420a3bb200b1dac5f96638dd`  
		Last Modified: Thu, 05 Feb 2026 22:20:56 GMT  
		Size: 20.5 KB (20535 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-alpine-3.22` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:5759f1e4423ea0ef6b13edeee257126754093dffd0ecc24e23bddfaac7506fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.9 MB (108922256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4c8ede3c307b940648477cbc6f1e3a7afcb00a11d77e6a2bfa4df74d2157e6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:19:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:19:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:19:28 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:19:28 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:19:35 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e8d928fb018eabb31a148ebadaa5a5ec69273e6562afede21c426960a6a67143';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='961f13ba0ee1e18c41c50ab642361e4283dee5e7947a48ed6a72c8a661d0cca0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 05 Feb 2026 22:19:36 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:19:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:19:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:19:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2531051470470c5a1a99610edbab7b15e7861ee195c10f7975f9dc6b46eed9ae`  
		Last Modified: Thu, 05 Feb 2026 22:19:51 GMT  
		Size: 14.4 MB (14352199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06afa35c9b098521c32501a973717bc4c2b7ac5c10f76fe43d80cd80a71165c7`  
		Last Modified: Thu, 05 Feb 2026 22:19:53 GMT  
		Size: 90.4 MB (90428129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ec104ae0a9cd30752b79b84cfa742dc4b8b9e282b7d660a93a4848f5b4dc59`  
		Last Modified: Thu, 05 Feb 2026 22:19:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bbbc84ac1ed06f73f1e36c165d3ea712ed084345ad42e0dfaf27b66b1ee77b`  
		Last Modified: Thu, 05 Feb 2026 22:19:51 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:881696b97847fa915072b8149900fd71f9abef24c7c3f3032c543f8eaaa49d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1136018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29bcabe28ddc12d263de7c20c98e291f37da722157eb156291ee4d0e66f71e88`

```dockerfile
```

-	Layers:
	-	`sha256:37b383af6bf39d2d414a58c0a7fa76061c67650f5f55ed40b328d514dcb13b8c`  
		Last Modified: Thu, 05 Feb 2026 22:19:51 GMT  
		Size: 1.1 MB (1115361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2804f278dfd5f9cb7d596a06c0285dd06a914b47212c5488fe6e61f20a7f340c`  
		Last Modified: Thu, 05 Feb 2026 22:19:50 GMT  
		Size: 20.7 KB (20657 bytes)  
		MIME: application/vnd.in-toto+json
