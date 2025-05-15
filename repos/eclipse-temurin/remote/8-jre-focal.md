## `eclipse-temurin:8-jre-focal`

```console
$ docker pull eclipse-temurin@sha256:88b4336f24b7db1f17944858736ae3a64e0729432ae5e3284c7abfc3522fc243
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

### `eclipse-temurin:8-jre-focal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:1fafcf02cf1b88bb2a6e049f04b9e18e3d3ab6baaa638695c8eadc7f5a6dd06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89662555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c7e67381e11cd587ef6335f0b80e5b34b18c98984f1e83750a646825d0d6bb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c76f94e1b400a4da932a3f581b0788af2101819083184f40a6c76ac9b97081f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='5d0c81fd8bee49d1b9931acaecdc528fdc9393547cf5b24880445ade6b3f2384';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='6c0f29b6011d0baa46f90a572691b77ea93a45b4e5037141777a236956945c50';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='d9b523defdea8b82647726de8f62b57a19f2c64020b9ab6dbc5ae4929d0ee64e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c500d980dd4fb5da49c41d8f8b1dcb954e443cbe9f126a6f1394803c28c15b9`  
		Last Modified: Thu, 08 May 2025 17:17:07 GMT  
		Size: 20.3 MB (20260595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c3c9359f6e125d6d99589f792dfdb697412673a82f30ba0cb75833ec08b58c`  
		Last Modified: Thu, 08 May 2025 17:17:09 GMT  
		Size: 41.9 MB (41889158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c18520b525a6240fd7e5c8fddccec5e012bdca60dbb341584157225039e25a3`  
		Last Modified: Thu, 08 May 2025 17:17:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88638a10f6c19f3e6e1816cc8bce1e34ad72c65648fd3460453eef6b97caa98f`  
		Last Modified: Thu, 08 May 2025 17:17:07 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-focal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2d51070a0ea9fa1770188205a0881653eca9ea25caeaccc961ef845edb3cfdb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a7a2ba58f99541be07de50b2f51f2f22a35e86ba5b9c38595dac45ada2ae44`

```dockerfile
```

-	Layers:
	-	`sha256:d1a40ed58e89c4a8c5dd75666bc21ba2acaba565b00f6209e9e595c8152b203f`  
		Last Modified: Mon, 28 Apr 2025 20:07:41 GMT  
		Size: 3.7 MB (3738181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ffee532ce946c60e76a61e5fd42366a67a732baf8f000937e47310009ee5be8`  
		Last Modified: Mon, 28 Apr 2025 20:07:41 GMT  
		Size: 22.0 KB (21959 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-focal` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:d06e34cc6f95f5b880d91c13086f809a64e538b51ff969f872259be4494d3323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81468972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a121d8f1847939feba55a897576d3c72a0fdade98daf0fff9024ecfd3195516d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:45:56 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:45:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:45:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:45:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:45:59 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 08 Apr 2025 10:45:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c76f94e1b400a4da932a3f581b0788af2101819083184f40a6c76ac9b97081f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='5d0c81fd8bee49d1b9931acaecdc528fdc9393547cf5b24880445ade6b3f2384';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='6c0f29b6011d0baa46f90a572691b77ea93a45b4e5037141777a236956945c50';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='d9b523defdea8b82647726de8f62b57a19f2c64020b9ab6dbc5ae4929d0ee64e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Thu, 08 May 2025 17:24:17 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584dcd1f0ae60202572ceaaf1d1ff21ed62161827b256dfd50433bbcba261dfd`  
		Last Modified: Fri, 09 May 2025 00:41:39 GMT  
		Size: 18.5 MB (18478140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc943b03b74149b48d8b0a81512c130569876f25bff2e62063c49ab9a15cf47`  
		Last Modified: Mon, 28 Apr 2025 20:10:27 GMT  
		Size: 39.4 MB (39364359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8caf59dcfbb95051f77af36674b50f4e3582166982f3a52a4c5894555d66e50c`  
		Last Modified: Mon, 28 Apr 2025 20:10:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b1c4ae64b3ba6c650afff40227352c75ddb82d078f73c469f11a5b05c93242`  
		Last Modified: Mon, 28 Apr 2025 20:10:25 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-focal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:007ec4dc424074b0479f0c4f65a01b6356c0949f146a49c5b0ab56f72a718462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3765888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a197aa9784628c1a417699b2a8c171c5c76faab211f640775631c6157bf66b05`

```dockerfile
```

-	Layers:
	-	`sha256:3efff30fdc7a005c8b705ddde95161241bfd4cf9fcb124cc8a522710c3620361`  
		Last Modified: Mon, 28 Apr 2025 20:10:25 GMT  
		Size: 3.7 MB (3743842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1600b6c7d44fec53d4a08331df0028d8ca381fbddb42eeb7eb4ea903ad6b51`  
		Last Modified: Mon, 28 Apr 2025 20:10:24 GMT  
		Size: 22.0 KB (22046 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-focal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:50499b787f5d689a503c08e4c964388ca065e1e55e0b57dea5558aff1117bc8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86952212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1017693e422cc94a4f05e360bd9a671f03bd2bb73edfd5b42fdc78a28dbcd0ea`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c76f94e1b400a4da932a3f581b0788af2101819083184f40a6c76ac9b97081f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='5d0c81fd8bee49d1b9931acaecdc528fdc9393547cf5b24880445ade6b3f2384';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='6c0f29b6011d0baa46f90a572691b77ea93a45b4e5037141777a236956945c50';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='d9b523defdea8b82647726de8f62b57a19f2c64020b9ab6dbc5ae4929d0ee64e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af9d62a97be401b93c2f6eb1dc4bb4c70329ac3b300956d3867dfc020b29c3e`  
		Last Modified: Thu, 08 May 2025 17:09:10 GMT  
		Size: 20.1 MB (20092976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0e8102e7140d18a52c8b359373273955b6d7a81debb667f4d409505191b48a`  
		Last Modified: Thu, 08 May 2025 19:36:07 GMT  
		Size: 40.9 MB (40879166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c76368c0f7d3f642913087796806042f0c184f0e84000cfa6a05c782e8afc0`  
		Last Modified: Thu, 08 May 2025 19:36:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde7faa96eef611e2ab44d9442f94944ef1d87957b633c2cd7c5a003511bb415`  
		Last Modified: Thu, 08 May 2025 19:36:03 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-focal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0ad1e6b9b4acd92cd30c7044f93aba7405b350f291ce473e7c5c921fc57142ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4921f3c5680221a97f79bc2cdc3777a90ac9751058f4f84e8fcc1357aba2a5ac`

```dockerfile
```

-	Layers:
	-	`sha256:db01a4c7d4a03daa0f6ca4feaa0906179d5f522f2fa1f11ae4819024cc5480ef`  
		Last Modified: Mon, 28 Apr 2025 20:09:01 GMT  
		Size: 3.7 MB (3738507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:248bb16b078640c3def960b3fc219496afb90cd2d6f37f463ade2479945d18af`  
		Last Modified: Mon, 28 Apr 2025 20:09:01 GMT  
		Size: 22.1 KB (22070 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-focal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:82808c4f182c40a1dc518abf22d49945684e506881d561735448f2ac3c0ed8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95764584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366917cee505c8634a8bd5b47cd9d631738636532609d9e3934b8506116bb9ec`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:47:01 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:47:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:47:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:47:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:47:04 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Tue, 08 Apr 2025 10:47:05 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c76f94e1b400a4da932a3f581b0788af2101819083184f40a6c76ac9b97081f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='5d0c81fd8bee49d1b9931acaecdc528fdc9393547cf5b24880445ade6b3f2384';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='6c0f29b6011d0baa46f90a572691b77ea93a45b4e5037141777a236956945c50';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='d9b523defdea8b82647726de8f62b57a19f2c64020b9ab6dbc5ae4929d0ee64e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Thu, 08 May 2025 21:39:31 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5eddb83d3002695f58ef132a43fe0c41ba6a1338438d3698725700dfbf1177`  
		Last Modified: Wed, 09 Apr 2025 04:33:49 GMT  
		Size: 22.4 MB (22424673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd2246c551ebc1fa2e32f974e299f15e79d0227eccf07a01715ddac7b6b4611`  
		Last Modified: Mon, 28 Apr 2025 20:12:01 GMT  
		Size: 41.3 MB (41260556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704fe6fcd24d7d99b82c6f6aa3ca8f04d4d687396cd3465a417fa07c3b45cdbc`  
		Last Modified: Mon, 28 Apr 2025 20:11:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0eb8583a52eca8bcc30b7c59aea60bb0446fbb8f6895e6ff3f40c3c581b619`  
		Last Modified: Mon, 28 Apr 2025 20:11:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-focal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f9025eccd3e1540d36b7ded1966e47a1739390e2d46372b9a0884a3652405122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95122b06052ac8f6e42568bfeccae3f71ddcbcc42ab447b7fbd357031004e5f`

```dockerfile
```

-	Layers:
	-	`sha256:4a544e575b6d1adb431c0c65e3abd500421901f2461aca8300b9f954d6acc1c4`  
		Last Modified: Mon, 28 Apr 2025 20:12:00 GMT  
		Size: 3.7 MB (3742734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0fd1380909ae1f0e2aee00c974f1d88065bdb7f5f65b77798c212f9dcb972ba`  
		Last Modified: Mon, 28 Apr 2025 20:11:59 GMT  
		Size: 22.0 KB (21996 bytes)  
		MIME: application/vnd.in-toto+json
