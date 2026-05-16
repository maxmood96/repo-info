<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `liquibase`

-	[`liquibase:5.0`](#liquibase50)
-	[`liquibase:5.0-alpine`](#liquibase50-alpine)
-	[`liquibase:5.0.1`](#liquibase501)
-	[`liquibase:5.0.1-alpine`](#liquibase501-alpine)
-	[`liquibase:alpine`](#liquibasealpine)
-	[`liquibase:latest`](#liquibaselatest)

## `liquibase:5.0`

```console
$ docker pull liquibase@sha256:af27034b7662d0f04a030e04d356704d1909f083466eb7e3edbfa942675afb5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0` - linux; amd64

```console
$ docker pull liquibase@sha256:1f9064427c1f4bc511a03ba125380d86252bc5336a4e5040c54f562b04136f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111450990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf1ff30aec52c8038ce39b64d9ad562bbfb3bc497f11aa90a444dfb8e490a1e`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:16:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:16:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:16:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:16:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:16:08 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 15 May 2026 21:16:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:16:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:16:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:16:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:46:16 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 15 May 2026 21:46:16 GMT
WORKDIR /liquibase
# Fri, 15 May 2026 21:46:17 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 15 May 2026 21:46:17 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 15 May 2026 21:46:17 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 15 May 2026 21:46:17 GMT
ARG LPM_VERSION=0.2.14
# Fri, 15 May 2026 21:46:17 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 15 May 2026 21:46:17 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 15 May 2026 21:46:17 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 15 May 2026 21:46:17 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 15 May 2026 21:46:17 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 15 May 2026 21:46:17 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 15 May 2026 21:46:17 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 15 May 2026 21:46:23 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 15 May 2026 21:46:23 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 15 May 2026 21:46:23 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 15 May 2026 21:46:23 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 15 May 2026 21:46:23 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 15 May 2026 21:46:23 GMT
USER liquibase:liquibase
# Fri, 15 May 2026 21:46:23 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:46:23 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5a0b6cb36c205fa8c9ef45406ef43ec624251108a5888140648cc4b33c6c55`  
		Last Modified: Fri, 15 May 2026 21:16:25 GMT  
		Size: 16.2 MB (16152745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49518c28c0b3c62624726aad57e80683d40b375b2400643477eee9fb6a278c98`  
		Last Modified: Fri, 15 May 2026 21:16:26 GMT  
		Size: 53.1 MB (53122802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41162acdcc29a9fd0a1e7740bb879e5192914f5814a43217fbc9222a7521947e`  
		Last Modified: Fri, 15 May 2026 21:16:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed0fd558ca3b009513993bf77af60ee5c03ce381c4d86b75dbda8fd93467027`  
		Last Modified: Fri, 15 May 2026 21:16:25 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e400438a03e2dceb0077e36ee13e000fd07bb2565eeee6bc7d280cad89e71c`  
		Last Modified: Fri, 15 May 2026 21:46:31 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ada9868deff67423d6e098e9a0c66934c5ae9f6395b48dde2c9f96050da96d`  
		Last Modified: Fri, 15 May 2026 21:46:32 GMT  
		Size: 8.7 MB (8665789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f76190c07012356011ad8815f52e65cffd0f3579221bf8ab1e1ca28a5db201a`  
		Last Modified: Fri, 15 May 2026 21:46:32 GMT  
		Size: 3.8 MB (3764588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32faf46f9dacb2eaed8f50b229184edec4bb84627d730a22d23d34a555198a1a`  
		Last Modified: Fri, 15 May 2026 21:46:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccbeaca5ddf6a05190168f8191384b8469b8f166faed0cbdc9aa716d528a1e2`  
		Last Modified: Fri, 15 May 2026 21:46:32 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:5e9d328a433dab4d236ce6fe2d5554dd9ff46a4933c582cf079ce7a706945188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d10444a857f3e691d461c67d6323d0be5eb2b19d8b74bf904928392ff157486`

```dockerfile
```

-	Layers:
	-	`sha256:2c9d34bcb5a672e4c16d2dac01e38c9b39c33dea01034f47ad5b47784b10b30d`  
		Last Modified: Fri, 15 May 2026 21:46:32 GMT  
		Size: 3.9 MB (3898378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:640297303e5e2752cc9dcfc8bf5e28b6a010f3912b6e4ec568cd8aa7144b35fe`  
		Last Modified: Fri, 15 May 2026 21:46:31 GMT  
		Size: 24.3 KB (24325 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:2c3c1a34dededb6be33af6689d6b56cac02e86a7fcbf5a30760299e9f6ccf3ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108113223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7070aac943df6f0c9d47f3c74a9760a0f6eba7c2f8e82461cea905fb5b580c85`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:15:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:15:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:15:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:15:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:15:49 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 15 May 2026 21:16:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:16:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:16:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:16:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:47:19 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 15 May 2026 21:47:19 GMT
WORKDIR /liquibase
# Fri, 15 May 2026 21:47:20 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 15 May 2026 21:47:20 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 15 May 2026 21:47:20 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 15 May 2026 21:47:20 GMT
ARG LPM_VERSION=0.2.14
# Fri, 15 May 2026 21:47:20 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 15 May 2026 21:47:20 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 15 May 2026 21:47:20 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 15 May 2026 21:47:20 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 15 May 2026 21:47:20 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 15 May 2026 21:47:20 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 15 May 2026 21:47:20 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 15 May 2026 21:47:28 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 15 May 2026 21:47:28 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 15 May 2026 21:47:28 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 15 May 2026 21:47:28 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 15 May 2026 21:47:28 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 15 May 2026 21:47:28 GMT
USER liquibase:liquibase
# Fri, 15 May 2026 21:47:28 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:47:28 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57ad989666c9e0dfc45a5f5a1a6ec026fe709513407113fd1d938cb641e13ca`  
		Last Modified: Fri, 15 May 2026 21:16:03 GMT  
		Size: 16.1 MB (16076205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2cd678502086cef6dba8f3127d023e5cdce1664a09143a8511e49ecc27f1c7`  
		Last Modified: Fri, 15 May 2026 21:16:28 GMT  
		Size: 52.3 MB (52314965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5318b9fee19514f8672bc32ae5b580b0eb3db47498220a70a4aee4675c2f79`  
		Last Modified: Fri, 15 May 2026 21:16:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671fab38f8b8067234c315c0ed43db9cd49bf63d19d293012dc0fb862a82caa6`  
		Last Modified: Fri, 15 May 2026 21:16:26 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694a1379d03b8e62c721cbe1d7854ec59b604d8702b37f3507c9a9fb979cd7c9`  
		Last Modified: Fri, 15 May 2026 21:47:35 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb173c2254b2bad5fc8285c3467b95be92439fac1f6219bb94c21c5ad060b1c`  
		Last Modified: Fri, 15 May 2026 21:47:36 GMT  
		Size: 8.7 MB (8665781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc95dca4874188ae4e93f64fb0a40ca4cb502cd96ccc6d5163c6a8f30952500`  
		Last Modified: Fri, 15 May 2026 21:47:36 GMT  
		Size: 3.4 MB (3441265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93817051be0bd4df635f063a14b28943d1ccb72e4c8d19b0daf0e9a5a6949ccd`  
		Last Modified: Fri, 15 May 2026 21:47:36 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7680614f5ae76c615f5bfa64884cf58bda4409f07b5bc744f380f896a4da92`  
		Last Modified: Fri, 15 May 2026 21:47:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:5b3f7a515af253389f3af38d3fcd067f1ccbc45ce8413635ba954df06e0bfd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d803cb10aa9beb4d79c355e7696a8da43d3a75bdbf46f70ba7f4371423ed0fcf`

```dockerfile
```

-	Layers:
	-	`sha256:988003bc3ab2e9a4ed6901d08251afb1ad7d5610320a5f6cab07b9217b989975`  
		Last Modified: Fri, 15 May 2026 21:47:36 GMT  
		Size: 3.9 MB (3898046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96f138f6cc4d497b1812b222b9ccadfedcd7b501765410f5e853040ce215f2cb`  
		Last Modified: Fri, 15 May 2026 21:47:35 GMT  
		Size: 24.4 KB (24448 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:5.0-alpine`

```console
$ docker pull liquibase@sha256:b131a24527add4d4eadc3300aa5cca684aa60abcd734b8d14d4a5c33b169b48b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:ac3e7f22a1f63434bec4e9ac9a459c3d14ff5fbf5b4cf23c41aaa15c8646c35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84056139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735cc69d2a472f1a3213f884cf38c27e7f07f9e006723d24b254987a2fc4c687`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:11 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 17 Apr 2026 00:30:13 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 17 Apr 2026 00:30:13 GMT
WORKDIR /liquibase
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 17 Apr 2026 00:30:15 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LPM_VERSION=0.2.14
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 17 Apr 2026 00:30:16 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 17 Apr 2026 00:30:16 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 17 Apr 2026 00:30:16 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 17 Apr 2026 00:30:16 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:30:16 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 17 Apr 2026 00:30:16 GMT
USER liquibase:liquibase
# Fri, 17 Apr 2026 00:30:16 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:16 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c968b03a929ffeffc74e342fa376b3edf03837491ffc31b33bf6355c7e7a7`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b8a26d38c62ddc3835ccdd169cdda87af0f6fc420b7a65a9ddd9f3321ca1a2`  
		Last Modified: Fri, 17 Apr 2026 00:30:30 GMT  
		Size: 67.9 MB (67873148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f7f520ce551a37b7e676a5e609d9729695d8ce07c806c1e101c9f205fecf03`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 8.7 MB (8688923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5eea34866b5479ef311e6f9062d31c5e6c8a3e9a51dbaf8a25c64f65f673223`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 3.7 MB (3683310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa91b0bcf56568c9049861b5321c46085544a6631527bdefdb84c18a6623fae`  
		Last Modified: Fri, 17 Apr 2026 00:30:29 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c03822eba8e0cf95dce574baa878c2167415ad48eef1ccbae83246ea874b9ed`  
		Last Modified: Fri, 17 Apr 2026 00:30:30 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:d088b7b55f51985159b6fe32611b0b4ebc925d08146919b22dc42fa7cd35dfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 KB (379645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2dd6a4bb49d474fcadd1abd2f52dc79ca67b31b11a96c5a34f239b5f7893db`

```dockerfile
```

-	Layers:
	-	`sha256:f2156f2fcd7c800b311863e493b109f04e64f083639871cd2b5efce1f17640f3`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 358.0 KB (357987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f79eec151e7ce7c7347244c9c8bfd7431205e45e6b30fa7e98e27e95e0f10e`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:02764df374a1709ff23d3a5dcdc44587ce282ec941977e0ca367393400d4dcc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83068134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e817e3c8378838c704e6f2db9767c81860a27f181249cb9e44be5299293faf43`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:31:15 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 17 Apr 2026 00:31:17 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 17 Apr 2026 00:31:18 GMT
WORKDIR /liquibase
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 17 Apr 2026 00:31:19 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LPM_VERSION=0.2.14
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 17 Apr 2026 00:31:21 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 17 Apr 2026 00:31:21 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 17 Apr 2026 00:31:21 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 17 Apr 2026 00:31:21 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:31:21 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 17 Apr 2026 00:31:21 GMT
USER liquibase:liquibase
# Fri, 17 Apr 2026 00:31:21 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:31:21 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831166d40df22727a0f749606435ab6a4409084cb7202d34b8b35ccd2fd53ea3`  
		Last Modified: Fri, 17 Apr 2026 00:31:32 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca45e9539c13dc3120e4487c5eb9306e5662fa360caef114c284f51f1f4f719`  
		Last Modified: Fri, 17 Apr 2026 00:31:34 GMT  
		Size: 66.9 MB (66875198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2a208d911ef09d8f8a6d13581c531ccc60d996bc210563f23f78e5861586d2`  
		Last Modified: Fri, 17 Apr 2026 00:31:33 GMT  
		Size: 8.7 MB (8688840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b5ab7263f6d6b43a369410afbf518ea077ad4e76614e0b52ce51e89eaa9cb7`  
		Last Modified: Fri, 17 Apr 2026 00:31:33 GMT  
		Size: 3.4 MB (3359632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be70c70dd84b0d04d247753d188bb7b592163f4fa2eca01b98d762f8d41963b5`  
		Last Modified: Fri, 17 Apr 2026 00:31:33 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec2acdb9ae64468ca511183e0e8d93e60650516f7ea7bb68d7593fa5a610c9b`  
		Last Modified: Fri, 17 Apr 2026 00:31:34 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:e3b85712d2657fcb95286ea159735ef6569569f9ddf0c378609ca2a5a9b461a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.0 KB (379029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab59b0f660b749ad5d77d3e747d5e622c3a40f4a290033d443b1cde84a3b8075`

```dockerfile
```

-	Layers:
	-	`sha256:2d73bc84012845f7b7fc5b6f5675adbae3ba5b0e44ba23b940acbcf56b91f5c2`  
		Last Modified: Fri, 17 Apr 2026 00:31:32 GMT  
		Size: 357.2 KB (357234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd48a19d885fdd36c300257a8e06f61a3d7d772787a3409329468d2924df5deb`  
		Last Modified: Fri, 17 Apr 2026 00:31:32 GMT  
		Size: 21.8 KB (21795 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:5.0.1`

```console
$ docker pull liquibase@sha256:af27034b7662d0f04a030e04d356704d1909f083466eb7e3edbfa942675afb5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0.1` - linux; amd64

```console
$ docker pull liquibase@sha256:1f9064427c1f4bc511a03ba125380d86252bc5336a4e5040c54f562b04136f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111450990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf1ff30aec52c8038ce39b64d9ad562bbfb3bc497f11aa90a444dfb8e490a1e`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:16:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:16:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:16:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:16:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:16:08 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 15 May 2026 21:16:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:16:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:16:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:16:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:46:16 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 15 May 2026 21:46:16 GMT
WORKDIR /liquibase
# Fri, 15 May 2026 21:46:17 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 15 May 2026 21:46:17 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 15 May 2026 21:46:17 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 15 May 2026 21:46:17 GMT
ARG LPM_VERSION=0.2.14
# Fri, 15 May 2026 21:46:17 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 15 May 2026 21:46:17 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 15 May 2026 21:46:17 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 15 May 2026 21:46:17 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 15 May 2026 21:46:17 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 15 May 2026 21:46:17 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 15 May 2026 21:46:17 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 15 May 2026 21:46:23 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 15 May 2026 21:46:23 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 15 May 2026 21:46:23 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 15 May 2026 21:46:23 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 15 May 2026 21:46:23 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 15 May 2026 21:46:23 GMT
USER liquibase:liquibase
# Fri, 15 May 2026 21:46:23 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:46:23 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5a0b6cb36c205fa8c9ef45406ef43ec624251108a5888140648cc4b33c6c55`  
		Last Modified: Fri, 15 May 2026 21:16:25 GMT  
		Size: 16.2 MB (16152745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49518c28c0b3c62624726aad57e80683d40b375b2400643477eee9fb6a278c98`  
		Last Modified: Fri, 15 May 2026 21:16:26 GMT  
		Size: 53.1 MB (53122802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41162acdcc29a9fd0a1e7740bb879e5192914f5814a43217fbc9222a7521947e`  
		Last Modified: Fri, 15 May 2026 21:16:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed0fd558ca3b009513993bf77af60ee5c03ce381c4d86b75dbda8fd93467027`  
		Last Modified: Fri, 15 May 2026 21:16:25 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e400438a03e2dceb0077e36ee13e000fd07bb2565eeee6bc7d280cad89e71c`  
		Last Modified: Fri, 15 May 2026 21:46:31 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ada9868deff67423d6e098e9a0c66934c5ae9f6395b48dde2c9f96050da96d`  
		Last Modified: Fri, 15 May 2026 21:46:32 GMT  
		Size: 8.7 MB (8665789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f76190c07012356011ad8815f52e65cffd0f3579221bf8ab1e1ca28a5db201a`  
		Last Modified: Fri, 15 May 2026 21:46:32 GMT  
		Size: 3.8 MB (3764588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32faf46f9dacb2eaed8f50b229184edec4bb84627d730a22d23d34a555198a1a`  
		Last Modified: Fri, 15 May 2026 21:46:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccbeaca5ddf6a05190168f8191384b8469b8f166faed0cbdc9aa716d528a1e2`  
		Last Modified: Fri, 15 May 2026 21:46:32 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1` - unknown; unknown

```console
$ docker pull liquibase@sha256:5e9d328a433dab4d236ce6fe2d5554dd9ff46a4933c582cf079ce7a706945188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d10444a857f3e691d461c67d6323d0be5eb2b19d8b74bf904928392ff157486`

```dockerfile
```

-	Layers:
	-	`sha256:2c9d34bcb5a672e4c16d2dac01e38c9b39c33dea01034f47ad5b47784b10b30d`  
		Last Modified: Fri, 15 May 2026 21:46:32 GMT  
		Size: 3.9 MB (3898378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:640297303e5e2752cc9dcfc8bf5e28b6a010f3912b6e4ec568cd8aa7144b35fe`  
		Last Modified: Fri, 15 May 2026 21:46:31 GMT  
		Size: 24.3 KB (24325 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0.1` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:2c3c1a34dededb6be33af6689d6b56cac02e86a7fcbf5a30760299e9f6ccf3ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108113223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7070aac943df6f0c9d47f3c74a9760a0f6eba7c2f8e82461cea905fb5b580c85`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:15:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:15:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:15:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:15:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:15:49 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 15 May 2026 21:16:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:16:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:16:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:16:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:47:19 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 15 May 2026 21:47:19 GMT
WORKDIR /liquibase
# Fri, 15 May 2026 21:47:20 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 15 May 2026 21:47:20 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 15 May 2026 21:47:20 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 15 May 2026 21:47:20 GMT
ARG LPM_VERSION=0.2.14
# Fri, 15 May 2026 21:47:20 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 15 May 2026 21:47:20 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 15 May 2026 21:47:20 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 15 May 2026 21:47:20 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 15 May 2026 21:47:20 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 15 May 2026 21:47:20 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 15 May 2026 21:47:20 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 15 May 2026 21:47:28 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 15 May 2026 21:47:28 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 15 May 2026 21:47:28 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 15 May 2026 21:47:28 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 15 May 2026 21:47:28 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 15 May 2026 21:47:28 GMT
USER liquibase:liquibase
# Fri, 15 May 2026 21:47:28 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:47:28 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57ad989666c9e0dfc45a5f5a1a6ec026fe709513407113fd1d938cb641e13ca`  
		Last Modified: Fri, 15 May 2026 21:16:03 GMT  
		Size: 16.1 MB (16076205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2cd678502086cef6dba8f3127d023e5cdce1664a09143a8511e49ecc27f1c7`  
		Last Modified: Fri, 15 May 2026 21:16:28 GMT  
		Size: 52.3 MB (52314965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5318b9fee19514f8672bc32ae5b580b0eb3db47498220a70a4aee4675c2f79`  
		Last Modified: Fri, 15 May 2026 21:16:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671fab38f8b8067234c315c0ed43db9cd49bf63d19d293012dc0fb862a82caa6`  
		Last Modified: Fri, 15 May 2026 21:16:26 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694a1379d03b8e62c721cbe1d7854ec59b604d8702b37f3507c9a9fb979cd7c9`  
		Last Modified: Fri, 15 May 2026 21:47:35 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb173c2254b2bad5fc8285c3467b95be92439fac1f6219bb94c21c5ad060b1c`  
		Last Modified: Fri, 15 May 2026 21:47:36 GMT  
		Size: 8.7 MB (8665781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc95dca4874188ae4e93f64fb0a40ca4cb502cd96ccc6d5163c6a8f30952500`  
		Last Modified: Fri, 15 May 2026 21:47:36 GMT  
		Size: 3.4 MB (3441265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93817051be0bd4df635f063a14b28943d1ccb72e4c8d19b0daf0e9a5a6949ccd`  
		Last Modified: Fri, 15 May 2026 21:47:36 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7680614f5ae76c615f5bfa64884cf58bda4409f07b5bc744f380f896a4da92`  
		Last Modified: Fri, 15 May 2026 21:47:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1` - unknown; unknown

```console
$ docker pull liquibase@sha256:5b3f7a515af253389f3af38d3fcd067f1ccbc45ce8413635ba954df06e0bfd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d803cb10aa9beb4d79c355e7696a8da43d3a75bdbf46f70ba7f4371423ed0fcf`

```dockerfile
```

-	Layers:
	-	`sha256:988003bc3ab2e9a4ed6901d08251afb1ad7d5610320a5f6cab07b9217b989975`  
		Last Modified: Fri, 15 May 2026 21:47:36 GMT  
		Size: 3.9 MB (3898046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96f138f6cc4d497b1812b222b9ccadfedcd7b501765410f5e853040ce215f2cb`  
		Last Modified: Fri, 15 May 2026 21:47:35 GMT  
		Size: 24.4 KB (24448 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:5.0.1-alpine`

```console
$ docker pull liquibase@sha256:b131a24527add4d4eadc3300aa5cca684aa60abcd734b8d14d4a5c33b169b48b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0.1-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:ac3e7f22a1f63434bec4e9ac9a459c3d14ff5fbf5b4cf23c41aaa15c8646c35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84056139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735cc69d2a472f1a3213f884cf38c27e7f07f9e006723d24b254987a2fc4c687`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:11 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 17 Apr 2026 00:30:13 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 17 Apr 2026 00:30:13 GMT
WORKDIR /liquibase
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 17 Apr 2026 00:30:15 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LPM_VERSION=0.2.14
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 17 Apr 2026 00:30:16 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 17 Apr 2026 00:30:16 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 17 Apr 2026 00:30:16 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 17 Apr 2026 00:30:16 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:30:16 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 17 Apr 2026 00:30:16 GMT
USER liquibase:liquibase
# Fri, 17 Apr 2026 00:30:16 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:16 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c968b03a929ffeffc74e342fa376b3edf03837491ffc31b33bf6355c7e7a7`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b8a26d38c62ddc3835ccdd169cdda87af0f6fc420b7a65a9ddd9f3321ca1a2`  
		Last Modified: Fri, 17 Apr 2026 00:30:30 GMT  
		Size: 67.9 MB (67873148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f7f520ce551a37b7e676a5e609d9729695d8ce07c806c1e101c9f205fecf03`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 8.7 MB (8688923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5eea34866b5479ef311e6f9062d31c5e6c8a3e9a51dbaf8a25c64f65f673223`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 3.7 MB (3683310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa91b0bcf56568c9049861b5321c46085544a6631527bdefdb84c18a6623fae`  
		Last Modified: Fri, 17 Apr 2026 00:30:29 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c03822eba8e0cf95dce574baa878c2167415ad48eef1ccbae83246ea874b9ed`  
		Last Modified: Fri, 17 Apr 2026 00:30:30 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:d088b7b55f51985159b6fe32611b0b4ebc925d08146919b22dc42fa7cd35dfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 KB (379645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2dd6a4bb49d474fcadd1abd2f52dc79ca67b31b11a96c5a34f239b5f7893db`

```dockerfile
```

-	Layers:
	-	`sha256:f2156f2fcd7c800b311863e493b109f04e64f083639871cd2b5efce1f17640f3`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 358.0 KB (357987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f79eec151e7ce7c7347244c9c8bfd7431205e45e6b30fa7e98e27e95e0f10e`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0.1-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:02764df374a1709ff23d3a5dcdc44587ce282ec941977e0ca367393400d4dcc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83068134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e817e3c8378838c704e6f2db9767c81860a27f181249cb9e44be5299293faf43`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:31:15 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 17 Apr 2026 00:31:17 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 17 Apr 2026 00:31:18 GMT
WORKDIR /liquibase
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 17 Apr 2026 00:31:19 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LPM_VERSION=0.2.14
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 17 Apr 2026 00:31:21 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 17 Apr 2026 00:31:21 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 17 Apr 2026 00:31:21 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 17 Apr 2026 00:31:21 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:31:21 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 17 Apr 2026 00:31:21 GMT
USER liquibase:liquibase
# Fri, 17 Apr 2026 00:31:21 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:31:21 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831166d40df22727a0f749606435ab6a4409084cb7202d34b8b35ccd2fd53ea3`  
		Last Modified: Fri, 17 Apr 2026 00:31:32 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca45e9539c13dc3120e4487c5eb9306e5662fa360caef114c284f51f1f4f719`  
		Last Modified: Fri, 17 Apr 2026 00:31:34 GMT  
		Size: 66.9 MB (66875198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2a208d911ef09d8f8a6d13581c531ccc60d996bc210563f23f78e5861586d2`  
		Last Modified: Fri, 17 Apr 2026 00:31:33 GMT  
		Size: 8.7 MB (8688840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b5ab7263f6d6b43a369410afbf518ea077ad4e76614e0b52ce51e89eaa9cb7`  
		Last Modified: Fri, 17 Apr 2026 00:31:33 GMT  
		Size: 3.4 MB (3359632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be70c70dd84b0d04d247753d188bb7b592163f4fa2eca01b98d762f8d41963b5`  
		Last Modified: Fri, 17 Apr 2026 00:31:33 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec2acdb9ae64468ca511183e0e8d93e60650516f7ea7bb68d7593fa5a610c9b`  
		Last Modified: Fri, 17 Apr 2026 00:31:34 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:e3b85712d2657fcb95286ea159735ef6569569f9ddf0c378609ca2a5a9b461a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.0 KB (379029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab59b0f660b749ad5d77d3e747d5e622c3a40f4a290033d443b1cde84a3b8075`

```dockerfile
```

-	Layers:
	-	`sha256:2d73bc84012845f7b7fc5b6f5675adbae3ba5b0e44ba23b940acbcf56b91f5c2`  
		Last Modified: Fri, 17 Apr 2026 00:31:32 GMT  
		Size: 357.2 KB (357234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd48a19d885fdd36c300257a8e06f61a3d7d772787a3409329468d2924df5deb`  
		Last Modified: Fri, 17 Apr 2026 00:31:32 GMT  
		Size: 21.8 KB (21795 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:b131a24527add4d4eadc3300aa5cca684aa60abcd734b8d14d4a5c33b169b48b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:ac3e7f22a1f63434bec4e9ac9a459c3d14ff5fbf5b4cf23c41aaa15c8646c35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84056139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735cc69d2a472f1a3213f884cf38c27e7f07f9e006723d24b254987a2fc4c687`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:11 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 17 Apr 2026 00:30:13 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 17 Apr 2026 00:30:13 GMT
WORKDIR /liquibase
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 17 Apr 2026 00:30:15 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LPM_VERSION=0.2.14
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 17 Apr 2026 00:30:16 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 17 Apr 2026 00:30:16 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 17 Apr 2026 00:30:16 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 17 Apr 2026 00:30:16 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:30:16 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 17 Apr 2026 00:30:16 GMT
USER liquibase:liquibase
# Fri, 17 Apr 2026 00:30:16 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:16 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c968b03a929ffeffc74e342fa376b3edf03837491ffc31b33bf6355c7e7a7`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b8a26d38c62ddc3835ccdd169cdda87af0f6fc420b7a65a9ddd9f3321ca1a2`  
		Last Modified: Fri, 17 Apr 2026 00:30:30 GMT  
		Size: 67.9 MB (67873148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f7f520ce551a37b7e676a5e609d9729695d8ce07c806c1e101c9f205fecf03`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 8.7 MB (8688923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5eea34866b5479ef311e6f9062d31c5e6c8a3e9a51dbaf8a25c64f65f673223`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 3.7 MB (3683310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa91b0bcf56568c9049861b5321c46085544a6631527bdefdb84c18a6623fae`  
		Last Modified: Fri, 17 Apr 2026 00:30:29 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c03822eba8e0cf95dce574baa878c2167415ad48eef1ccbae83246ea874b9ed`  
		Last Modified: Fri, 17 Apr 2026 00:30:30 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:d088b7b55f51985159b6fe32611b0b4ebc925d08146919b22dc42fa7cd35dfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 KB (379645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2dd6a4bb49d474fcadd1abd2f52dc79ca67b31b11a96c5a34f239b5f7893db`

```dockerfile
```

-	Layers:
	-	`sha256:f2156f2fcd7c800b311863e493b109f04e64f083639871cd2b5efce1f17640f3`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 358.0 KB (357987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f79eec151e7ce7c7347244c9c8bfd7431205e45e6b30fa7e98e27e95e0f10e`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:02764df374a1709ff23d3a5dcdc44587ce282ec941977e0ca367393400d4dcc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83068134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e817e3c8378838c704e6f2db9767c81860a27f181249cb9e44be5299293faf43`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:31:15 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 17 Apr 2026 00:31:17 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 17 Apr 2026 00:31:18 GMT
WORKDIR /liquibase
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 17 Apr 2026 00:31:19 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LPM_VERSION=0.2.14
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 17 Apr 2026 00:31:21 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 17 Apr 2026 00:31:21 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 17 Apr 2026 00:31:21 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 17 Apr 2026 00:31:21 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:31:21 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 17 Apr 2026 00:31:21 GMT
USER liquibase:liquibase
# Fri, 17 Apr 2026 00:31:21 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:31:21 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831166d40df22727a0f749606435ab6a4409084cb7202d34b8b35ccd2fd53ea3`  
		Last Modified: Fri, 17 Apr 2026 00:31:32 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca45e9539c13dc3120e4487c5eb9306e5662fa360caef114c284f51f1f4f719`  
		Last Modified: Fri, 17 Apr 2026 00:31:34 GMT  
		Size: 66.9 MB (66875198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2a208d911ef09d8f8a6d13581c531ccc60d996bc210563f23f78e5861586d2`  
		Last Modified: Fri, 17 Apr 2026 00:31:33 GMT  
		Size: 8.7 MB (8688840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b5ab7263f6d6b43a369410afbf518ea077ad4e76614e0b52ce51e89eaa9cb7`  
		Last Modified: Fri, 17 Apr 2026 00:31:33 GMT  
		Size: 3.4 MB (3359632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be70c70dd84b0d04d247753d188bb7b592163f4fa2eca01b98d762f8d41963b5`  
		Last Modified: Fri, 17 Apr 2026 00:31:33 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec2acdb9ae64468ca511183e0e8d93e60650516f7ea7bb68d7593fa5a610c9b`  
		Last Modified: Fri, 17 Apr 2026 00:31:34 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:e3b85712d2657fcb95286ea159735ef6569569f9ddf0c378609ca2a5a9b461a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.0 KB (379029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab59b0f660b749ad5d77d3e747d5e622c3a40f4a290033d443b1cde84a3b8075`

```dockerfile
```

-	Layers:
	-	`sha256:2d73bc84012845f7b7fc5b6f5675adbae3ba5b0e44ba23b940acbcf56b91f5c2`  
		Last Modified: Fri, 17 Apr 2026 00:31:32 GMT  
		Size: 357.2 KB (357234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd48a19d885fdd36c300257a8e06f61a3d7d772787a3409329468d2924df5deb`  
		Last Modified: Fri, 17 Apr 2026 00:31:32 GMT  
		Size: 21.8 KB (21795 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:latest`

```console
$ docker pull liquibase@sha256:af27034b7662d0f04a030e04d356704d1909f083466eb7e3edbfa942675afb5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:1f9064427c1f4bc511a03ba125380d86252bc5336a4e5040c54f562b04136f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111450990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf1ff30aec52c8038ce39b64d9ad562bbfb3bc497f11aa90a444dfb8e490a1e`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:16:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:16:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:16:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:16:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:16:08 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 15 May 2026 21:16:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:16:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:16:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:16:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:46:16 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 15 May 2026 21:46:16 GMT
WORKDIR /liquibase
# Fri, 15 May 2026 21:46:17 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 15 May 2026 21:46:17 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 15 May 2026 21:46:17 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 15 May 2026 21:46:17 GMT
ARG LPM_VERSION=0.2.14
# Fri, 15 May 2026 21:46:17 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 15 May 2026 21:46:17 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 15 May 2026 21:46:17 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 15 May 2026 21:46:17 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 15 May 2026 21:46:17 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 15 May 2026 21:46:17 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 15 May 2026 21:46:17 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 15 May 2026 21:46:23 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 15 May 2026 21:46:23 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 15 May 2026 21:46:23 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 15 May 2026 21:46:23 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 15 May 2026 21:46:23 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 15 May 2026 21:46:23 GMT
USER liquibase:liquibase
# Fri, 15 May 2026 21:46:23 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:46:23 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5a0b6cb36c205fa8c9ef45406ef43ec624251108a5888140648cc4b33c6c55`  
		Last Modified: Fri, 15 May 2026 21:16:25 GMT  
		Size: 16.2 MB (16152745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49518c28c0b3c62624726aad57e80683d40b375b2400643477eee9fb6a278c98`  
		Last Modified: Fri, 15 May 2026 21:16:26 GMT  
		Size: 53.1 MB (53122802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41162acdcc29a9fd0a1e7740bb879e5192914f5814a43217fbc9222a7521947e`  
		Last Modified: Fri, 15 May 2026 21:16:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed0fd558ca3b009513993bf77af60ee5c03ce381c4d86b75dbda8fd93467027`  
		Last Modified: Fri, 15 May 2026 21:16:25 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e400438a03e2dceb0077e36ee13e000fd07bb2565eeee6bc7d280cad89e71c`  
		Last Modified: Fri, 15 May 2026 21:46:31 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ada9868deff67423d6e098e9a0c66934c5ae9f6395b48dde2c9f96050da96d`  
		Last Modified: Fri, 15 May 2026 21:46:32 GMT  
		Size: 8.7 MB (8665789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f76190c07012356011ad8815f52e65cffd0f3579221bf8ab1e1ca28a5db201a`  
		Last Modified: Fri, 15 May 2026 21:46:32 GMT  
		Size: 3.8 MB (3764588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32faf46f9dacb2eaed8f50b229184edec4bb84627d730a22d23d34a555198a1a`  
		Last Modified: Fri, 15 May 2026 21:46:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccbeaca5ddf6a05190168f8191384b8469b8f166faed0cbdc9aa716d528a1e2`  
		Last Modified: Fri, 15 May 2026 21:46:32 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:5e9d328a433dab4d236ce6fe2d5554dd9ff46a4933c582cf079ce7a706945188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d10444a857f3e691d461c67d6323d0be5eb2b19d8b74bf904928392ff157486`

```dockerfile
```

-	Layers:
	-	`sha256:2c9d34bcb5a672e4c16d2dac01e38c9b39c33dea01034f47ad5b47784b10b30d`  
		Last Modified: Fri, 15 May 2026 21:46:32 GMT  
		Size: 3.9 MB (3898378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:640297303e5e2752cc9dcfc8bf5e28b6a010f3912b6e4ec568cd8aa7144b35fe`  
		Last Modified: Fri, 15 May 2026 21:46:31 GMT  
		Size: 24.3 KB (24325 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:2c3c1a34dededb6be33af6689d6b56cac02e86a7fcbf5a30760299e9f6ccf3ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108113223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7070aac943df6f0c9d47f3c74a9760a0f6eba7c2f8e82461cea905fb5b580c85`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:15:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:15:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:15:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:15:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:15:49 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 15 May 2026 21:16:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:16:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:16:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:16:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:47:19 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 15 May 2026 21:47:19 GMT
WORKDIR /liquibase
# Fri, 15 May 2026 21:47:20 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 15 May 2026 21:47:20 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 15 May 2026 21:47:20 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 15 May 2026 21:47:20 GMT
ARG LPM_VERSION=0.2.14
# Fri, 15 May 2026 21:47:20 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 15 May 2026 21:47:20 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 15 May 2026 21:47:20 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 15 May 2026 21:47:20 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 15 May 2026 21:47:20 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 15 May 2026 21:47:20 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 15 May 2026 21:47:20 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 15 May 2026 21:47:28 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 15 May 2026 21:47:28 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 15 May 2026 21:47:28 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 15 May 2026 21:47:28 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 15 May 2026 21:47:28 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 15 May 2026 21:47:28 GMT
USER liquibase:liquibase
# Fri, 15 May 2026 21:47:28 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:47:28 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57ad989666c9e0dfc45a5f5a1a6ec026fe709513407113fd1d938cb641e13ca`  
		Last Modified: Fri, 15 May 2026 21:16:03 GMT  
		Size: 16.1 MB (16076205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2cd678502086cef6dba8f3127d023e5cdce1664a09143a8511e49ecc27f1c7`  
		Last Modified: Fri, 15 May 2026 21:16:28 GMT  
		Size: 52.3 MB (52314965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5318b9fee19514f8672bc32ae5b580b0eb3db47498220a70a4aee4675c2f79`  
		Last Modified: Fri, 15 May 2026 21:16:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671fab38f8b8067234c315c0ed43db9cd49bf63d19d293012dc0fb862a82caa6`  
		Last Modified: Fri, 15 May 2026 21:16:26 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694a1379d03b8e62c721cbe1d7854ec59b604d8702b37f3507c9a9fb979cd7c9`  
		Last Modified: Fri, 15 May 2026 21:47:35 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb173c2254b2bad5fc8285c3467b95be92439fac1f6219bb94c21c5ad060b1c`  
		Last Modified: Fri, 15 May 2026 21:47:36 GMT  
		Size: 8.7 MB (8665781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc95dca4874188ae4e93f64fb0a40ca4cb502cd96ccc6d5163c6a8f30952500`  
		Last Modified: Fri, 15 May 2026 21:47:36 GMT  
		Size: 3.4 MB (3441265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93817051be0bd4df635f063a14b28943d1ccb72e4c8d19b0daf0e9a5a6949ccd`  
		Last Modified: Fri, 15 May 2026 21:47:36 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7680614f5ae76c615f5bfa64884cf58bda4409f07b5bc744f380f896a4da92`  
		Last Modified: Fri, 15 May 2026 21:47:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:5b3f7a515af253389f3af38d3fcd067f1ccbc45ce8413635ba954df06e0bfd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d803cb10aa9beb4d79c355e7696a8da43d3a75bdbf46f70ba7f4371423ed0fcf`

```dockerfile
```

-	Layers:
	-	`sha256:988003bc3ab2e9a4ed6901d08251afb1ad7d5610320a5f6cab07b9217b989975`  
		Last Modified: Fri, 15 May 2026 21:47:36 GMT  
		Size: 3.9 MB (3898046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96f138f6cc4d497b1812b222b9ccadfedcd7b501765410f5e853040ce215f2cb`  
		Last Modified: Fri, 15 May 2026 21:47:35 GMT  
		Size: 24.4 KB (24448 bytes)  
		MIME: application/vnd.in-toto+json
