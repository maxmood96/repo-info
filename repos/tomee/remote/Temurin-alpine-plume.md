## `tomee:Temurin-alpine-plume`

```console
$ docker pull tomee@sha256:a765c0a40300d2a71ceebef42a6fcd7d5d9244fb1f210c8df46fed1a420a69b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `tomee:Temurin-alpine-plume` - linux; amd64

```console
$ docker pull tomee@sha256:2a208f8d870997347d7fd448245b1072457c301a9dc8abefab57af043643cc39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142773956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed08f2e91064b2a32dd48efdb5d5eb008e57bf78417da134beb6093283f0856e`
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
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6972a6251bc88d6fbb64a188557cf165f1c415ded550d2a280bbcbc4272caff1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
RUN apk add --no-cache gpg gpg-agent dirmngr curl  && rm -rf /var/cache/apk/* # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
ENV TOMEE_VER=9.1.3
# Tue, 16 Apr 2024 02:54:00 GMT
ENV TOMEE_BUILD=plume
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
	-	`sha256:1e3d1cfa98477703d37bdfee5d9c7b99c0256916840d96e9bc0b4d10c8e66628`  
		Last Modified: Wed, 24 Apr 2024 19:11:45 GMT  
		Size: 43.6 MB (43550586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29f1605bed22bdbed842212962c7cf81fea5196c466c33964d33ac3271c227e`  
		Last Modified: Wed, 24 Apr 2024 19:11:40 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17f30e766d9eada0e56ff7b2fdcf616bc834834bea453e938536243d819c653`  
		Last Modified: Wed, 24 Apr 2024 19:11:39 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d128b72e7d409e767e735df3eea65160cb0a4c879170a9e21903b3ef0d0443`  
		Last Modified: Wed, 29 May 2024 19:59:21 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36336e577d157a345f126c1f2a921a3608ed75e15c10c4e8c0e6be09282bd75`  
		Last Modified: Wed, 29 May 2024 19:59:22 GMT  
		Size: 6.2 MB (6247843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a1392201d929bcb84de2c41b19c6119fa4f51b7e99db814ce196a6114120dd`  
		Last Modified: Wed, 29 May 2024 19:59:21 GMT  
		Size: 69.3 KB (69285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ff8989b02aa09905d4de71dc7b6cfda3ed28edb7248537632ccce60e8a4e9b`  
		Last Modified: Wed, 29 May 2024 19:59:24 GMT  
		Size: 81.0 MB (80959019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:Temurin-alpine-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:73f39816e06634fd6fd3c11bceb8b754214224b2e91a4d22e853fe04c9ae0e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 MB (1505849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc8d0d87acd14fdc063a0be652ade09179832189650462669d6768cc640c1d6`

```dockerfile
```

-	Layers:
	-	`sha256:3a3c9f3a44df77ac478a28827eccaaf46d3e8d2341d0b196880862a38a8905d0`  
		Last Modified: Wed, 29 May 2024 19:59:21 GMT  
		Size: 1.5 MB (1477161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da396a37e83f062c305c9fb8578f3ced48caf1e361b20dd37225093c35f3d3f1`  
		Last Modified: Wed, 29 May 2024 19:59:21 GMT  
		Size: 28.7 KB (28688 bytes)  
		MIME: application/vnd.in-toto+json
