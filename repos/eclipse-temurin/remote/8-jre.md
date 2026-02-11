## `eclipse-temurin:8-jre`

```console
$ docker pull eclipse-temurin@sha256:ffd1c6f41f9a0187c34e369a345e11de2d39a1f2ab6f42cfb2f1f3698620db5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `eclipse-temurin:8-jre` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:815c215bb5f18d112c486a7956ba9c327607865b179d462a3510fd32853fe260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97534586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d427285ff2d1b127eb6929a62b94a6c96ca9f37d2974ab8eac2c4bc09c5c0b9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:14:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:14:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:14:51 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:14:51 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:14:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='29c93e29421b9f77bc95305834f3239313466fd988111b5cf409fd9a2f727cff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 05 Feb 2026 22:14:54 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:14:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:14:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199d4528d3c4775b4bdc5bf4fde1b45609ba75be6d41cec44a22f4756c5f90c8`  
		Last Modified: Thu, 05 Feb 2026 22:15:06 GMT  
		Size: 25.5 MB (25474657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d7e74a8fdfb836219f2b267183c499a4fe82d8206aee2e83d64f88f719ddfa`  
		Last Modified: Thu, 05 Feb 2026 22:15:07 GMT  
		Size: 42.3 MB (42331509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd6e14f0cb33d9c375fe3b8d66d8c18003d652497809519a509152e194c9d11`  
		Last Modified: Thu, 05 Feb 2026 22:15:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c4fafac5828cb2d0471572584c7b62a70d62e78b4709fa1107f66d88cbb1f9`  
		Last Modified: Thu, 05 Feb 2026 22:15:05 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4bbf98fa7cd502e9e3d607856dafb050d5602c7a54df5dc8122fffdf39c3eae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3338660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38bd029358d5f0e39919aa373bacacb6dcd16a06a91b6f39b6ce4cb8fc013246`

```dockerfile
```

-	Layers:
	-	`sha256:9cb4b9d23910b5c985c9b2e69a3a3b1cf93629581b50084fb31b435060a86785`  
		Last Modified: Thu, 05 Feb 2026 22:15:05 GMT  
		Size: 3.3 MB (3316099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:079fdaf70af5ad157a59a4048ab63d3b6ca2af3d5c83a3ef82b24f184a646436`  
		Last Modified: Thu, 05 Feb 2026 22:15:05 GMT  
		Size: 22.6 KB (22561 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:8d0e673e64f4937eb55fbf75155fcf410da64c693b7c2753ef99ea4ffe9d9ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89552791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d89120242f236ec45b049aa71b99eee3e9211ccf658e0bda0a6a6968777a5225`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:59 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:02 GMT
ADD file:9e6534a5b837dcbcc4b9596878a4feeb07210fb34c7385aeee0217ff03c2460e in / 
# Tue, 13 Jan 2026 05:40:03 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:15:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:15:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:15:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:15:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:15:39 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:15:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='29c93e29421b9f77bc95305834f3239313466fd988111b5cf409fd9a2f727cff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 05 Feb 2026 22:15:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:15:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:15:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:a56277e49d30e9a430d5cefad3038f88470a8681e48b806fff292791ed54f1fc`  
		Last Modified: Tue, 13 Jan 2026 06:35:51 GMT  
		Size: 26.9 MB (26853837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d7c3bb5261257ceddd7e0dbba0261b5bfa39d70af918766e535f56980f1b5f`  
		Last Modified: Thu, 05 Feb 2026 22:16:01 GMT  
		Size: 22.9 MB (22934432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0113afb25de8abe1a3e0323cdeed49935734e569ab22f824636b8b3da0b530d`  
		Last Modified: Thu, 05 Feb 2026 22:16:01 GMT  
		Size: 39.8 MB (39762114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b436d3de5ce1cff3d855bda04de523f212d228f610f77107d04ae1da256cfef`  
		Last Modified: Thu, 05 Feb 2026 22:16:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a01af5d45e28762d657ecbf0ba81263a7d31d1678d8a3cd67b132055a7d026`  
		Last Modified: Thu, 05 Feb 2026 22:16:00 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:83a8492ffae828dbc87bee4c5cf486b34e1558e5ed47a6b926e70f1bcf673076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5f2c66e5f6b5932abb1d475bbb55a11e4cad282aa677245d282e742625f461`

```dockerfile
```

-	Layers:
	-	`sha256:f92c7e7e45fc044aa3231872095251cfe977483a8f105e68511c3908854c53e2`  
		Last Modified: Thu, 05 Feb 2026 22:16:00 GMT  
		Size: 3.3 MB (3322099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f128376b58c72bc5b1fb718bbe41b6163345cda95e427d068d26b9feb40f59c9`  
		Last Modified: Thu, 05 Feb 2026 22:15:59 GMT  
		Size: 22.7 KB (22667 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:fd3adec08166cd6b21e2b3a671d7f4fc0bf834b9b108f71f1288d9a5ce3c25e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95225443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad00d1f93561fc197715751ca18976486785f663f2c01446384646ea52a01665`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:13:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:13:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:13:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:13:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:13:24 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:13:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='29c93e29421b9f77bc95305834f3239313466fd988111b5cf409fd9a2f727cff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 05 Feb 2026 22:13:51 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:13:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:13:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0493720b8d8524b2c676f6eb5c5ec1f85ea66e648b37bc97a9c40ec8d9b8e688`  
		Last Modified: Thu, 05 Feb 2026 22:13:41 GMT  
		Size: 25.1 MB (25069393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01166e6a48560b5ba36237c4c608c8a4afd7b81aa30fbe40292e3f8c52ca6e5a`  
		Last Modified: Thu, 05 Feb 2026 22:14:02 GMT  
		Size: 41.3 MB (41289818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede7fdeb899c0e427949b1fa52a01a670a2536076791cc9452b860581924392d`  
		Last Modified: Thu, 05 Feb 2026 22:14:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e809d6a4afd76e3502446827e59d8ab359a8c9385aab6968755c9bbbd80ec522`  
		Last Modified: Thu, 05 Feb 2026 22:14:01 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b21e6e636af4374abd4c876b8d3eab1cc7d19979dc93de5455eedf63bf90c48c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3339957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45b5b24d4052eb4582ff6677c864d879136a4b44b15435da5c909a5b512bbcf`

```dockerfile
```

-	Layers:
	-	`sha256:1283b59b64b1313a4fcc972bb35a047082c3baa7e5839ff5013778d9ef57355e`  
		Last Modified: Thu, 05 Feb 2026 22:14:02 GMT  
		Size: 3.3 MB (3317262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba9bc9caeaaa5a6259c708266c40a39fa9ea5b6b2e2c0fd23119ed46d38ec8f`  
		Last Modified: Thu, 05 Feb 2026 22:14:02 GMT  
		Size: 22.7 KB (22695 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:69e5d156bc4958b271fdc63fc2b8a6f421c899757579f53d6b7cadef9fafd43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104338567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8099858f3bf6d96c05cab3f9b359a189fd7f7d765506fdedc0bff6d9d36a9a5e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:15:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:15:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:15:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:15:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:15:06 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:16:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='29c93e29421b9f77bc95305834f3239313466fd988111b5cf409fd9a2f727cff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 05 Feb 2026 22:16:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:16:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:16:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4438ac1f4b9f9f88cf7d7982d911db40f34e73f7406e5ec71ff6bebd876883`  
		Last Modified: Thu, 05 Feb 2026 22:15:40 GMT  
		Size: 28.3 MB (28306219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffaefea7bf0bf2577704e48a3461551749aefc8934f9bc1de9543489cdff715`  
		Last Modified: Thu, 05 Feb 2026 22:17:20 GMT  
		Size: 41.7 MB (41723781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed17e6077a240ba9dcb01882bce124f767f30340a1020035b40c7251da03268`  
		Last Modified: Thu, 05 Feb 2026 22:17:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beddb0c2823a02b47d54cb41b79031102d4507016f464b52e7e8e55024f7c286`  
		Last Modified: Thu, 05 Feb 2026 22:17:19 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f72e931a132ec8440497b27699747d5b79c816f24ac300d6afae7d50c5391432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb09a2a413087c2ff8569bf152f6cfc377de185f0a7e09281df8137aee1f2d71`

```dockerfile
```

-	Layers:
	-	`sha256:788642393abd1c94de876d00c76587108bb11e8005e87fa727d352827cd21906`  
		Last Modified: Thu, 05 Feb 2026 22:17:19 GMT  
		Size: 3.3 MB (3320859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01cc3ba194cd1c97b4c6e24678de920f4fbe9e9b556e2b4fa11d8953da04461f`  
		Last Modified: Thu, 05 Feb 2026 22:17:19 GMT  
		Size: 22.6 KB (22609 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre` - windows version 10.0.26100.32370; amd64

```console
$ docker pull eclipse-temurin@sha256:cd2e7a97196d62d28ca07e04568ef915c52aa20f89ec06770e686d1357267d9b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037045373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d834f3a619e94635a44355fb7f292a38214c8919d25e679d59254c722fad1a1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:53:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 22:53:21 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 10 Feb 2026 22:53:38 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_windows_hotspot_8u482b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_windows_hotspot_8u482b08.msi ;     Write-Host ('Verifying sha256 (4e0dbdff6537f43b012e2376de59845968afc99f5901303a28a881b42d93d795) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4e0dbdff6537f43b012e2376de59845968afc99f5901303a28a881b42d93d795') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Feb 2026 22:53:43 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcfd35fb91d5c96c95008501f15273667b38b3c34c813a77275adb8e4064973`  
		Last Modified: Tue, 10 Feb 2026 22:53:48 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4578e737ca97fc2098d4c2f88fc46f3dd3ce9473f2cc986ab1b0389e911f22`  
		Last Modified: Tue, 10 Feb 2026 22:53:48 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ab05c1d6722e4634b510cecbb24fe709c929992160193a200483222944342c`  
		Last Modified: Tue, 10 Feb 2026 22:53:53 GMT  
		Size: 71.9 MB (71936071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1990c4865a76722ce3eb890d85ae7d24549e1eeb9388071ae6d2f662f3d776e`  
		Last Modified: Tue, 10 Feb 2026 22:53:48 GMT  
		Size: 346.8 KB (346805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre` - windows version 10.0.20348.4773; amd64

```console
$ docker pull eclipse-temurin@sha256:6a402bb1b49bfea80aebee1904dce9f09aac6f5f6b2afc7d16033c7ba63a0e4d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1934956870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10a31d58d34aee1e66f976076dfddc1f689fbc25ccbe884787cac142e8ec135`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Tue, 10 Feb 2026 22:51:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 23:00:07 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 10 Feb 2026 23:00:20 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_windows_hotspot_8u482b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_windows_hotspot_8u482b08.msi ;     Write-Host ('Verifying sha256 (4e0dbdff6537f43b012e2376de59845968afc99f5901303a28a881b42d93d795) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4e0dbdff6537f43b012e2376de59845968afc99f5901303a28a881b42d93d795') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Feb 2026 23:00:25 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf582aa59c8f589f6cc77378809eabf79b679ef8c09e8e900a5ce77bf0b77e38`  
		Last Modified: Tue, 10 Feb 2026 22:55:10 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2febe100bc3ef134e143540cca5a4b86f1e880a4f4d8dd1bc5f3ec2bd1f27c5`  
		Last Modified: Tue, 10 Feb 2026 23:00:32 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83126138a16639b9b4cb4daae8c468e08de2fcabdd8fbbdf5264bbe69344e629`  
		Last Modified: Tue, 10 Feb 2026 23:00:36 GMT  
		Size: 71.9 MB (71945193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfc0bc0e5a5f0bff50388c1d65dab516647824a40a9bb571a6a3e3e899a262e`  
		Last Modified: Tue, 10 Feb 2026 23:00:30 GMT  
		Size: 351.8 KB (351848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
