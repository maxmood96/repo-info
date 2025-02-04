## `tomee:jre17-Temurin-ubuntu-plume`

```console
$ docker pull tomee@sha256:aac56025b2420c00f8bd4181af9d067dcdd63655c1adbc5d80a7b9621cb62719
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:jre17-Temurin-ubuntu-plume` - linux; amd64

```console
$ docker pull tomee@sha256:ed71062954b02e41b3a1509af8eeea952f1637b5f5c0d950158ed38ada0d1614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175509905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90583bbd5f693e95ea0b98bd1900126169fed21a1ea7782ba7f41271fa1001b3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 29 Dec 2024 01:38:24 GMT
ARG RELEASE
# Sun, 29 Dec 2024 01:38:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 29 Dec 2024 01:38:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 29 Dec 2024 01:38:24 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 29 Dec 2024 01:38:24 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Sun, 29 Dec 2024 01:38:24 GMT
CMD ["/bin/bash"]
# Sun, 29 Dec 2024 01:38:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 29 Dec 2024 01:38:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 29 Dec 2024 01:38:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 29 Dec 2024 01:38:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 29 Dec 2024 01:38:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 29 Dec 2024 01:38:24 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 29 Dec 2024 01:38:24 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
WORKDIR /usr/local/tomee
# Sun, 29 Dec 2024 01:38:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
ENV TOMEE_VER=10.0.0
# Sun, 29 Dec 2024 01:38:24 GMT
ENV TOMEE_BUILD=plume
# Sun, 29 Dec 2024 01:38:24 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
EXPOSE map[8080/tcp:{}]
# Sun, 29 Dec 2024 01:38:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d86b113ae4cba6d42b88d3beb9bb838cf4223581d8abe79c71ffb95b6cfb00f`  
		Last Modified: Tue, 04 Feb 2025 05:20:37 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39ada801a28fbc471f040a5583e732038b36dff3c6d9adc4bcbae1df992c4a1`  
		Last Modified: Tue, 04 Feb 2025 05:20:39 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6928d7dfad015409b453274106e83a6c2bcd95f4db710ee560ebf0b17737ce4a`  
		Last Modified: Tue, 04 Feb 2025 05:20:39 GMT  
		Size: 75.7 KB (75663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68203bb49964640bf2906dcd1e1e33acd3a1727334015ae05a13a95f9276dbf7`  
		Last Modified: Tue, 04 Feb 2025 05:20:41 GMT  
		Size: 81.8 MB (81761665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre17-Temurin-ubuntu-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:3e2a4ad9ea7fbaf94c7429c02ba4850a2ae9b7401c990a9c807aa9054e3f0c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3548952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8553c6fd9c663803a21d3218dd6a5f0bea6d11320dac5642745d7155f74c63`

```dockerfile
```

-	Layers:
	-	`sha256:55b28299d41e4580279c9546ea2a88179e360a95846e1d7c11f653254b4540c6`  
		Last Modified: Tue, 04 Feb 2025 05:20:39 GMT  
		Size: 3.5 MB (3519598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:535c8e134e685f5ccc6bc6ab7acf0b395c71d59d29fa371bf8dcd8d6862f8da7`  
		Last Modified: Tue, 04 Feb 2025 05:20:39 GMT  
		Size: 29.4 KB (29354 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:jre17-Temurin-ubuntu-plume` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:9842cbd5b0fb4285a0ee2c8d02c174a9708552befcaf22e6fe5e1c7fd3900597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174179839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d45d37ed61862f6fa6dc96dfb956b0358a6231b45c226626578ed6363323bdb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Sun, 29 Dec 2024 01:38:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 29 Dec 2024 01:38:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 29 Dec 2024 01:38:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 29 Dec 2024 01:38:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 29 Dec 2024 01:38:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 29 Dec 2024 01:38:24 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 29 Dec 2024 01:38:24 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
WORKDIR /usr/local/tomee
# Sun, 29 Dec 2024 01:38:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
ENV TOMEE_VER=10.0.0
# Sun, 29 Dec 2024 01:38:24 GMT
ENV TOMEE_BUILD=plume
# Sun, 29 Dec 2024 01:38:24 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
EXPOSE map[8080/tcp:{}]
# Sun, 29 Dec 2024 01:38:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370f8a7b7cf214f61cc1a2546f38e47ba749cb698659b51aa07e70fcecbd7e2f`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 17.0 MB (16982856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdf56be796e06869f79797ec2f94851f8273a303e6f3fcaa6988296b5f77381`  
		Last Modified: Fri, 31 Jan 2025 01:43:22 GMT  
		Size: 46.5 MB (46463806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8260ceaafcab9714596ba4d69c9f23aebab641359adc1720ffc705e75c749d`  
		Last Modified: Fri, 31 Jan 2025 01:43:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3b39d002240b6b685d23574f681a9673bbcbf96ce4f75330ddbbe567a30fea`  
		Last Modified: Fri, 31 Jan 2025 01:43:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519e1ec8e9250a90132b4b1754d800811ee02d719890e4a292d58bdae2b26cdc`  
		Last Modified: Fri, 31 Jan 2025 04:39:54 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68f0262b408b738dca55aa07731732673c733f8f75de604a73cec367134b8cb`  
		Last Modified: Fri, 31 Jan 2025 04:39:54 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ede7c752f2c70abeb4eadfc459d3e85d9b527f3aa5e41de825ba6bfd45cae8`  
		Last Modified: Fri, 31 Jan 2025 04:39:54 GMT  
		Size: 75.7 KB (75681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d533d1513427b2055e8ae2f1fe0371e835011dfc36f3ed07703d2e2a0e3fa81f`  
		Last Modified: Fri, 31 Jan 2025 04:40:28 GMT  
		Size: 81.8 MB (81761687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre17-Temurin-ubuntu-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:02e8874928712312459e188a487c5e3f36da596045458098e53791bfca8d98c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3546510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214ee7d46d6640e055bf519ea06fae6231a9da5e40567cc692c43411939332ad`

```dockerfile
```

-	Layers:
	-	`sha256:b2cd2ab6f9b5d60509a260c1ea1c67afc91e55f7421412c7849a0c87cf406e12`  
		Last Modified: Fri, 31 Jan 2025 04:40:26 GMT  
		Size: 3.5 MB (3516863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87d012a08f1008c3a2bdec1933aa2cda0d85068a3a080a03ceb04216c32ea685`  
		Last Modified: Fri, 31 Jan 2025 04:40:25 GMT  
		Size: 29.6 KB (29647 bytes)  
		MIME: application/vnd.in-toto+json
