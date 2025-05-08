## `tomee:10-jre17-Temurin-ubuntu-plume`

```console
$ docker pull tomee@sha256:3df6f8a017a9f50ffea32cda9baa5e270564da31e81e7650838acd8c914263fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:10-jre17-Temurin-ubuntu-plume` - linux; amd64

```console
$ docker pull tomee@sha256:e0c574b5fa5ec31c239d952d8fa5268af2981cc98e719ef913f38de6c6a61e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176064181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23deaa4fd16492d7754063dfd026dd8affd87710d2af4b6cc52efa40925fbfe1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 07 Apr 2025 14:29:55 GMT
ARG RELEASE
# Mon, 07 Apr 2025 14:29:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 14:29:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 14:29:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Apr 2025 14:29:55 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 07 Apr 2025 14:29:55 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 14:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Apr 2025 14:29:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 14:29:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='392d179be0f9fde0b74aeb1f308be8324c2aa8c970a5c5ea456993fcbb7aa798';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 07 Apr 2025 14:29:55 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 14:29:55 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
WORKDIR /usr/local/tomee
# Mon, 07 Apr 2025 14:29:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
ENV TOMEE_VER=10.0.1
# Mon, 07 Apr 2025 14:29:55 GMT
ENV TOMEE_BUILD=plume
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 07 Apr 2025 14:29:55 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f791a7fe25117f87474e2caa3cf018143aac62fbf851e3f5907e4f6b485b0403`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 17.0 MB (16967844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747fc38fa8124104daf82578d761c01cd86e557417b8dbbd993e35db511647a0`  
		Last Modified: Thu, 08 May 2025 17:04:43 GMT  
		Size: 47.0 MB (46958454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2588e7e6673e44254e321f97ff43ac1a411604528a7ca8edd191a08d1f2c041`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f32a0234e340f0b136c88151aad3bae5cb68485c7d1ed671fe677d1fa3a3f4c`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f88bc82254ef2a9a77f9a8b3da7cfe9a7e156ab285abdc17f5e8f14902fd58f`  
		Last Modified: Mon, 05 May 2025 17:06:09 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cda39c3114fd8eb5af5973a4b9446ae6baf990945c511f3b35bcb532a0e243a`  
		Last Modified: Mon, 05 May 2025 17:06:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fdb0f9410d889e745f1ceefe08406a741547b44eec62fb4f520944a40ee6b6`  
		Last Modified: Mon, 05 May 2025 17:06:09 GMT  
		Size: 75.6 KB (75601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7389cc7ee339bc44b4c68f8d3c4753a000ce3ca2376c96c9b34460c57568cc55`  
		Last Modified: Mon, 05 May 2025 17:06:11 GMT  
		Size: 82.3 MB (82341612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre17-Temurin-ubuntu-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:1934dff8a07f37b1d001d3c4c01cdca31e2b9a5506b0a0a3a275031de40038e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3544060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891680d7a2bcfb8adc1d739285e858a34d89c6e9620b72b211b51e943868e2fe`

```dockerfile
```

-	Layers:
	-	`sha256:8f51e2766ec45971726292e59e61ee9b7c20361122da2e2fefa7a8ed42ba05ac`  
		Last Modified: Mon, 05 May 2025 17:06:09 GMT  
		Size: 3.5 MB (3514707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056cde1f397f7055eddb6ccbaa98a6f05331699d8cc4e8d7e57030fcda972ebc`  
		Last Modified: Mon, 05 May 2025 17:06:09 GMT  
		Size: 29.4 KB (29353 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:10-jre17-Temurin-ubuntu-plume` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:beaca223ecc3bb6c7d29c10177fde70ce8606e77e6a5ac492a940a145d4f9ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174728936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35dafcf3c822c4df88b14d927ebf0935143ab08e67a568e450aea5fa8d784a3c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 07 Apr 2025 14:29:55 GMT
ARG RELEASE
# Mon, 07 Apr 2025 14:29:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 14:29:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 14:29:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Apr 2025 14:29:55 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 07 Apr 2025 14:29:55 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 14:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Apr 2025 14:29:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 14:29:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='392d179be0f9fde0b74aeb1f308be8324c2aa8c970a5c5ea456993fcbb7aa798';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 07 Apr 2025 14:29:55 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 14:29:55 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
WORKDIR /usr/local/tomee
# Mon, 07 Apr 2025 14:29:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
ENV TOMEE_VER=10.0.1
# Mon, 07 Apr 2025 14:29:55 GMT
ENV TOMEE_BUILD=plume
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 07 Apr 2025 14:29:55 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:221bb599db571d0f1d7eeb8d411225ab740641d4953fd9721b204d9e5952ef69`  
		Last Modified: Thu, 08 May 2025 17:06:50 GMT  
		Size: 46.5 MB (46474435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32e56f2e807ff0934c297eb99c4a26839a95fc6b856fc9ac3b77b9266830cfc`  
		Last Modified: Thu, 08 May 2025 17:06:46 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91ad827d9d8126cbb3c15dec5851d6626b569d94bec1b7ab345d4eb449adfdc`  
		Last Modified: Thu, 08 May 2025 17:06:46 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6663ae1a3f41c681100d39c561de3897ef74ce66b1154b633590266d7c97bf`  
		Last Modified: Mon, 05 May 2025 23:58:48 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068f9b61840189d3ff24802bdb64b898ba2c93c554f6f2a610535e5d717adc1b`  
		Last Modified: Mon, 05 May 2025 23:58:48 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08bcc9a89fab1efca45a638902c0f89ecb3fec0e1c2d2e92ac3a811dccfd97b`  
		Last Modified: Mon, 05 May 2025 23:58:48 GMT  
		Size: 75.6 KB (75623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f70f781a03455dd65be31e4a275d0903e6648b4c088aac1d8826d3475fece3`  
		Last Modified: Mon, 05 May 2025 23:59:17 GMT  
		Size: 82.3 MB (82341612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre17-Temurin-ubuntu-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:e215da6250c832deeef619ee29e51e0d3d8779c2c50533d9f33a8eb29896feac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3544969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c17f500ee2e226c5f56a0353bb15321be4afbb909143706436bb881546dacfd`

```dockerfile
```

-	Layers:
	-	`sha256:e1dcc5e5cb0b42e9539ba1a100285781a0e4806ba056b1147a9167512ee431d1`  
		Last Modified: Mon, 05 May 2025 23:59:15 GMT  
		Size: 3.5 MB (3515322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82bc6b3fd1d79f80b3354d875145a276efd203f31dfaba8773e0f58d4249d225`  
		Last Modified: Mon, 05 May 2025 23:59:15 GMT  
		Size: 29.6 KB (29647 bytes)  
		MIME: application/vnd.in-toto+json
