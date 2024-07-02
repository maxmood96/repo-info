## `tomee:9-jre11-Temurin-ubuntu`

```console
$ docker pull tomee@sha256:c0f746db12a09846a3e73d5bed2bc43c2428e77e5466d484842341f9c23dd9a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:9-jre11-Temurin-ubuntu` - linux; amd64

```console
$ docker pull tomee@sha256:7f4069f441a912a31c55257a048bb4e5fb0197d5a008843b627afc2a2ba30db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160772184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fbdc1540cf25e0a056584cfca417fa46747ab9ea44f56f2d10fc07048147e2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 16 Apr 2024 02:54:00 GMT
ARG RELEASE
# Tue, 16 Apr 2024 02:54:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 02:54:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 02:54:00 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 16 Apr 2024 02:54:00 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 16 Apr 2024 02:54:00 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:54:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 02:54:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 02:54:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7290ace47a030d89ea023c28e7aa555c9da72b4194f73b39ec9d058011bf06dd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='786a72296189ba8e43999532aa73730d87ec1fce558eb3c4e98b611b423375e3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='025f994549708f7291ce3b0fa7c41f7e78ec3af3eae3f85fffe9c5fa4a54889f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b3fbd324620fd914bd8462e292124493fcf846fd69195c4b9a231131dc68d5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='25abb7f74f55847b0d509402111084bd7a244d904744f3bfffa89528bc3b8a69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 16 Apr 2024 02:54:00 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 02:54:00 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
WORKDIR /usr/local/tomee
# Tue, 16 Apr 2024 02:54:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
ENV TOMEE_VER=9.1.3
# Tue, 16 Apr 2024 02:54:00 GMT
ENV TOMEE_BUILD=microprofile
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 16 Apr 2024 02:54:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e49404950a550f6205b66ae147060d18dcb3ba07d8df8ee31a5c83c540a67c`  
		Last Modified: Tue, 02 Jul 2024 06:01:40 GMT  
		Size: 47.2 MB (47186001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27110d8581e6469d85c00f6c85d6d5ac62b9a2c38b96919993a0734aea4abe26`  
		Last Modified: Tue, 02 Jul 2024 06:01:34 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3d9b80aea7a3d789b713c5070a62a15dc28669ec287b0e4d73eeec7b30a62f`  
		Last Modified: Tue, 02 Jul 2024 06:01:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4fb69d207da6c408e634b6f91e212fdfd412400558533d5c0feed3108ee867`  
		Last Modified: Tue, 02 Jul 2024 07:10:47 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c204cb5b2594002b4eae189c251602f543a4a0a63328e457b760c1dee8b5af`  
		Last Modified: Tue, 02 Jul 2024 07:10:47 GMT  
		Size: 2.4 MB (2359485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f215221875753a8e8f5a78bd4ae6599f59d00616c07e79e24adfac9d6ea9c3`  
		Last Modified: Tue, 02 Jul 2024 07:10:47 GMT  
		Size: 69.2 KB (69237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0deffa71fd7af45c6bae586c11d361d51bca222d7539807bf6603072fae98a2`  
		Last Modified: Tue, 02 Jul 2024 07:10:48 GMT  
		Size: 67.8 MB (67845432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:9-jre11-Temurin-ubuntu` - unknown; unknown

```console
$ docker pull tomee@sha256:6f81930c6373eadeeffc13ec9afce04952f82458405d553ae8473c4e6b6743bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3879177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782d5aa3106a4484db3d8fa29605bd5c8062941b39408bacc3ef890ff6d3491e`

```dockerfile
```

-	Layers:
	-	`sha256:040b17b3c69da2f0d5c5f9ff1e8a7627f3abcf062e872ba9a6cd99754ff1e86a`  
		Last Modified: Tue, 02 Jul 2024 07:10:47 GMT  
		Size: 3.8 MB (3834706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67ddcd619584de8668cd99e5a30a56b795f2ae6ca2a946f08784481f2565660c`  
		Last Modified: Tue, 02 Jul 2024 07:10:47 GMT  
		Size: 44.5 KB (44471 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:9-jre11-Temurin-ubuntu` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:9d891edfec259f8141e20504639d5e19ebfdd90b80253f51e93401ec72358ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157068085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da35d924b9283d7372c60fecb13f1f6a0a736d08a696068d0104c052a3175e28`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 16 Apr 2024 02:54:00 GMT
ARG RELEASE
# Tue, 16 Apr 2024 02:54:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 02:54:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 02:54:00 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 16 Apr 2024 02:54:00 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Tue, 16 Apr 2024 02:54:00 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:54:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 02:54:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 02:54:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7290ace47a030d89ea023c28e7aa555c9da72b4194f73b39ec9d058011bf06dd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='786a72296189ba8e43999532aa73730d87ec1fce558eb3c4e98b611b423375e3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='025f994549708f7291ce3b0fa7c41f7e78ec3af3eae3f85fffe9c5fa4a54889f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b3fbd324620fd914bd8462e292124493fcf846fd69195c4b9a231131dc68d5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='25abb7f74f55847b0d509402111084bd7a244d904744f3bfffa89528bc3b8a69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 16 Apr 2024 02:54:00 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 02:54:00 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
WORKDIR /usr/local/tomee
# Tue, 16 Apr 2024 02:54:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
ENV TOMEE_VER=9.1.3
# Tue, 16 Apr 2024 02:54:00 GMT
ENV TOMEE_BUILD=microprofile
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 16 Apr 2024 02:54:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd918abfec0657ade8aeeffe2722e92948e13fa403fd238ae22b1a9881e9402`  
		Last Modified: Wed, 05 Jun 2024 04:55:01 GMT  
		Size: 12.8 MB (12847839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff112211e57f20f65abc1d0616a35351bfdf9b288ceec97953e23918d2208ad5`  
		Last Modified: Wed, 05 Jun 2024 04:56:37 GMT  
		Size: 45.6 MB (45554901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbae6de5b669a00b6619be94e3432b925eb4caba809366251f48bc2f77f9fae`  
		Last Modified: Wed, 05 Jun 2024 04:56:31 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776174bc5ab4f6736baddf0a490b2d57fbb58776bc00fa4e8ae0967cf26a895c`  
		Last Modified: Wed, 05 Jun 2024 04:56:31 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2457674d4769c8a9b946fa700f601aaa237158724bb663fabc66d3a9682db07e`  
		Last Modified: Wed, 05 Jun 2024 17:44:10 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2530568fc73163aea7fe80d658013c77a5d687f5efab5aad01e8722d39f6fcf`  
		Last Modified: Wed, 05 Jun 2024 17:44:11 GMT  
		Size: 2.3 MB (2347283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a662692f54b1f6ef4320430afc0775ece962f8dd67906187e5c3f6c406f41549`  
		Last Modified: Wed, 05 Jun 2024 17:44:10 GMT  
		Size: 69.3 KB (69263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c114a00b227c9a640c3de92799313de37f878363ba1db11544420c59774f00df`  
		Last Modified: Wed, 05 Jun 2024 17:44:13 GMT  
		Size: 67.8 MB (67845398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:9-jre11-Temurin-ubuntu` - unknown; unknown

```console
$ docker pull tomee@sha256:996c105a4ace871647101a1f5fc15f0356aa281f2fc9a83b3a72c6c843711850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3881171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec6b9d6767288f27e9720f53d53c33a887022c2078d8712db17ef83fcc7fd2e`

```dockerfile
```

-	Layers:
	-	`sha256:b9f51a514ecdf760af1ad8a97ffcdb343ea7731b376504d7cf0dcf2841bb54f8`  
		Last Modified: Wed, 05 Jun 2024 17:44:11 GMT  
		Size: 3.8 MB (3835713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1082ad2cbb966619e92ee05c7a9e2737b4a4af49f92f4e584034be098a5a57c8`  
		Last Modified: Wed, 05 Jun 2024 17:44:10 GMT  
		Size: 45.5 KB (45458 bytes)  
		MIME: application/vnd.in-toto+json
