## `tomee:jre21-alpine-plume`

```console
$ docker pull tomee@sha256:49df30d9a842e7808e2057b3180d10749962b7ee155a323a82a53f5f6d74865a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:jre21-alpine-plume` - linux; amd64

```console
$ docker pull tomee@sha256:c26386d3f6b0947b992ad6ba14e54f6cfec34af000840e680ef46218aa117680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156446935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06cbfbd5ebf381ab6eb29ceeed468e789f285df817566a1ff5427c9624a1650`
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
RUN apk add --no-cache gpg gpg-agent dirmngr curl  && rm -rf /var/cache/apk/* # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
ENV TOMEE_VER=10.0.1
# Mon, 07 Apr 2025 14:29:55 GMT
ENV TOMEE_BUILD=plume
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
	-	`sha256:93b1dfbc6aa035a280b80f76b19b8880006325992f24657c2d5379299664c391`  
		Last Modified: Fri, 09 May 2025 12:21:01 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5c9b17af3aaea9c35cfd696767317e064aa54d6ba5781259f94ab10cbceb96`  
		Last Modified: Fri, 09 May 2025 12:21:01 GMT  
		Size: 1.1 MB (1148489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975b92a2a232ad41342b6f9081986257f0e1fcfa43e63f25b6ce7892093d88db`  
		Last Modified: Fri, 09 May 2025 12:21:01 GMT  
		Size: 75.6 KB (75626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc155d06d797311d770187e2de637dca922f7a6e5e74a616ee5a54a7df920daa`  
		Last Modified: Fri, 09 May 2025 12:21:05 GMT  
		Size: 82.3 MB (82341482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre21-alpine-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:2ef34e0a243a64854ba1f8550b749407eafc628ac05dd2876c76de1a1e035033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1330862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0de5648fb4aef713c17a6439ee3dbef1993c4f4ed8ba8d65625dc8952130c35`

```dockerfile
```

-	Layers:
	-	`sha256:d0e50aca722c993d79b78d1b2fc84a41a864bf9edd6dcaedf6455c3e6eea1997`  
		Last Modified: Wed, 23 Apr 2025 17:14:35 GMT  
		Size: 1.3 MB (1301808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46403545ac6d7eb4da4192338bb3fef0ab30e58dd061c4400ec188175525387a`  
		Last Modified: Wed, 23 Apr 2025 17:14:34 GMT  
		Size: 29.1 KB (29054 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:jre21-alpine-plume` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:1e154ce4e05f71734e7d5ade39688e088beb375a5cb83254591920a292c6ed45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155809297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c234a85e7752f3d3de6c45278823d4e79d25412b429cf408be9659a5c2b4426`
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
RUN apk add --no-cache gpg gpg-agent dirmngr curl  && rm -rf /var/cache/apk/* # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
ENV TOMEE_VER=10.0.1
# Mon, 07 Apr 2025 14:29:55 GMT
ENV TOMEE_BUILD=plume
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
	-	`sha256:ab0c736dcb9be8b72271d33c6a5db146293571c7e61f1561adb7dd98256db1f0`  
		Last Modified: Wed, 23 Apr 2025 19:24:08 GMT  
		Size: 1.1 MB (1138620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f7aa399db87d8b65702eaad6cced9629b2b21e3faaed102e773fe79da2fdb7`  
		Last Modified: Wed, 23 Apr 2025 19:24:08 GMT  
		Size: 75.7 KB (75658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c44d4613eda9c7c8df8cea6628350ffad37dd6e9e8879f516fb708c98e44ae`  
		Last Modified: Wed, 23 Apr 2025 19:24:11 GMT  
		Size: 82.3 MB (82341653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre21-alpine-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:226b3138eac5e05cb4c5126f977c1bcd3bee1eda55c20ba3ad13a798de1a3556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1330736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2ea90ddfa04e6dbc181e7654148fe25ff960adf0e2b761add3f1acf9632239`

```dockerfile
```

-	Layers:
	-	`sha256:52e6054ed4b95ac1fb3a30a7fc36515c6446bd05ba24d045e4ff67a1077ddba5`  
		Last Modified: Wed, 23 Apr 2025 19:24:08 GMT  
		Size: 1.3 MB (1301390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75838b48e6068b850d598826bf63f0a1dca1dd9549cdb42c6e17d415f113e3f`  
		Last Modified: Wed, 23 Apr 2025 19:24:08 GMT  
		Size: 29.3 KB (29346 bytes)  
		MIME: application/vnd.in-toto+json
