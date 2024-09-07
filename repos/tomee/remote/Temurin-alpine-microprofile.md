## `tomee:Temurin-alpine-microprofile`

```console
$ docker pull tomee@sha256:616110b08923c361a5578ede49e94a33d5b793ed7bcbcfa08cbc8420e1b312ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `tomee:Temurin-alpine-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:532fc25a70943a72d3fe5a7282f6b271e9f7918cbe6e24dc2ea2a8908fdaeae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131224974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bcf4c3ad902faa952b44471faf59d07ccd6637b5a5690981e55f9ab453e657`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 23 Jul 2024 18:18:20 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 23 Jul 2024 18:18:20 GMT
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
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 23 Jul 2024 18:18:20 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='0ac795729cc11f47323a71713eac2a5b22d4615fd9b66c8766f964c03fb6e160';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
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
ENV TOMEE_VER=9.1.3
# Tue, 23 Jul 2024 18:18:20 GMT
ENV TOMEE_BUILD=microprofile
# Tue, 23 Jul 2024 18:18:20 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 23 Jul 2024 18:18:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb0eeeb44ea727a6840e888ba4140371726ac8b86f199aa403faf61b4de2106`  
		Last Modified: Fri, 06 Sep 2024 22:43:01 GMT  
		Size: 9.4 MB (9388900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0134e7b8333dd4fcc1a8290fa23aabe0f1e06bf7fa38b9c80d9bab53666b689e`  
		Last Modified: Fri, 06 Sep 2024 22:44:01 GMT  
		Size: 43.6 MB (43555914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375eef2b0838c81a0a486232bf1cb0d5fb98d6b206f8e582934c37becf1373b3`  
		Last Modified: Fri, 06 Sep 2024 22:43:55 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ceab00d652976aa48a3f666a2fd1a6af382aed83311992002db5053486e2e58`  
		Last Modified: Fri, 06 Sep 2024 22:43:55 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3995ae5a5160713639fb698571f02afb61b9ae8b7613d5a817ae6b02e50ac57`  
		Last Modified: Sat, 07 Sep 2024 00:08:31 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e544216de3ba586f490d244e508a3ce60a6955cd00455a1cf97c3955df8cc0bb`  
		Last Modified: Sat, 07 Sep 2024 00:08:32 GMT  
		Size: 6.7 MB (6739302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c81eaf9814a62b442d6c16b0ca9a0535bb6f3976bdf2229d654c33ff45566ce`  
		Last Modified: Sat, 07 Sep 2024 00:08:32 GMT  
		Size: 69.2 KB (69208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fea107485d6ef6ef174e26b663b3f1b6621afe79a44678b88a2421535262a2`  
		Last Modified: Sat, 07 Sep 2024 00:08:33 GMT  
		Size: 67.8 MB (67845392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:Temurin-alpine-microprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:dea15332368843fc8656da701a89ce84cabb2ce2902d6ee0263783fe424ecf08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1182220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b0703edf037bd29bfd89ffcb4bb13a6538c03df73606cc88284e8e44870ee8`

```dockerfile
```

-	Layers:
	-	`sha256:b8ffd5c3c49b48c5e883283ba56cc9495f5961274b3a7f6aecae0e20e439e9b9`  
		Last Modified: Sat, 07 Sep 2024 00:08:32 GMT  
		Size: 1.1 MB (1148164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:319bfcd41cd0a0148c13c70928a3f4c454fa3a764eec8526c946fe15adf92d7b`  
		Last Modified: Sat, 07 Sep 2024 00:08:32 GMT  
		Size: 34.1 KB (34056 bytes)  
		MIME: application/vnd.in-toto+json
