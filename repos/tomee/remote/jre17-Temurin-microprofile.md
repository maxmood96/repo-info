## `tomee:jre17-Temurin-microprofile`

```console
$ docker pull tomee@sha256:843bac261b3390c2ac20b2dd67719bed418eb907aecef0c8d6d8255da86e12bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:jre17-Temurin-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:9cc319de8e8268a7d4110fecd7742d029a515a19732efb62ceedadf1fcf6b67a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166672255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816a5f2aa71bf9b734926b63bee089e86ffaa41f0924093a11885f981611694f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Thu, 07 May 2026 23:59:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:59:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:59:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:59:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 23:59:33 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Thu, 07 May 2026 23:59:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='08c8c193fc2e8e6eb4450d3ddcefa78889eef338b2bbc0b30e5a6d586fc6d646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 07 May 2026 23:59:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:59:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:59:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:25:29 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:25:29 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Fri, 08 May 2026 00:25:29 GMT
WORKDIR /usr/local/tomee
# Fri, 08 May 2026 00:25:32 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:25:43 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Fri, 08 May 2026 00:25:43 GMT
ENV TOMEE_VER=10.1.5
# Fri, 08 May 2026 00:25:43 GMT
ENV TOMEE_BUILD=microprofile
# Fri, 08 May 2026 00:25:44 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Fri, 08 May 2026 00:25:44 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 08 May 2026 00:25:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b419ce69b7492def2771bf179c9ff6e02c56d494802d6ba1a56cffb6ee6b1d0`  
		Last Modified: Thu, 07 May 2026 23:59:47 GMT  
		Size: 17.0 MB (16984056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b915181aaf7c04e2cf1641ec5c26247922173f6dde90793a8d49ceeaaee46edc`  
		Last Modified: Thu, 07 May 2026 23:59:50 GMT  
		Size: 47.6 MB (47565016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb964fafce6eb62a36389e3a01144710c7fc99ebfbaf4bc3a7bb214acb10d8f7`  
		Last Modified: Thu, 07 May 2026 23:59:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b317ba485df97a68cb8e6e60aa4e28bb41e662be5eaf897cf5aa09e315a50e`  
		Last Modified: Thu, 07 May 2026 23:59:46 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc62e78090abb1e8238e5f3602702b4211a561d583d3e5f84424cd280a783c12`  
		Last Modified: Fri, 08 May 2026 00:25:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05557a21c5ff51ff425f6a4f69d42700adb018c24a68683115087c07ea512217`  
		Last Modified: Fri, 08 May 2026 00:25:54 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cafd97a899904431824508778c77b56ab6d35c602d55f35c5d9dafc32c61ab9`  
		Last Modified: Fri, 08 May 2026 00:25:55 GMT  
		Size: 75.6 KB (75634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac2bff7bbb47e8c1ab9b76dd70eaae5fb0687a84520c4e08cbe76a50d1b4758`  
		Last Modified: Fri, 08 May 2026 00:25:56 GMT  
		Size: 72.3 MB (72311428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre17-Temurin-microprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:f0b8c76b5903bf27d98dc91a6f809a8ae5057e7e975666d1bd3810237e3ec83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3712497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cf1268e7886123a3e9273f817d4339be027d006d76ef14d4cc76e347404330`

```dockerfile
```

-	Layers:
	-	`sha256:d0f1508a1d427514470716d67bb320c34c5810d7ca6d64be0dde5178c38dd63c`  
		Last Modified: Fri, 08 May 2026 00:25:55 GMT  
		Size: 3.7 MB (3676733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a22adfaa20bcca56b47e71e7047dd1fa1a3cb6556150e8c34dfe86724dffc2e`  
		Last Modified: Fri, 08 May 2026 00:25:54 GMT  
		Size: 35.8 KB (35764 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:jre17-Temurin-microprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:37e05a3d69728c7269b04b4cf9eab6632317ed0a605c00525494575e249ac1e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165313727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e842aeafb6273adb7bff552bdf7ca254d2924beddb9b4587f0039730474092`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Thu, 07 May 2026 23:58:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:58:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:58:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:58:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 23:58:56 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Thu, 07 May 2026 23:58:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='08c8c193fc2e8e6eb4450d3ddcefa78889eef338b2bbc0b30e5a6d586fc6d646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 07 May 2026 23:58:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:58:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:58:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:06:49 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:06:49 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Fri, 08 May 2026 00:06:49 GMT
WORKDIR /usr/local/tomee
# Fri, 08 May 2026 00:06:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:07:06 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Fri, 08 May 2026 00:07:06 GMT
ENV TOMEE_VER=10.1.5
# Fri, 08 May 2026 00:07:06 GMT
ENV TOMEE_BUILD=microprofile
# Fri, 08 May 2026 00:07:07 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Fri, 08 May 2026 00:07:07 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 08 May 2026 00:07:07 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23892ba79f85a72c97e9f6ffd7eee9884b681317a9998d5cd0a6753d77e25979`  
		Last Modified: Thu, 07 May 2026 23:59:11 GMT  
		Size: 17.0 MB (16997481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd63287ffff8e6b3a9e9d7060a8d080083dedfa5512352a8415ded0304b8a0ba`  
		Last Modified: Thu, 07 May 2026 23:59:12 GMT  
		Size: 47.1 MB (47050254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582493c6c3c919ffd24e17870811a733953fa5035d34503bc1d73968f107c629`  
		Last Modified: Thu, 07 May 2026 23:59:11 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2445ed0c0bfb140398df91ee6a3e20a1c1fc8853aeb6ab1a11af4f04d19d87e8`  
		Last Modified: Thu, 07 May 2026 23:59:11 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fcb79cf250140b9a7e4245d884638c8e621f3516054f1c7eede5b2bc31c82b`  
		Last Modified: Fri, 08 May 2026 00:07:19 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45bd55bb62587629a8034f10a98ef0366d2f5c781bdbf7958c9185e04b85b0a`  
		Last Modified: Fri, 08 May 2026 00:07:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c712805b8c7b727e54fbf484a9df977717e3e045f2dd8cccdc5ae84aa21b08`  
		Last Modified: Fri, 08 May 2026 00:07:19 GMT  
		Size: 75.7 KB (75676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410625064ef143ea694e6892182cd61db2448220e60ee780f838c98033468a88`  
		Last Modified: Fri, 08 May 2026 00:07:21 GMT  
		Size: 72.3 MB (72311390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre17-Temurin-microprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:4a2cd688cddc21ee663b958ec66a7df19745c525ee5ced902a830f91691aa7f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3713789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f593dd66761bff8f335cbca996cc998090fec609bf6115a0d1a704c639b0d30`

```dockerfile
```

-	Layers:
	-	`sha256:500c16f2f6a5fbe813cbb94b707180027cc05aa9edb3bd84e1a15a0523033473`  
		Last Modified: Fri, 08 May 2026 00:07:19 GMT  
		Size: 3.7 MB (3677540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faf0695836b25067531196ea4838c518f0ad1f166936f0364173b86f6a6e4fb9`  
		Last Modified: Fri, 08 May 2026 00:07:19 GMT  
		Size: 36.2 KB (36249 bytes)  
		MIME: application/vnd.in-toto+json
