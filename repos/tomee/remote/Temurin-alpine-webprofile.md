## `tomee:Temurin-alpine-webprofile`

```console
$ docker pull tomee@sha256:5f89745e889f6a4d47a2be9a4dfe2ceacf0b19c51ed13f95c3f653afdc4cf91b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `tomee:Temurin-alpine-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:db5fe483291748cc8ab77300f9ac24df25261a0be714402bf99ab4ef33459abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.6 MB (121628864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c019816b9866a9d43da624fd85d60f8b1c5090ad8c6ed75962e3551720f5a51f`
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
	-	`sha256:9768b8b2682ab07a53ca043ed093f0936b83d1dd961cacb9d088c035838e955c`  
		Last Modified: Wed, 29 May 2024 19:59:10 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a3cd3a25fb99b093f1ad07a1fb559e3073f9069dc44bc2475b32e073bb4512`  
		Last Modified: Wed, 29 May 2024 19:59:10 GMT  
		Size: 6.2 MB (6247940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619e7a3be43d4fb68a787f609c9e86c8e89a618c1f7f546ce3479ebfb53a03be`  
		Last Modified: Wed, 29 May 2024 19:59:10 GMT  
		Size: 69.2 KB (69222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ddd636c132d639f84544a03f54d8767354ec22a2aee4d49a5478b6defd3a04`  
		Last Modified: Wed, 29 May 2024 19:59:11 GMT  
		Size: 59.8 MB (59813893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:Temurin-alpine-webprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:f2cda031e2c66f4086c3f708de9de8a7a138d4b804fbd68a759be6d9896d81a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1415616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae63160e4911b1ec07463b810c022b207ed956068ab52a7e49b5832ee61d5ef`

```dockerfile
```

-	Layers:
	-	`sha256:5b1e991227413db9eb1db56ac220f1fa7f7c8153c870aa305ff57d0f34ddcc97`  
		Last Modified: Wed, 29 May 2024 19:59:10 GMT  
		Size: 1.4 MB (1386745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe7276a8a3a45fa733f60a6607b96c49b7175930e6f52ea3728022e5f07d2866`  
		Last Modified: Wed, 29 May 2024 19:59:09 GMT  
		Size: 28.9 KB (28871 bytes)  
		MIME: application/vnd.in-toto+json
