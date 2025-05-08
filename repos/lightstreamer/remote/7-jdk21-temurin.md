## `lightstreamer:7-jdk21-temurin`

```console
$ docker pull lightstreamer@sha256:0b6846f9249dbccd0dac3a0a25954d797a3577f2cce921f64b79b8f19abd918e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `lightstreamer:7-jdk21-temurin` - linux; amd64

```console
$ docker pull lightstreamer@sha256:16e23c9430b4a0026cf5b6c86be89596a4631569996074ef6d9a691f5ed29b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269396730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8568ba7a9c20f209f4516d530b887c7370703f8e01048acabd9cd0fc5e94192`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `[".\/LS.sh","run"]`

```dockerfile
# Thu, 20 Feb 2025 11:07:31 GMT
ARG RELEASE
# Thu, 20 Feb 2025 11:07:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Feb 2025 11:07:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Feb 2025 11:07:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 20 Feb 2025 11:07:31 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Thu, 20 Feb 2025 11:07:31 GMT
CMD ["/bin/bash"]
# Thu, 20 Feb 2025 11:07:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Feb 2025 11:07:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Feb 2025 11:07:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 20 Feb 2025 11:07:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 11:07:31 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Thu, 20 Feb 2025 11:07:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='974d3acef0b7193f541acb61b76e81670890551366625d4f6ca01b91ac152ce0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='31dba70ba928c78c20d62049ac000f79f7a7ab11f9d9c11e703f52d60aa64f93';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='2ddc0dc14b07d9e853875aac7f84c23826fff18b9cea618c93efe0bcc8f419c2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='d75f33ee7f9e5532bce263db83443ffed7d9bae7ff3ed41e48d137808adfe513';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='216edbccab2d677639c90d2cb09dfa39c257788a62b8b83d879528c447b9ad33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 20 Feb 2025 11:07:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 20 Feb 2025 11:07:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 20 Feb 2025 11:07:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 20 Feb 2025 11:07:31 GMT
CMD ["jshell"]
# Thu, 20 Feb 2025 11:07:31 GMT
LABEL maintainer=Lightstreamer Server Development Team <support@lightstreamer.com>
# Thu, 20 Feb 2025 11:07:31 GMT
RUN apt-get -y update         && apt-get -y install gnupg         && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 11:07:31 GMT
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9B90BFD14309C7DA5EF58D7D4A8C08966F29B4D2 # buildkit
# Thu, 20 Feb 2025 11:07:31 GMT
ENV LIGHTSTREAMER_VERSION=7.4.6
# Thu, 20 Feb 2025 11:07:31 GMT
ENV LIGHTSTREAMER_URL_DOWNLOAD=https://lightstreamer.com/distros/ls-server/7.4.6/Lightstreamer-7.4.6.tar.gz
# Thu, 20 Feb 2025 11:07:31 GMT
RUN set -ex;         mkdir /lightstreamer && cd /lightstreamer         && curl -fSL -o Lightstreamer.tar.gz ${LIGHTSTREAMER_URL_DOWNLOAD}         && curl -fSL -o Lightstreamer.tar.gz.asc ${LIGHTSTREAMER_URL_DOWNLOAD}.asc         && gpg --batch --verify Lightstreamer.tar.gz.asc Lightstreamer.tar.gz         && tar -xvf Lightstreamer.tar.gz --strip-components=1         && sed -i -e 's/<appender-ref ref="LSDailyRolling" \/>/<appender-ref ref="LSConsole" \/>/'                   -e '/<logger name="LightstreamerLogger.init/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerLogger.license/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerProxyAdapters/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   conf/lightstreamer_log_conf.xml         && groupadd -r -g 10000 lightstreamer         && useradd --no-log-init -r -g lightstreamer -u 10000 lightstreamer         && chown -R lightstreamer:lightstreamer ../lightstreamer         && rm Lightstreamer.tar.gz Lightstreamer.tar.gz.asc # buildkit
# Thu, 20 Feb 2025 11:07:31 GMT
USER lightstreamer
# Thu, 20 Feb 2025 11:07:31 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 20 Feb 2025 11:07:31 GMT
WORKDIR /lightstreamer/bin/unix-like
# Thu, 20 Feb 2025 11:07:31 GMT
CMD ["./LS.sh" "run"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f526e30db5f3400aedfafd9fee4a897e6136cad2ba5377063a3ba2f4d9372697`  
		Last Modified: Thu, 08 May 2025 17:04:57 GMT  
		Size: 23.0 MB (22952890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bb17fdf011e86a2dc27b9b6d8df16cacad4a411aaf601bc9ab24f7f4b326db`  
		Last Modified: Thu, 08 May 2025 17:05:04 GMT  
		Size: 157.6 MB (157648162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4223556ed03c6bd1c69dff886afb2d3500c92850eaa663c9d88b1c0488b7f7a9`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cc8efa6ea79682d3418b90549eda220179c60092f15c979408627839067c6c`  
		Last Modified: Thu, 08 May 2025 17:04:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c85b8c1fcd0b3ab275d1a2db356910786c43501afe76555c7ec99b8a4e4fe76`  
		Last Modified: Thu, 08 May 2025 17:26:53 GMT  
		Size: 2.6 KB (2646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc85297036e261d6b8db3474db4046fbfdf8a8b7d432889f43f150c916ed96`  
		Last Modified: Thu, 08 May 2025 17:26:59 GMT  
		Size: 59.1 MB (59072998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `lightstreamer:7-jdk21-temurin` - unknown; unknown

```console
$ docker pull lightstreamer@sha256:d532ff5e23b4c8d8c87f4293040a6700f42b2c1c2e5d59b3a54a7143a287ea17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dfd1c78e71d1d194d7752473a7da7327f43924b2cbc1956674781e110feef0d`

```dockerfile
```

-	Layers:
	-	`sha256:d9c7190f311520bb7cd9a732a165cf7e0927c165347802d551daf04e675b6d9c`  
		Last Modified: Mon, 05 May 2025 17:03:38 GMT  
		Size: 20.8 KB (20788 bytes)  
		MIME: application/vnd.in-toto+json

### `lightstreamer:7-jdk21-temurin` - linux; arm64 variant v8

```console
$ docker pull lightstreamer@sha256:cb0f7de6cf111f8f5fc14ea0d8b76f405347a96959e700ea054cf2239505e7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268020081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2247980d65714c5ce37041e352ede4f0554f096213aa8863ccf44b2a87363b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `[".\/LS.sh","run"]`

```dockerfile
# Thu, 20 Feb 2025 11:07:31 GMT
ARG RELEASE
# Thu, 20 Feb 2025 11:07:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Feb 2025 11:07:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Feb 2025 11:07:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 20 Feb 2025 11:07:31 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Thu, 20 Feb 2025 11:07:31 GMT
CMD ["/bin/bash"]
# Thu, 20 Feb 2025 11:07:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Feb 2025 11:07:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Feb 2025 11:07:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 20 Feb 2025 11:07:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 11:07:31 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Thu, 20 Feb 2025 11:07:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='974d3acef0b7193f541acb61b76e81670890551366625d4f6ca01b91ac152ce0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='31dba70ba928c78c20d62049ac000f79f7a7ab11f9d9c11e703f52d60aa64f93';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='2ddc0dc14b07d9e853875aac7f84c23826fff18b9cea618c93efe0bcc8f419c2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='d75f33ee7f9e5532bce263db83443ffed7d9bae7ff3ed41e48d137808adfe513';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='216edbccab2d677639c90d2cb09dfa39c257788a62b8b83d879528c447b9ad33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 20 Feb 2025 11:07:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 20 Feb 2025 11:07:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 20 Feb 2025 11:07:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 20 Feb 2025 11:07:31 GMT
CMD ["jshell"]
# Thu, 20 Feb 2025 11:07:31 GMT
LABEL maintainer=Lightstreamer Server Development Team <support@lightstreamer.com>
# Thu, 20 Feb 2025 11:07:31 GMT
RUN apt-get -y update         && apt-get -y install gnupg         && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 11:07:31 GMT
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9B90BFD14309C7DA5EF58D7D4A8C08966F29B4D2 # buildkit
# Thu, 20 Feb 2025 11:07:31 GMT
ENV LIGHTSTREAMER_VERSION=7.4.6
# Thu, 20 Feb 2025 11:07:31 GMT
ENV LIGHTSTREAMER_URL_DOWNLOAD=https://lightstreamer.com/distros/ls-server/7.4.6/Lightstreamer-7.4.6.tar.gz
# Thu, 20 Feb 2025 11:07:31 GMT
RUN set -ex;         mkdir /lightstreamer && cd /lightstreamer         && curl -fSL -o Lightstreamer.tar.gz ${LIGHTSTREAMER_URL_DOWNLOAD}         && curl -fSL -o Lightstreamer.tar.gz.asc ${LIGHTSTREAMER_URL_DOWNLOAD}.asc         && gpg --batch --verify Lightstreamer.tar.gz.asc Lightstreamer.tar.gz         && tar -xvf Lightstreamer.tar.gz --strip-components=1         && sed -i -e 's/<appender-ref ref="LSDailyRolling" \/>/<appender-ref ref="LSConsole" \/>/'                   -e '/<logger name="LightstreamerLogger.init/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerLogger.license/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerProxyAdapters/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   conf/lightstreamer_log_conf.xml         && groupadd -r -g 10000 lightstreamer         && useradd --no-log-init -r -g lightstreamer -u 10000 lightstreamer         && chown -R lightstreamer:lightstreamer ../lightstreamer         && rm Lightstreamer.tar.gz Lightstreamer.tar.gz.asc # buildkit
# Thu, 20 Feb 2025 11:07:31 GMT
USER lightstreamer
# Thu, 20 Feb 2025 11:07:31 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 20 Feb 2025 11:07:31 GMT
WORKDIR /lightstreamer/bin/unix-like
# Thu, 20 Feb 2025 11:07:31 GMT
CMD ["./LS.sh" "run"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866e6e02a3bf59e32bfbd1d02232a5ba0268ea326e2ed72d9f05413d95c3dad2`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 24.2 MB (24163318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495e17cf917ed9f99f148bed91db100ec46f6f817f356eb12d8076b91dd4f456`  
		Last Modified: Thu, 08 May 2025 17:06:33 GMT  
		Size: 155.9 MB (155931746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966861f2a23809fda596d6f285cb6e4caa902d18bb726d1a7d3656620c2170e0`  
		Last Modified: Thu, 08 May 2025 17:06:18 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1b55ea8a34655b4a97b3358aa49763f45e877cea7287f1b3c34962306d2ccb`  
		Last Modified: Thu, 08 May 2025 17:06:18 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecfc0280c8e88b7fc8f8390011820d5aa8a99ac58d73f7eb17a833d6e37990c`  
		Last Modified: Mon, 05 May 2025 21:51:59 GMT  
		Size: 2.6 KB (2644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100805ed5c84e702baf92b5cdab9db38cb5aeafe4617a69cf2c5e9e5f631e951`  
		Last Modified: Mon, 05 May 2025 21:52:01 GMT  
		Size: 59.1 MB (59072992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `lightstreamer:7-jdk21-temurin` - unknown; unknown

```console
$ docker pull lightstreamer@sha256:60e872e0d3414224fa76b7e51701f0888f307400142605c9152b02d5c4029dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d869a93a86ccd0ef712de81ff977ef0fd6d1e5681692c67e00a93acf5867be0`

```dockerfile
```

-	Layers:
	-	`sha256:d01457604277b15c752c0db1df35241dfd5de7fba9d84bc4faea2c8025e080c2`  
		Last Modified: Mon, 05 May 2025 21:51:59 GMT  
		Size: 21.0 KB (20995 bytes)  
		MIME: application/vnd.in-toto+json
