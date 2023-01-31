## `tomee:jre11-plume`

```console
$ docker pull tomee@sha256:6e99e3b59e0013afab8a4195668dc1338a7d70cf4aea519e79cbb75c243bf8e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomee:jre11-plume` - linux; amd64

```console
$ docker pull tomee@sha256:dc54dd47e84ad20cf80597a900351835c0273e2ea1add4dd1a22aef6992eeb04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.2 MB (173160157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d228d2f209cba1f02eae0ede0887c9a7a38086c7e06265bddf89b5d8be8a0fce`
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
# Tue, 24 Jan 2023 18:43:45 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 24 Jan 2023 18:44:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 24 Jan 2023 18:44:55 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 24 Jan 2023 23:43:43 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 23:43:44 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 24 Jan 2023 23:43:44 GMT
WORKDIR /usr/local/tomee
# Tue, 24 Jan 2023 23:43:50 GMT
RUN apt-get update   && apt-get install -y  gpg   && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 23:43:59 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 24 Jan 2023 23:43:59 GMT
ENV TOMEE_VER=8.0.14
# Tue, 24 Jan 2023 23:44:21 GMT
ENV TOMEE_BUILD=plume
# Tue, 24 Jan 2023 23:44:29 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz*
# Tue, 24 Jan 2023 23:44:30 GMT
EXPOSE 8080
# Tue, 24 Jan 2023 23:44:30 GMT
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
	-	`sha256:d675ec7caedf9048f68226923204569d35728223f57ebef2ed7711d29acaf8b2`  
		Last Modified: Tue, 24 Jan 2023 18:52:11 GMT  
		Size: 46.6 MB (46632325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece60d0232551a0fee82970bcee86763b281c84c9e68892f62a0db0a0ffd8cd5`  
		Last Modified: Tue, 24 Jan 2023 18:52:04 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f021e3fab010f14a20a5117e4d3b2e77689c0c50a029c4c4e19d2618892938`  
		Last Modified: Wed, 25 Jan 2023 00:12:25 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9792b07a9059e141e786951bb795afbae7c5f38f40f3b7e4bdee67b2aa53f6ea`  
		Last Modified: Wed, 25 Jan 2023 00:12:26 GMT  
		Size: 3.7 MB (3662874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8030b5b0a8d028c6d00489eb587d5d260eede2531dd836638d391bd2f03fd97a`  
		Last Modified: Wed, 25 Jan 2023 00:12:25 GMT  
		Size: 62.9 KB (62905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4816e5c7940ef6e8946797dab8010f8f94234f981e41ec12ea73eb579b46d7c0`  
		Last Modified: Wed, 25 Jan 2023 00:14:37 GMT  
		Size: 77.9 MB (77891773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:jre11-plume` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:807b20beecf9fb31c30a3190e354279b090a9c366b8c404778f139f207771ce3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.0 MB (169984168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4fc3b3ac4a88f2108bddba907e801e65dced11ef393ad13050d2f40533cbf3`
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
# Tue, 31 Jan 2023 17:45:05 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 31 Jan 2023 17:45:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 31 Jan 2023 17:45:55 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 31 Jan 2023 22:52:56 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 22:52:57 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 31 Jan 2023 22:52:57 GMT
WORKDIR /usr/local/tomee
# Tue, 31 Jan 2023 22:53:01 GMT
RUN apt-get update   && apt-get install -y  gpg   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 22:53:10 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 31 Jan 2023 22:53:10 GMT
ENV TOMEE_VER=8.0.14
# Tue, 31 Jan 2023 22:53:29 GMT
ENV TOMEE_BUILD=plume
# Tue, 31 Jan 2023 22:53:37 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz*
# Tue, 31 Jan 2023 22:53:37 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 22:53:37 GMT
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
	-	`sha256:76723b8da9c095f872e8c72bcb2f65f48c079d7c5d1d7e3ddb2b66e9921ebdc3`  
		Last Modified: Tue, 31 Jan 2023 17:52:04 GMT  
		Size: 45.0 MB (44979511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ba91aabc296675431dfe8822579d384e9d38d4389d616f5ffc7bc865710029`  
		Last Modified: Tue, 31 Jan 2023 17:51:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5819d98de56129ec5ab76377b2dd53cf1ca0c1b6e1b97142f7b1353e73bdbba`  
		Last Modified: Tue, 31 Jan 2023 23:16:31 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606e5c98421ecb7689e0f5721963f71a0770c77e0056fb4b2fc0a3c988d7a7e8`  
		Last Modified: Tue, 31 Jan 2023 23:16:32 GMT  
		Size: 3.7 MB (3651153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e886c833790ae98dcefe141acd90a56320f4ab87c410806b9b922f8891e45812`  
		Last Modified: Tue, 31 Jan 2023 23:16:31 GMT  
		Size: 62.9 KB (62879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b637af9774e55dd7f0ba749b8e7a7cc424d8921bc122778cf93ea78bc3f6d219`  
		Last Modified: Tue, 31 Jan 2023 23:18:33 GMT  
		Size: 77.9 MB (77891793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
