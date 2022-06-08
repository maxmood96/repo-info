## `tomee:9-jre11-Temurin-alpine-webprofile`

```console
$ docker pull tomee@sha256:36d46e4c9011422f4584073361fc41e6a568cec483a888454a2a45325dc9e912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:9-jre11-Temurin-alpine-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:c003ab88f0966c1ff7faa6fc91d7d3f1d5ebec06ecf9b4dfbd130f433435fb33
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107631210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57f0f9433d43d98df2a9f462cda040f6c0a5231b533f592c234db9553bd9579`
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
# Wed, 08 Jun 2022 18:21:14 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Wed, 08 Jun 2022 18:21:53 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='364b0f4faac666a9e81bf17b4e8b5cefa655b0f688cf3e0c1e78eb9d0ce9dca0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 08 Jun 2022 18:21:54 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jun 2022 18:21:54 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 08 Jun 2022 19:52:20 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jun 2022 19:52:21 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 08 Jun 2022 19:52:21 GMT
WORKDIR /usr/local/tomee
# Wed, 08 Jun 2022 19:52:23 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/*
# Wed, 08 Jun 2022 19:52:32 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Wed, 08 Jun 2022 19:57:03 GMT
ENV TOMEE_VER=9.0.0-M7
# Wed, 08 Jun 2022 19:57:04 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 08 Jun 2022 19:57:10 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo "`cat tomee.tar.gz.sha512`  apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz" | sha512sum -c   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz*
# Wed, 08 Jun 2022 19:57:10 GMT
EXPOSE 8080
# Wed, 08 Jun 2022 19:57:10 GMT
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
	-	`sha256:c41a2047547fbd817a6ffe41f4609e4229a8467c40f26a4de3f781c98dfdb036`  
		Last Modified: Wed, 08 Jun 2022 18:26:21 GMT  
		Size: 43.1 MB (43141175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d516bce9ddef42610f5b5de7d25e2905190a437932e2ec7da850b855a9d6c3`  
		Last Modified: Wed, 08 Jun 2022 18:26:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274aa84b83655c979050119f0117ae7ec0c143a6fad8956cde922a35778ff215`  
		Last Modified: Wed, 08 Jun 2022 20:20:17 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584b2be4cddcf028f32de9d13a9dae3846669e6ee00cfc67a6aaecf4fd9cb07e`  
		Last Modified: Wed, 08 Jun 2022 20:20:18 GMT  
		Size: 6.6 MB (6613549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8b107a48650ad795e687734e55689e92e9771e17f7c309abf8f36ea58d2854`  
		Last Modified: Wed, 08 Jun 2022 20:20:17 GMT  
		Size: 62.9 KB (62902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6705a8bed8d266bdbe6a43e487a09d8b47543caf8d209c3f53dea35f0fc61cf`  
		Last Modified: Wed, 08 Jun 2022 20:30:52 GMT  
		Size: 54.6 MB (54568249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
