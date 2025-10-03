<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `liquibase`

-	[`liquibase:5.0`](#liquibase50)
-	[`liquibase:5.0-alpine`](#liquibase50-alpine)
-	[`liquibase:5.0.0`](#liquibase500)
-	[`liquibase:5.0.0-alpine`](#liquibase500-alpine)
-	[`liquibase:alpine`](#liquibasealpine)
-	[`liquibase:latest`](#liquibaselatest)

## `liquibase:5.0`

```console
$ docker pull liquibase@sha256:dcc5f6e15e681949733fc16147dfce92355a18be7bd1f0954930b933ce1bb0a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0` - linux; amd64

```console
$ docker pull liquibase@sha256:6a51e909caeea347778c5ca048d354dc36d99292d1c3aee438a0b1beecd31365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111097910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de00fb1bd0d6a2989057f3cef4a82d86ae063c1c89fad0ebd9d2c34412a5360a`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
WORKDIR /liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LIQUIBASE_VERSION=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_VERSION=0.2.14
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.version=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ENV LIQUIBASE_HOME=/liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENV DOCKER_LIQUIBASE=true
# Tue, 30 Sep 2025 15:04:02 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
COPY liquibase.docker.properties ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
USER liquibase:liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
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
	-	`sha256:be77879968105c33adaeebbf24e1475d08f4e74c75bece9895773840d9c1f5a0`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d618df64695f93607e4efc49609ce242152313e07d99c80c52fb854ce8ef6d`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 8.7 MB (8669274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b3d2504c6a100aea7f9eed94630f5e22b180f3defdf43b1faf5a98b5ba9cc0`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 3.8 MB (3764456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2bf6d56447fe2494cef880d7ba65aa9b5bc23ded8a3ff773e0d5cedd234c74`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40de97febdb451a1495c21d97c84bacd6a0144d0a8c22ba6f312d1b98b678ee`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:7181ee7c2c63b6b5d50bf4b54d46c04e2b1eb3d3ad2356a17c91e0c75fd6c533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410e4dbca62a07bdc181af6292d2a4ba123801050492779d3487bcbf706e254a`

```dockerfile
```

-	Layers:
	-	`sha256:e1d8e3b4d797abb9a9657de6b7eab36068a851f0be86e6de3ba5a48b986a8846`  
		Last Modified: Fri, 03 Oct 2025 00:39:23 GMT  
		Size: 3.9 MB (3897731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:106a6b991adbe3326462298b8b3155874dc3b04996b47a7b74419d30a02c3ca3`  
		Last Modified: Fri, 03 Oct 2025 00:39:24 GMT  
		Size: 24.4 KB (24363 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:18d1ae08d229a388bd50e2c7d03c61695579d4c7db7785391ff7b9f659370c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107715970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef8d1794d87016d6a0431694a69478045fe658e60a9973a0e16f94ee634f640`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
WORKDIR /liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LIQUIBASE_VERSION=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_VERSION=0.2.14
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.version=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ENV LIQUIBASE_HOME=/liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENV DOCKER_LIQUIBASE=true
# Tue, 30 Sep 2025 15:04:02 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
COPY liquibase.docker.properties ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
USER liquibase:liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
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
	-	`sha256:b80be112527499995d28a958896162c9fbc4095e7ccec3ff4aeb5142e99e621d`  
		Last Modified: Thu, 02 Oct 2025 22:16:02 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f945d13e904bd226bfd39e8bcadc52c1479506028e01340e169333c7c1d2b6ec`  
		Last Modified: Fri, 03 Oct 2025 01:41:21 GMT  
		Size: 8.7 MB (8669275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff262dbf270b42e457118e474b8905a19b8073b271af9850212a77027e09782d`  
		Last Modified: Thu, 02 Oct 2025 22:16:06 GMT  
		Size: 3.4 MB (3441228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41590a39c7b02128c59731b508966f027f2c97b2d9071d52ef4980b1507a628`  
		Last Modified: Thu, 02 Oct 2025 22:16:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11350c52ca5dfb25fbcb237e0906418de1a214848c278b266e755bd0681f713d`  
		Last Modified: Thu, 02 Oct 2025 22:16:15 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:058baeebf8d9ebfa467f129cd0989030429be156b37545c18719b3cefc47b8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bf019941c1f71f4c370539ffe98c4af2ff0d614e5546fad8cd2b196e09b05a`

```dockerfile
```

-	Layers:
	-	`sha256:805a68f760bef600479c4ef9ee2743e7b1a18763ea4b2883aa02134f7d8f5dfb`  
		Last Modified: Fri, 03 Oct 2025 00:39:28 GMT  
		Size: 3.9 MB (3897399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0befed28379558c7fc399129fda3e4746a2efe6ef3be9e81812a07c8ab6cdd6d`  
		Last Modified: Fri, 03 Oct 2025 00:39:29 GMT  
		Size: 24.5 KB (24485 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:5.0-alpine`

```console
$ docker pull liquibase@sha256:e6a9cdafe35fffa64c2745ae983e4d056bdae8b15303a7960e99327475f088f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:9e7039a4ded4044950759e5070a477d2f10b8aad5ad53d9df62ee0358491e57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (84029824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bf59a8a4e9bd7a622b69f6d3449349e18dbc9c6deeb909f60e8b84666ce109`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
WORKDIR /liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LIQUIBASE_VERSION=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_VERSION=0.2.14
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.version=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ENV LIQUIBASE_HOME=/liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENV DOCKER_LIQUIBASE=true
# Tue, 30 Sep 2025 15:04:02 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
COPY liquibase.docker.properties ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
USER liquibase:liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518e1aa708cfa18cfedc614a413d1f831a7f3f50fc80c1c06623c581211c1fac`  
		Last Modified: Thu, 02 Oct 2025 21:54:16 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426176daf2496e381d4467270fd5db89d14f7d3f5e0b39b98b46f5341ada49f4`  
		Last Modified: Thu, 02 Oct 2025 21:54:28 GMT  
		Size: 67.9 MB (67852312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9816a16c8d6a36b6eaf6abbc2c941004fe3c9790c0d9d0c2628c4c71bbd33b8`  
		Last Modified: Thu, 02 Oct 2025 21:54:17 GMT  
		Size: 8.7 MB (8691850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b25550aa5253d74145a1e0bd78ffacf66f48905e96528d20cb4a6317ff1053a`  
		Last Modified: Thu, 02 Oct 2025 21:54:16 GMT  
		Size: 3.7 MB (3683404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d5d6a359711114f103a92c481f9334eb7c9c93fd090d02c0b839964247d7e9`  
		Last Modified: Thu, 02 Oct 2025 21:54:16 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c56fcb591d40668e987df1ec65a7a381f1a1e0d1f484aa8e2a7282198a7cd2`  
		Last Modified: Thu, 02 Oct 2025 21:54:16 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:be1ebf379892599f922f4408060627b2acf310be521869b12f6ad52a6d808a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.5 KB (381452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2700ed0ba5f147ffb5c314bf2ed7b5d0c630286967a352fdb4f421b433ad61c`

```dockerfile
```

-	Layers:
	-	`sha256:4504ea88ec018f7557bd1b650ae11465275a5efd0195c5e3a3457917301c16f6`  
		Last Modified: Fri, 03 Oct 2025 00:39:34 GMT  
		Size: 359.8 KB (359751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd21a4b48cf0e6fc2421795469ca693c9aa93544078ccb621e25fb4b6d4f75ad`  
		Last Modified: Fri, 03 Oct 2025 00:39:34 GMT  
		Size: 21.7 KB (21701 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:9f15a21dcee2dccd0a772bf89f3c77402011ca6ba2848d2917a3b567532eda4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83035839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d94d835cb88c75d0cf83a58447638a5996a53f0333e508a0c99ee0c7a1775c`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
WORKDIR /liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LIQUIBASE_VERSION=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_VERSION=0.2.14
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.version=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ENV LIQUIBASE_HOME=/liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENV DOCKER_LIQUIBASE=true
# Tue, 30 Sep 2025 15:04:02 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
COPY liquibase.docker.properties ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
USER liquibase:liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa20d2352397589c2f8f52aeb2dbc68be4f0cd227eeb0f3c46880f43e71dada2`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be19e04180cb6378c995449285fb86d1c424c1b0de8af3b103899c32e8f599b2`  
		Last Modified: Thu, 02 Oct 2025 21:54:04 GMT  
		Size: 66.9 MB (66851026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccd3b313a5c3fcda2e1d12f6b3ea46b2a68e19b026059e739d2e776930299a8`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 8.7 MB (8691817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8672aa7503754f3920446ceffcfc7ab5494d5941382d85e0226f0e4ac4d1dd07`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 3.4 MB (3359676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56c28097446bb852fe63740bf96f333e088aeb9a1c7dc128a4944143476f48b`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e642049143d1f47758d3ded89c3fa34ac26983d28e1f9273e8f4d0a0fb498032`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:2432a2473a72e23e3a0adbeda86facab0d283e42b73cd11910e2df40d4606136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.8 KB (380835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7331577b46c897354b313efaec0140cf16ebab7497ce5ca90d6626f0da38cec2`

```dockerfile
```

-	Layers:
	-	`sha256:121388263faeb99a5291371592a303989a928f591d06c08d4a0d79f8aab0ddc4`  
		Last Modified: Fri, 03 Oct 2025 00:39:38 GMT  
		Size: 359.0 KB (358998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f62d22505aa473ad00351aa6a2e5c4e1a217646bf280e5d33db44c79f582f463`  
		Last Modified: Fri, 03 Oct 2025 00:39:39 GMT  
		Size: 21.8 KB (21837 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:5.0.0`

```console
$ docker pull liquibase@sha256:dcc5f6e15e681949733fc16147dfce92355a18be7bd1f0954930b933ce1bb0a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0.0` - linux; amd64

```console
$ docker pull liquibase@sha256:6a51e909caeea347778c5ca048d354dc36d99292d1c3aee438a0b1beecd31365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111097910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de00fb1bd0d6a2989057f3cef4a82d86ae063c1c89fad0ebd9d2c34412a5360a`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
WORKDIR /liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LIQUIBASE_VERSION=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_VERSION=0.2.14
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.version=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ENV LIQUIBASE_HOME=/liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENV DOCKER_LIQUIBASE=true
# Tue, 30 Sep 2025 15:04:02 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
COPY liquibase.docker.properties ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
USER liquibase:liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
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
	-	`sha256:be77879968105c33adaeebbf24e1475d08f4e74c75bece9895773840d9c1f5a0`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d618df64695f93607e4efc49609ce242152313e07d99c80c52fb854ce8ef6d`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 8.7 MB (8669274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b3d2504c6a100aea7f9eed94630f5e22b180f3defdf43b1faf5a98b5ba9cc0`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 3.8 MB (3764456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2bf6d56447fe2494cef880d7ba65aa9b5bc23ded8a3ff773e0d5cedd234c74`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40de97febdb451a1495c21d97c84bacd6a0144d0a8c22ba6f312d1b98b678ee`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:7181ee7c2c63b6b5d50bf4b54d46c04e2b1eb3d3ad2356a17c91e0c75fd6c533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410e4dbca62a07bdc181af6292d2a4ba123801050492779d3487bcbf706e254a`

```dockerfile
```

-	Layers:
	-	`sha256:e1d8e3b4d797abb9a9657de6b7eab36068a851f0be86e6de3ba5a48b986a8846`  
		Last Modified: Fri, 03 Oct 2025 00:39:23 GMT  
		Size: 3.9 MB (3897731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:106a6b991adbe3326462298b8b3155874dc3b04996b47a7b74419d30a02c3ca3`  
		Last Modified: Fri, 03 Oct 2025 00:39:24 GMT  
		Size: 24.4 KB (24363 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:18d1ae08d229a388bd50e2c7d03c61695579d4c7db7785391ff7b9f659370c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107715970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef8d1794d87016d6a0431694a69478045fe658e60a9973a0e16f94ee634f640`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
WORKDIR /liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LIQUIBASE_VERSION=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_VERSION=0.2.14
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.version=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ENV LIQUIBASE_HOME=/liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENV DOCKER_LIQUIBASE=true
# Tue, 30 Sep 2025 15:04:02 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
COPY liquibase.docker.properties ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
USER liquibase:liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
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
	-	`sha256:b80be112527499995d28a958896162c9fbc4095e7ccec3ff4aeb5142e99e621d`  
		Last Modified: Thu, 02 Oct 2025 22:16:02 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f945d13e904bd226bfd39e8bcadc52c1479506028e01340e169333c7c1d2b6ec`  
		Last Modified: Fri, 03 Oct 2025 01:41:21 GMT  
		Size: 8.7 MB (8669275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff262dbf270b42e457118e474b8905a19b8073b271af9850212a77027e09782d`  
		Last Modified: Thu, 02 Oct 2025 22:16:06 GMT  
		Size: 3.4 MB (3441228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41590a39c7b02128c59731b508966f027f2c97b2d9071d52ef4980b1507a628`  
		Last Modified: Thu, 02 Oct 2025 22:16:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11350c52ca5dfb25fbcb237e0906418de1a214848c278b266e755bd0681f713d`  
		Last Modified: Thu, 02 Oct 2025 22:16:15 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:058baeebf8d9ebfa467f129cd0989030429be156b37545c18719b3cefc47b8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bf019941c1f71f4c370539ffe98c4af2ff0d614e5546fad8cd2b196e09b05a`

```dockerfile
```

-	Layers:
	-	`sha256:805a68f760bef600479c4ef9ee2743e7b1a18763ea4b2883aa02134f7d8f5dfb`  
		Last Modified: Fri, 03 Oct 2025 00:39:28 GMT  
		Size: 3.9 MB (3897399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0befed28379558c7fc399129fda3e4746a2efe6ef3be9e81812a07c8ab6cdd6d`  
		Last Modified: Fri, 03 Oct 2025 00:39:29 GMT  
		Size: 24.5 KB (24485 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:5.0.0-alpine`

```console
$ docker pull liquibase@sha256:e6a9cdafe35fffa64c2745ae983e4d056bdae8b15303a7960e99327475f088f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0.0-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:9e7039a4ded4044950759e5070a477d2f10b8aad5ad53d9df62ee0358491e57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (84029824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bf59a8a4e9bd7a622b69f6d3449349e18dbc9c6deeb909f60e8b84666ce109`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
WORKDIR /liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LIQUIBASE_VERSION=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_VERSION=0.2.14
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.version=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ENV LIQUIBASE_HOME=/liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENV DOCKER_LIQUIBASE=true
# Tue, 30 Sep 2025 15:04:02 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
COPY liquibase.docker.properties ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
USER liquibase:liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518e1aa708cfa18cfedc614a413d1f831a7f3f50fc80c1c06623c581211c1fac`  
		Last Modified: Thu, 02 Oct 2025 21:54:16 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426176daf2496e381d4467270fd5db89d14f7d3f5e0b39b98b46f5341ada49f4`  
		Last Modified: Thu, 02 Oct 2025 21:54:28 GMT  
		Size: 67.9 MB (67852312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9816a16c8d6a36b6eaf6abbc2c941004fe3c9790c0d9d0c2628c4c71bbd33b8`  
		Last Modified: Thu, 02 Oct 2025 21:54:17 GMT  
		Size: 8.7 MB (8691850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b25550aa5253d74145a1e0bd78ffacf66f48905e96528d20cb4a6317ff1053a`  
		Last Modified: Thu, 02 Oct 2025 21:54:16 GMT  
		Size: 3.7 MB (3683404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d5d6a359711114f103a92c481f9334eb7c9c93fd090d02c0b839964247d7e9`  
		Last Modified: Thu, 02 Oct 2025 21:54:16 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c56fcb591d40668e987df1ec65a7a381f1a1e0d1f484aa8e2a7282198a7cd2`  
		Last Modified: Thu, 02 Oct 2025 21:54:16 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:be1ebf379892599f922f4408060627b2acf310be521869b12f6ad52a6d808a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.5 KB (381452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2700ed0ba5f147ffb5c314bf2ed7b5d0c630286967a352fdb4f421b433ad61c`

```dockerfile
```

-	Layers:
	-	`sha256:4504ea88ec018f7557bd1b650ae11465275a5efd0195c5e3a3457917301c16f6`  
		Last Modified: Fri, 03 Oct 2025 00:39:34 GMT  
		Size: 359.8 KB (359751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd21a4b48cf0e6fc2421795469ca693c9aa93544078ccb621e25fb4b6d4f75ad`  
		Last Modified: Fri, 03 Oct 2025 00:39:34 GMT  
		Size: 21.7 KB (21701 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0.0-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:9f15a21dcee2dccd0a772bf89f3c77402011ca6ba2848d2917a3b567532eda4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83035839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d94d835cb88c75d0cf83a58447638a5996a53f0333e508a0c99ee0c7a1775c`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
WORKDIR /liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LIQUIBASE_VERSION=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_VERSION=0.2.14
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.version=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ENV LIQUIBASE_HOME=/liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENV DOCKER_LIQUIBASE=true
# Tue, 30 Sep 2025 15:04:02 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
COPY liquibase.docker.properties ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
USER liquibase:liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa20d2352397589c2f8f52aeb2dbc68be4f0cd227eeb0f3c46880f43e71dada2`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be19e04180cb6378c995449285fb86d1c424c1b0de8af3b103899c32e8f599b2`  
		Last Modified: Thu, 02 Oct 2025 21:54:04 GMT  
		Size: 66.9 MB (66851026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccd3b313a5c3fcda2e1d12f6b3ea46b2a68e19b026059e739d2e776930299a8`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 8.7 MB (8691817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8672aa7503754f3920446ceffcfc7ab5494d5941382d85e0226f0e4ac4d1dd07`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 3.4 MB (3359676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56c28097446bb852fe63740bf96f333e088aeb9a1c7dc128a4944143476f48b`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e642049143d1f47758d3ded89c3fa34ac26983d28e1f9273e8f4d0a0fb498032`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:2432a2473a72e23e3a0adbeda86facab0d283e42b73cd11910e2df40d4606136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.8 KB (380835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7331577b46c897354b313efaec0140cf16ebab7497ce5ca90d6626f0da38cec2`

```dockerfile
```

-	Layers:
	-	`sha256:121388263faeb99a5291371592a303989a928f591d06c08d4a0d79f8aab0ddc4`  
		Last Modified: Fri, 03 Oct 2025 00:39:38 GMT  
		Size: 359.0 KB (358998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f62d22505aa473ad00351aa6a2e5c4e1a217646bf280e5d33db44c79f582f463`  
		Last Modified: Fri, 03 Oct 2025 00:39:39 GMT  
		Size: 21.8 KB (21837 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:e6a9cdafe35fffa64c2745ae983e4d056bdae8b15303a7960e99327475f088f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:9e7039a4ded4044950759e5070a477d2f10b8aad5ad53d9df62ee0358491e57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (84029824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bf59a8a4e9bd7a622b69f6d3449349e18dbc9c6deeb909f60e8b84666ce109`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
WORKDIR /liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LIQUIBASE_VERSION=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_VERSION=0.2.14
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.version=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ENV LIQUIBASE_HOME=/liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENV DOCKER_LIQUIBASE=true
# Tue, 30 Sep 2025 15:04:02 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
COPY liquibase.docker.properties ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
USER liquibase:liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518e1aa708cfa18cfedc614a413d1f831a7f3f50fc80c1c06623c581211c1fac`  
		Last Modified: Thu, 02 Oct 2025 21:54:16 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426176daf2496e381d4467270fd5db89d14f7d3f5e0b39b98b46f5341ada49f4`  
		Last Modified: Thu, 02 Oct 2025 21:54:28 GMT  
		Size: 67.9 MB (67852312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9816a16c8d6a36b6eaf6abbc2c941004fe3c9790c0d9d0c2628c4c71bbd33b8`  
		Last Modified: Thu, 02 Oct 2025 21:54:17 GMT  
		Size: 8.7 MB (8691850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b25550aa5253d74145a1e0bd78ffacf66f48905e96528d20cb4a6317ff1053a`  
		Last Modified: Thu, 02 Oct 2025 21:54:16 GMT  
		Size: 3.7 MB (3683404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d5d6a359711114f103a92c481f9334eb7c9c93fd090d02c0b839964247d7e9`  
		Last Modified: Thu, 02 Oct 2025 21:54:16 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c56fcb591d40668e987df1ec65a7a381f1a1e0d1f484aa8e2a7282198a7cd2`  
		Last Modified: Thu, 02 Oct 2025 21:54:16 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:be1ebf379892599f922f4408060627b2acf310be521869b12f6ad52a6d808a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.5 KB (381452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2700ed0ba5f147ffb5c314bf2ed7b5d0c630286967a352fdb4f421b433ad61c`

```dockerfile
```

-	Layers:
	-	`sha256:4504ea88ec018f7557bd1b650ae11465275a5efd0195c5e3a3457917301c16f6`  
		Last Modified: Fri, 03 Oct 2025 00:39:34 GMT  
		Size: 359.8 KB (359751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd21a4b48cf0e6fc2421795469ca693c9aa93544078ccb621e25fb4b6d4f75ad`  
		Last Modified: Fri, 03 Oct 2025 00:39:34 GMT  
		Size: 21.7 KB (21701 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:9f15a21dcee2dccd0a772bf89f3c77402011ca6ba2848d2917a3b567532eda4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83035839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d94d835cb88c75d0cf83a58447638a5996a53f0333e508a0c99ee0c7a1775c`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
WORKDIR /liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LIQUIBASE_VERSION=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_VERSION=0.2.14
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.version=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ENV LIQUIBASE_HOME=/liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENV DOCKER_LIQUIBASE=true
# Tue, 30 Sep 2025 15:04:02 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
COPY liquibase.docker.properties ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
USER liquibase:liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa20d2352397589c2f8f52aeb2dbc68be4f0cd227eeb0f3c46880f43e71dada2`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be19e04180cb6378c995449285fb86d1c424c1b0de8af3b103899c32e8f599b2`  
		Last Modified: Thu, 02 Oct 2025 21:54:04 GMT  
		Size: 66.9 MB (66851026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccd3b313a5c3fcda2e1d12f6b3ea46b2a68e19b026059e739d2e776930299a8`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 8.7 MB (8691817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8672aa7503754f3920446ceffcfc7ab5494d5941382d85e0226f0e4ac4d1dd07`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 3.4 MB (3359676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56c28097446bb852fe63740bf96f333e088aeb9a1c7dc128a4944143476f48b`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e642049143d1f47758d3ded89c3fa34ac26983d28e1f9273e8f4d0a0fb498032`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:2432a2473a72e23e3a0adbeda86facab0d283e42b73cd11910e2df40d4606136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.8 KB (380835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7331577b46c897354b313efaec0140cf16ebab7497ce5ca90d6626f0da38cec2`

```dockerfile
```

-	Layers:
	-	`sha256:121388263faeb99a5291371592a303989a928f591d06c08d4a0d79f8aab0ddc4`  
		Last Modified: Fri, 03 Oct 2025 00:39:38 GMT  
		Size: 359.0 KB (358998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f62d22505aa473ad00351aa6a2e5c4e1a217646bf280e5d33db44c79f582f463`  
		Last Modified: Fri, 03 Oct 2025 00:39:39 GMT  
		Size: 21.8 KB (21837 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:latest`

```console
$ docker pull liquibase@sha256:dcc5f6e15e681949733fc16147dfce92355a18be7bd1f0954930b933ce1bb0a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:6a51e909caeea347778c5ca048d354dc36d99292d1c3aee438a0b1beecd31365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111097910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de00fb1bd0d6a2989057f3cef4a82d86ae063c1c89fad0ebd9d2c34412a5360a`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
WORKDIR /liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LIQUIBASE_VERSION=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_VERSION=0.2.14
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.version=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ENV LIQUIBASE_HOME=/liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENV DOCKER_LIQUIBASE=true
# Tue, 30 Sep 2025 15:04:02 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
COPY liquibase.docker.properties ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
USER liquibase:liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
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
	-	`sha256:be77879968105c33adaeebbf24e1475d08f4e74c75bece9895773840d9c1f5a0`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d618df64695f93607e4efc49609ce242152313e07d99c80c52fb854ce8ef6d`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 8.7 MB (8669274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b3d2504c6a100aea7f9eed94630f5e22b180f3defdf43b1faf5a98b5ba9cc0`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 3.8 MB (3764456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2bf6d56447fe2494cef880d7ba65aa9b5bc23ded8a3ff773e0d5cedd234c74`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40de97febdb451a1495c21d97c84bacd6a0144d0a8c22ba6f312d1b98b678ee`  
		Last Modified: Thu, 02 Oct 2025 21:53:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:7181ee7c2c63b6b5d50bf4b54d46c04e2b1eb3d3ad2356a17c91e0c75fd6c533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410e4dbca62a07bdc181af6292d2a4ba123801050492779d3487bcbf706e254a`

```dockerfile
```

-	Layers:
	-	`sha256:e1d8e3b4d797abb9a9657de6b7eab36068a851f0be86e6de3ba5a48b986a8846`  
		Last Modified: Fri, 03 Oct 2025 00:39:23 GMT  
		Size: 3.9 MB (3897731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:106a6b991adbe3326462298b8b3155874dc3b04996b47a7b74419d30a02c3ca3`  
		Last Modified: Fri, 03 Oct 2025 00:39:24 GMT  
		Size: 24.4 KB (24363 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:18d1ae08d229a388bd50e2c7d03c61695579d4c7db7785391ff7b9f659370c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107715970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef8d1794d87016d6a0431694a69478045fe658e60a9973a0e16f94ee634f640`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
WORKDIR /liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LIQUIBASE_VERSION=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_VERSION=0.2.14
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Tue, 30 Sep 2025 15:04:02 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.version=5.0.0
# Tue, 30 Sep 2025 15:04:02 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Tue, 30 Sep 2025 15:04:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.0 LB_SHA256=4865954d3b95032beae8cd10ccdb4a4feb7e7e684d886fd979fdbb1305fb6a44 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
ENV LIQUIBASE_HOME=/liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENV DOCKER_LIQUIBASE=true
# Tue, 30 Sep 2025 15:04:02 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
COPY liquibase.docker.properties ./ # buildkit
# Tue, 30 Sep 2025 15:04:02 GMT
USER liquibase:liquibase
# Tue, 30 Sep 2025 15:04:02 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 15:04:02 GMT
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
	-	`sha256:b80be112527499995d28a958896162c9fbc4095e7ccec3ff4aeb5142e99e621d`  
		Last Modified: Thu, 02 Oct 2025 22:16:02 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f945d13e904bd226bfd39e8bcadc52c1479506028e01340e169333c7c1d2b6ec`  
		Last Modified: Fri, 03 Oct 2025 01:41:21 GMT  
		Size: 8.7 MB (8669275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff262dbf270b42e457118e474b8905a19b8073b271af9850212a77027e09782d`  
		Last Modified: Thu, 02 Oct 2025 22:16:06 GMT  
		Size: 3.4 MB (3441228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41590a39c7b02128c59731b508966f027f2c97b2d9071d52ef4980b1507a628`  
		Last Modified: Thu, 02 Oct 2025 22:16:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11350c52ca5dfb25fbcb237e0906418de1a214848c278b266e755bd0681f713d`  
		Last Modified: Thu, 02 Oct 2025 22:16:15 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:058baeebf8d9ebfa467f129cd0989030429be156b37545c18719b3cefc47b8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bf019941c1f71f4c370539ffe98c4af2ff0d614e5546fad8cd2b196e09b05a`

```dockerfile
```

-	Layers:
	-	`sha256:805a68f760bef600479c4ef9ee2743e7b1a18763ea4b2883aa02134f7d8f5dfb`  
		Last Modified: Fri, 03 Oct 2025 00:39:28 GMT  
		Size: 3.9 MB (3897399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0befed28379558c7fc399129fda3e4746a2efe6ef3be9e81812a07c8ab6cdd6d`  
		Last Modified: Fri, 03 Oct 2025 00:39:29 GMT  
		Size: 24.5 KB (24485 bytes)  
		MIME: application/vnd.in-toto+json
