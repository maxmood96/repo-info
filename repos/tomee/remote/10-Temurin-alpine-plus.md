## `tomee:10-Temurin-alpine-plus`

```console
$ docker pull tomee@sha256:82b7b7b87d806e21e2458e5409be8a74447fa563760bc66a06a42f2e9d3323dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `tomee:10-Temurin-alpine-plus` - linux; amd64

```console
$ docker pull tomee@sha256:bebc680b1d16ed65ec51eeda0312ab13157e920646c438ac2d5f84300b88d5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141765306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695536e78781fbfe078a21aa8a97ec25e2fd64da88be2742136924c19f751f93`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 18:18:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Jul 2024 18:18:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 18:18:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Jul 2024 18:18:20 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 23 Jul 2024 18:18:20 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='63bae276cc322532b451ae7473127c92a75db16cc95473577f133cd09349822a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Jul 2024 18:18:20 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 18:18:20 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
WORKDIR /usr/local/tomee
# Tue, 23 Jul 2024 18:18:20 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
ENV TOMEE_VER=10.0.0-M2
# Tue, 23 Jul 2024 18:18:20 GMT
ENV TOMEE_BUILD=plus
# Tue, 23 Jul 2024 18:18:20 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 23 Jul 2024 18:18:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dff7dc6fc2858af0a16833a15a63741d58d895a9d1a9a2de411e9921a0de0dd`  
		Last Modified: Thu, 25 Jul 2024 17:25:18 GMT  
		Size: 9.4 MB (9394889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f5650f3ff3cbac78a5ddc894de21bb232ed2cc7038ae6440a33d9fa494711f`  
		Last Modified: Thu, 25 Jul 2024 17:30:24 GMT  
		Size: 47.0 MB (46988407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25c44b9167a8f0d71bc58f67c439ac4e294f54780a414f8c7367136b652cd86`  
		Last Modified: Thu, 25 Jul 2024 17:30:17 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6596ba099baa21107eeae01921800730fcc39c95a2220c8e13ec7ec356bf45`  
		Last Modified: Thu, 25 Jul 2024 17:30:17 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2448ce63e3b8ad032ed0d30df5053bc1ac3766b5aeefb64737f39d88d3f72630`  
		Last Modified: Thu, 25 Jul 2024 19:06:49 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8625fcdd09cf5e8d4ad6b586a6a1b71f9ea1f244982f9da41ca238b43f8978`  
		Last Modified: Thu, 25 Jul 2024 19:06:49 GMT  
		Size: 6.7 MB (6739679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de36c5d0fedf38f3a64501efcb56a7e38012b75ea7e6673cf9eb863ea6da938`  
		Last Modified: Thu, 25 Jul 2024 19:06:49 GMT  
		Size: 69.2 KB (69217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be73369318bbc27c264150b5ef50b0592eb343224d4d560566fc950bfac3037`  
		Last Modified: Thu, 25 Jul 2024 19:06:50 GMT  
		Size: 74.9 MB (74948014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-Temurin-alpine-plus` - unknown; unknown

```console
$ docker pull tomee@sha256:9f1866cc4a8ddf392ff66a3c2c26ae87be5063162e21538bc9c19ce6a14e85f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1198215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84994098273369b7687c6549b32439e6c609a1553ea318f385aa971fca8bf486`

```dockerfile
```

-	Layers:
	-	`sha256:8611f13aade3c99c2f4f6814be94868b3f2afbfb8e392e6732950db0853eb102`  
		Last Modified: Thu, 25 Jul 2024 19:06:49 GMT  
		Size: 1.2 MB (1170724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:626d9b8f266bc4c41eabad32002d1b26081f1780d2d7a8167e456b78ba7d7b9a`  
		Last Modified: Thu, 25 Jul 2024 19:06:49 GMT  
		Size: 27.5 KB (27491 bytes)  
		MIME: application/vnd.in-toto+json
