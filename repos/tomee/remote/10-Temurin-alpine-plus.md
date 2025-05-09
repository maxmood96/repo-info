## `tomee:10-Temurin-alpine-plus`

```console
$ docker pull tomee@sha256:695a426add52e10d42a1e6c3399863b51864ebbcfab1f508386d3558bdec60dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:10-Temurin-alpine-plus` - linux; amd64

```console
$ docker pull tomee@sha256:7360956dd4971b527a5ed0d75ef892ec5b98e447701743643fe9ac4fae8e10ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148342886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d413bda43e5f0ca9f292fd17c953eb037add5c940e04bd4a13107f797aec314f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 14:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Apr 2025 14:29:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 14:29:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='53877576d3a9dcbf2024789208aa5f045cc65a5645b07d67124b09c2a84f4e1a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.7_6.tar.gz';          ;;        x86_64)          ESUM='f252e13683b381f9f3bfa4948c827ebd80b8e5bd444a1f99de02c56d76c7ad4c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
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
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
ENV TOMEE_VER=10.0.1
# Mon, 07 Apr 2025 14:29:55 GMT
ENV TOMEE_BUILD=plus
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 07 Apr 2025 14:29:55 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cd406c8d97cafcb893e824126c17fa19907b2bbc8d759931089e1be1e75750`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 16.2 MB (16176564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f6a226ed936757680facf9b217f62a2af16b663a69df8e4b3ece925e27ed2a`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 53.1 MB (53059918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6744199aa66ab985e37e72924f1568a6751afa2c508c42a1b3b945f3a8850a7`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda86626eeb372589c3378d030f4522ba1b0c78ec58b1db87960fa4e5fcd3e34`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525be62a98a127ab9cfe699d8b3556642276b78eb551de3ae8fd662f497f5739`  
		Last Modified: Fri, 09 May 2025 12:21:13 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607361b7e574187ed568a04e28537f3617f260abe8b019fcaecb866fee2b61c9`  
		Last Modified: Fri, 09 May 2025 12:21:13 GMT  
		Size: 1.1 MB (1148483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabc6e08f7c1633c4646c21915f0291adfce66f05afdf3f2547c7f943f81a536`  
		Last Modified: Fri, 09 May 2025 12:21:13 GMT  
		Size: 75.6 KB (75619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea68c0a64fe018f130339a66d8dd2adaaf07313e44f9fc5d9a78b341fb35915`  
		Last Modified: Fri, 09 May 2025 12:21:19 GMT  
		Size: 74.2 MB (74237448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-Temurin-alpine-plus` - unknown; unknown

```console
$ docker pull tomee@sha256:02da7b59de19ad1746f06f1bbf055983d4cf3d46717b506e3779423d195a0d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1315423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fb5a3a6d556b68ccc090a113d891e278f4909c047362913efcd0b7f877f5b5`

```dockerfile
```

-	Layers:
	-	`sha256:fed3b65cb9b81700d22672e85256510c47560ac4cd474b1dbfa082f9cbe2a1bf`  
		Last Modified: Wed, 23 Apr 2025 17:14:37 GMT  
		Size: 1.3 MB (1286403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25de94bd816d79ace36b43db33966d61a65b250e4e496d15b622043fdd13b217`  
		Last Modified: Wed, 23 Apr 2025 17:14:37 GMT  
		Size: 29.0 KB (29020 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:10-Temurin-alpine-plus` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:8d566e834021fc06f6bf25662719d19eecbcb7794a25d3414d1d57bd455bd599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147705055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de5e37f712baa372827087f6cf619b403f47d6e830046021ad3de8df2d4ffb8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 14:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Apr 2025 14:29:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 14:29:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='53877576d3a9dcbf2024789208aa5f045cc65a5645b07d67124b09c2a84f4e1a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.7_6.tar.gz';          ;;        x86_64)          ESUM='f252e13683b381f9f3bfa4948c827ebd80b8e5bd444a1f99de02c56d76c7ad4c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
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
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
ENV TOMEE_VER=10.0.1
# Mon, 07 Apr 2025 14:29:55 GMT
ENV TOMEE_BUILD=plus
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 07 Apr 2025 14:29:55 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e54fdbff4d1839121d84498c497a8933bf178d59d3f6b07144fa173bdc9b972`  
		Last Modified: Thu, 08 May 2025 17:10:27 GMT  
		Size: 16.1 MB (16138642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43093295be6dd627a7ea37c164e5752459e9dd1b60176a3b33aa852bcdcfe9c`  
		Last Modified: Thu, 08 May 2025 17:10:30 GMT  
		Size: 52.1 MB (52119086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48ca9244b555e57c5f69e6b2c4f7ece9a0141e2e55e0459ee103e7371c78511`  
		Last Modified: Thu, 08 May 2025 17:10:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6049c5689637305c8302022d96d4f3692ce889e51390a4d8fc85d9cef97be5be`  
		Last Modified: Thu, 08 May 2025 17:10:26 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f2a99a046247d762d57900e5e0696353ff996818e9b752451fceec316b2dc8`  
		Last Modified: Wed, 23 Apr 2025 19:23:33 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af792d318ce9df3464581c56bfa3232cc644eadc252d5c1d0aa8a364472c4ec`  
		Last Modified: Wed, 23 Apr 2025 19:23:33 GMT  
		Size: 1.1 MB (1138620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84c25a3e8ee359ca6aac2c0c82518088a473c5d5e2a321af8d8f3b3e90c02f0`  
		Last Modified: Wed, 23 Apr 2025 19:23:33 GMT  
		Size: 75.6 KB (75648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082b565f73c5a56cc77e4a8ca0906bd16b6cd286908f2b6db4e2aebc31a51916`  
		Last Modified: Wed, 23 Apr 2025 19:24:36 GMT  
		Size: 74.2 MB (74237421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-Temurin-alpine-plus` - unknown; unknown

```console
$ docker pull tomee@sha256:188da5906da96bf1ba5b8f56c28f875257b6521ad480f5ed72c573535ee35807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1315298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94cd8419e4c0b46808aa266096db141428c73fbc44a8032dfd442836a8431bc0`

```dockerfile
```

-	Layers:
	-	`sha256:62cd0aff0c15efeb794677b7dd40014d507d75988f73de3afd317ffcd340a586`  
		Last Modified: Wed, 23 Apr 2025 19:24:34 GMT  
		Size: 1.3 MB (1285985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb54378079b9510a79b5b5f97041d101c46ece96c51b0218fac339506d4b38ee`  
		Last Modified: Wed, 23 Apr 2025 19:24:33 GMT  
		Size: 29.3 KB (29313 bytes)  
		MIME: application/vnd.in-toto+json
