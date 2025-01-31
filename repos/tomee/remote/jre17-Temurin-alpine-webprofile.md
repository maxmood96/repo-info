## `tomee:jre17-Temurin-alpine-webprofile`

```console
$ docker pull tomee@sha256:c135a67f54a39105d043c7655119dada5cf51207058862f78558ab6bd646e216
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `tomee:jre17-Temurin-alpine-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:2319b4bc34c66c6841ab4f4a470ffdc530f61ed83ab526589ff9e3dbd08afbdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126636471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f106d7d9978d82a2ee7e30c075c66d379468b5f63cbb7be9cf54fc6963f7b4d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 29 Dec 2024 01:38:24 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
CMD ["/bin/sh"]
# Sun, 29 Dec 2024 01:38:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 29 Dec 2024 01:38:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 29 Dec 2024 01:38:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 29 Dec 2024 01:38:24 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 29 Dec 2024 01:38:24 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='9dcc53a30676692e604571a6e0bd13ac0c1b15f4bc2b78d19f88bd316075f84a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
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
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
ENV TOMEE_VER=10.0.0
# Sun, 29 Dec 2024 01:38:24 GMT
ENV TOMEE_BUILD=webprofile
# Sun, 29 Dec 2024 01:38:24 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
EXPOSE map[8080/tcp:{}]
# Sun, 29 Dec 2024 01:38:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ab26856ac4f725d325530eb0ee080b037f945aa0a7d1b6ba9884132373e0e5`  
		Last Modified: Fri, 31 Jan 2025 01:30:45 GMT  
		Size: 16.1 MB (16135200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb326cca950e7e93fb8a8742863258c98582d6d2df90935e1926c352584514e`  
		Last Modified: Fri, 31 Jan 2025 01:30:47 GMT  
		Size: 46.6 MB (46619364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c7f77008c462a2554e8ba35bfa3631292409ebe3f44b52206cd181866c2695`  
		Last Modified: Fri, 31 Jan 2025 01:30:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b0c9453479824b697beefdd4f4a6e47fc09a3d0e65f2b8b1bc732ffb696fd`  
		Last Modified: Fri, 31 Jan 2025 01:30:45 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca063a69b55251c6df2afd56b3d283ff4f2643bff6de67008974b6ae9541229`  
		Last Modified: Fri, 31 Jan 2025 02:13:27 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c39a7f15bf95061472223bc56eb73345a174592f93c571c72324b81ef62da3f`  
		Last Modified: Fri, 31 Jan 2025 02:13:27 GMT  
		Size: 1.1 MB (1141703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76f4195b0cc4fe8cab14ddb215a53f13f4d4b11f53e08f91bbc7078d1d966af`  
		Last Modified: Fri, 31 Jan 2025 02:13:27 GMT  
		Size: 75.6 KB (75609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9755cbc6e99ea76aa34ac2562bc29caf5cf998a95583f502ca9a2607a5e99a11`  
		Last Modified: Fri, 31 Jan 2025 02:13:29 GMT  
		Size: 59.0 MB (59020270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre17-Temurin-alpine-webprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:be9bdcdd0d02ae7174f478d6f63af932bb45781bae88e8f6f59fb4a27a07f3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1191077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601e21a92d4196d177279a305e1af5fe9b6d34db6bb463ca42fcabcd559bd8e5`

```dockerfile
```

-	Layers:
	-	`sha256:d48430bc09ffe15d89dd71e8be4d993638ca77d612518e691eb198d956404af0`  
		Last Modified: Fri, 31 Jan 2025 02:13:27 GMT  
		Size: 1.2 MB (1164503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b145590a124c999fb388621bd9615db051f5ee49224fdb03e6cf023b6990d90`  
		Last Modified: Fri, 31 Jan 2025 02:13:27 GMT  
		Size: 26.6 KB (26574 bytes)  
		MIME: application/vnd.in-toto+json
