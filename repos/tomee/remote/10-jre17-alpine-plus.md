## `tomee:10-jre17-alpine-plus`

```console
$ docker pull tomee@sha256:fc24a0bd66ef7afdc6a75de8b756a8bf4414f9fa22d928ec540799aa93893a26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `tomee:10-jre17-alpine-plus` - linux; amd64

```console
$ docker pull tomee@sha256:f768400361e026e28b6fc77e87102d2b577626b145f1cd14b2894db7a63b44d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140726790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29caaf0002aedd37137ca7b3a79f366fa9723b6cb93152ab7260f09bf021ccb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 16:13:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jul 2024 16:13:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jul 2024 16:13:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jul 2024 16:13:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jul 2024 16:13:57 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 22 Jul 2024 16:13:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='63bae276cc322532b451ae7473127c92a75db16cc95473577f133cd09349822a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:0b502c76566e71337b4737a25ae762dd54193bc78dba7f7474ea005c07de9efc`  
		Last Modified: Tue, 23 Jul 2024 01:08:16 GMT  
		Size: 8.4 MB (8371901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470b7c21f90c416505c5901e5ae2dc4a6a315754d31af26e1d7d23764d79648f`  
		Last Modified: Tue, 23 Jul 2024 01:08:21 GMT  
		Size: 47.0 MB (46988362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fda088e83ffe4cb0dd87d2788cf604b5681474d8e4ffe7a92e24e0b992b0a9`  
		Last Modified: Tue, 23 Jul 2024 01:08:15 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7031008d0f5d9a0cf6c47471b6ba33130dc95daad90f22cf4837c5ea3d0687bc`  
		Last Modified: Tue, 23 Jul 2024 01:08:15 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2a06532f19cd1ddb512fdac4b22bc491d5f21cd25866d57fe057f9c43649ec`  
		Last Modified: Tue, 23 Jul 2024 19:12:22 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a10c53125a112320bf9530cb178237ff340208aad654e95110f701da22c7022`  
		Last Modified: Tue, 23 Jul 2024 19:12:22 GMT  
		Size: 6.7 MB (6724723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6c1a119ae60a7888a03918b04032fecdc1c0e138ea24114c5151f96ee52e21`  
		Last Modified: Tue, 23 Jul 2024 19:12:22 GMT  
		Size: 69.2 KB (69197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cf7d34905ddaf235fe7dbb6ae8e0096ce0b7eed061f01381954488ab6bd77c`  
		Last Modified: Tue, 23 Jul 2024 19:12:24 GMT  
		Size: 74.9 MB (74947939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre17-alpine-plus` - unknown; unknown

```console
$ docker pull tomee@sha256:1073b21f28182179b38218528aaa16966c0e27308a73dac564e8a87e77b0d788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1179692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380ec61f08e701f757548645c93c349e23b3d0f191b95a9c852e18e55c6d4378`

```dockerfile
```

-	Layers:
	-	`sha256:c8bbfa8ad78c82c4118133b03a4729541a608b58e3b441f9c88675fb9cdc2cb4`  
		Last Modified: Tue, 23 Jul 2024 19:12:22 GMT  
		Size: 1.2 MB (1152201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5b64a156bd1d27dc89f3bd532535ef3cb14492bcbe1ad43c9e95ba494a96aee`  
		Last Modified: Tue, 23 Jul 2024 19:12:22 GMT  
		Size: 27.5 KB (27491 bytes)  
		MIME: application/vnd.in-toto+json
