## `eclipse-temurin:8u442-b06-jre-jammy`

```console
$ docker pull eclipse-temurin@sha256:ae02650a3b13893ef6dd7a08cbe880e53d6748d0eb3d70bd4a889b74ba58e6a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8u442-b06-jre-jammy` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:4d2b7b290dc8b08d242dc90c8bdd80c5993a0dcb9bb08e571b9d1337f3a41ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87560134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d1fb66a2fca305f8370318cc5b7688243da0122e4bf66c2a7065127328fa26`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='055c47c5c1dfe8c9c135d87fed7a3745c17374618bc8d5acb9316d1b812c0e6d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebc2b7ae30a79a2123735c5dc35348c02905872b61a9d70ea637affbbe437e`  
		Last Modified: Wed, 09 Apr 2025 01:15:20 GMT  
		Size: 16.1 MB (16146033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0287b9521316d6ebf213ba3111d833da2447046a953c2073efdc4b93f11072bc`  
		Last Modified: Wed, 09 Apr 2025 01:15:21 GMT  
		Size: 41.9 MB (41879326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146f3a2016063e689e24ae453dfd69a556dad3e68603ba8bb31ca4191e5edc43`  
		Last Modified: Wed, 09 Apr 2025 01:15:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178c66146304559b5b9efecae9527ce1f43c667d4c402a00cdf5e15a8ffe3cbd`  
		Last Modified: Wed, 09 Apr 2025 01:15:20 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:535b16d4bde78e7fbb3447685ef1a28a9761e9c066e7f444c50cbfd132daa590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982b9abc760726fd72dd61062e15625024b78afc22ec4642edb53a231e5e5a8e`

```dockerfile
```

-	Layers:
	-	`sha256:8fe12b354abb62c009342ca7ae587d0a7fd41dcdcca6676e3b2d2da0c70f9a5b`  
		Last Modified: Wed, 09 Apr 2025 01:15:20 GMT  
		Size: 3.7 MB (3738101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:002c2aeec200b5399c9297507f086523d08f1398742ddc4798628d4ba5c9f084`  
		Last Modified: Wed, 09 Apr 2025 01:15:20 GMT  
		Size: 22.0 KB (21959 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u442-b06-jre-jammy` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:52da22ed1471b0b7c59fa9fb3e30430be297ba6b8400eccff890b617bef85cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81888255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1044fa2fabca7cc6dcf4096b3a2903dc85ef47724da99c16b8896c12388062d4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:11 GMT
ADD file:7e9e4d557a66a31de2a39930803dbe849ba710af36b4731e9cbc856f55c10018 in / 
# Sun, 26 Jan 2025 05:32:11 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='055c47c5c1dfe8c9c135d87fed7a3745c17374618bc8d5acb9316d1b812c0e6d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:eeaefd3c974dfe1d5e1b8eb1929496ae7befe434399b37e601701f6d012e3169`  
		Last Modified: Sun, 26 Jan 2025 07:02:14 GMT  
		Size: 26.6 MB (26639267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5bc4151aca7aee0d14e2a39ddf8e63d8b5b3ab7cb73799f25458d2cec004ff`  
		Last Modified: Tue, 04 Feb 2025 10:51:37 GMT  
		Size: 15.9 MB (15885582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf93834145627b76f3f94a98c01446d9229c00c4e5ef889c4cb9720469c14cdf`  
		Last Modified: Tue, 04 Feb 2025 10:53:28 GMT  
		Size: 39.4 MB (39360998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6eb49bd297dddc9b52e601ff89f9ea80485ee18ceac5b62f67a145b017dde30`  
		Last Modified: Tue, 04 Feb 2025 10:53:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8c725478888af5247a510987e41955b02421efdcbf03247ceeff0d81500bfe`  
		Last Modified: Tue, 04 Feb 2025 10:53:27 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8d19498ba1f2c7922d8c771d0582d1b6a26c6c6518f1f3416e00e1321ba8fdab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3763280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e10c286f0265cef93ba71303b03240f964b4b1cdcbbfb7337b99cb66e1d83a9`

```dockerfile
```

-	Layers:
	-	`sha256:d893b4ab5d1498e6a94cc0166fa01109ec609ab6843114794ecc736882dc7199`  
		Last Modified: Tue, 04 Feb 2025 10:53:28 GMT  
		Size: 3.7 MB (3741234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f074560afeb8a7f2ddd5244405ac22fa255b4bfdf0762f240ef00b37658f890`  
		Last Modified: Tue, 04 Feb 2025 10:53:27 GMT  
		Size: 22.0 KB (22046 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u442-b06-jre-jammy` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:6650aad24c0e3e17fe39357b4facc2f0e6f49c016946067e4459d79b7298bf3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84292250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b81794ecfab2cda381ac5d628bea51cbbc3d5c6cb45d5eba235ac5f6a09ed8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='055c47c5c1dfe8c9c135d87fed7a3745c17374618bc8d5acb9316d1b812c0e6d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00937d13923579bb64d2d8eaadc6ab4c6f4eca98da664f5a5852304064566a3`  
		Last Modified: Tue, 04 Feb 2025 09:18:10 GMT  
		Size: 40.9 MB (40879014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd22d609dd99f68521bf885e0ed4ad842d1ab831187ca9c69fe7ba1f9a1d199`  
		Last Modified: Tue, 04 Feb 2025 09:18:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0f86d6e638a989f23991c816082c67f62f1c05a3b5501e686cf2e3987c1a47`  
		Last Modified: Tue, 04 Feb 2025 09:18:08 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7661f99eed35add54eba576d1ef7ffa87f133b9acbbfef6a59277d1ac96e1f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3757938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618f64328a018abf275ce0ec1e6f4ba62f055ca0f77af0bc49224c1b6c72081f`

```dockerfile
```

-	Layers:
	-	`sha256:b9696572ec4b33cc560732764b21c5aa82096fd34cc626437042752e94e1048a`  
		Last Modified: Tue, 04 Feb 2025 09:18:08 GMT  
		Size: 3.7 MB (3735869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b2cb1084b602636cd6f5d8ba381365a6222189cc3009478d61df7de007b303`  
		Last Modified: Tue, 04 Feb 2025 09:18:08 GMT  
		Size: 22.1 KB (22069 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u442-b06-jre-jammy` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:1d714cd58ffd0743a8a17ba18af0f2dc3c3e81fcd73cab5bc7852da970edb33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93327296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe4b9cc25a6cf5e49357115c374f7058bdba7c073124e3f6c800ce544c47bd2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='055c47c5c1dfe8c9c135d87fed7a3745c17374618bc8d5acb9316d1b812c0e6d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8c38ec2b4ee36ca93f19596eb065a396e648e65a58e52db4e0886be5ded596`  
		Last Modified: Wed, 09 Apr 2025 04:35:13 GMT  
		Size: 17.6 MB (17617815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62699f117465a850c7c812b4277991594415532feeee93e0a63f932cce7c9a37`  
		Last Modified: Wed, 09 Apr 2025 04:37:53 GMT  
		Size: 41.3 MB (41264374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740260084550584a4e88414d2e99b9b749f71ab6a604ded072da44b36f42b161`  
		Last Modified: Wed, 09 Apr 2025 04:37:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2146e7d897f1d40099a0b13c6c6ebb985f892ae9dc35e9f2a767927140b5e871`  
		Last Modified: Wed, 09 Apr 2025 04:37:51 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:501dd06c92104d2ce81e16f4f2a26906bc04acd54635a2711a67a6948333ef36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9997ea161ae3d1cfdc0eba3f8b3ffffb0c6c0f3c7d36078da14fdd6de51a69`

```dockerfile
```

-	Layers:
	-	`sha256:3aeac8f8ca33e59efcad31b153677933e922ef3c12009418faa2e1c477b2edba`  
		Last Modified: Wed, 09 Apr 2025 04:37:52 GMT  
		Size: 3.7 MB (3742714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bb5d9184216fdb909a66295433d7b35d213f65e032baa153da751555f56221b`  
		Last Modified: Wed, 09 Apr 2025 04:37:51 GMT  
		Size: 22.0 KB (21996 bytes)  
		MIME: application/vnd.in-toto+json
