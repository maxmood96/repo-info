## `tomee:9-jre17-Temurin-alpine-webprofile`

```console
$ docker pull tomee@sha256:5f6166259e372aa015e8ca702aef3d34016226eb9855907437297f653cff6a5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `tomee:9-jre17-Temurin-alpine-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:18df6c0e08660341d1bb404084ddd80b3f75f7bdfc8eba2c28bf6f5f9f9b4277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (125038191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110e2f94e03840af3737d78873c2f41a8c4e55df3836e379c1f46204c5b1dc7f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 02:54:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 02:54:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 02:54:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b5dffd0be08c464d9c3903e2947508c1a5c21804ea1cff5556991a2a47d617d8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
ENV TOMEE_VER=9.1.3
# Tue, 16 Apr 2024 02:54:00 GMT
ENV TOMEE_BUILD=webprofile
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 16 Apr 2024 02:54:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21a63612cbe8d148f75173be90696fbe03e2a6e9c901e2c039bcf1bcdeec0b9`  
		Last Modified: Thu, 28 Mar 2024 02:02:51 GMT  
		Size: 8.5 MB (8537401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044b9313de2afda99e3d271191e0d2073d7a727c9df216c038388ffd94f908b7`  
		Last Modified: Wed, 24 Apr 2024 19:14:50 GMT  
		Size: 47.0 MB (46959908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c25709ed33f3c499e1c54719b8dffff0e975b8c2d6d5936a82ce1b39509a6c`  
		Last Modified: Wed, 24 Apr 2024 19:14:44 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0286f19aa81e34bfcb4aab7b73cf3d3e927b3d0d3c9211a3f12e65049e1b304b`  
		Last Modified: Wed, 24 Apr 2024 19:14:44 GMT  
		Size: 715.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233bdf591a357aedc3f6cc26e00862154e7534e6a6c937d3355e6b8936ce85a5`  
		Last Modified: Wed, 29 May 2024 19:57:35 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01449b9db7a1d69df9fa5b64a6798ba9187e3b5fbca4f2c83e0f4fbc66039321`  
		Last Modified: Wed, 29 May 2024 19:57:35 GMT  
		Size: 6.2 MB (6247951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdb33ac4c89422122fe101fe2bbe5b2de869d24a375d1fc20f954638e88e0d0`  
		Last Modified: Wed, 29 May 2024 19:57:35 GMT  
		Size: 69.2 KB (69227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b1558423a229798fd9e4066de41b7d236a47ff2ba71f15158dec99a1d59d57`  
		Last Modified: Wed, 29 May 2024 19:57:36 GMT  
		Size: 59.8 MB (59813883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:9-jre17-Temurin-alpine-webprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:9286c6a6a4ff7c4c41ddfb763cadea6c6663579495110b8f9f0807b6eaba0c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1410310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04a83f653cbc4a985f56dfeab65b4364f0343f43229985ae9b249c7a31f3977`

```dockerfile
```

-	Layers:
	-	`sha256:abb0afbea2780138e628ec9acd70abe77cadeb7ec4f76ee179571b836a54d944`  
		Last Modified: Wed, 29 May 2024 19:57:35 GMT  
		Size: 1.4 MB (1384094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a425702e848ad08d53738849e69a2522892609fe916de0a43a412d8f9d631789`  
		Last Modified: Wed, 29 May 2024 19:57:35 GMT  
		Size: 26.2 KB (26216 bytes)  
		MIME: application/vnd.in-toto+json
