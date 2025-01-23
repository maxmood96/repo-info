## `lightstreamer:latest`

```console
$ docker pull lightstreamer@sha256:ca7da1bf28ca11980d9b58c7d0ad15abeffb167385da6df70523ceb88454980e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `lightstreamer:latest` - linux; amd64

```console
$ docker pull lightstreamer@sha256:e2d996d7aa5939a079205641b290da50914c3c617f8280201708780d2ecd758f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269251516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f11a714724fcfdab2a8c5102bd9720cb7da041544160ad7a623308a659b426`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `[".\/LS.sh","run"]`

```dockerfile
# Fri, 04 Oct 2024 12:48:42 GMT
ARG RELEASE
# Fri, 04 Oct 2024 12:48:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Oct 2024 12:48:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Oct 2024 12:48:42 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 04 Oct 2024 12:48:42 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Fri, 04 Oct 2024 12:48:42 GMT
CMD ["/bin/bash"]
# Fri, 04 Oct 2024 12:48:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Oct 2024 12:48:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Oct 2024 12:48:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 04 Oct 2024 12:48:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Fri, 04 Oct 2024 12:48:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c654d98404c073b8a7e66bffb27f4ae3e7ede47d13284c132d40a83144bfd8c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='6482639ed9fd22aa2e704cc366848b1b3e1586d2bf1213869c43e80bca58fe5c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='3c6f4c358facfb6c19d90faf02bfe0fc7512d6b0e80ac18146bbd7e0d01deeef';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        riscv64)          ESUM='2f1b3e401e36de803398dfb9818861f9f14ca8ae7db650ea0946ab048fefe3b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='51a7ca42cc2e8cb5f3e7a326c28912ee84ff0791a1ca66650a8c53af07510a7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Oct 2024 12:48:42 GMT
CMD ["jshell"]
# Fri, 04 Oct 2024 12:48:42 GMT
LABEL maintainer=Lightstreamer Server Development Team <support@lightstreamer.com>
# Fri, 04 Oct 2024 12:48:42 GMT
RUN apt-get -y update         && apt-get -y install gnupg         && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9B90BFD14309C7DA5EF58D7D4A8C08966F29B4D2 # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
ENV LIGHTSTREAMER_VERSION=7.4.5
# Fri, 04 Oct 2024 12:48:42 GMT
ENV LIGHTSTREAMER_URL_DOWNLOAD=https://lightstreamer.com/distros/ls-server/7.4.5/Lightstreamer-7.4.5.tar.gz
# Fri, 04 Oct 2024 12:48:42 GMT
RUN set -ex;         mkdir /lightstreamer && cd /lightstreamer         && curl -fSL -o Lightstreamer.tar.gz ${LIGHTSTREAMER_URL_DOWNLOAD}         && curl -fSL -o Lightstreamer.tar.gz.asc ${LIGHTSTREAMER_URL_DOWNLOAD}.asc         && gpg --batch --verify Lightstreamer.tar.gz.asc Lightstreamer.tar.gz         && tar -xvf Lightstreamer.tar.gz --strip-components=1         && sed -i -e 's/<appender-ref ref="LSDailyRolling" \/>/<appender-ref ref="LSConsole" \/>/'                   -e '/<logger name="LightstreamerLogger.init/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerLogger.license/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerProxyAdapters/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   conf/lightstreamer_log_conf.xml         && groupadd -r -g 10000 lightstreamer         && useradd --no-log-init -r -g lightstreamer -u 10000 lightstreamer         && chown -R lightstreamer:lightstreamer ../lightstreamer         && rm Lightstreamer.tar.gz Lightstreamer.tar.gz.asc # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
USER lightstreamer
# Fri, 04 Oct 2024 12:48:42 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Oct 2024 12:48:42 GMT
WORKDIR /lightstreamer/bin/unix-like
# Fri, 04 Oct 2024 12:48:42 GMT
CMD ["./LS.sh" "run"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a4f8d91b1f8a0a903f2a4b72dfccaadc2f8f2730b7fa54de2fcdec8398e798`  
		Last Modified: Wed, 22 Jan 2025 18:28:19 GMT  
		Size: 22.9 MB (22948807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976191fda61e68b93e830e6181d42272470323360a899ecdddd96a9d3f9341ec`  
		Last Modified: Wed, 22 Jan 2025 18:28:22 GMT  
		Size: 157.6 MB (157585749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba28ded3b3cc481144a16330ec70aad7583b9d17a067ca094bfa3597672a1501`  
		Last Modified: Wed, 22 Jan 2025 18:28:17 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe286c336aed51cc16fe58c34b135cff2a610280a534fcf72f368c53d3a8a6d9`  
		Last Modified: Wed, 22 Jan 2025 18:28:18 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4f1f62f3e00a845e8529ff275af7fac83cfe299f2be4c234f050ab329efb89`  
		Last Modified: Wed, 22 Jan 2025 19:38:29 GMT  
		Size: 2.6 KB (2642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309711cc603102e5e53a8370c9c8cd053e285a3342233911b314a09e0de63fce`  
		Last Modified: Wed, 22 Jan 2025 19:38:31 GMT  
		Size: 59.0 MB (58959844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `lightstreamer:latest` - unknown; unknown

```console
$ docker pull lightstreamer@sha256:779b43dc7e52de6aae551e1bceed7b9a2459315a1dcd05310229e9343f71e7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ce319df57573b1524cc406cd39fed3c34a3abaa3d1472ab4f9bd9fd9396a23`

```dockerfile
```

-	Layers:
	-	`sha256:aa078e0830cf5826072d38eb3e96e0a6a8ae2e307cf856011c28b359d437439c`  
		Last Modified: Wed, 22 Jan 2025 19:38:28 GMT  
		Size: 20.8 KB (20792 bytes)  
		MIME: application/vnd.in-toto+json

### `lightstreamer:latest` - linux; arm64 variant v8

```console
$ docker pull lightstreamer@sha256:f61154d23fe31c332f304d06f4403e71858155edf580fea0261b6e46e90f54d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267823192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825d1251970d4eaca018080e9cbad061a07ecf491cce449708a2f98bdc8855d8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `[".\/LS.sh","run"]`

```dockerfile
# Fri, 04 Oct 2024 12:48:42 GMT
ARG RELEASE
# Fri, 04 Oct 2024 12:48:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Oct 2024 12:48:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Oct 2024 12:48:42 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 04 Oct 2024 12:48:42 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Fri, 04 Oct 2024 12:48:42 GMT
CMD ["/bin/bash"]
# Fri, 04 Oct 2024 12:48:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Oct 2024 12:48:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Oct 2024 12:48:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 04 Oct 2024 12:48:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Fri, 04 Oct 2024 12:48:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c654d98404c073b8a7e66bffb27f4ae3e7ede47d13284c132d40a83144bfd8c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='6482639ed9fd22aa2e704cc366848b1b3e1586d2bf1213869c43e80bca58fe5c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='3c6f4c358facfb6c19d90faf02bfe0fc7512d6b0e80ac18146bbd7e0d01deeef';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        riscv64)          ESUM='2f1b3e401e36de803398dfb9818861f9f14ca8ae7db650ea0946ab048fefe3b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='51a7ca42cc2e8cb5f3e7a326c28912ee84ff0791a1ca66650a8c53af07510a7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Oct 2024 12:48:42 GMT
CMD ["jshell"]
# Fri, 04 Oct 2024 12:48:42 GMT
LABEL maintainer=Lightstreamer Server Development Team <support@lightstreamer.com>
# Fri, 04 Oct 2024 12:48:42 GMT
RUN apt-get -y update         && apt-get -y install gnupg         && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9B90BFD14309C7DA5EF58D7D4A8C08966F29B4D2 # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
ENV LIGHTSTREAMER_VERSION=7.4.5
# Fri, 04 Oct 2024 12:48:42 GMT
ENV LIGHTSTREAMER_URL_DOWNLOAD=https://lightstreamer.com/distros/ls-server/7.4.5/Lightstreamer-7.4.5.tar.gz
# Fri, 04 Oct 2024 12:48:42 GMT
RUN set -ex;         mkdir /lightstreamer && cd /lightstreamer         && curl -fSL -o Lightstreamer.tar.gz ${LIGHTSTREAMER_URL_DOWNLOAD}         && curl -fSL -o Lightstreamer.tar.gz.asc ${LIGHTSTREAMER_URL_DOWNLOAD}.asc         && gpg --batch --verify Lightstreamer.tar.gz.asc Lightstreamer.tar.gz         && tar -xvf Lightstreamer.tar.gz --strip-components=1         && sed -i -e 's/<appender-ref ref="LSDailyRolling" \/>/<appender-ref ref="LSConsole" \/>/'                   -e '/<logger name="LightstreamerLogger.init/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerLogger.license/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerProxyAdapters/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   conf/lightstreamer_log_conf.xml         && groupadd -r -g 10000 lightstreamer         && useradd --no-log-init -r -g lightstreamer -u 10000 lightstreamer         && chown -R lightstreamer:lightstreamer ../lightstreamer         && rm Lightstreamer.tar.gz Lightstreamer.tar.gz.asc # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
USER lightstreamer
# Fri, 04 Oct 2024 12:48:42 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Oct 2024 12:48:42 GMT
WORKDIR /lightstreamer/bin/unix-like
# Fri, 04 Oct 2024 12:48:42 GMT
CMD ["./LS.sh" "run"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8112b468d97fc1b8e58f23cc45c7b4449288dfc6348767e8522c42643be9f62f`  
		Last Modified: Wed, 22 Jan 2025 21:03:59 GMT  
		Size: 24.2 MB (24159896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4070d123f1c8024fe0d23b9df0abdff5c37994fc0511bff566849036140f38`  
		Last Modified: Wed, 22 Jan 2025 21:10:20 GMT  
		Size: 155.8 MB (155805647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3586bd8e35a27844797c828dbd4b64e1953605c6e09926eaf070349e568ab61`  
		Last Modified: Wed, 22 Jan 2025 21:10:16 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2faf97487b15d11995a875b77fba63c54af9f60c47cc8670c541dd171df7eeb`  
		Last Modified: Wed, 22 Jan 2025 21:10:16 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f44a5b518f3752bd5839ae505d069bf234db41b0d263d498b9e18ec46993c16`  
		Last Modified: Thu, 23 Jan 2025 00:46:22 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3c877a2798717d1123f1612e0a369557686a0010c3052b88370544420cd203`  
		Last Modified: Thu, 23 Jan 2025 00:46:24 GMT  
		Size: 59.0 MB (58959833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `lightstreamer:latest` - unknown; unknown

```console
$ docker pull lightstreamer@sha256:40cf8d8d336d226aca319d272935d225375ac614c454d279854545060bda9aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e473a18ae0323997a35603f279631dfc6dd65d4de3bb3491994202899cbd28`

```dockerfile
```

-	Layers:
	-	`sha256:39124cd34c826f5b8b1853d7655f1c3d424bd2d69972201af2a5e80ba3bde651`  
		Last Modified: Thu, 23 Jan 2025 00:46:21 GMT  
		Size: 21.0 KB (20998 bytes)  
		MIME: application/vnd.in-toto+json
