## `lightstreamer:7-jdk11-temurin`

```console
$ docker pull lightstreamer@sha256:00ded7f05ca10379ba015cedbc96b5808a6ef782bb71a5ebdc534b9136d14ef0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `lightstreamer:7-jdk11-temurin` - linux; amd64

```console
$ docker pull lightstreamer@sha256:905c51c91e147e4c11e15fc681af118a9d9703e8ca93ff7195e2b773571c1c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251408249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85b4b917425a82b535f08c72d50041ab6ac8caac99b15f82eb4e921594ff61fb`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 11:07:31 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Thu, 20 Feb 2025 11:07:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='dc6136eaa8c1898cbf8973bb1e203e1f653f4c9166be0f5bebe0b02c5f3b5ae3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='4decd2e5caf4667144091cf723458b14148dc990730b3ecb34bba5eb1aa4ad5d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='5eb00b18e37757775e6f46c706eae38d9e91be49de5712987801cba8ffd77767';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='9407ecef765ec681fb187f084f1e029001abd5baf7a13b32067e9cbdfb140130';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='89df8583779b880f21b6cf29ddd9438961e2b1a092f416d05255fd6cd7f0e9fe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:9ea5a509df298cf38e68f05470427ca0916c94878e56dd6a1115d3d58a5ea8c2`  
		Last Modified: Thu, 08 May 2025 17:08:26 GMT  
		Size: 17.0 MB (16967762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5237d93da24e4debba6f2e8318814c8c3991df8f4e2fa2f17cf8c8b316a9e4d7`  
		Last Modified: Thu, 08 May 2025 17:08:38 GMT  
		Size: 145.6 MB (145644823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dced65dce150f2f9daeae4c3d2cab6ef042dd5972f0c1d1f97e88fb9e516ae89`  
		Last Modified: Thu, 08 May 2025 17:08:24 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96103e3519e13ac7a5535cc613dbcefc69ed92bd014abdc37e091aeccf0a3d5e`  
		Last Modified: Thu, 08 May 2025 17:08:25 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37096dcfdc26a05fed0795a96a935b565b1cc602e444983e6922c52b271755d`  
		Last Modified: Mon, 05 May 2025 17:03:36 GMT  
		Size: 2.6 KB (2645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607b509a8713d74c7eabedde50b161835df36cd0284f870b04629bba7d43802f`  
		Last Modified: Mon, 05 May 2025 17:03:37 GMT  
		Size: 59.1 MB (59072984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `lightstreamer:7-jdk11-temurin` - unknown; unknown

```console
$ docker pull lightstreamer@sha256:de865dd0fe5308a8252f70c12c7d68cb8827e26301ab7a2f22a98fecb7e560a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fa5653c65a7187925f26d362f875e3f0d3b6697ee66ef7c92a0423b88a6599`

```dockerfile
```

-	Layers:
	-	`sha256:13f2db26239783e0ccdcab5e2719bf19c0b4c8712f7c27804a5b1742a80ded05`  
		Last Modified: Mon, 05 May 2025 17:03:36 GMT  
		Size: 19.6 KB (19562 bytes)  
		MIME: application/vnd.in-toto+json

### `lightstreamer:7-jdk11-temurin` - linux; arm64 variant v8

```console
$ docker pull lightstreamer@sha256:9bcaf9c564f0265d77092c196ee63921b2ef7da1ad59c7f4264b2eaa03272c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247344290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f34515bf9bd91d54d2d7573baad43e1b624c29d877a1d15848ca0e772a2454`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 11:07:31 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Thu, 20 Feb 2025 11:07:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='dc6136eaa8c1898cbf8973bb1e203e1f653f4c9166be0f5bebe0b02c5f3b5ae3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='4decd2e5caf4667144091cf723458b14148dc990730b3ecb34bba5eb1aa4ad5d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='5eb00b18e37757775e6f46c706eae38d9e91be49de5712987801cba8ffd77767';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='9407ecef765ec681fb187f084f1e029001abd5baf7a13b32067e9cbdfb140130';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='89df8583779b880f21b6cf29ddd9438961e2b1a092f416d05255fd6cd7f0e9fe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:44030c5633c35d5105714bc1403c988244c1f643b1d66f623b7e1beade4140a0`  
		Last Modified: Thu, 08 May 2025 17:05:03 GMT  
		Size: 17.0 MB (16987252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9675235e846214e368835907fe9655bea78cad506c48c22196afab8e8daa71e`  
		Last Modified: Thu, 08 May 2025 17:08:25 GMT  
		Size: 142.4 MB (142432046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec07b40a06bdb98c53134ee9bf54ebcf557b93b34597345274d02cafd429c31d`  
		Last Modified: Thu, 08 May 2025 17:08:33 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed0a44d0975e1975b3897afc2495d455c77d243a6e1b6bdce8f87bc4836ae3`  
		Last Modified: Thu, 08 May 2025 17:08:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1affc692d6ded9f4360900975e5bb31b99a74fc003fe7c5cc20bdc846ae179e9`  
		Last Modified: Mon, 05 May 2025 21:51:13 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e67cef462902f0b8458c2072a6657a2dd0dfd0a3408d7220f8de2e15b084a48`  
		Last Modified: Mon, 05 May 2025 21:51:16 GMT  
		Size: 59.1 MB (59072973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `lightstreamer:7-jdk11-temurin` - unknown; unknown

```console
$ docker pull lightstreamer@sha256:70f2cd4cecb2762a852562bd29c2ba744c37afe5f56d99ac1050c673f82c6557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005914fbb335dcd45c83a629e17bcf9bfffba850de73b6c137ef470dc69a52b0`

```dockerfile
```

-	Layers:
	-	`sha256:18e5a58d834975ba57ed470800e7d1f80193bd916ef7f25c344d8a4fac4278e2`  
		Last Modified: Mon, 05 May 2025 21:51:13 GMT  
		Size: 19.7 KB (19720 bytes)  
		MIME: application/vnd.in-toto+json
