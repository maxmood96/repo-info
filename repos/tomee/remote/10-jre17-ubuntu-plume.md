## `tomee:10-jre17-ubuntu-plume`

```console
$ docker pull tomee@sha256:a84d9346e85a783d6a77544de3b0cf08db36249aa14d50d1bfa1bda8237a4916
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:10-jre17-ubuntu-plume` - linux; amd64

```console
$ docker pull tomee@sha256:0158b82fea7945940278f8b49e31546f2dc63836546bc225d647da8857bfe5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176058302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3e27c6b37f8cf2483656d85d02896ba439c7c53db3b5ba992b5eb92c727621`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb7a286e7ca2118d3733c9d28bf9307c31433be29907b8f34f33e7db2423c8`  
		Last Modified: Wed, 09 Apr 2025 01:16:06 GMT  
		Size: 17.0 MB (16967610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff98e09c72e1bb2921db542b2a4eaa27ac0f36d3437cea164f58c18a8b15ff08`  
		Last Modified: Wed, 09 Apr 2025 01:16:07 GMT  
		Size: 47.0 MB (46952682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c75f759c134d210bf1f7c1705f5ba4180fada3609fd22f229a5f618460e1811`  
		Last Modified: Wed, 09 Apr 2025 01:16:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0d9be831dada318543f96db05bf1a054976aa0758c56ada4ea6855294c3230`  
		Last Modified: Wed, 09 Apr 2025 01:16:06 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16ac6b50745dae148be58722a30718184b1e193151395f4b831708b6a435bac`  
		Last Modified: Mon, 14 Apr 2025 17:27:20 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffdabe3d296f3455c47d740c6f7ded936b9ec6dda311614f496b8172e6f3c2b`  
		Last Modified: Mon, 14 Apr 2025 17:27:20 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec2be93387ee62ad7dd4817b285314445024f40e58c947080287380a47c6665`  
		Last Modified: Mon, 14 Apr 2025 17:27:20 GMT  
		Size: 75.6 KB (75615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3139ff4b76e3632bc81364b5b40f1279fcdbae0864a89e1ecefe53cbfda1a0c3`  
		Last Modified: Mon, 14 Apr 2025 17:27:21 GMT  
		Size: 82.3 MB (82341602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre17-ubuntu-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:678a6645aec4b34e827f24cd60ca0238e4a39334b3443e33eeef3d885016f5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3544056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83101eb28d772e219242716d852fd5bbc9d7d5d69239ae1297e71da944c0f8f8`

```dockerfile
```

-	Layers:
	-	`sha256:9a785f6890a3868f0e53e5394e10ce3920c3e6aa7fe50945822da64bba4496b3`  
		Last Modified: Mon, 14 Apr 2025 17:27:20 GMT  
		Size: 3.5 MB (3514703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dceeb081b8d96dfdc721a745fe4a0804f50dc4806635b8c5ab2145ebb69da19f`  
		Last Modified: Mon, 14 Apr 2025 17:27:20 GMT  
		Size: 29.4 KB (29353 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:10-jre17-ubuntu-plume` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:3b83764f801c08c159f84bfabf41ba9680a5d4fa730387688b76028de19fbd7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174718335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b279b3c22c971fb2efc3478bf3c55e8d26f19088c8256343aab4a634f75c823a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
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
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787aea36c8936222fd96cbbd68c43aadaafb0e67fe9615a7545f05fd317f522d`  
		Last Modified: Wed, 09 Apr 2025 06:58:50 GMT  
		Size: 17.0 MB (16987241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3fcfbd7cdd46cc6da1b7ca322a5fae240ecf8c2ddee52d3757a50fb8a7f99b`  
		Last Modified: Wed, 09 Apr 2025 07:06:47 GMT  
		Size: 46.5 MB (46463775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951c3464fc3980701a0f93833a4500513bf69ed4503ced14136593b45b11bacf`  
		Last Modified: Wed, 09 Apr 2025 07:06:45 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7fa53a112f421caf5e90ad5babcb688d10f79421cd4bed4cb1ff76c73ef5d4`  
		Last Modified: Wed, 09 Apr 2025 07:06:45 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5c202c74dd50a23523ecc3988d8705daaefbdabf86551c4d704f02855f2571`  
		Last Modified: Mon, 14 Apr 2025 17:33:34 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77703ca6ff656df8139d6ad29c6622639aca75989494f63d749ba9ed6d874203`  
		Last Modified: Mon, 14 Apr 2025 17:33:34 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ab916dbc3685e903e7a873be4759b428d16f57c6c70717ae241c36d68f81ad`  
		Last Modified: Mon, 14 Apr 2025 17:33:35 GMT  
		Size: 75.6 KB (75630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9371c55f304c7da7323febd7abcb29df5658ca0a62bb361c12d5c062fcda7c`  
		Last Modified: Mon, 14 Apr 2025 17:34:04 GMT  
		Size: 82.3 MB (82341592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre17-ubuntu-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:e32eedf18b17d47f97398b511c39e1af4ed90b0e90ce8ac10863982510274f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3544965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d051ec050477e86246b2f3e0f77296b5c4e8fa22293530648f681999408207d6`

```dockerfile
```

-	Layers:
	-	`sha256:740f84347c6d1e727f97c2402a59141006e59141db71c3d4710f475a2ee945b2`  
		Last Modified: Mon, 14 Apr 2025 17:34:01 GMT  
		Size: 3.5 MB (3515318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5391ac82dd2480965f91e3559dd0273c41eb252d7f8b53b4e8ada94ea526f20`  
		Last Modified: Mon, 14 Apr 2025 17:34:00 GMT  
		Size: 29.6 KB (29647 bytes)  
		MIME: application/vnd.in-toto+json
