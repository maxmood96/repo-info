## `eclipse-temurin:8u432-b06-jre-focal`

```console
$ docker pull eclipse-temurin@sha256:b8878bf69a6a370847fe17a6498ed3c047dff8777ffe69650b8ea65cc892f76a
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

### `eclipse-temurin:8u432-b06-jre-focal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:393399d7779e1d9a8dd4af8b408b493e7f32b431eafc7e8ca83ef78984de363b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89654812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6c99bdfdce48981242747fedf89bc4088b880ce3ea1c6432b16e1ead016045`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='bb8c8cc575b69e68e12a213674ec2e3848baff4f1955d2973d98e67666ab94d7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='786522da4c761104dd8274c81edc90126a25acaafbbbc5da886b3fb51f33cba2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='49894dbe2f915dfad026cf7b4013118c0284e88359172499b1b25a4dac195ff1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='c573f33f9e5ba49a4838847d0d34efc9c1dc57a9ba71b926599530bbcda87f65';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd28385908e0a9e00986ebf7ea0efd3da1c43d0ca7e4bdcef3a5913b3de53ef`  
		Last Modified: Thu, 24 Oct 2024 00:56:50 GMT  
		Size: 20.3 MB (20256519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b976e3f54b1ccb59126bbebdd9dddd00f4330598a66b99a3af092c2327bcf6`  
		Last Modified: Thu, 24 Oct 2024 00:56:50 GMT  
		Size: 41.9 MB (41884825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cd7d015707d2f742c801bb7950e6cf59ad8d36e72e6a842ad68b6588973533`  
		Last Modified: Thu, 24 Oct 2024 00:56:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11584e3ad5a8fe35048b9480485aed5451d387ccba7d327b050bccb5bc0f792`  
		Last Modified: Thu, 24 Oct 2024 00:56:50 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u432-b06-jre-focal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2795908d1374a9619ef854ef944b92a99825cb19248d3289e8e987af8dea8941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3762076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb61d93dff71b73c145a30279dca29155547622ff4a28862c6beecf64d1c23d`

```dockerfile
```

-	Layers:
	-	`sha256:33f15168e94ee4ad7ef22304374349d326b19554ea920cf3cac08c1148e2f619`  
		Last Modified: Thu, 24 Oct 2024 00:56:50 GMT  
		Size: 3.7 MB (3740060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa0d3836c6ebd06cdb524e39f272bd3268aa23516988474ef30ae92fb8c8908b`  
		Last Modified: Thu, 24 Oct 2024 00:56:50 GMT  
		Size: 22.0 KB (22016 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u432-b06-jre-focal` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:94f5d82833bfbb957210cd86581a5ec33e3333326c1adf5de20dd64878f0c889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81453580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8fdc076531fdcfbb2ed0ae50c6c68a2c37e8e7778c863f0ea6deeb968470a95`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:34 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:36 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Fri, 11 Oct 2024 03:38:37 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='bb8c8cc575b69e68e12a213674ec2e3848baff4f1955d2973d98e67666ab94d7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='786522da4c761104dd8274c81edc90126a25acaafbbbc5da886b3fb51f33cba2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='49894dbe2f915dfad026cf7b4013118c0284e88359172499b1b25a4dac195ff1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='c573f33f9e5ba49a4838847d0d34efc9c1dc57a9ba71b926599530bbcda87f65';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf7dfa91dfefd2d38b8ffd98f5296dec749e2c8b186d41439b07e2e8ade5eba`  
		Last Modified: Thu, 24 Oct 2024 00:57:44 GMT  
		Size: 18.5 MB (18475795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fcfb4122c55ba8f444a6548e448147951f47a17a77f174074f653646c7caac`  
		Last Modified: Thu, 24 Oct 2024 01:02:13 GMT  
		Size: 39.4 MB (39354964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d139be951bef920b334722dfed8b29d63ea8350a5c3c277ea8dddad15ee22c`  
		Last Modified: Thu, 24 Oct 2024 01:02:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc950120cee4a57e9352b3b04180f968f437e30aa198c65ee961523550e56dc`  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u432-b06-jre-focal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:39b91cbba465ca285d919d36dd147d20e9cf2a47161db3ed651186e928bc946c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3767822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2e3613dae6c48bb5b3ef2e983c14ca4053a74872a830b712bb66a4d03d8207`

```dockerfile
```

-	Layers:
	-	`sha256:0ac6e0cd136351195535bab29a1d9bbed573533a69b6957748f7a5b95b4d3611`  
		Last Modified: Thu, 24 Oct 2024 01:02:12 GMT  
		Size: 3.7 MB (3745720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ea4b736ba7d4c5b5a6a99e194734bf482b0714bc3d0dbb5944ba96530d9c071`  
		Last Modified: Thu, 24 Oct 2024 01:02:11 GMT  
		Size: 22.1 KB (22102 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u432-b06-jre-focal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:0a49b19dde6945687c8746f9d6d9d6a18bac646760f72643896edae83a16d558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86937449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd187c0b88acae06cb9c6826f782aa9e81fef77849ff9152b5c06075e691b7c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='bb8c8cc575b69e68e12a213674ec2e3848baff4f1955d2973d98e67666ab94d7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='786522da4c761104dd8274c81edc90126a25acaafbbbc5da886b3fb51f33cba2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='49894dbe2f915dfad026cf7b4013118c0284e88359172499b1b25a4dac195ff1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='c573f33f9e5ba49a4838847d0d34efc9c1dc57a9ba71b926599530bbcda87f65';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7944fa14982850a5d6fef396e75bb75cff1a66cd0eb74db10ed75ba31d11c024`  
		Last Modified: Thu, 24 Oct 2024 00:56:58 GMT  
		Size: 20.1 MB (20093942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d7742bf75e9f548b9cad550f7d38433ceb1c73a1e2ba68509f53a8f73b77b3`  
		Last Modified: Thu, 24 Oct 2024 01:00:54 GMT  
		Size: 40.9 MB (40867269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3322a350fa3f095851250a8b23a470ffc75f358f910f7d881e545b7ed5a79776`  
		Last Modified: Thu, 24 Oct 2024 01:00:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1197c8b21b66735ccb4f40c68ac95ff7b56ef5adcd15dc645a4cb370730063`  
		Last Modified: Thu, 24 Oct 2024 01:00:53 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u432-b06-jre-focal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:dc91aaf8d3cb75c22a3c979982182e3e8731418da9ccb073a87e7988ac2eadf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3762511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42938d7d8636563b174786d768bdcebda4d1067712f65f97a9e32ea2ce8e3c3`

```dockerfile
```

-	Layers:
	-	`sha256:afc8b0a8a5c895f57890f44834fa1c6d33a176dfa9ea999d59f8e1eeea490793`  
		Last Modified: Thu, 24 Oct 2024 01:00:53 GMT  
		Size: 3.7 MB (3740385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa637461bb3fff368df701fd604e6ff64a764900e0c30b39585ef9248b7986ab`  
		Last Modified: Thu, 24 Oct 2024 01:00:53 GMT  
		Size: 22.1 KB (22126 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u432-b06-jre-focal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:4dcfe1d1327a017d3ec0744ba67d84e2f68b716dbe574364f303f5c93294e3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95758491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc86a97e86adb0b0eec951ea414d75fd62805ae0a921fed2d6a338699f3462d2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='bb8c8cc575b69e68e12a213674ec2e3848baff4f1955d2973d98e67666ab94d7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='786522da4c761104dd8274c81edc90126a25acaafbbbc5da886b3fb51f33cba2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='49894dbe2f915dfad026cf7b4013118c0284e88359172499b1b25a4dac195ff1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='c573f33f9e5ba49a4838847d0d34efc9c1dc57a9ba71b926599530bbcda87f65';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f77674583b715acfc520100d8d6868a767a5eb5d74c71bcd1f0883576efdcc`  
		Last Modified: Thu, 24 Oct 2024 00:57:23 GMT  
		Size: 22.4 MB (22419063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52e427f1c80dad050e2313825db7beed45d618448851273fcc69320ade0d493`  
		Last Modified: Thu, 24 Oct 2024 05:50:46 GMT  
		Size: 41.3 MB (41260513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196ded33e8af7a61cebd94016a7c1406db225a9af520a1f82df04b6e325c3e7b`  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065f8cca55b216add5c7ba49c3067bd34da56b4a07f8ec7e1f51dd3ecd3459ca`  
		Last Modified: Thu, 24 Oct 2024 05:50:44 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u432-b06-jre-focal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:134ae620155cbee5a2c20d35a9f2ffbfa77c5c87dcfdd94cdbd24579325ae97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3766664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a035aa2a85a5f112742f6690e51c511da22ba1963ce25f339fb409840c30482b`

```dockerfile
```

-	Layers:
	-	`sha256:ceceffdcaaff2cfcc6301a28c447e33948fef422b171e69f56882bb0a259fcb5`  
		Last Modified: Thu, 24 Oct 2024 05:50:45 GMT  
		Size: 3.7 MB (3744612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5c158d5d9baf135c03f30a0f94d3056780bd474bf1ee9fafc9910879388d528`  
		Last Modified: Thu, 24 Oct 2024 05:50:44 GMT  
		Size: 22.1 KB (22052 bytes)  
		MIME: application/vnd.in-toto+json
