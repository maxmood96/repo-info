## `tomee:jre8-Temurin`

```console
$ docker pull tomee@sha256:0c77b6fdfb906d9cff344d359cb70933b185e8fdf2429b5a5b7e435121211ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomee:jre8-Temurin` - linux; amd64

```console
$ docker pull tomee@sha256:2df1d44967a8eec826d12fe36d8dee36facbee57566cd494b86f3e6ae959b41a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137943993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d722e2a159b8a8e049e6e15d782bf9bfce3802f3e70d69d7422dd0bfe97c9516`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:42:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 01:42:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 01:42:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 01:42:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:19:58 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 19:20:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 19:20:45 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 20:48:26 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 20:48:26 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 25 Jan 2023 20:48:26 GMT
WORKDIR /usr/local/tomee
# Wed, 25 Jan 2023 20:48:33 GMT
RUN apt-get update   && apt-get install -y  gpg   && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 20:48:42 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Wed, 25 Jan 2023 20:50:16 GMT
ENV TOMEE_VER=8.0.14
# Wed, 25 Jan 2023 20:50:16 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 25 Jan 2023 20:50:22 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz*
# Wed, 25 Jan 2023 20:50:22 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 20:50:22 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9923132fe6ab2c95fb9e2363f361139b8e50b7264d78acb7cf60147742acc985`  
		Last Modified: Fri, 09 Dec 2022 01:49:42 GMT  
		Size: 16.3 MB (16333067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48683cc1956721415c3f31ebffff58999e3b52f38a61345dd9006da0d71dbb1f`  
		Last Modified: Wed, 25 Jan 2023 19:27:30 GMT  
		Size: 41.8 MB (41824108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febac0649e9131da439e9eaf9297ba182840b4a25f39a37a82f28f315f3dc978`  
		Last Modified: Wed, 25 Jan 2023 19:27:25 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d765bdb7cc2509aedb6d3ac58cac75c0af2bc9bfe2acd587dd0e24a14fa26b`  
		Last Modified: Wed, 25 Jan 2023 21:04:57 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263b2c193d9ece183428bbaa3693bfebe9ab6c97acdc65fed580c472aa9f46aa`  
		Last Modified: Wed, 25 Jan 2023 21:04:57 GMT  
		Size: 3.7 MB (3662847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a3774cf144b3d82300962a26ab1d376fc818527ab0ca93a47be90de6bb1910`  
		Last Modified: Wed, 25 Jan 2023 21:04:56 GMT  
		Size: 62.9 KB (62906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46951ca338ae5e35ae5533015ea7d74b9d8d4a7c6c099683768278a2f506d762`  
		Last Modified: Wed, 25 Jan 2023 21:08:42 GMT  
		Size: 47.5 MB (47483852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:jre8-Temurin` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:18669f97733db45f2589eddcb53f827b6c13d04828a87d262a78c8400d9adc11
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135405611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24d0cc14702190f7bad8577fc2cc1825721722b5218ba9e6d0ee6d0f551287a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 26 Jan 2023 13:50:26 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:50:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:50:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:50:26 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:50:33 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Thu, 26 Jan 2023 13:50:33 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:43:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Jan 2023 17:43:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 17:43:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Jan 2023 17:43:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:43:47 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Tue, 31 Jan 2023 17:44:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 31 Jan 2023 17:44:53 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 31 Jan 2023 22:53:50 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 22:53:50 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 31 Jan 2023 22:53:51 GMT
WORKDIR /usr/local/tomee
# Tue, 31 Jan 2023 22:53:55 GMT
RUN apt-get update   && apt-get install -y  gpg   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 22:54:04 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 31 Jan 2023 22:54:04 GMT
ENV TOMEE_VER=8.0.14
# Tue, 31 Jan 2023 22:54:04 GMT
ENV TOMEE_BUILD=webprofile
# Tue, 31 Jan 2023 22:54:10 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz*
# Tue, 31 Jan 2023 22:54:10 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 22:54:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df2d776c5c5ff7acd285901b61b2f581c9497f13a32d1a49db14e3a2b7536be`  
		Last Modified: Tue, 31 Jan 2023 17:50:10 GMT  
		Size: 16.2 MB (16204764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b0fb8f69d11793dda23c1a161357fba15314605986ee080d1ad79070aedfea`  
		Last Modified: Tue, 31 Jan 2023 17:50:47 GMT  
		Size: 40.8 MB (40808828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97de89094949687426aded5e695c6aa3bbe838604da5d83667fa689309fdd28`  
		Last Modified: Tue, 31 Jan 2023 17:50:43 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4f73574bec73278b38445c0f8667787bd4cb159e34c903ebe6b1e407644811`  
		Last Modified: Tue, 31 Jan 2023 23:19:55 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded3b397768956aed2420bdd6119aaa577fdca2e3d4ec2a2c70f9f6996a2de6d`  
		Last Modified: Tue, 31 Jan 2023 23:19:56 GMT  
		Size: 3.7 MB (3651144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae462889b8fe36166be51324df20ad8f9c578c783967fdf3ef12a1c69ff1f19`  
		Last Modified: Tue, 31 Jan 2023 23:19:55 GMT  
		Size: 62.9 KB (62914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0b899d4a8d6a33492e26cd205baba837c2e481065483ae23ae283786c98756`  
		Last Modified: Tue, 31 Jan 2023 23:19:58 GMT  
		Size: 47.5 MB (47483892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
