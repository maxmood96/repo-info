<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `liquibase`

-	[`liquibase:4.33`](#liquibase433)
-	[`liquibase:4.33-alpine`](#liquibase433-alpine)
-	[`liquibase:4.33.0`](#liquibase4330)
-	[`liquibase:4.33.0-alpine`](#liquibase4330-alpine)
-	[`liquibase:alpine`](#liquibasealpine)
-	[`liquibase:latest`](#liquibaselatest)

## `liquibase:4.33`

```console
$ docker pull liquibase@sha256:3c9676c964fc196cbddf8880709efeb764914ee2ed1326377ddd880439e28881
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.33` - linux; amd64

```console
$ docker pull liquibase@sha256:c480030e4162104fd04f51feb96de33d75030ef699d7a956e83584a37a0831c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.8 MB (456768609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7df879df156ed13647ba616baa47399ca91476b529f1295d850d2b8bcd3a75d`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 09 Jul 2025 14:57:56 GMT
ARG RELEASE
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 09 Jul 2025 14:57:56 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["/bin/bash"]
# Wed, 09 Jul 2025 14:57:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Jul 2025 14:57:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Jul 2025 14:57:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Wed, 09 Jul 2025 14:57:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22d4e398983a6297ffbf74ad58db85e0e2ff9787f8f650fca93ef3389270707`  
		Last Modified: Tue, 12 Aug 2025 17:24:44 GMT  
		Size: 16.2 MB (16150701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74362a1bde1d60a877e9f5db8099e0ad1b488263b6271373d6992fc9554b0d7f`  
		Last Modified: Tue, 12 Aug 2025 17:24:48 GMT  
		Size: 53.0 MB (52968659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34f25f9917c8328ed8e364b4033defd59b401b52265a6d2af32bf8faa06ad25`  
		Last Modified: Tue, 12 Aug 2025 17:24:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ea2ced528387fba2622680db2f289ff6b4858fc630d175eec776c663dc3ecc`  
		Last Modified: Tue, 12 Aug 2025 17:24:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d72a02f463cfef2961cb8deee1cafc92c1353cb8f638732b981b725f9b5d80`  
		Last Modified: Tue, 12 Aug 2025 18:39:36 GMT  
		Size: 4.3 KB (4298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8651682657aaccb55fe69b8048abdd05891d0746d8c0450748cd59d3bc5ea8f1`  
		Last Modified: Tue, 12 Aug 2025 19:36:06 GMT  
		Size: 354.4 MB (354408289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa037d5cb946fa29a47925ccef8c0349c07abae5ebc0a856f95530e2e3d2803`  
		Last Modified: Tue, 12 Aug 2025 18:39:37 GMT  
		Size: 3.7 MB (3696552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d2148bb2decf5a58cc884f78f63cb8273ab22533f4316f83a860f5b0a92209`  
		Last Modified: Tue, 12 Aug 2025 18:39:38 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be94b71f442568a74208ab6f024cc9b5bccab7ed5b0729f91dc919e930681198`  
		Last Modified: Tue, 12 Aug 2025 18:39:38 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.33` - unknown; unknown

```console
$ docker pull liquibase@sha256:93b9937188cab45f3ea175854e5750ba92a673514fd064717111f094c3420cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d356c15f13d9c4f2f454605d67ab458eb379d36ab18e366c835115a4b62bd88`

```dockerfile
```

-	Layers:
	-	`sha256:63d00af46ee58092b168388ea9aa55fca4bdd4a36957151046b43e5beccdac0c`  
		Last Modified: Tue, 12 Aug 2025 18:39:25 GMT  
		Size: 3.9 MB (3940477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2d6e11db4e81f24eee1e032e7e67bee0af5299d6f10170bbaf41a8dd21da8ce`  
		Last Modified: Tue, 12 Aug 2025 18:39:26 GMT  
		Size: 24.4 KB (24423 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.33` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:f78f7c96e2fde5faaadfc7cfae22d3db5500c3a5136f88b8a5b947a56abff378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.4 MB (453392618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6454748975cae8df15e9c7acd39368bbba76529fc8e296346976479923111e50`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 09 Jul 2025 14:57:56 GMT
ARG RELEASE
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 09 Jul 2025 14:57:56 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["/bin/bash"]
# Wed, 09 Jul 2025 14:57:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Jul 2025 14:57:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Jul 2025 14:57:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Wed, 09 Jul 2025 14:57:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b5bc71170396faf6c1c291a060d5d6b6d6700719a4f7f1f47d7e8a843b7a6d`  
		Last Modified: Tue, 12 Aug 2025 18:31:02 GMT  
		Size: 16.1 MB (16063741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e52f3080aac2f7abe2d858a9dfe47d820850f11dcba9da3ee78a5072085399`  
		Last Modified: Tue, 12 Aug 2025 18:39:07 GMT  
		Size: 52.1 MB (52148319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222689666f0565f2906e70d8a5eb586c7ba09eaef163ff5625994374a9b3bfdd`  
		Last Modified: Tue, 12 Aug 2025 18:38:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca372eebceee03ecddb4b24f67489039af1d4266be937af8e10492ed348c23df`  
		Last Modified: Tue, 12 Aug 2025 18:38:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b2e7e3bf8cce57c9dccb03aa365849efcfa9d32b432f7cde3ef3465e2d6e86`  
		Last Modified: Tue, 12 Aug 2025 23:33:32 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dedf163b134bbe88921dffdbffc7f9fcde209aeaca5eb60ac3eab670786a0f3`  
		Last Modified: Wed, 13 Aug 2025 01:42:24 GMT  
		Size: 354.4 MB (354408370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c3e2fd9f9e555777d6ad994c2d125be63db5794f450c65c0ad1fde869e126b`  
		Last Modified: Tue, 12 Aug 2025 23:33:34 GMT  
		Size: 3.4 MB (3405515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0ae56e57c69617196fa3a5ae435a10c10786b9813002fbda9187e12cecd260`  
		Last Modified: Tue, 12 Aug 2025 23:33:32 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b00bae4998d43e4614211b7aab42deae32aa3dbdef80cbf7dfa07aa0eb8703e`  
		Last Modified: Tue, 12 Aug 2025 23:33:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.33` - unknown; unknown

```console
$ docker pull liquibase@sha256:3f581a31b0bed9ab68e2254cb48e819763b1f4a7576955edd84dfc2bcd0b306c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbbf474cb71a1419ca2222c23e15bba81a3cbb2e5e39b5688c0c72462ac824e`

```dockerfile
```

-	Layers:
	-	`sha256:0fde0210fb5d55b326389e76ba151b5c5fdb2979a922a3fa8b5e29d1d8d4d7c7`  
		Last Modified: Wed, 13 Aug 2025 00:39:22 GMT  
		Size: 3.9 MB (3940145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e38516bcb649e9df77ecde6b604de5fd2b09a6c8e508bce4e8dba92da61b78a3`  
		Last Modified: Wed, 13 Aug 2025 00:39:23 GMT  
		Size: 24.5 KB (24545 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.33-alpine`

```console
$ docker pull liquibase@sha256:6cea0dff52800aa4c7a24cdfbfd84c98f41b0ab583274d37d0caece14d7d33bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.33-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:e96dd04edaeec6002ba39385640b23014f4225f6f3656c179304b3647ae5182f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.6 MB (429635568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98323fa9b91eb9354e55bb7164f54deb7bafe937225883d42b943fed34e475e0`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 09 Jul 2025 14:57:56 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c3b264b65a529e06951646a37573132cb04d969c14cc1392823634c420e538`  
		Last Modified: Tue, 15 Jul 2025 19:28:04 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941c0831ca4d90044d1b1f99a6405b52d8abb7a81b9f057a07cdd28072eff29f`  
		Last Modified: Tue, 15 Jul 2025 19:28:16 GMT  
		Size: 67.8 MB (67787243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5865751478b337d80a2e6e0eea98e2bcdc072fdf532632fbacfef4d7bf9389c5`  
		Last Modified: Wed, 16 Jul 2025 00:26:37 GMT  
		Size: 354.4 MB (354431260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb968475d81969c98483f351864e4b7b67ebf92640cb4e8e0e38a9734d43f67`  
		Last Modified: Tue, 15 Jul 2025 19:28:06 GMT  
		Size: 3.6 MB (3615768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98020d1d721e8ba2a08a5d0943ccbe39ad08796bc60dc1a4d7a43f607bff0624`  
		Last Modified: Tue, 15 Jul 2025 19:28:04 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df7876ba48e7c74621d323b343b5515c23ebae668879742b8d214eb2da58cb6`  
		Last Modified: Tue, 15 Jul 2025 19:28:04 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.33-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:4c7e899dd3f19a647866fb3a1cd238e95f3e9f713a77dec703a858eb64d55adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.2 KB (421200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e06940187ffab633c2ecc6410f4d64213ff19cd68704116b030055305c935ba`

```dockerfile
```

-	Layers:
	-	`sha256:f947564a1d44b1388aa99be884844b131a41f6bf1db3f771dcf2932af4a63886`  
		Last Modified: Tue, 15 Jul 2025 21:39:19 GMT  
		Size: 399.5 KB (399489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bba6ac697446fc90adcefcaaf35f795368a27ef2b825d4d80ff552acce07731`  
		Last Modified: Tue, 15 Jul 2025 21:39:19 GMT  
		Size: 21.7 KB (21711 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.33-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:4903c17833c7890e44e674298c601ee4fd48de47cbd1703e6b26999637bb1a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.7 MB (428680056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cdf0f7a760ccfe621197a9544bc8c2c9d346bbf2870bd08539d373b8fa0d6f9`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 09 Jul 2025 14:57:56 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef8cf8b9371aee62199c1e9f7f4bc0a626925d34f8bb448409f94e715150611`  
		Last Modified: Wed, 16 Jul 2025 00:18:23 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e9a9771a8a3da18140ec47c7b661d11b38ca280072df3ee86645d51f7087bd`  
		Last Modified: Wed, 16 Jul 2025 00:18:27 GMT  
		Size: 66.8 MB (66792466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b93f850224c06dc79725a8fbbc500545400db8c9bfdc4ef4b037bec1d3ac0a8`  
		Last Modified: Wed, 16 Jul 2025 02:45:20 GMT  
		Size: 354.4 MB (354430749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464e79db19d93d4af11382fd5711050d251575c5e6b1589b2ad0109fdf4aa676`  
		Last Modified: Wed, 16 Jul 2025 00:18:23 GMT  
		Size: 3.3 MB (3324484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13c979c7c238a9798011c8d71cd8e3e30a1d6ae5cec34e1a253f57828acff3d`  
		Last Modified: Wed, 16 Jul 2025 00:18:22 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d305e29280161b0cd0d34cdeb8c9acd45ab2d00123a1ea130d396a3dd8ea6ac`  
		Last Modified: Wed, 16 Jul 2025 00:18:22 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.33-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:50e0f2c77f5658ebefdee2ea7561873b3c85df3a2fbe7263d8b17fdab9d08cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.6 KB (420586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d3ae9b7bdab04cc9d1d058e41d8ec5b56ace6b6b38cf5251640a76286acf36`

```dockerfile
```

-	Layers:
	-	`sha256:4e53c97d9ecc98a1a84b3213e7680e52bade78fbd259ef5c61e644f0ea4d4742`  
		Last Modified: Wed, 16 Jul 2025 00:39:25 GMT  
		Size: 398.7 KB (398736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:923d1dd4af7b2e8bd934415f53f4ba09ffe3044cfe90ceb4606b97fa1b8b8e28`  
		Last Modified: Wed, 16 Jul 2025 00:39:25 GMT  
		Size: 21.9 KB (21850 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.33.0`

```console
$ docker pull liquibase@sha256:3c9676c964fc196cbddf8880709efeb764914ee2ed1326377ddd880439e28881
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.33.0` - linux; amd64

```console
$ docker pull liquibase@sha256:c480030e4162104fd04f51feb96de33d75030ef699d7a956e83584a37a0831c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.8 MB (456768609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7df879df156ed13647ba616baa47399ca91476b529f1295d850d2b8bcd3a75d`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 09 Jul 2025 14:57:56 GMT
ARG RELEASE
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 09 Jul 2025 14:57:56 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["/bin/bash"]
# Wed, 09 Jul 2025 14:57:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Jul 2025 14:57:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Jul 2025 14:57:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Wed, 09 Jul 2025 14:57:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22d4e398983a6297ffbf74ad58db85e0e2ff9787f8f650fca93ef3389270707`  
		Last Modified: Tue, 12 Aug 2025 17:24:44 GMT  
		Size: 16.2 MB (16150701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74362a1bde1d60a877e9f5db8099e0ad1b488263b6271373d6992fc9554b0d7f`  
		Last Modified: Tue, 12 Aug 2025 17:24:48 GMT  
		Size: 53.0 MB (52968659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34f25f9917c8328ed8e364b4033defd59b401b52265a6d2af32bf8faa06ad25`  
		Last Modified: Tue, 12 Aug 2025 17:24:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ea2ced528387fba2622680db2f289ff6b4858fc630d175eec776c663dc3ecc`  
		Last Modified: Tue, 12 Aug 2025 17:24:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d72a02f463cfef2961cb8deee1cafc92c1353cb8f638732b981b725f9b5d80`  
		Last Modified: Tue, 12 Aug 2025 18:39:36 GMT  
		Size: 4.3 KB (4298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8651682657aaccb55fe69b8048abdd05891d0746d8c0450748cd59d3bc5ea8f1`  
		Last Modified: Tue, 12 Aug 2025 19:36:06 GMT  
		Size: 354.4 MB (354408289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa037d5cb946fa29a47925ccef8c0349c07abae5ebc0a856f95530e2e3d2803`  
		Last Modified: Tue, 12 Aug 2025 18:39:37 GMT  
		Size: 3.7 MB (3696552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d2148bb2decf5a58cc884f78f63cb8273ab22533f4316f83a860f5b0a92209`  
		Last Modified: Tue, 12 Aug 2025 18:39:38 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be94b71f442568a74208ab6f024cc9b5bccab7ed5b0729f91dc919e930681198`  
		Last Modified: Tue, 12 Aug 2025 18:39:38 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.33.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:93b9937188cab45f3ea175854e5750ba92a673514fd064717111f094c3420cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d356c15f13d9c4f2f454605d67ab458eb379d36ab18e366c835115a4b62bd88`

```dockerfile
```

-	Layers:
	-	`sha256:63d00af46ee58092b168388ea9aa55fca4bdd4a36957151046b43e5beccdac0c`  
		Last Modified: Tue, 12 Aug 2025 18:39:25 GMT  
		Size: 3.9 MB (3940477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2d6e11db4e81f24eee1e032e7e67bee0af5299d6f10170bbaf41a8dd21da8ce`  
		Last Modified: Tue, 12 Aug 2025 18:39:26 GMT  
		Size: 24.4 KB (24423 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.33.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:f78f7c96e2fde5faaadfc7cfae22d3db5500c3a5136f88b8a5b947a56abff378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.4 MB (453392618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6454748975cae8df15e9c7acd39368bbba76529fc8e296346976479923111e50`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 09 Jul 2025 14:57:56 GMT
ARG RELEASE
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 09 Jul 2025 14:57:56 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["/bin/bash"]
# Wed, 09 Jul 2025 14:57:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Jul 2025 14:57:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Jul 2025 14:57:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Wed, 09 Jul 2025 14:57:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b5bc71170396faf6c1c291a060d5d6b6d6700719a4f7f1f47d7e8a843b7a6d`  
		Last Modified: Tue, 12 Aug 2025 18:31:02 GMT  
		Size: 16.1 MB (16063741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e52f3080aac2f7abe2d858a9dfe47d820850f11dcba9da3ee78a5072085399`  
		Last Modified: Tue, 12 Aug 2025 18:39:07 GMT  
		Size: 52.1 MB (52148319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222689666f0565f2906e70d8a5eb586c7ba09eaef163ff5625994374a9b3bfdd`  
		Last Modified: Tue, 12 Aug 2025 18:38:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca372eebceee03ecddb4b24f67489039af1d4266be937af8e10492ed348c23df`  
		Last Modified: Tue, 12 Aug 2025 18:38:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b2e7e3bf8cce57c9dccb03aa365849efcfa9d32b432f7cde3ef3465e2d6e86`  
		Last Modified: Tue, 12 Aug 2025 23:33:32 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dedf163b134bbe88921dffdbffc7f9fcde209aeaca5eb60ac3eab670786a0f3`  
		Last Modified: Wed, 13 Aug 2025 01:42:24 GMT  
		Size: 354.4 MB (354408370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c3e2fd9f9e555777d6ad994c2d125be63db5794f450c65c0ad1fde869e126b`  
		Last Modified: Tue, 12 Aug 2025 23:33:34 GMT  
		Size: 3.4 MB (3405515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0ae56e57c69617196fa3a5ae435a10c10786b9813002fbda9187e12cecd260`  
		Last Modified: Tue, 12 Aug 2025 23:33:32 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b00bae4998d43e4614211b7aab42deae32aa3dbdef80cbf7dfa07aa0eb8703e`  
		Last Modified: Tue, 12 Aug 2025 23:33:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.33.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:3f581a31b0bed9ab68e2254cb48e819763b1f4a7576955edd84dfc2bcd0b306c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbbf474cb71a1419ca2222c23e15bba81a3cbb2e5e39b5688c0c72462ac824e`

```dockerfile
```

-	Layers:
	-	`sha256:0fde0210fb5d55b326389e76ba151b5c5fdb2979a922a3fa8b5e29d1d8d4d7c7`  
		Last Modified: Wed, 13 Aug 2025 00:39:22 GMT  
		Size: 3.9 MB (3940145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e38516bcb649e9df77ecde6b604de5fd2b09a6c8e508bce4e8dba92da61b78a3`  
		Last Modified: Wed, 13 Aug 2025 00:39:23 GMT  
		Size: 24.5 KB (24545 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.33.0-alpine`

```console
$ docker pull liquibase@sha256:6cea0dff52800aa4c7a24cdfbfd84c98f41b0ab583274d37d0caece14d7d33bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.33.0-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:e96dd04edaeec6002ba39385640b23014f4225f6f3656c179304b3647ae5182f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.6 MB (429635568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98323fa9b91eb9354e55bb7164f54deb7bafe937225883d42b943fed34e475e0`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 09 Jul 2025 14:57:56 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c3b264b65a529e06951646a37573132cb04d969c14cc1392823634c420e538`  
		Last Modified: Tue, 15 Jul 2025 19:28:04 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941c0831ca4d90044d1b1f99a6405b52d8abb7a81b9f057a07cdd28072eff29f`  
		Last Modified: Tue, 15 Jul 2025 19:28:16 GMT  
		Size: 67.8 MB (67787243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5865751478b337d80a2e6e0eea98e2bcdc072fdf532632fbacfef4d7bf9389c5`  
		Last Modified: Wed, 16 Jul 2025 00:26:37 GMT  
		Size: 354.4 MB (354431260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb968475d81969c98483f351864e4b7b67ebf92640cb4e8e0e38a9734d43f67`  
		Last Modified: Tue, 15 Jul 2025 19:28:06 GMT  
		Size: 3.6 MB (3615768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98020d1d721e8ba2a08a5d0943ccbe39ad08796bc60dc1a4d7a43f607bff0624`  
		Last Modified: Tue, 15 Jul 2025 19:28:04 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df7876ba48e7c74621d323b343b5515c23ebae668879742b8d214eb2da58cb6`  
		Last Modified: Tue, 15 Jul 2025 19:28:04 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.33.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:4c7e899dd3f19a647866fb3a1cd238e95f3e9f713a77dec703a858eb64d55adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.2 KB (421200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e06940187ffab633c2ecc6410f4d64213ff19cd68704116b030055305c935ba`

```dockerfile
```

-	Layers:
	-	`sha256:f947564a1d44b1388aa99be884844b131a41f6bf1db3f771dcf2932af4a63886`  
		Last Modified: Tue, 15 Jul 2025 21:39:19 GMT  
		Size: 399.5 KB (399489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bba6ac697446fc90adcefcaaf35f795368a27ef2b825d4d80ff552acce07731`  
		Last Modified: Tue, 15 Jul 2025 21:39:19 GMT  
		Size: 21.7 KB (21711 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.33.0-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:4903c17833c7890e44e674298c601ee4fd48de47cbd1703e6b26999637bb1a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.7 MB (428680056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cdf0f7a760ccfe621197a9544bc8c2c9d346bbf2870bd08539d373b8fa0d6f9`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 09 Jul 2025 14:57:56 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef8cf8b9371aee62199c1e9f7f4bc0a626925d34f8bb448409f94e715150611`  
		Last Modified: Wed, 16 Jul 2025 00:18:23 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e9a9771a8a3da18140ec47c7b661d11b38ca280072df3ee86645d51f7087bd`  
		Last Modified: Wed, 16 Jul 2025 00:18:27 GMT  
		Size: 66.8 MB (66792466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b93f850224c06dc79725a8fbbc500545400db8c9bfdc4ef4b037bec1d3ac0a8`  
		Last Modified: Wed, 16 Jul 2025 02:45:20 GMT  
		Size: 354.4 MB (354430749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464e79db19d93d4af11382fd5711050d251575c5e6b1589b2ad0109fdf4aa676`  
		Last Modified: Wed, 16 Jul 2025 00:18:23 GMT  
		Size: 3.3 MB (3324484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13c979c7c238a9798011c8d71cd8e3e30a1d6ae5cec34e1a253f57828acff3d`  
		Last Modified: Wed, 16 Jul 2025 00:18:22 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d305e29280161b0cd0d34cdeb8c9acd45ab2d00123a1ea130d396a3dd8ea6ac`  
		Last Modified: Wed, 16 Jul 2025 00:18:22 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.33.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:50e0f2c77f5658ebefdee2ea7561873b3c85df3a2fbe7263d8b17fdab9d08cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.6 KB (420586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d3ae9b7bdab04cc9d1d058e41d8ec5b56ace6b6b38cf5251640a76286acf36`

```dockerfile
```

-	Layers:
	-	`sha256:4e53c97d9ecc98a1a84b3213e7680e52bade78fbd259ef5c61e644f0ea4d4742`  
		Last Modified: Wed, 16 Jul 2025 00:39:25 GMT  
		Size: 398.7 KB (398736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:923d1dd4af7b2e8bd934415f53f4ba09ffe3044cfe90ceb4606b97fa1b8b8e28`  
		Last Modified: Wed, 16 Jul 2025 00:39:25 GMT  
		Size: 21.9 KB (21850 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:6cea0dff52800aa4c7a24cdfbfd84c98f41b0ab583274d37d0caece14d7d33bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:e96dd04edaeec6002ba39385640b23014f4225f6f3656c179304b3647ae5182f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.6 MB (429635568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98323fa9b91eb9354e55bb7164f54deb7bafe937225883d42b943fed34e475e0`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 09 Jul 2025 14:57:56 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c3b264b65a529e06951646a37573132cb04d969c14cc1392823634c420e538`  
		Last Modified: Tue, 15 Jul 2025 19:28:04 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941c0831ca4d90044d1b1f99a6405b52d8abb7a81b9f057a07cdd28072eff29f`  
		Last Modified: Tue, 15 Jul 2025 19:28:16 GMT  
		Size: 67.8 MB (67787243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5865751478b337d80a2e6e0eea98e2bcdc072fdf532632fbacfef4d7bf9389c5`  
		Last Modified: Wed, 16 Jul 2025 00:26:37 GMT  
		Size: 354.4 MB (354431260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb968475d81969c98483f351864e4b7b67ebf92640cb4e8e0e38a9734d43f67`  
		Last Modified: Tue, 15 Jul 2025 19:28:06 GMT  
		Size: 3.6 MB (3615768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98020d1d721e8ba2a08a5d0943ccbe39ad08796bc60dc1a4d7a43f607bff0624`  
		Last Modified: Tue, 15 Jul 2025 19:28:04 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df7876ba48e7c74621d323b343b5515c23ebae668879742b8d214eb2da58cb6`  
		Last Modified: Tue, 15 Jul 2025 19:28:04 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:4c7e899dd3f19a647866fb3a1cd238e95f3e9f713a77dec703a858eb64d55adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.2 KB (421200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e06940187ffab633c2ecc6410f4d64213ff19cd68704116b030055305c935ba`

```dockerfile
```

-	Layers:
	-	`sha256:f947564a1d44b1388aa99be884844b131a41f6bf1db3f771dcf2932af4a63886`  
		Last Modified: Tue, 15 Jul 2025 21:39:19 GMT  
		Size: 399.5 KB (399489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bba6ac697446fc90adcefcaaf35f795368a27ef2b825d4d80ff552acce07731`  
		Last Modified: Tue, 15 Jul 2025 21:39:19 GMT  
		Size: 21.7 KB (21711 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:4903c17833c7890e44e674298c601ee4fd48de47cbd1703e6b26999637bb1a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.7 MB (428680056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cdf0f7a760ccfe621197a9544bc8c2c9d346bbf2870bd08539d373b8fa0d6f9`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 09 Jul 2025 14:57:56 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef8cf8b9371aee62199c1e9f7f4bc0a626925d34f8bb448409f94e715150611`  
		Last Modified: Wed, 16 Jul 2025 00:18:23 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e9a9771a8a3da18140ec47c7b661d11b38ca280072df3ee86645d51f7087bd`  
		Last Modified: Wed, 16 Jul 2025 00:18:27 GMT  
		Size: 66.8 MB (66792466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b93f850224c06dc79725a8fbbc500545400db8c9bfdc4ef4b037bec1d3ac0a8`  
		Last Modified: Wed, 16 Jul 2025 02:45:20 GMT  
		Size: 354.4 MB (354430749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464e79db19d93d4af11382fd5711050d251575c5e6b1589b2ad0109fdf4aa676`  
		Last Modified: Wed, 16 Jul 2025 00:18:23 GMT  
		Size: 3.3 MB (3324484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13c979c7c238a9798011c8d71cd8e3e30a1d6ae5cec34e1a253f57828acff3d`  
		Last Modified: Wed, 16 Jul 2025 00:18:22 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d305e29280161b0cd0d34cdeb8c9acd45ab2d00123a1ea130d396a3dd8ea6ac`  
		Last Modified: Wed, 16 Jul 2025 00:18:22 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:50e0f2c77f5658ebefdee2ea7561873b3c85df3a2fbe7263d8b17fdab9d08cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.6 KB (420586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d3ae9b7bdab04cc9d1d058e41d8ec5b56ace6b6b38cf5251640a76286acf36`

```dockerfile
```

-	Layers:
	-	`sha256:4e53c97d9ecc98a1a84b3213e7680e52bade78fbd259ef5c61e644f0ea4d4742`  
		Last Modified: Wed, 16 Jul 2025 00:39:25 GMT  
		Size: 398.7 KB (398736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:923d1dd4af7b2e8bd934415f53f4ba09ffe3044cfe90ceb4606b97fa1b8b8e28`  
		Last Modified: Wed, 16 Jul 2025 00:39:25 GMT  
		Size: 21.9 KB (21850 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:latest`

```console
$ docker pull liquibase@sha256:3c9676c964fc196cbddf8880709efeb764914ee2ed1326377ddd880439e28881
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:c480030e4162104fd04f51feb96de33d75030ef699d7a956e83584a37a0831c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.8 MB (456768609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7df879df156ed13647ba616baa47399ca91476b529f1295d850d2b8bcd3a75d`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 09 Jul 2025 14:57:56 GMT
ARG RELEASE
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 09 Jul 2025 14:57:56 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["/bin/bash"]
# Wed, 09 Jul 2025 14:57:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Jul 2025 14:57:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Jul 2025 14:57:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Wed, 09 Jul 2025 14:57:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22d4e398983a6297ffbf74ad58db85e0e2ff9787f8f650fca93ef3389270707`  
		Last Modified: Tue, 12 Aug 2025 17:24:44 GMT  
		Size: 16.2 MB (16150701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74362a1bde1d60a877e9f5db8099e0ad1b488263b6271373d6992fc9554b0d7f`  
		Last Modified: Tue, 12 Aug 2025 17:24:48 GMT  
		Size: 53.0 MB (52968659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34f25f9917c8328ed8e364b4033defd59b401b52265a6d2af32bf8faa06ad25`  
		Last Modified: Tue, 12 Aug 2025 17:24:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ea2ced528387fba2622680db2f289ff6b4858fc630d175eec776c663dc3ecc`  
		Last Modified: Tue, 12 Aug 2025 17:24:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d72a02f463cfef2961cb8deee1cafc92c1353cb8f638732b981b725f9b5d80`  
		Last Modified: Tue, 12 Aug 2025 18:39:36 GMT  
		Size: 4.3 KB (4298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8651682657aaccb55fe69b8048abdd05891d0746d8c0450748cd59d3bc5ea8f1`  
		Last Modified: Tue, 12 Aug 2025 19:36:06 GMT  
		Size: 354.4 MB (354408289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa037d5cb946fa29a47925ccef8c0349c07abae5ebc0a856f95530e2e3d2803`  
		Last Modified: Tue, 12 Aug 2025 18:39:37 GMT  
		Size: 3.7 MB (3696552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d2148bb2decf5a58cc884f78f63cb8273ab22533f4316f83a860f5b0a92209`  
		Last Modified: Tue, 12 Aug 2025 18:39:38 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be94b71f442568a74208ab6f024cc9b5bccab7ed5b0729f91dc919e930681198`  
		Last Modified: Tue, 12 Aug 2025 18:39:38 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:93b9937188cab45f3ea175854e5750ba92a673514fd064717111f094c3420cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d356c15f13d9c4f2f454605d67ab458eb379d36ab18e366c835115a4b62bd88`

```dockerfile
```

-	Layers:
	-	`sha256:63d00af46ee58092b168388ea9aa55fca4bdd4a36957151046b43e5beccdac0c`  
		Last Modified: Tue, 12 Aug 2025 18:39:25 GMT  
		Size: 3.9 MB (3940477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2d6e11db4e81f24eee1e032e7e67bee0af5299d6f10170bbaf41a8dd21da8ce`  
		Last Modified: Tue, 12 Aug 2025 18:39:26 GMT  
		Size: 24.4 KB (24423 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:f78f7c96e2fde5faaadfc7cfae22d3db5500c3a5136f88b8a5b947a56abff378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.4 MB (453392618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6454748975cae8df15e9c7acd39368bbba76529fc8e296346976479923111e50`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 09 Jul 2025 14:57:56 GMT
ARG RELEASE
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 09 Jul 2025 14:57:56 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["/bin/bash"]
# Wed, 09 Jul 2025 14:57:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Jul 2025 14:57:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Jul 2025 14:57:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Wed, 09 Jul 2025 14:57:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b5bc71170396faf6c1c291a060d5d6b6d6700719a4f7f1f47d7e8a843b7a6d`  
		Last Modified: Tue, 12 Aug 2025 18:31:02 GMT  
		Size: 16.1 MB (16063741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e52f3080aac2f7abe2d858a9dfe47d820850f11dcba9da3ee78a5072085399`  
		Last Modified: Tue, 12 Aug 2025 18:39:07 GMT  
		Size: 52.1 MB (52148319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222689666f0565f2906e70d8a5eb586c7ba09eaef163ff5625994374a9b3bfdd`  
		Last Modified: Tue, 12 Aug 2025 18:38:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca372eebceee03ecddb4b24f67489039af1d4266be937af8e10492ed348c23df`  
		Last Modified: Tue, 12 Aug 2025 18:38:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b2e7e3bf8cce57c9dccb03aa365849efcfa9d32b432f7cde3ef3465e2d6e86`  
		Last Modified: Tue, 12 Aug 2025 23:33:32 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dedf163b134bbe88921dffdbffc7f9fcde209aeaca5eb60ac3eab670786a0f3`  
		Last Modified: Wed, 13 Aug 2025 01:42:24 GMT  
		Size: 354.4 MB (354408370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c3e2fd9f9e555777d6ad994c2d125be63db5794f450c65c0ad1fde869e126b`  
		Last Modified: Tue, 12 Aug 2025 23:33:34 GMT  
		Size: 3.4 MB (3405515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0ae56e57c69617196fa3a5ae435a10c10786b9813002fbda9187e12cecd260`  
		Last Modified: Tue, 12 Aug 2025 23:33:32 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b00bae4998d43e4614211b7aab42deae32aa3dbdef80cbf7dfa07aa0eb8703e`  
		Last Modified: Tue, 12 Aug 2025 23:33:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:3f581a31b0bed9ab68e2254cb48e819763b1f4a7576955edd84dfc2bcd0b306c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbbf474cb71a1419ca2222c23e15bba81a3cbb2e5e39b5688c0c72462ac824e`

```dockerfile
```

-	Layers:
	-	`sha256:0fde0210fb5d55b326389e76ba151b5c5fdb2979a922a3fa8b5e29d1d8d4d7c7`  
		Last Modified: Wed, 13 Aug 2025 00:39:22 GMT  
		Size: 3.9 MB (3940145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e38516bcb649e9df77ecde6b604de5fd2b09a6c8e508bce4e8dba92da61b78a3`  
		Last Modified: Wed, 13 Aug 2025 00:39:23 GMT  
		Size: 24.5 KB (24545 bytes)  
		MIME: application/vnd.in-toto+json
