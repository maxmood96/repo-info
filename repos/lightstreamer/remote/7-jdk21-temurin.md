## `lightstreamer:7-jdk21-temurin`

```console
$ docker pull lightstreamer@sha256:3e0a9dde47bf58b0a158c766afd922bb1b31ebcb11e270ecf4f22fb072100737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `lightstreamer:7-jdk21-temurin` - linux; amd64

```console
$ docker pull lightstreamer@sha256:2cf554b502f958fabee6637db199aa7757cd6ff514d0dce81d00709a6d41ae85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269835986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90e2917b00dabe8c6f44210a85bc7a92f4437b9b2f9c3bea0b1847957af0a61`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `[".\/LS.sh","run"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7d3ab0e8eba95bd682cfda8041c6cb6fa21e09d0d9131316fd7c96c78969de31';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fffa52c22d797b715a962e6c8d11ec7d79b90dd819b5bc51d62137ea4b22a340';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9a1079d7f0fc72951fdc9a0029e49a15f6ba114683aee626f882ee2c761f1d57';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f57a078d417614e5d78c07c77a6d8a04701058cf692c8e2868d593582be92768';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Thu, 02 May 2024 06:34:55 GMT
LABEL maintainer=Lightstreamer Server Development Team <support@lightstreamer.com>
# Thu, 02 May 2024 06:35:01 GMT
RUN apt-get -y update         && apt-get -y install gnupg         && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 06:35:02 GMT
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9B90BFD14309C7DA5EF58D7D4A8C08966F29B4D2
# Thu, 02 May 2024 06:35:02 GMT
ENV LIGHTSTREAMER_VERSION=7.4.2
# Thu, 02 May 2024 06:35:02 GMT
ENV LIGHTSTREAMER_URL_DOWNLOAD=https://lightstreamer.com/distr/ls-server/7.4.2/Lightstreamer-7.4.2.tar.gz
# Thu, 02 May 2024 06:35:05 GMT
RUN set -ex;         mkdir /lightstreamer && cd /lightstreamer         && curl -fSL -o Lightstreamer.tar.gz ${LIGHTSTREAMER_URL_DOWNLOAD}         && curl -fSL -o Lightstreamer.tar.gz.asc ${LIGHTSTREAMER_URL_DOWNLOAD}.asc         && gpg --batch --verify Lightstreamer.tar.gz.asc Lightstreamer.tar.gz         && tar -xvf Lightstreamer.tar.gz --strip-components=1         && sed -i -e 's/<appender-ref ref="LSDailyRolling" \/>/<appender-ref ref="LSConsole" \/>/'                   -e '/<logger name="LightstreamerLogger.init/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerLogger.license/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerProxyAdapters/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   conf/lightstreamer_log_conf.xml         && groupadd -r -g 10000 lightstreamer         && useradd --no-log-init -r -g lightstreamer -u 10000 lightstreamer         && chown -R lightstreamer:lightstreamer ../lightstreamer         && rm Lightstreamer.tar.gz Lightstreamer.tar.gz.asc
# Thu, 02 May 2024 06:35:05 GMT
USER lightstreamer
# Thu, 02 May 2024 06:35:05 GMT
EXPOSE 8080
# Thu, 02 May 2024 06:35:05 GMT
WORKDIR /lightstreamer/bin/unix-like
# Thu, 02 May 2024 06:35:05 GMT
CMD ["./LS.sh" "run"]
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5d1bccc5440d3a24f4a620704b9e687b4163c6c872fcc8e812e200c9bbac58`  
		Last Modified: Thu, 02 May 2024 01:18:08 GMT  
		Size: 17.5 MB (17456240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd7ada947ce7661ad85815ab478851ccf7b0d064cde9c9195bafb2bd499b29e`  
		Last Modified: Thu, 02 May 2024 01:19:17 GMT  
		Size: 158.5 MB (158512068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478e5694bb3e0cbd54a331514092737b8a8de5a4fe7069a3f00e6eb1b98fd605`  
		Last Modified: Thu, 02 May 2024 01:19:05 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fa38685928ae1a460299486cb01d7d2db1eff47fbd68c8ac6c936e89af1641`  
		Last Modified: Thu, 02 May 2024 01:19:05 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2077a5737957b2cd052df598d8d9df4f48bd1a6e6dc8de83abeb53578cca00`  
		Last Modified: Thu, 02 May 2024 06:39:44 GMT  
		Size: 3.6 MB (3602320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6021f0cd674d9dd034ef4ede4a7066cc5bc384ccace65b441792593f34c34dfb`  
		Last Modified: Thu, 02 May 2024 06:39:43 GMT  
		Size: 2.4 KB (2399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faad40191ab5be1f302147026757820b9abe36948a504bfb86825d72156bcd9f`  
		Last Modified: Thu, 02 May 2024 06:39:47 GMT  
		Size: 59.8 MB (59822401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `lightstreamer:7-jdk21-temurin` - linux; arm64 variant v8

```console
$ docker pull lightstreamer@sha256:fb49edce80a5524eaecdd58b6fb270ba4a2fa28a86bb33df43883170ccd44605
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267337092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42e6478ddd6b60e71a372d1d6a1d2f696edea9feda5976bea05985ef7c6ada8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `[".\/LS.sh","run"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7d3ab0e8eba95bd682cfda8041c6cb6fa21e09d0d9131316fd7c96c78969de31';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fffa52c22d797b715a962e6c8d11ec7d79b90dd819b5bc51d62137ea4b22a340';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9a1079d7f0fc72951fdc9a0029e49a15f6ba114683aee626f882ee2c761f1d57';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f57a078d417614e5d78c07c77a6d8a04701058cf692c8e2868d593582be92768';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Wed, 05 Jun 2024 09:18:24 GMT
LABEL maintainer=Lightstreamer Server Development Team <support@lightstreamer.com>
# Wed, 05 Jun 2024 09:18:39 GMT
RUN apt-get -y update         && apt-get -y install gnupg         && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 09:18:40 GMT
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9B90BFD14309C7DA5EF58D7D4A8C08966F29B4D2
# Wed, 05 Jun 2024 09:18:40 GMT
ENV LIGHTSTREAMER_VERSION=7.4.2
# Wed, 05 Jun 2024 09:18:40 GMT
ENV LIGHTSTREAMER_URL_DOWNLOAD=https://lightstreamer.com/distr/ls-server/7.4.2/Lightstreamer-7.4.2.tar.gz
# Wed, 05 Jun 2024 09:18:43 GMT
RUN set -ex;         mkdir /lightstreamer && cd /lightstreamer         && curl -fSL -o Lightstreamer.tar.gz ${LIGHTSTREAMER_URL_DOWNLOAD}         && curl -fSL -o Lightstreamer.tar.gz.asc ${LIGHTSTREAMER_URL_DOWNLOAD}.asc         && gpg --batch --verify Lightstreamer.tar.gz.asc Lightstreamer.tar.gz         && tar -xvf Lightstreamer.tar.gz --strip-components=1         && sed -i -e 's/<appender-ref ref="LSDailyRolling" \/>/<appender-ref ref="LSConsole" \/>/'                   -e '/<logger name="LightstreamerLogger.init/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerLogger.license/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerProxyAdapters/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   conf/lightstreamer_log_conf.xml         && groupadd -r -g 10000 lightstreamer         && useradd --no-log-init -r -g lightstreamer -u 10000 lightstreamer         && chown -R lightstreamer:lightstreamer ../lightstreamer         && rm Lightstreamer.tar.gz Lightstreamer.tar.gz.asc
# Wed, 05 Jun 2024 09:18:43 GMT
USER lightstreamer
# Wed, 05 Jun 2024 09:18:43 GMT
EXPOSE 8080
# Wed, 05 Jun 2024 09:18:43 GMT
WORKDIR /lightstreamer/bin/unix-like
# Wed, 05 Jun 2024 09:18:43 GMT
CMD ["./LS.sh" "run"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd5d7dbc0eb75f9bc71643e6dcfed8b6cef6295e5c7d5f5ba90aa14f0d9cc6f`  
		Last Modified: Wed, 05 Jun 2024 04:57:07 GMT  
		Size: 18.9 MB (18859083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0a2a7710d9d7d0f88f9f13ede1b7ff2f89343d79308778db178dc4f312ae4a`  
		Last Modified: Wed, 05 Jun 2024 04:58:04 GMT  
		Size: 156.7 MB (156672853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e96aef1e76c15d9c20747e43105bca90537c6bb652ea98bc96ef69728de212`  
		Last Modified: Wed, 05 Jun 2024 04:57:54 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a3dedce6ac6bb05c0e8a5dbdcc1f91df5880b0dd7eb1e077172730f1f2322e`  
		Last Modified: Wed, 05 Jun 2024 04:57:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97b4958722847081ce6d384c1e2104de279cefd65da409640abbcfbb01be071`  
		Last Modified: Wed, 05 Jun 2024 09:23:06 GMT  
		Size: 3.6 MB (3577170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce94f5bd46ced6a0007957837eda7b9da764f35607ab52d3b11e3160d09016a7`  
		Last Modified: Wed, 05 Jun 2024 09:23:06 GMT  
		Size: 2.4 KB (2364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262bd03ad1057cc2a1a5fb4f7b259d4133783b3d2d0dfbbdc9fe3bb4514a7fe5`  
		Last Modified: Wed, 05 Jun 2024 09:23:09 GMT  
		Size: 59.8 MB (59822409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
