## `tomee:10-jre25-Temurin-plus`

```console
$ docker pull tomee@sha256:3d1d4a4439659bdb2b478686c27252fb634ecae891816af1acf9c130460146bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:10-jre25-Temurin-plus` - linux; amd64

```console
$ docker pull tomee@sha256:282dadc2e068021f8e10b253ec7624cc3884b933e1fc8ada5f324821aaf182d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183406272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f18e3256c9c095c1adcf84a97d6b2b3c473d05c76c334607109250313c87e7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 25 Sep 2025 19:59:06 GMT
ARG RELEASE
# Thu, 25 Sep 2025 19:59:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 19:59:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 19:59:06 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 25 Sep 2025 19:59:06 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5e3de13a1487ecc90f8b0cddc83a6cd4e053b4cd48ddcfe5d1f19178e6089fba';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='939a1517971985363b2b57b8c6008f4bd48b91f565366d6eb3bae3aa503a05e2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='f593d6c435f6498cfbdb1ca07d7b1fa33829b159abb31b992b6234c324794dad';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        riscv64)          ESUM='3ec1d5906104fb273821a5865235b673fcd2b55674c5aee68d15b429fdc7837c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_riscv64_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='485af5746df1bf3cd46da4e7f771e6d1eae5a31db695ab819c4c2401688a6871';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 05 Oct 2025 18:19:29 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 05 Oct 2025 18:19:29 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
WORKDIR /usr/local/tomee
# Sun, 05 Oct 2025 18:19:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent curl   && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
ENV TOMEE_VER=10.1.2
# Sun, 05 Oct 2025 18:19:29 GMT
ENV TOMEE_BUILD=plus
# Sun, 05 Oct 2025 18:19:29 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
EXPOSE map[8080/tcp:{}]
# Sun, 05 Oct 2025 18:19:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8742a8577b1b7f8ad9a60e705ce2a944b64b200f601c5a527281945b6dfc4c`  
		Last Modified: Thu, 09 Oct 2025 21:14:35 GMT  
		Size: 11.5 MB (11475153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad12b5cf65c46c316883130113108e23b6a0bf64f3bd52b737ce81f17bd37ae7`  
		Last Modified: Thu, 09 Oct 2025 21:14:40 GMT  
		Size: 62.7 MB (62713672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ebb2d4bd2d2640b2c015c888d99db30cc99932e894fee9f06ccff713fdc048`  
		Last Modified: Thu, 09 Oct 2025 21:14:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb92f23c1762c0f38e4394c8b1540e59ce9c0a758f001fea0fff431e3964441`  
		Last Modified: Thu, 09 Oct 2025 22:25:08 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e56f3907ba895f2bbf1dbae4cc3e3b8761261c7bf0e5c17d43c89dc6308e82`  
		Last Modified: Thu, 09 Oct 2025 22:25:09 GMT  
		Size: 4.5 MB (4477436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6e1522a6e44db808875c63ff8a2e31d65014ff3f79b7515d3b5c32ecaea01e`  
		Last Modified: Thu, 09 Oct 2025 22:25:09 GMT  
		Size: 75.6 KB (75640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67598640ac8372fcf5e5f1a2c5c5aedc2962969211a43b27ba360a644ec66524`  
		Last Modified: Thu, 09 Oct 2025 22:25:19 GMT  
		Size: 74.9 MB (74938705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre25-Temurin-plus` - unknown; unknown

```console
$ docker pull tomee@sha256:5e2481d9f858160ec483bf7cf5a66ddd6656f0668de3ec8fd5443ba209bff62a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3684528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974eff865afd919aca62eaaee37a01ebf6302072add1091aa1ff40d78055b7e8`

```dockerfile
```

-	Layers:
	-	`sha256:c976be3ea5997927012e83fea7f790d05072b863ce7a09405c00971539babb58`  
		Last Modified: Fri, 10 Oct 2025 04:11:49 GMT  
		Size: 3.6 MB (3649046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42111fe55655e215dc69ef6cda774cf777b149b886ce246d919b63f2f93c6534`  
		Last Modified: Fri, 10 Oct 2025 04:11:50 GMT  
		Size: 35.5 KB (35482 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:10-jre25-Temurin-plus` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:592014aa06205f178830ee4491c62248399dd10b8efd3a6f231657fff55c3ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181502896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cf999d861b167a0e05efa0898d5e3c86be54fe7de0c31c808fc1d2cd278218`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 25 Sep 2025 19:59:06 GMT
ARG RELEASE
# Thu, 25 Sep 2025 19:59:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 19:59:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 19:59:06 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 25 Sep 2025 19:59:06 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5e3de13a1487ecc90f8b0cddc83a6cd4e053b4cd48ddcfe5d1f19178e6089fba';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='939a1517971985363b2b57b8c6008f4bd48b91f565366d6eb3bae3aa503a05e2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='f593d6c435f6498cfbdb1ca07d7b1fa33829b159abb31b992b6234c324794dad';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        riscv64)          ESUM='3ec1d5906104fb273821a5865235b673fcd2b55674c5aee68d15b429fdc7837c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_riscv64_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='485af5746df1bf3cd46da4e7f771e6d1eae5a31db695ab819c4c2401688a6871';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 05 Oct 2025 18:19:29 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 05 Oct 2025 18:19:29 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
WORKDIR /usr/local/tomee
# Sun, 05 Oct 2025 18:19:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent curl   && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
ENV TOMEE_VER=10.1.2
# Sun, 05 Oct 2025 18:19:29 GMT
ENV TOMEE_BUILD=plus
# Sun, 05 Oct 2025 18:19:29 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
EXPOSE map[8080/tcp:{}]
# Sun, 05 Oct 2025 18:19:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b70954c9848c5484bec01f7f3af75ad4e877da3c09ac207bcdb7f4076b4883b`  
		Last Modified: Thu, 09 Oct 2025 21:15:21 GMT  
		Size: 11.5 MB (11469857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cbd9517df285273d485bfa40ef24fa4f973fabdfb6a34b509cde8e66e38d8e`  
		Last Modified: Thu, 09 Oct 2025 21:15:26 GMT  
		Size: 61.7 MB (61655764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090ffc73b904b3c81818f91b0b9d8c83af123ee885ef21aa89b0120f48bfd9fd`  
		Last Modified: Thu, 09 Oct 2025 21:15:20 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cacf9078faebf74ed650c3616b3d13c1c68a1fdfccc61191be74c27242feb5`  
		Last Modified: Thu, 09 Oct 2025 22:25:11 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519110281350e9741249340e11749e8ca204014fb5e36b351f89adcf0b3a60cd`  
		Last Modified: Thu, 09 Oct 2025 22:25:11 GMT  
		Size: 4.5 MB (4498712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b1cebf83f7eba0ae765aa41f05c85eeaa3b9c9684798814f860591eb1c5328`  
		Last Modified: Thu, 09 Oct 2025 22:25:12 GMT  
		Size: 75.6 KB (75632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2f08386e13c9ef01dfc35cd3850a0f8c0e0256152306af2fc708acbff8d05b`  
		Last Modified: Thu, 09 Oct 2025 22:25:17 GMT  
		Size: 74.9 MB (74938702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre25-Temurin-plus` - unknown; unknown

```console
$ docker pull tomee@sha256:2b53137dae61fbc0f2bbe5ede70155b73b7363116c973fed43e5371d395f8125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3685817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43763c97a6c4ef75ff5d8d35cc06f78879e7cf16a668c78fdd126ff0ece4bd2c`

```dockerfile
```

-	Layers:
	-	`sha256:e54695a143c842826a0563e9df5ebc12816cb57b5606b4e564e91f2d1204fc19`  
		Last Modified: Fri, 10 Oct 2025 04:11:56 GMT  
		Size: 3.6 MB (3649850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93629822bb9b496df9b534b98b59222e3d01114109b3cdaa638baaaeba850860`  
		Last Modified: Fri, 10 Oct 2025 04:11:56 GMT  
		Size: 36.0 KB (35967 bytes)  
		MIME: application/vnd.in-toto+json
