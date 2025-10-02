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
$ docker pull liquibase@sha256:25328ef2d762e15d02c733b43b6f142ab4a5071ffd985ad002ba9010a20fb2af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.33` - linux; amd64

```console
$ docker pull liquibase@sha256:b0ed2dedd9e37f8c456ff7e9d8e65fe19ab0d59ca312f22e634d082402adccb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.8 MB (456768101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da97367ae79395efb50f55eae6a1a9ec4cca5943ebc489850ea529795c7001dd`
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
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
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
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a55b01e3ac44fd314137f34c2089a82e6266936a8a7a2e28ce60499bd91791`  
		Last Modified: Thu, 02 Oct 2025 05:02:00 GMT  
		Size: 16.2 MB (16150303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a412a34a90e9c7e90943ae8125908b2321b7e4265ad339c99a628dd2d704027`  
		Last Modified: Thu, 02 Oct 2025 05:02:09 GMT  
		Size: 53.0 MB (52968679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b072ed4655dd0505a0227f4b39e45856d97fdad63b0386f018b36594098ce12a`  
		Last Modified: Thu, 02 Oct 2025 05:02:05 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b49e514d0b6e3b401a83663a81353ef5944c24666c9373cb6f21fbbb5c9800f`  
		Last Modified: Thu, 02 Oct 2025 05:02:05 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35221078213246ed213979b051f7352acab773f3501823f90502c6c59ba1352`  
		Last Modified: Thu, 02 Oct 2025 09:29:19 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3fe4355dc61c2e2f3ec927f57443e76a97b667ec20cc17db59ff9a4081f0da`  
		Last Modified: Thu, 02 Oct 2025 09:35:55 GMT  
		Size: 354.4 MB (354408366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db2464c42dbe58582b4125b20061999a9941db49525a2da6573db928b528fc9`  
		Last Modified: Thu, 02 Oct 2025 09:29:22 GMT  
		Size: 3.7 MB (3696523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db80c9dcc24c0753a13883b33f75cafeabf18f2e7e95083c62e687b604ac315`  
		Last Modified: Thu, 02 Oct 2025 09:29:19 GMT  
		Size: 470.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767283bebb6e9262d931c887ad925bc5dbb11c2a7965b873307a88375aec75c0`  
		Last Modified: Thu, 02 Oct 2025 09:29:19 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.33` - unknown; unknown

```console
$ docker pull liquibase@sha256:46fd20674342c12c43451e065e5bee321c962a0f9be5fe1bc3567377a7e06ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ea58a7a86c97613c2850168422d8901d57334a67ab5c3b36406aa4e7c98467`

```dockerfile
```

-	Layers:
	-	`sha256:22e5f6121c6022c49f183f0600fb25e868c641fbd3146a9bb35c2622b3614606`  
		Last Modified: Thu, 02 Oct 2025 09:39:26 GMT  
		Size: 3.9 MB (3940493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95905a9724883421b65b84d34d94c44adfeb1fe5def4abc40b4ab12db06abc6d`  
		Last Modified: Thu, 02 Oct 2025 09:39:27 GMT  
		Size: 24.4 KB (24423 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.33` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:9b4224d6fd1179b234101a919ee9c14f78d1eb90763d586c69d84705ada1a344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.4 MB (453418414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50db44ae4a907e0beb5e90d9b52f418b3f65cc8c86fceb4fb122cf8d315485a7`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467d494d86601559a7c580a845a24d7c3c4e03397a8e6172f73c42ceaea86b78`  
		Last Modified: Thu, 02 Oct 2025 01:17:23 GMT  
		Size: 16.1 MB (16065710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698ba22d0a21bf3b9a2595bf748316d27c7cbfa7fb014888aa87919ba1ab6b34`  
		Last Modified: Thu, 02 Oct 2025 01:18:02 GMT  
		Size: 52.1 MB (52148270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107e1343051be61a638672025678478109f16777345ea0f686a6ff3acf350001`  
		Last Modified: Thu, 02 Oct 2025 01:17:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8638ac656cf58a686e913d6ff24b9568968c949eb31951f04bdfa835ef450334`  
		Last Modified: Thu, 02 Oct 2025 01:17:59 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1410e3d94994363dbf5de1ff67c7f1b3219ab2020cfe9b801486f619d1001f`  
		Last Modified: Thu, 02 Oct 2025 03:20:35 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7358e4ce951b86e608ebdcee54373085a8fba3b94e46edd843bbf2228011a7db`  
		Last Modified: Thu, 02 Oct 2025 03:36:39 GMT  
		Size: 354.4 MB (354408369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7405c0fc1faf3b1a089a9cb3e78e03aba25f3b2d59a437344165cf606000c92`  
		Last Modified: Thu, 02 Oct 2025 03:20:37 GMT  
		Size: 3.4 MB (3405535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d5e1ea95a074da15cf7191e1810ca7051e32e79a3514b3bd349a1d0733af51`  
		Last Modified: Thu, 02 Oct 2025 03:20:36 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3325a664c74e3f0e671182ade34050ffea360d1601c09d63c6cdee133f7a3220`  
		Last Modified: Thu, 02 Oct 2025 03:20:36 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.33` - unknown; unknown

```console
$ docker pull liquibase@sha256:4ada81f2d603d3ef1835bac437bf75111e0516aa8965bf1da2d950ba5c4fa090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940406a2d8b11ae207018664d2cd0e7c59718f0ab543a37727211f815f840c15`

```dockerfile
```

-	Layers:
	-	`sha256:fc5c170520b1a9982d25642086a80f10d043c49b3748e8a9ba487dff5cb78a4f`  
		Last Modified: Thu, 02 Oct 2025 03:39:22 GMT  
		Size: 3.9 MB (3940161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a501041b287a3b0cb9c165764bef9db54480beb7ce574f0f37f455bcd6663cd4`  
		Last Modified: Thu, 02 Oct 2025 03:39:23 GMT  
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
$ docker pull liquibase@sha256:25328ef2d762e15d02c733b43b6f142ab4a5071ffd985ad002ba9010a20fb2af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.33.0` - linux; amd64

```console
$ docker pull liquibase@sha256:b0ed2dedd9e37f8c456ff7e9d8e65fe19ab0d59ca312f22e634d082402adccb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.8 MB (456768101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da97367ae79395efb50f55eae6a1a9ec4cca5943ebc489850ea529795c7001dd`
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
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
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
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a55b01e3ac44fd314137f34c2089a82e6266936a8a7a2e28ce60499bd91791`  
		Last Modified: Thu, 02 Oct 2025 05:02:00 GMT  
		Size: 16.2 MB (16150303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a412a34a90e9c7e90943ae8125908b2321b7e4265ad339c99a628dd2d704027`  
		Last Modified: Thu, 02 Oct 2025 05:02:09 GMT  
		Size: 53.0 MB (52968679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b072ed4655dd0505a0227f4b39e45856d97fdad63b0386f018b36594098ce12a`  
		Last Modified: Thu, 02 Oct 2025 05:02:05 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b49e514d0b6e3b401a83663a81353ef5944c24666c9373cb6f21fbbb5c9800f`  
		Last Modified: Thu, 02 Oct 2025 05:02:05 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35221078213246ed213979b051f7352acab773f3501823f90502c6c59ba1352`  
		Last Modified: Thu, 02 Oct 2025 09:29:19 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3fe4355dc61c2e2f3ec927f57443e76a97b667ec20cc17db59ff9a4081f0da`  
		Last Modified: Thu, 02 Oct 2025 09:35:55 GMT  
		Size: 354.4 MB (354408366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db2464c42dbe58582b4125b20061999a9941db49525a2da6573db928b528fc9`  
		Last Modified: Thu, 02 Oct 2025 09:29:22 GMT  
		Size: 3.7 MB (3696523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db80c9dcc24c0753a13883b33f75cafeabf18f2e7e95083c62e687b604ac315`  
		Last Modified: Thu, 02 Oct 2025 09:29:19 GMT  
		Size: 470.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767283bebb6e9262d931c887ad925bc5dbb11c2a7965b873307a88375aec75c0`  
		Last Modified: Thu, 02 Oct 2025 09:29:19 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.33.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:46fd20674342c12c43451e065e5bee321c962a0f9be5fe1bc3567377a7e06ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ea58a7a86c97613c2850168422d8901d57334a67ab5c3b36406aa4e7c98467`

```dockerfile
```

-	Layers:
	-	`sha256:22e5f6121c6022c49f183f0600fb25e868c641fbd3146a9bb35c2622b3614606`  
		Last Modified: Thu, 02 Oct 2025 09:39:26 GMT  
		Size: 3.9 MB (3940493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95905a9724883421b65b84d34d94c44adfeb1fe5def4abc40b4ab12db06abc6d`  
		Last Modified: Thu, 02 Oct 2025 09:39:27 GMT  
		Size: 24.4 KB (24423 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.33.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:9b4224d6fd1179b234101a919ee9c14f78d1eb90763d586c69d84705ada1a344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.4 MB (453418414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50db44ae4a907e0beb5e90d9b52f418b3f65cc8c86fceb4fb122cf8d315485a7`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467d494d86601559a7c580a845a24d7c3c4e03397a8e6172f73c42ceaea86b78`  
		Last Modified: Thu, 02 Oct 2025 01:17:23 GMT  
		Size: 16.1 MB (16065710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698ba22d0a21bf3b9a2595bf748316d27c7cbfa7fb014888aa87919ba1ab6b34`  
		Last Modified: Thu, 02 Oct 2025 01:18:02 GMT  
		Size: 52.1 MB (52148270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107e1343051be61a638672025678478109f16777345ea0f686a6ff3acf350001`  
		Last Modified: Thu, 02 Oct 2025 01:17:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8638ac656cf58a686e913d6ff24b9568968c949eb31951f04bdfa835ef450334`  
		Last Modified: Thu, 02 Oct 2025 01:17:59 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1410e3d94994363dbf5de1ff67c7f1b3219ab2020cfe9b801486f619d1001f`  
		Last Modified: Thu, 02 Oct 2025 03:20:35 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7358e4ce951b86e608ebdcee54373085a8fba3b94e46edd843bbf2228011a7db`  
		Last Modified: Thu, 02 Oct 2025 03:36:39 GMT  
		Size: 354.4 MB (354408369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7405c0fc1faf3b1a089a9cb3e78e03aba25f3b2d59a437344165cf606000c92`  
		Last Modified: Thu, 02 Oct 2025 03:20:37 GMT  
		Size: 3.4 MB (3405535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d5e1ea95a074da15cf7191e1810ca7051e32e79a3514b3bd349a1d0733af51`  
		Last Modified: Thu, 02 Oct 2025 03:20:36 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3325a664c74e3f0e671182ade34050ffea360d1601c09d63c6cdee133f7a3220`  
		Last Modified: Thu, 02 Oct 2025 03:20:36 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.33.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:4ada81f2d603d3ef1835bac437bf75111e0516aa8965bf1da2d950ba5c4fa090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940406a2d8b11ae207018664d2cd0e7c59718f0ab543a37727211f815f840c15`

```dockerfile
```

-	Layers:
	-	`sha256:fc5c170520b1a9982d25642086a80f10d043c49b3748e8a9ba487dff5cb78a4f`  
		Last Modified: Thu, 02 Oct 2025 03:39:22 GMT  
		Size: 3.9 MB (3940161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a501041b287a3b0cb9c165764bef9db54480beb7ce574f0f37f455bcd6663cd4`  
		Last Modified: Thu, 02 Oct 2025 03:39:23 GMT  
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
$ docker pull liquibase@sha256:25328ef2d762e15d02c733b43b6f142ab4a5071ffd985ad002ba9010a20fb2af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:b0ed2dedd9e37f8c456ff7e9d8e65fe19ab0d59ca312f22e634d082402adccb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.8 MB (456768101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da97367ae79395efb50f55eae6a1a9ec4cca5943ebc489850ea529795c7001dd`
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
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
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
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a55b01e3ac44fd314137f34c2089a82e6266936a8a7a2e28ce60499bd91791`  
		Last Modified: Thu, 02 Oct 2025 05:02:00 GMT  
		Size: 16.2 MB (16150303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a412a34a90e9c7e90943ae8125908b2321b7e4265ad339c99a628dd2d704027`  
		Last Modified: Thu, 02 Oct 2025 05:02:09 GMT  
		Size: 53.0 MB (52968679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b072ed4655dd0505a0227f4b39e45856d97fdad63b0386f018b36594098ce12a`  
		Last Modified: Thu, 02 Oct 2025 05:02:05 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b49e514d0b6e3b401a83663a81353ef5944c24666c9373cb6f21fbbb5c9800f`  
		Last Modified: Thu, 02 Oct 2025 05:02:05 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35221078213246ed213979b051f7352acab773f3501823f90502c6c59ba1352`  
		Last Modified: Thu, 02 Oct 2025 09:29:19 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3fe4355dc61c2e2f3ec927f57443e76a97b667ec20cc17db59ff9a4081f0da`  
		Last Modified: Thu, 02 Oct 2025 09:35:55 GMT  
		Size: 354.4 MB (354408366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db2464c42dbe58582b4125b20061999a9941db49525a2da6573db928b528fc9`  
		Last Modified: Thu, 02 Oct 2025 09:29:22 GMT  
		Size: 3.7 MB (3696523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db80c9dcc24c0753a13883b33f75cafeabf18f2e7e95083c62e687b604ac315`  
		Last Modified: Thu, 02 Oct 2025 09:29:19 GMT  
		Size: 470.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767283bebb6e9262d931c887ad925bc5dbb11c2a7965b873307a88375aec75c0`  
		Last Modified: Thu, 02 Oct 2025 09:29:19 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:46fd20674342c12c43451e065e5bee321c962a0f9be5fe1bc3567377a7e06ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ea58a7a86c97613c2850168422d8901d57334a67ab5c3b36406aa4e7c98467`

```dockerfile
```

-	Layers:
	-	`sha256:22e5f6121c6022c49f183f0600fb25e868c641fbd3146a9bb35c2622b3614606`  
		Last Modified: Thu, 02 Oct 2025 09:39:26 GMT  
		Size: 3.9 MB (3940493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95905a9724883421b65b84d34d94c44adfeb1fe5def4abc40b4ab12db06abc6d`  
		Last Modified: Thu, 02 Oct 2025 09:39:27 GMT  
		Size: 24.4 KB (24423 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:9b4224d6fd1179b234101a919ee9c14f78d1eb90763d586c69d84705ada1a344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.4 MB (453418414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50db44ae4a907e0beb5e90d9b52f418b3f65cc8c86fceb4fb122cf8d315485a7`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467d494d86601559a7c580a845a24d7c3c4e03397a8e6172f73c42ceaea86b78`  
		Last Modified: Thu, 02 Oct 2025 01:17:23 GMT  
		Size: 16.1 MB (16065710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698ba22d0a21bf3b9a2595bf748316d27c7cbfa7fb014888aa87919ba1ab6b34`  
		Last Modified: Thu, 02 Oct 2025 01:18:02 GMT  
		Size: 52.1 MB (52148270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107e1343051be61a638672025678478109f16777345ea0f686a6ff3acf350001`  
		Last Modified: Thu, 02 Oct 2025 01:17:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8638ac656cf58a686e913d6ff24b9568968c949eb31951f04bdfa835ef450334`  
		Last Modified: Thu, 02 Oct 2025 01:17:59 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1410e3d94994363dbf5de1ff67c7f1b3219ab2020cfe9b801486f619d1001f`  
		Last Modified: Thu, 02 Oct 2025 03:20:35 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7358e4ce951b86e608ebdcee54373085a8fba3b94e46edd843bbf2228011a7db`  
		Last Modified: Thu, 02 Oct 2025 03:36:39 GMT  
		Size: 354.4 MB (354408369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7405c0fc1faf3b1a089a9cb3e78e03aba25f3b2d59a437344165cf606000c92`  
		Last Modified: Thu, 02 Oct 2025 03:20:37 GMT  
		Size: 3.4 MB (3405535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d5e1ea95a074da15cf7191e1810ca7051e32e79a3514b3bd349a1d0733af51`  
		Last Modified: Thu, 02 Oct 2025 03:20:36 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3325a664c74e3f0e671182ade34050ffea360d1601c09d63c6cdee133f7a3220`  
		Last Modified: Thu, 02 Oct 2025 03:20:36 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:4ada81f2d603d3ef1835bac437bf75111e0516aa8965bf1da2d950ba5c4fa090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940406a2d8b11ae207018664d2cd0e7c59718f0ab543a37727211f815f840c15`

```dockerfile
```

-	Layers:
	-	`sha256:fc5c170520b1a9982d25642086a80f10d043c49b3748e8a9ba487dff5cb78a4f`  
		Last Modified: Thu, 02 Oct 2025 03:39:22 GMT  
		Size: 3.9 MB (3940161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a501041b287a3b0cb9c165764bef9db54480beb7ce574f0f37f455bcd6663cd4`  
		Last Modified: Thu, 02 Oct 2025 03:39:23 GMT  
		Size: 24.5 KB (24545 bytes)  
		MIME: application/vnd.in-toto+json
