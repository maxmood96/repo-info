## `lightstreamer:7-jdk11-temurin`

```console
$ docker pull lightstreamer@sha256:7f61e1cb3f3998b4ffa0b0db2f591bdbec0197f765c33f18cd7e55343d5563e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `lightstreamer:7-jdk11-temurin` - linux; amd64

```console
$ docker pull lightstreamer@sha256:26f9fa7fd086300c23cd30627f80d4cb4be4f10d36c1f511426ef3c29fc2f48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.3 MB (251292670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee14c3e547d0a79c1a3c02df537435abd0a22aff887c5d39774739593cc35d5`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Fri, 04 Oct 2024 12:48:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='191baa2e052627614022171400a917d28f0987dc54da48aaf07b06f552bb9884';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='f2087cc3abdd509b74facf8e43e81e36244d14c70dec080b8f3a662695417ca7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6bdd7da08c9f8fedded8da0411b6566c16cb9a904d164b68a0b7f11c8376673a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='0014ffdae26d2b8f840b4842e3f9d4edc3576b4a961770708273d8ecc86ba5b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='5fb661da82943f42a14bed94beda6d4dd3188987bd13b77e8b6f907054a73e9d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:3821a13f2b31421584f6d74839f18b0fb1989084be5d424eadbffb78d173abf7`  
		Last Modified: Wed, 22 Jan 2025 18:27:54 GMT  
		Size: 17.0 MB (16966728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d83cad2e0a1624b2f5d9115bbd6760c79b9bd1d7076d776fdf434ff42da8e7b`  
		Last Modified: Wed, 22 Jan 2025 18:27:56 GMT  
		Size: 145.6 MB (145608992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838d869a877530e00422b76b4d652da4f151143772e7a938b693caf44198405a`  
		Last Modified: Wed, 22 Jan 2025 18:27:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f9cf0f943b65414cb0e3376ce0edc15fb285a135b6523b5f695e51ece38a6`  
		Last Modified: Wed, 22 Jan 2025 18:27:54 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6738637ee86e525733d0ada1c7c48f4a558a66d5856c21e336a86d1ef97a680b`  
		Last Modified: Wed, 22 Jan 2025 19:38:15 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667d9e6213005d6414174ee505fdfc3792a0236071c589cf335a5eb93281651d`  
		Last Modified: Wed, 22 Jan 2025 19:38:17 GMT  
		Size: 59.0 MB (58959839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `lightstreamer:7-jdk11-temurin` - unknown; unknown

```console
$ docker pull lightstreamer@sha256:c238f57cabfcfdd2fea0535310d34313f3ddcbda58b29c0c859a348369a59edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6d98c2a5e086b9c417fd60ef841cb63c5f66bffe5b84ebb05a383816fcabb7`

```dockerfile
```

-	Layers:
	-	`sha256:7caa5255c29dc9fbc25481981951c1e45f4fc7cf1912624f33af5f5ce3a7abff`  
		Last Modified: Wed, 22 Jan 2025 19:38:15 GMT  
		Size: 19.6 KB (19562 bytes)  
		MIME: application/vnd.in-toto+json

### `lightstreamer:7-jdk11-temurin` - linux; arm64 variant v8

```console
$ docker pull lightstreamer@sha256:b6fdfefc6e04aa3f50b37342efd6f81ca31c9568ea0099d7fc4a1c3c35d0b54d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247227844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d91184dacf6ec6705ecef55c603b556f619b01470663ad5516ac93b192a5a1`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Fri, 04 Oct 2024 12:48:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='191baa2e052627614022171400a917d28f0987dc54da48aaf07b06f552bb9884';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='f2087cc3abdd509b74facf8e43e81e36244d14c70dec080b8f3a662695417ca7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6bdd7da08c9f8fedded8da0411b6566c16cb9a904d164b68a0b7f11c8376673a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='0014ffdae26d2b8f840b4842e3f9d4edc3576b4a961770708273d8ecc86ba5b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='5fb661da82943f42a14bed94beda6d4dd3188987bd13b77e8b6f907054a73e9d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:370f8a7b7cf214f61cc1a2546f38e47ba749cb698659b51aa07e70fcecbd7e2f`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 17.0 MB (16982856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c530cc6ab046b19072365b8fb7487e6403ab28eafc4b1af8a84c7f66621b0e33`  
		Last Modified: Wed, 22 Jan 2025 20:58:17 GMT  
		Size: 142.4 MB (142387296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b071da2e36cd1c43af95f429b3fb3695cbcf1f18fbaff07102104308cb330460`  
		Last Modified: Wed, 22 Jan 2025 20:58:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fbfab1f1c0c83577e4bf53eab3ddc2a97a14bfcd47729e3749066c2f987494`  
		Last Modified: Wed, 22 Jan 2025 20:58:14 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9770bb95df1e9d574575e0d0b8ebdf0fa685ba98ef21b4206513117ec2018cd`  
		Last Modified: Thu, 23 Jan 2025 00:45:44 GMT  
		Size: 2.6 KB (2645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106db73a847795c11b4d47f784978518d5fc1159aced00191176669cc606fd66`  
		Last Modified: Thu, 23 Jan 2025 00:45:46 GMT  
		Size: 59.0 MB (58959870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `lightstreamer:7-jdk11-temurin` - unknown; unknown

```console
$ docker pull lightstreamer@sha256:fc8ca50cf7f1879ab3d9495b6885fc7cc77e330cb5f02529f4d41faea72f8870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8130d01eb10588e2a9d1c959747bd3a7a00bc5a2d7ef165b88b796edc5a9b7`

```dockerfile
```

-	Layers:
	-	`sha256:2b13b11aeec0aa9606d8d2641f698f90e71051d04a3037e1efecf63fd31af259`  
		Last Modified: Thu, 23 Jan 2025 00:45:44 GMT  
		Size: 19.7 KB (19720 bytes)  
		MIME: application/vnd.in-toto+json
