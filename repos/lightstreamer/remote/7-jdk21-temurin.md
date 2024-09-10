## `lightstreamer:7-jdk21-temurin`

```console
$ docker pull lightstreamer@sha256:7dbfe93c29005b9065440c8a7de2b73ff0afb84efff4d49b9c3dd273473db0ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `lightstreamer:7-jdk21-temurin` - linux; amd64

```console
$ docker pull lightstreamer@sha256:049ad4c115880b9b6ac51e4131f13a3df63439f502586e5583e18fa423fd056c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272289335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c70978056e95eb59753e06a66551a20469507d4c5e203c1f4aacc8f94401c0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `[".\/LS.sh","run"]`

```dockerfile
# Tue, 09 Jul 2024 14:15:05 GMT
ARG RELEASE
# Tue, 09 Jul 2024 14:15:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Jul 2024 14:15:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Jul 2024 14:15:05 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 09 Jul 2024 14:15:05 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Tue, 09 Jul 2024 14:15:05 GMT
CMD ["/bin/bash"]
# Tue, 09 Jul 2024 14:15:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 14:15:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 14:15:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 09 Jul 2024 14:15:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jul 2024 14:15:05 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Tue, 09 Jul 2024 14:15:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        riscv64)          ESUM='b04fd7f52d18268a935f1a7144dae802b25db600ec97156ddd46b3100cbd13da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 09 Jul 2024 14:15:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 09 Jul 2024 14:15:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 09 Jul 2024 14:15:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 09 Jul 2024 14:15:05 GMT
CMD ["jshell"]
# Tue, 09 Jul 2024 14:15:05 GMT
LABEL maintainer=Lightstreamer Server Development Team <support@lightstreamer.com>
# Tue, 09 Jul 2024 14:15:05 GMT
RUN apt-get -y update         && apt-get -y install gnupg         && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jul 2024 14:15:05 GMT
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9B90BFD14309C7DA5EF58D7D4A8C08966F29B4D2 # buildkit
# Tue, 09 Jul 2024 14:15:05 GMT
ENV LIGHTSTREAMER_VERSION=7.4.4
# Tue, 09 Jul 2024 14:15:05 GMT
ENV LIGHTSTREAMER_URL_DOWNLOAD=https://lightstreamer.com/distr/ls-server/7.4.4/Lightstreamer-7.4.4.tar.gz
# Tue, 09 Jul 2024 14:15:05 GMT
RUN set -ex;         mkdir /lightstreamer && cd /lightstreamer         && curl -fSL -o Lightstreamer.tar.gz ${LIGHTSTREAMER_URL_DOWNLOAD}         && curl -fSL -o Lightstreamer.tar.gz.asc ${LIGHTSTREAMER_URL_DOWNLOAD}.asc         && gpg --batch --verify Lightstreamer.tar.gz.asc Lightstreamer.tar.gz         && tar -xvf Lightstreamer.tar.gz --strip-components=1         && sed -i -e 's/<appender-ref ref="LSDailyRolling" \/>/<appender-ref ref="LSConsole" \/>/'                   -e '/<logger name="LightstreamerLogger.init/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerLogger.license/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerProxyAdapters/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   conf/lightstreamer_log_conf.xml         && groupadd -r -g 10000 lightstreamer         && useradd --no-log-init -r -g lightstreamer -u 10000 lightstreamer         && chown -R lightstreamer:lightstreamer ../lightstreamer         && rm Lightstreamer.tar.gz Lightstreamer.tar.gz.asc # buildkit
# Tue, 09 Jul 2024 14:15:05 GMT
USER lightstreamer
# Tue, 09 Jul 2024 14:15:05 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 09 Jul 2024 14:15:05 GMT
WORKDIR /lightstreamer/bin/unix-like
# Tue, 09 Jul 2024 14:15:05 GMT
CMD ["./LS.sh" "run"]
```

-	Layers:
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6d67df44ebaf68af30549648235de86e15355c7fc9afc496d8d73df71a7a3d`  
		Last Modified: Sat, 17 Aug 2024 01:12:58 GMT  
		Size: 19.8 MB (19765195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:facf7d693a40c7b09d711beecddef9142e6074a9d517b5b2f44a16299654b031`  
		Last Modified: Fri, 23 Aug 2024 19:28:43 GMT  
		Size: 158.6 MB (158587392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3fe075c198ddd7a31193d47754cdb43d384b3bcd7585284f478d8bd5fa5107`  
		Last Modified: Fri, 23 Aug 2024 19:28:30 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28f0ce2ee5faf000467e3072dbaa09ec07d716c591a6871791efa036d05e9d`  
		Last Modified: Fri, 23 Aug 2024 19:28:30 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5fa072558e2e79b3348562fb715c15e44ddeca3e33327b6ad54438340588e2`  
		Last Modified: Tue, 10 Sep 2024 01:02:06 GMT  
		Size: 3.4 MB (3426431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af66922d1903683f65a7cadd59e60b341a57d6c9a8fac82f91c901c8c4ea877`  
		Last Modified: Tue, 10 Sep 2024 01:02:05 GMT  
		Size: 2.4 KB (2360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc72f6a80496fc691696769f7cbe71033601649525d4a047296db80ecf4b636`  
		Last Modified: Tue, 10 Sep 2024 01:02:06 GMT  
		Size: 59.9 MB (59938336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `lightstreamer:7-jdk21-temurin` - unknown; unknown

```console
$ docker pull lightstreamer@sha256:0533754bddfc96515495540892ac6264376d1d22a881cb297a247079d51f9b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c5251badc22679f6a290fe32c24dfc3fdd52e2e4268bfeb484db507291d6a5`

```dockerfile
```

-	Layers:
	-	`sha256:ea279f7871000a887567c91dea7817108e39f0f6468335780fc5749936a80b52`  
		Last Modified: Tue, 10 Sep 2024 01:02:05 GMT  
		Size: 20.7 KB (20729 bytes)  
		MIME: application/vnd.in-toto+json

### `lightstreamer:7-jdk21-temurin` - linux; arm64 variant v8

```console
$ docker pull lightstreamer@sha256:c5bd8835f1b1f122cc71f1fea026115d48a22068472332435a53084994274ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.0 MB (270991983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52015dfe7b2a91f22bc5366925af2476566a234068ace71b79080f856140785b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `[".\/LS.sh","run"]`

```dockerfile
# Tue, 09 Jul 2024 14:15:05 GMT
ARG RELEASE
# Tue, 09 Jul 2024 14:15:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Jul 2024 14:15:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Jul 2024 14:15:05 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 09 Jul 2024 14:15:05 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Tue, 09 Jul 2024 14:15:05 GMT
CMD ["/bin/bash"]
# Tue, 09 Jul 2024 14:15:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 14:15:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 14:15:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 09 Jul 2024 14:15:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jul 2024 14:15:05 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Tue, 09 Jul 2024 14:15:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        riscv64)          ESUM='b04fd7f52d18268a935f1a7144dae802b25db600ec97156ddd46b3100cbd13da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 09 Jul 2024 14:15:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 09 Jul 2024 14:15:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 09 Jul 2024 14:15:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 09 Jul 2024 14:15:05 GMT
CMD ["jshell"]
# Tue, 09 Jul 2024 14:15:05 GMT
LABEL maintainer=Lightstreamer Server Development Team <support@lightstreamer.com>
# Tue, 09 Jul 2024 14:15:05 GMT
RUN apt-get -y update         && apt-get -y install gnupg         && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jul 2024 14:15:05 GMT
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9B90BFD14309C7DA5EF58D7D4A8C08966F29B4D2 # buildkit
# Tue, 09 Jul 2024 14:15:05 GMT
ENV LIGHTSTREAMER_VERSION=7.4.4
# Tue, 09 Jul 2024 14:15:05 GMT
ENV LIGHTSTREAMER_URL_DOWNLOAD=https://lightstreamer.com/distr/ls-server/7.4.4/Lightstreamer-7.4.4.tar.gz
# Tue, 09 Jul 2024 14:15:05 GMT
RUN set -ex;         mkdir /lightstreamer && cd /lightstreamer         && curl -fSL -o Lightstreamer.tar.gz ${LIGHTSTREAMER_URL_DOWNLOAD}         && curl -fSL -o Lightstreamer.tar.gz.asc ${LIGHTSTREAMER_URL_DOWNLOAD}.asc         && gpg --batch --verify Lightstreamer.tar.gz.asc Lightstreamer.tar.gz         && tar -xvf Lightstreamer.tar.gz --strip-components=1         && sed -i -e 's/<appender-ref ref="LSDailyRolling" \/>/<appender-ref ref="LSConsole" \/>/'                   -e '/<logger name="LightstreamerLogger.init/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerLogger.license/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerProxyAdapters/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   conf/lightstreamer_log_conf.xml         && groupadd -r -g 10000 lightstreamer         && useradd --no-log-init -r -g lightstreamer -u 10000 lightstreamer         && chown -R lightstreamer:lightstreamer ../lightstreamer         && rm Lightstreamer.tar.gz Lightstreamer.tar.gz.asc # buildkit
# Tue, 09 Jul 2024 14:15:05 GMT
USER lightstreamer
# Tue, 09 Jul 2024 14:15:05 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 09 Jul 2024 14:15:05 GMT
WORKDIR /lightstreamer/bin/unix-like
# Tue, 09 Jul 2024 14:15:05 GMT
CMD ["./LS.sh" "run"]
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d730088f68183e8bde2999ed48782fec63b9dea3c9a5d270fdede5082140ac57`  
		Last Modified: Sat, 17 Aug 2024 01:35:47 GMT  
		Size: 21.0 MB (20962516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14f04caf9bed59074ef3aef2f88e85708db40de00edc54ae8ff795d1c4495d7`  
		Last Modified: Fri, 23 Aug 2024 19:46:09 GMT  
		Size: 156.8 MB (156756964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b24eef44af83099ffdc11fb18199e5203c9ba74be9d1caf8a92782368b78d07`  
		Last Modified: Fri, 23 Aug 2024 19:45:59 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba26bf8b117fb371b47bc0e1c92c8bbf4937ba2e3fe7ce5b58222c2dc1a72586`  
		Last Modified: Fri, 23 Aug 2024 19:45:59 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f38d6621a4569f95e10434188b19417d187c56879a5b954fb3e528a5459965`  
		Last Modified: Tue, 10 Sep 2024 05:23:30 GMT  
		Size: 3.4 MB (3419442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6200d59c1c0de42c8478520a6e6a7a1fe02c2675f6af6061c40a3b6209447d9`  
		Last Modified: Tue, 10 Sep 2024 05:23:30 GMT  
		Size: 2.4 KB (2367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30209e9d8c0fb3a0882aeb36e9c045e62bdba37740cf5161c03c4bb9b3c5c037`  
		Last Modified: Tue, 10 Sep 2024 05:23:32 GMT  
		Size: 59.9 MB (59938349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `lightstreamer:7-jdk21-temurin` - unknown; unknown

```console
$ docker pull lightstreamer@sha256:355c86a8c68003f1e5d38ecc2b6503c78c870ac5ee1ff308e62c684e1668f97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5615066f125044238d456ec1edbb06cb381e24d9361bc68cd3d62b6e82fd6ac5`

```dockerfile
```

-	Layers:
	-	`sha256:eaf0b02e133c96e1373b390434159c9c95c8b3d9f8c4e79f2dc628c692831fa7`  
		Last Modified: Tue, 10 Sep 2024 05:23:30 GMT  
		Size: 21.1 KB (21112 bytes)  
		MIME: application/vnd.in-toto+json
