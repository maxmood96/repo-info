## `tomee:10-jre17-webprofile`

```console
$ docker pull tomee@sha256:27e19a46759974c6b692a199f49e950106ac7cb7932ac297c1464f2b91d24f5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:10-jre17-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:c28c36a9f475295c158093ad6e78b8118ac5a3d0a61407a65b2a0a4f7c0484fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153440684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1832ba4739797e52b4a7c871684dc461aae429bf8cee0fddefd1f184a5220fb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='392d179be0f9fde0b74aeb1f308be8324c2aa8c970a5c5ea456993fcbb7aa798';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 27 Jun 2025 00:04:37 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Jun 2025 00:04:37 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Fri, 27 Jun 2025 00:04:37 GMT
WORKDIR /usr/local/tomee
# Fri, 27 Jun 2025 00:04:37 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Jun 2025 00:04:37 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Fri, 27 Jun 2025 00:04:37 GMT
ENV TOMEE_VER=10.1.0
# Fri, 27 Jun 2025 00:04:37 GMT
ENV TOMEE_BUILD=webprofile
# Fri, 27 Jun 2025 00:04:37 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Fri, 27 Jun 2025 00:04:37 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 27 Jun 2025 00:04:37 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78734509d335eca0d1c58a3d48cff10dd51f076babdc1594794bbe8cbafd588`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 17.0 MB (16969579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d152eceffbe884bcc304a521184b55bd117c57c65393e46c8e7afc8b58064f`  
		Last Modified: Tue, 03 Jun 2025 13:30:29 GMT  
		Size: 47.0 MB (46958575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e468c91228755a3fd96e3e0f5c149606b23c97ff54e18933eea04d6c3d54e29c`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308cfdda1249a6531a87680d2016986fbd02b99194f36112a1da28f687647487`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d0a62aca4d893b1894bb07bf94fc0894153d4fc15dc75ba1806509e7ccf86c`  
		Last Modified: Fri, 27 Jun 2025 00:17:21 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689aab6a2afb37771d37f9773d8374ec1af21ce22f765c22e55b88610d44bc8f`  
		Last Modified: Fri, 27 Jun 2025 00:17:21 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d577ecf62e081896c656e96b841e6ce841eeb1b75a112384afcbb774bb02664`  
		Last Modified: Fri, 27 Jun 2025 00:17:21 GMT  
		Size: 75.6 KB (75592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c47591eda64a4074b5b33c823e4dd0ff67e409f3372b336812ac9f3f01e977b`  
		Last Modified: Fri, 27 Jun 2025 00:17:31 GMT  
		Size: 59.7 MB (59718462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre17-webprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:29797978bd36b83095845086d3e8927dbeac8ca3c38e4481af5e1b2e1253d815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ad7e85adf95f9d15815ebae40730e68c41a5f4c34dbbea9800b6c3c260c0bc`

```dockerfile
```

-	Layers:
	-	`sha256:e66d5c0d94f5583358f0ec1875c636ef59dc771a9820a7d6f884d07e5766d327`  
		Last Modified: Fri, 27 Jun 2025 01:14:27 GMT  
		Size: 3.6 MB (3554618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e85b6255586de7ae40d7f3a847ee22f9a322cf5aa4e8f51e36a440cc48a0c37`  
		Last Modified: Fri, 27 Jun 2025 01:14:27 GMT  
		Size: 30.7 KB (30665 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:10-jre17-webprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:df7c585b2ae4f0942fd1eee933193b8b756fb5ee802f7d338d9e00a011d18413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152111834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b398a6da7066aeee4496f335a9e5e8120d0b0a5aaa0bdebded047314f598d844`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='392d179be0f9fde0b74aeb1f308be8324c2aa8c970a5c5ea456993fcbb7aa798';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 27 Jun 2025 00:04:37 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Jun 2025 00:04:37 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Fri, 27 Jun 2025 00:04:37 GMT
WORKDIR /usr/local/tomee
# Fri, 27 Jun 2025 00:04:37 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Jun 2025 00:04:37 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Fri, 27 Jun 2025 00:04:37 GMT
ENV TOMEE_VER=10.1.0
# Fri, 27 Jun 2025 00:04:37 GMT
ENV TOMEE_BUILD=webprofile
# Fri, 27 Jun 2025 00:04:37 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Fri, 27 Jun 2025 00:04:37 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 27 Jun 2025 00:04:37 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb5cdde15082c2c264c46bd2f1aa0a8ad43d7590dd7374853ce1748ae4259a4`  
		Last Modified: Tue, 03 Jun 2025 13:30:28 GMT  
		Size: 17.0 MB (16988306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40cf1c06f50de6ec97f12f6099906a5c09940adce66d3f85fa8964651550fac9`  
		Last Modified: Tue, 03 Jun 2025 13:30:35 GMT  
		Size: 46.5 MB (46474392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3790f5e56d3199420b90752ae9fadccdd125189d2a723774568fcf8eef87c768`  
		Last Modified: Tue, 03 Jun 2025 13:30:28 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01de15c36901dba78b0f48401a6a9259b9f51b7b9cd784ea65342e6033b6d45e`  
		Last Modified: Tue, 03 Jun 2025 13:30:29 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e302ec95ce5b5e7f16b27158251dedbf9407672fdd3289d67dbeed86179a1e`  
		Last Modified: Fri, 27 Jun 2025 00:23:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1378188b93a53cefb150060604b090d7675a97b1455cc8603c93f3b797c2e633`  
		Last Modified: Fri, 27 Jun 2025 00:23:37 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dd0487018b871eccc0bd9674cc38f9ec4c406032e161ef1ebb93988f2e639`  
		Last Modified: Fri, 27 Jun 2025 00:23:38 GMT  
		Size: 75.6 KB (75626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf414b60ee882c64bedc9911b7c128906d2dd78c1c3f962aec3ceeef01f04bd`  
		Last Modified: Fri, 27 Jun 2025 00:24:49 GMT  
		Size: 59.7 MB (59718470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre17-webprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:a3797212cb8b31d439ba0eea68ca3e40aab5e6bd9e65cc1b48351ef7046ad92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3586191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b85d0d31f97d50c16d1ea2225ccfedf352d79f80eff580b67acc633c4d34ea`

```dockerfile
```

-	Layers:
	-	`sha256:398bd64b465289c50deb05c6f2ec0a6e85f24d37564c53250b097f6b422f45a6`  
		Last Modified: Fri, 27 Jun 2025 01:14:32 GMT  
		Size: 3.6 MB (3555233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74457d71a4e617957f4c19c0506b215e8b8f0b34982fce3ebad1fbc82711368b`  
		Last Modified: Fri, 27 Jun 2025 01:14:32 GMT  
		Size: 31.0 KB (30958 bytes)  
		MIME: application/vnd.in-toto+json
