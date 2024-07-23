## `tomee:10-jre17-webprofile`

```console
$ docker pull tomee@sha256:429808a9fadda97b603ba5ebba02c7811a9d6c85746c7d192a893757b2d698ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:10-jre17-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:d824879b4dad83f1f4eb559c8d1a0ec1bdcce43d98f53f4815b3bfc4b11f35ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153765956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10688570c9a9a632e7ab3fb3051ea6741f898db55ddb5dd685ce862f2e8f7ce`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 16:13:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jul 2024 16:13:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jul 2024 16:13:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jul 2024 16:13:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jul 2024 16:13:57 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 22 Jul 2024 16:13:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 22 Jul 2024 16:13:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jul 2024 16:13:57 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:13:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Jul 2024 18:18:20 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 18:18:20 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
WORKDIR /usr/local/tomee
# Tue, 23 Jul 2024 18:18:20 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
ENV TOMEE_VER=10.0.0-M2
# Tue, 23 Jul 2024 18:18:20 GMT
ENV TOMEE_BUILD=webprofile
# Tue, 23 Jul 2024 18:18:20 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 23 Jul 2024 18:18:20 GMT
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
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4e485fb305a744f5c14c75e3aca62600470492c3c43ad509e511f8c2b7dce`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce19657e96cf464cd3386de228766d187304e88eccf513641fa91787eb20480c`  
		Last Modified: Tue, 23 Jul 2024 19:12:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f82519a99d03e29f40c47a8b09188a481a12f5d1b31738c689240ea3c04cf56`  
		Last Modified: Tue, 23 Jul 2024 19:12:29 GMT  
		Size: 2.4 MB (2359484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31e86b2af890ea0e9c1f76e223302fcd40fac4a135d2f2ac4445affc2d99ceb`  
		Last Modified: Tue, 23 Jul 2024 19:12:29 GMT  
		Size: 69.2 KB (69221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80524986b9e2a5e2a2e23a36ee9d8d20ad62ddd2c9aa84c79ccccc8c57591d6a`  
		Last Modified: Tue, 23 Jul 2024 19:12:31 GMT  
		Size: 60.7 MB (60744357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre17-webprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:fe6e4d5416d19414022455d8f33ce2d62a46c9a1ddc4d3204de7362fafc254e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5c45846ab89accd5913b1dca3f9b1f778b3388d1bec01feb0751a9c3830766`

```dockerfile
```

-	Layers:
	-	`sha256:8ad8ebc7b3f3dca791b959c0552c88b00fbf95536b63ed09877b700ece3ac5bc`  
		Last Modified: Tue, 23 Jul 2024 19:12:29 GMT  
		Size: 3.8 MB (3821635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ce70126402fbf1eb26ea46695cf41cef2ec5bf40c59c85c4c11cd769d5481`  
		Last Modified: Tue, 23 Jul 2024 19:12:29 GMT  
		Size: 31.9 KB (31947 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:10-jre17-webprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:6dce7b54f1d24f8f72335e74b2d53d8de39b5866132d782df9242e788b90df1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149936739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a38f2c35b01fc89cf3c89281e3064fcc1d8037b9aa02c8288c98e840f3f6982`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
ENV TOMEE_VER=10.0.0-M1
# Tue, 16 Apr 2024 02:54:00 GMT
ENV TOMEE_BUILD=webprofile
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 16 Apr 2024 02:54:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bcba8e4ae31e5690436469ea0cbe8b0380eac630b99dd454816782517fe3ed`  
		Last Modified: Tue, 02 Jul 2024 04:35:53 GMT  
		Size: 46.7 MB (46716436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1bee0a5ee9a69e90c6a18762b53d2f3872890196bef46a24a14c7e8cd7efe8`  
		Last Modified: Tue, 02 Jul 2024 04:35:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e2fe8e514adf85f13f482dc533f6a54a31ca0f7e9f593af808c0a45b5eb036`  
		Last Modified: Tue, 02 Jul 2024 04:35:48 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1486af89982217f1a8e25271db9dff22e591f36362a03f9f1c84b756dbdd0b`  
		Last Modified: Wed, 03 Jul 2024 01:03:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5a31994f4290b7859e9524441ff46d3249c8ad71291ad3eee2733d89f15b3c`  
		Last Modified: Wed, 03 Jul 2024 01:03:56 GMT  
		Size: 2.3 MB (2345804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efa954bbee93aabdbadd47bfc0d7be203d6b33d120e5b84708061822cccffc1`  
		Last Modified: Wed, 03 Jul 2024 01:03:56 GMT  
		Size: 69.3 KB (69260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc0fd48c06e817257dc766a9c263504116a12e124e3dffe9b098d68dd7b29c3`  
		Last Modified: Wed, 03 Jul 2024 01:10:13 GMT  
		Size: 59.6 MB (59590048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre17-webprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:dce0f75ad9b1d242a340a6a542edf4116207f4c4574ae3d3fabd8e78bc311eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04f8d71f0340b9c24f92a7622d9384563281a2f3f271065ed2caf20e07e539c`

```dockerfile
```

-	Layers:
	-	`sha256:c54a2e645403fcb5947d72983c4b26eb373fa95f5324d7a4717bb5234d7e3208`  
		Last Modified: Wed, 03 Jul 2024 01:10:11 GMT  
		Size: 3.8 MB (3756247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9ffa79295e9697ba0a9ee61632137e5b5f4178d9ac446e67fe609f5a78e7e78`  
		Last Modified: Wed, 03 Jul 2024 01:10:10 GMT  
		Size: 28.4 KB (28382 bytes)  
		MIME: application/vnd.in-toto+json
