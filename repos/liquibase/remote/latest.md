## `liquibase:latest`

```console
$ docker pull liquibase@sha256:c9970984c1f20eec9fa06cea8e4b5db3f9a95044b1dc6cffb4170a0da8732da5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:1fab78c149fc96b53e27f7a6b26ce6f085a76764616b2962c760323ee1f30740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.9 MB (447948873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f3c7d6857a7da2b4943127d6f7fed89df3c2c4bb257f9e613a06412c3b550b4`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Mon, 17 Feb 2025 16:29:17 GMT
ARG RELEASE
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 17 Feb 2025 16:29:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 17 Feb 2025 16:29:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 17 Feb 2025 16:29:17 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 17 Feb 2025 16:29:17 GMT
CMD ["/bin/bash"]
# Mon, 17 Feb 2025 16:29:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Feb 2025 16:29:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Feb 2025 16:29:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Feb 2025 16:29:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Mon, 17 Feb 2025 16:29:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 17 Feb 2025 16:29:17 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
WORKDIR /liquibase
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LIQUIBASE_VERSION=4.31.1
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LB_SHA256=0555808b59941d497f0c1114c3f2225698afde11c60d191c88e449506a60a3ea
# Mon, 17 Feb 2025 16:29:17 GMT
# ARGS: LIQUIBASE_VERSION=4.31.1 LB_SHA256=0555808b59941d497f0c1114c3f2225698afde11c60d191c88e449506a60a3ea
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LPM_VERSION=0.2.8
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Mon, 17 Feb 2025 16:29:17 GMT
# ARGS: LIQUIBASE_VERSION=4.31.1 LB_SHA256=0555808b59941d497f0c1114c3f2225698afde11c60d191c88e449506a60a3ea LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
ENV LIQUIBASE_HOME=/liquibase
# Mon, 17 Feb 2025 16:29:17 GMT
ENV DOCKER_LIQUIBASE=true
# Mon, 17 Feb 2025 16:29:17 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
COPY liquibase.docker.properties ./ # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
USER liquibase:liquibase
# Mon, 17 Feb 2025 16:29:17 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Mon, 17 Feb 2025 16:29:17 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97781601768cddddc35e23ddf38633ea2e4a0a4ae0a8f59f11856fffbd8a3bad`  
		Last Modified: Wed, 23 Apr 2025 16:31:54 GMT  
		Size: 16.1 MB (16146029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa68485484727aa6d5321f078fb21840fd2a8bdd598f4f8a3e1672a95317733e`  
		Last Modified: Wed, 23 Apr 2025 16:31:56 GMT  
		Size: 47.0 MB (46958421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e85f04a42eb69d25f9b02e9a1c46559467f5274b45bb338cd0809534deef05e`  
		Last Modified: Wed, 23 Apr 2025 16:31:53 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0137fea4bef4dc4ff919d973a8ae36f29edacba15f7b5129ebe177983d665fe0`  
		Last Modified: Wed, 23 Apr 2025 16:31:53 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84121b79e8fa73fb11faa2c6d37f033e2e711dc34062bbdffec253ce23f8a3b`  
		Last Modified: Wed, 23 Apr 2025 17:12:51 GMT  
		Size: 4.3 KB (4303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b649d164575fb6fec94a60047cee7de4e58c415376bfa46711d4e91c23d744b9`  
		Last Modified: Wed, 23 Apr 2025 17:12:57 GMT  
		Size: 352.0 MB (351985744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca44302b37d1b5ee70e0737de4bcd7cf288af99354684db62d28e98a2928d0ef`  
		Last Modified: Wed, 23 Apr 2025 17:12:51 GMT  
		Size: 3.3 MB (3318898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a9a61b0fc0387ce4f99faa3e6b0692b03906474566b096e700a8d0efca4643`  
		Last Modified: Wed, 23 Apr 2025 17:12:51 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e6ee0c90f0827c825e808730f081ae45ddf6a22401ca0ddc15f27e64f0ee0f`  
		Last Modified: Wed, 23 Apr 2025 17:12:51 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:175ce0058710b9882c06aed0ea03681d2e59a2b7e0e31b1e0c045678424a26f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3777340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436ba0c042ed548afa96d5a9f7b6a6fb1915f890996c1bf957eb0cab12db69da`

```dockerfile
```

-	Layers:
	-	`sha256:73e93ef4d8990f29c99bf629b451f5261c900ac873dbcf1d786ee51ae52265f0`  
		Last Modified: Wed, 23 Apr 2025 17:12:51 GMT  
		Size: 3.8 MB (3753133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd243796b727579582359cd10c5a87cc38914ef086d75f0e0b4114876139d141`  
		Last Modified: Wed, 23 Apr 2025 17:12:50 GMT  
		Size: 24.2 KB (24207 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:8a0136c727bc2fac2e34b2be9e6d7f6379f114b227ebfa9fef823d9e2fe3dc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.9 MB (444943960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce672040fc113c3772ba6d8dd4f5ec9a90d52731af91a03e2fa4bbcb3b83dd7`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
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
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 17 Feb 2025 16:29:17 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
WORKDIR /liquibase
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LIQUIBASE_VERSION=4.31.1
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LB_SHA256=0555808b59941d497f0c1114c3f2225698afde11c60d191c88e449506a60a3ea
# Mon, 17 Feb 2025 16:29:17 GMT
# ARGS: LIQUIBASE_VERSION=4.31.1 LB_SHA256=0555808b59941d497f0c1114c3f2225698afde11c60d191c88e449506a60a3ea
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LPM_VERSION=0.2.8
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Mon, 17 Feb 2025 16:29:17 GMT
# ARGS: LIQUIBASE_VERSION=4.31.1 LB_SHA256=0555808b59941d497f0c1114c3f2225698afde11c60d191c88e449506a60a3ea LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
ENV LIQUIBASE_HOME=/liquibase
# Mon, 17 Feb 2025 16:29:17 GMT
ENV DOCKER_LIQUIBASE=true
# Mon, 17 Feb 2025 16:29:17 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
COPY liquibase.docker.properties ./ # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
USER liquibase:liquibase
# Mon, 17 Feb 2025 16:29:17 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Mon, 17 Feb 2025 16:29:17 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d988c284109adb0ee08f6d6a95a152f6e364456e1a4853bb6c3ebc58c40f099`  
		Last Modified: Wed, 09 Apr 2025 06:58:01 GMT  
		Size: 16.1 MB (16059566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e33a6af69490ac4a5ecfc3e027286d47e3a0070cfdb663a81213cf8d5a24459`  
		Last Modified: Wed, 09 Apr 2025 07:06:24 GMT  
		Size: 46.5 MB (46463543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6766658187816c9cfa3a64d81a99de5d5dd95ed2521fe04889d20c6738cf773`  
		Last Modified: Wed, 09 Apr 2025 07:06:22 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874b78843a76a79650a3319555c7237bd8a86082c56ca8fcfcf1b4771e56fd1c`  
		Last Modified: Wed, 09 Apr 2025 07:06:22 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85a76c5568eefb93df64e7074ae2e182ba8e92075d533f8fe148b1875db5b60`  
		Last Modified: Wed, 09 Apr 2025 15:14:37 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227da80899e15ca51c4af924536d5fb8b714ee0d930b454159f3623d5675d64d`  
		Last Modified: Wed, 09 Apr 2025 15:14:48 GMT  
		Size: 352.0 MB (351985761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fefb839c3ab9993bc6b69d5815cf0f5814662e40804177068ad18a3402effe`  
		Last Modified: Wed, 09 Apr 2025 15:14:38 GMT  
		Size: 3.1 MB (3073440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2295b5b32723740153b98b3ff1d42e0f84975a3923be79e9d2f0e7c02c160867`  
		Last Modified: Wed, 09 Apr 2025 15:14:37 GMT  
		Size: 470.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6022649074f788c4f8277d386ed14f88a637c13f0c0d04a46ae01ae5550405`  
		Last Modified: Wed, 09 Apr 2025 15:14:38 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:fe0cbf37703493bb279312e1f10d72b7b1b2b1a771c02c6bf97b1f45c91c5323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3777130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbe4e88871de6e4df3bc29db390e57a6c28fc6505b1d83a43857b74072f5d9b`

```dockerfile
```

-	Layers:
	-	`sha256:8db6abecff88cab1d478de32ab927a7ddb0e8287bef41a916c2b9b0a650d4f3e`  
		Last Modified: Wed, 09 Apr 2025 15:14:37 GMT  
		Size: 3.8 MB (3752801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5141e294aefa25b390ff7adfcd82eaa1e9d28bfaaa24df857e1c81e0d3c79b17`  
		Last Modified: Wed, 09 Apr 2025 15:14:37 GMT  
		Size: 24.3 KB (24329 bytes)  
		MIME: application/vnd.in-toto+json
