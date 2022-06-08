## `tomee:8-Temurin-alpine-webprofile`

```console
$ docker pull tomee@sha256:cc6c5f17d8b8413bd388b6f6bfec5f4ca7a7eb1856bc8bcf90caa5d466434d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:8-Temurin-alpine-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:3e9e5a12295ed2a466bfe9f264817ac3b3a9d599c7bd5754b192142df0f85e2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103210793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac7defff0a41bf29c24f9738cadbbcc0d2ef4d83b11735d62464dfe1a103867`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:55:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 08 Jun 2022 18:20:30 GMT
RUN apk add --no-cache libretls musl-locales musl-locales-lang tzdata zlib     && rm -rf /var/cache/apk/*
# Wed, 08 Jun 2022 18:22:03 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Wed, 08 Jun 2022 18:22:35 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='27e4589db9b8e6df60a75737f12ab7df63f796ecf8e46c0a196f77b2c99af1ac';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 08 Jun 2022 18:22:35 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jun 2022 18:22:36 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 08 Jun 2022 19:50:35 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jun 2022 19:50:36 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 08 Jun 2022 19:50:36 GMT
WORKDIR /usr/local/tomee
# Wed, 08 Jun 2022 19:50:37 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/*
# Wed, 08 Jun 2022 19:50:47 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Wed, 08 Jun 2022 19:50:47 GMT
ENV TOMEE_VER=8.0.11
# Wed, 08 Jun 2022 19:50:47 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 08 Jun 2022 19:50:53 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo "`cat tomee.tar.gz.sha512`  apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz" | sha512sum -c   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz*
# Wed, 08 Jun 2022 19:50:54 GMT
EXPOSE 8080
# Wed, 08 Jun 2022 19:50:54 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6611b459a9f120c9f22143fbef6dda47c621957b1c86d4cbdf8fe3d9c762d728`  
		Last Modified: Wed, 08 Jun 2022 18:25:04 GMT  
		Size: 430.4 KB (430445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112e65bbbd8096d560c40ac99c9ff887b570b76b3098c361475584a2ec5ed0c8`  
		Last Modified: Wed, 08 Jun 2022 18:27:11 GMT  
		Size: 46.6 MB (46582095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd15597cd87c71f63fe92e9c9b49b253848718a0ea545030a443bd6bf49fdc1e`  
		Last Modified: Wed, 08 Jun 2022 18:27:04 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a95ab91c0f55261df9ac0950f7dd05dcbed99c82d3816e05356ac9280fd2a2`  
		Last Modified: Wed, 08 Jun 2022 20:15:37 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ac52ab9edf5f03e017605e92cc0dafbde0653234856824934d3f2cd2208d62`  
		Last Modified: Wed, 08 Jun 2022 20:15:39 GMT  
		Size: 6.6 MB (6613527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb2d55aca49fa0654ade6f4bc590e572a1dbda31d34ae0240992489aa378895`  
		Last Modified: Wed, 08 Jun 2022 20:15:38 GMT  
		Size: 62.9 KB (62924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43caf17995ac9eece2fd5aaa95ab11732a36dd03532e66bda5f12b78c1e08fb4`  
		Last Modified: Wed, 08 Jun 2022 20:15:40 GMT  
		Size: 46.7 MB (46706911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
