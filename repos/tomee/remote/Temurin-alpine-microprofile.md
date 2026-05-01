## `tomee:Temurin-alpine-microprofile`

```console
$ docker pull tomee@sha256:bb78bf2cd195ca1e2b0237ad74cfc148d38104f87fd0156795116f7305d37d46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:Temurin-alpine-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:58963506d86fa544759355711c25b413dff18ab2f88e27d367f5199bda76b912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153244959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de653c5b9c1cca247f888221a2d9ddd353e9664f135d586af45d330d39251a2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:28:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:28:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:28:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:28:48 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Apr 2026 23:28:48 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:28:52 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='48aa0908d9f4d501c1070ebbc8a4da93ca1f066c41ff2e34a22a34dd3ca2dac1';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='ad202c8f8b216800ed0d6581130f92e5680b685ba394ba38e62e7605c3fd9494';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Thu, 30 Apr 2026 23:28:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:28:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:28:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Apr 2026 23:52:30 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:52:30 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Thu, 30 Apr 2026 23:52:30 GMT
WORKDIR /usr/local/tomee
# Thu, 30 Apr 2026 23:52:31 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Apr 2026 23:52:40 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Thu, 30 Apr 2026 23:52:40 GMT
ENV TOMEE_VER=10.1.4
# Thu, 30 Apr 2026 23:52:40 GMT
ENV TOMEE_BUILD=microprofile
# Thu, 30 Apr 2026 23:52:41 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Thu, 30 Apr 2026 23:52:41 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 30 Apr 2026 23:52:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1335792811458e3e4c22ab6e0025df0f3de8a92b49e4e96b6ccd8b88c370781f`  
		Last Modified: Thu, 30 Apr 2026 23:29:05 GMT  
		Size: 9.4 MB (9437616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53473754426f243fd00d95d8839b6a0fedb13efffa3d3ccdf63b9b1d5386388b`  
		Last Modified: Thu, 30 Apr 2026 23:29:06 GMT  
		Size: 62.1 MB (62119875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20ccdd0c7bb68e396b2c66aa39ca2d60c83bd97e3b8ad8bb29b4eba112ef532`  
		Last Modified: Thu, 30 Apr 2026 23:29:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e109dd049422d199ac3c3328c12b15431660a3a1bc64d8fdd24f2f88da5efc4`  
		Last Modified: Thu, 30 Apr 2026 23:29:05 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb7670fc97c004f0e1d8da753df7f879b8abeeeeff28827096cbc12352f83b5`  
		Last Modified: Thu, 30 Apr 2026 23:52:51 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de30e552896b7addab1ead54cb273ae6be25b7e24f0b43906ec3c7a29358e070`  
		Last Modified: Thu, 30 Apr 2026 23:52:52 GMT  
		Size: 7.2 MB (7238060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904a4f4d6a85c9fa4a383bd7bdf4984436a55f6e4630ce12aa910bed9e980798`  
		Last Modified: Thu, 30 Apr 2026 23:52:51 GMT  
		Size: 75.7 KB (75657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd336a0a993ccd6f377c59d7e399c8d655cb4e013c577663581fa16e9109feeb`  
		Last Modified: Thu, 30 Apr 2026 23:52:54 GMT  
		Size: 70.5 MB (70506951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:Temurin-alpine-microprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:29ba0703dff9959c84f82dee2813a4f03fec53d3b84561b40f4504489210049f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1329360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0670a425b1e97cb4a1d0f11706f0e02c2b3e9cedaa0e092549f6119b9b25805c`

```dockerfile
```

-	Layers:
	-	`sha256:d3b3845843f0defe809dda8a864e213fe6bb91c45862e04829266813a812e48d`  
		Last Modified: Thu, 30 Apr 2026 23:52:51 GMT  
		Size: 1.3 MB (1293889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95b063657ef5558ded6cab9813800605c23ced8b4277a036673ce3ca92288bd3`  
		Last Modified: Thu, 30 Apr 2026 23:52:51 GMT  
		Size: 35.5 KB (35471 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:Temurin-alpine-microprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:93c9a5d90fd34050911d5e874fa22d2aca80966499bf3a602fc726dbc32637f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152450152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abab3ad2bd60f979731985f8505f4b2079430e3bb7e835a2bcd13143bdb1ef7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:28:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:28:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:28:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:28:52 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Apr 2026 23:28:52 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:28:58 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='48aa0908d9f4d501c1070ebbc8a4da93ca1f066c41ff2e34a22a34dd3ca2dac1';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='ad202c8f8b216800ed0d6581130f92e5680b685ba394ba38e62e7605c3fd9494';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Thu, 30 Apr 2026 23:28:58 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:28:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:28:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Apr 2026 23:51:58 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:51:58 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Thu, 30 Apr 2026 23:51:58 GMT
WORKDIR /usr/local/tomee
# Thu, 30 Apr 2026 23:51:59 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Apr 2026 23:52:08 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Thu, 30 Apr 2026 23:52:08 GMT
ENV TOMEE_VER=10.1.4
# Thu, 30 Apr 2026 23:52:08 GMT
ENV TOMEE_BUILD=microprofile
# Thu, 30 Apr 2026 23:52:10 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Thu, 30 Apr 2026 23:52:10 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 30 Apr 2026 23:52:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea87a7a676e6ed46ad18a59819fd003f60e091562044d350b9534dbf1cc19c3`  
		Last Modified: Thu, 30 Apr 2026 23:29:11 GMT  
		Size: 9.5 MB (9467938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3141fab2d8b9fd9f3fc180255ad9cc94fc995a5a69d452ff48020c58f003b8`  
		Last Modified: Thu, 30 Apr 2026 23:29:13 GMT  
		Size: 61.0 MB (61049419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1edb42d6c7963ddbb1752ef7ec70f042d75f8daaf69b1924bac3f83d383c9e`  
		Last Modified: Thu, 30 Apr 2026 23:29:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebd003d1369d71668442108c8fb25bd5cc26c550d748996fecf29e3701f58e1`  
		Last Modified: Thu, 30 Apr 2026 23:29:10 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e004ebbad245861e1da7f02a3477edac04874d1306a1e8a79193ad390c6cff42`  
		Last Modified: Thu, 30 Apr 2026 23:52:19 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648ba25b3fefe7d88eb23bee5527149dad3fbfee137706f2bba7d01beeb8863f`  
		Last Modified: Thu, 30 Apr 2026 23:52:20 GMT  
		Size: 7.1 MB (7147736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969599b0bc02b9bc2f86c0a8cfea85e47033a88798d8eaf6f73493a80355c489`  
		Last Modified: Thu, 30 Apr 2026 23:52:20 GMT  
		Size: 75.6 KB (75637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43a60c9f5b0ea895409e4041f3f36d7c2f1856c0673a842aad37a681bdee8b9`  
		Last Modified: Thu, 30 Apr 2026 23:52:22 GMT  
		Size: 70.5 MB (70506944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:Temurin-alpine-microprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:e05544404bd0ccf7ec028f2cfe5c5c4aebd86f2dfee1c69f08b9d882d4dbfee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cddccbc979cb10e4d18e6956c5a2897140effe1d029464fc7a20ee66141ba5a9`

```dockerfile
```

-	Layers:
	-	`sha256:a960683df51428187bdbd86433e1a15d6f66e111591d09b04f1f7a470987787a`  
		Last Modified: Thu, 30 Apr 2026 23:52:20 GMT  
		Size: 1.3 MB (1293010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:820b7effe799dcfd888243276e74471fa275511a1add1c5076350adefc1fec5c`  
		Last Modified: Thu, 30 Apr 2026 23:52:19 GMT  
		Size: 36.0 KB (35956 bytes)  
		MIME: application/vnd.in-toto+json
