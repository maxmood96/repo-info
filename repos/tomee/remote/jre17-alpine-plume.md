## `tomee:jre17-alpine-plume`

```console
$ docker pull tomee@sha256:ff1348cc6937079c6ba8aee9bd4127f0ca74aea0451c29fe8b3b62ba74c5ed1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:jre17-alpine-plume` - linux; amd64

```console
$ docker pull tomee@sha256:f41c6f40b182712551ea798d03eb26e68cf79b8e4d16c1af55f5550cc48bb609
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146463459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08c1901b01d0c32b068e035169bd1df3dbaa2a44f0dd679f63a70db0f6d058a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:48:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Mar 2023 19:48:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Mar 2023 19:48:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Mar 2023 19:48:58 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Wed, 26 Apr 2023 19:22:30 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Wed, 26 Apr 2023 19:23:42 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='711f837bacf8222dee9e8cd7f39941a4a0acf869243f03e6038ca3ba189f66ca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 26 Apr 2023 19:23:43 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 26 Apr 2023 22:01:25 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Apr 2023 22:01:25 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 26 Apr 2023 22:01:25 GMT
WORKDIR /usr/local/tomee
# Wed, 26 Apr 2023 22:02:13 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl  && rm -rf /var/cache/apk/*
# Wed, 26 Apr 2023 22:02:22 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Thu, 18 May 2023 17:23:32 GMT
ENV TOMEE_VER=8.0.15
# Thu, 18 May 2023 17:23:33 GMT
ENV TOMEE_BUILD=plume
# Thu, 18 May 2023 17:23:41 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz*
# Thu, 18 May 2023 17:23:41 GMT
EXPOSE 8080
# Thu, 18 May 2023 17:23:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ed194273be4d4d02a2158c3e7c9ea96095ed70f65939d53f4968b0f225c628`  
		Last Modified: Wed, 29 Mar 2023 19:52:03 GMT  
		Size: 12.0 MB (12019605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1fad4208ae4da715716444000ec00bcb7c7661084dfe69e2f0bd5738c71ca0`  
		Last Modified: Wed, 26 Apr 2023 19:34:16 GMT  
		Size: 46.8 MB (46776688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f30391b61e9f3eb7356ef46c0d0f49ee7cc848da94710eb833e824e5120835`  
		Last Modified: Wed, 26 Apr 2023 19:34:09 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c753e98fc9321bfd1d99f9d1e1aa08ef4941d41586e82e9ab378df04a125c3b`  
		Last Modified: Wed, 26 Apr 2023 22:22:43 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b688cee2dbf09fe8691c408b7b6ea6f838ce2dcc7e53927158e85d206b4bfbce`  
		Last Modified: Wed, 26 Apr 2023 22:24:31 GMT  
		Size: 6.5 MB (6482648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5467b9a4fe58c5b23242a545ca36a39c64ce066ff5043be336ad0dd17b10da`  
		Last Modified: Wed, 26 Apr 2023 22:24:30 GMT  
		Size: 62.9 KB (62894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456999f1882dc20f29c6a2ed8dd6dc5679bb8e32c531c5bfd33167135232532b`  
		Last Modified: Thu, 18 May 2023 17:41:41 GMT  
		Size: 77.7 MB (77746731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
