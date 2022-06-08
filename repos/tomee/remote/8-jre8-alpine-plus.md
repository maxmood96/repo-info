## `tomee:8-jre8-alpine-plus`

```console
$ docker pull tomee@sha256:261799d5820228e8177a2de616a14a21e49b511a0453ccf3dc6eca2bc6ef821b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:8-jre8-alpine-plus` - linux; amd64

```console
$ docker pull tomee@sha256:439437f174052f2585c674a65a88e133bb5704d42368e18821b6d1f02131736c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121670289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1c3cd580cb4ea9f2dc465aa640c303f20ae6a8a1bca9dc58d7af6165fd5d97`
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
# Wed, 08 Jun 2022 18:20:30 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Wed, 08 Jun 2022 18:21:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='58d584ac185c21ce8e90124cdfdf29621c7af52ac8a4e3aa9bdb08d53249a7f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 08 Jun 2022 18:21:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jun 2022 18:21:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 08 Jun 2022 19:53:47 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jun 2022 19:53:48 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 08 Jun 2022 19:53:48 GMT
WORKDIR /usr/local/tomee
# Wed, 08 Jun 2022 19:53:49 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/*
# Wed, 08 Jun 2022 19:53:59 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Wed, 08 Jun 2022 19:53:59 GMT
ENV TOMEE_VER=8.0.11
# Wed, 08 Jun 2022 19:54:45 GMT
ENV TOMEE_BUILD=plus
# Wed, 08 Jun 2022 19:54:53 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo "`cat tomee.tar.gz.sha512`  apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz" | sha512sum -c   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz*
# Wed, 08 Jun 2022 19:54:53 GMT
EXPOSE 8080
# Wed, 08 Jun 2022 19:54:53 GMT
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
	-	`sha256:6aea14557a82e943cf796fdf2deda96027076f12b86ef2fd1adc421d91da2516`  
		Last Modified: Wed, 08 Jun 2022 18:25:34 GMT  
		Size: 41.8 MB (41758960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7c91ae80cd6fbffffacfdbf443f6b7eb1b203ead030d80c7e17298c210876f`  
		Last Modified: Wed, 08 Jun 2022 18:25:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba37515a7d29214134f3656e485dd2cdfddee2ad418679e16dc0a7401de7ff3`  
		Last Modified: Wed, 08 Jun 2022 20:23:04 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed364dae0a609fc1c0e5c22e17addf5bcc40356d699369b7dfd7fb7fdd3f9f4e`  
		Last Modified: Wed, 08 Jun 2022 20:23:06 GMT  
		Size: 6.6 MB (6613529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beabeb836f095724354d5e18d945bf2bc8dae7df5dd449751904806e715f1165`  
		Last Modified: Wed, 08 Jun 2022 20:23:04 GMT  
		Size: 62.9 KB (62925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a40574840b87641f66062ea5c6d112c3f9ad420a3b5562d85ad4cf2eaa02a70`  
		Last Modified: Wed, 08 Jun 2022 20:25:06 GMT  
		Size: 70.0 MB (69989539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
