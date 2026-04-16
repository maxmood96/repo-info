## `tomee:jre25-alpine`

```console
$ docker pull tomee@sha256:03e95d0f986f9ae72bb3bd6d46deb7a7857b7dbe257be4a3c55099d27419662e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:jre25-alpine` - linux; amd64

```console
$ docker pull tomee@sha256:858ae59c24703808f47a7301797032a1745fd3d21c1bd65c83e70a205ab65503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153114447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd93c6d8cb56bf635d92f15a5d9684081aedda74e58018b0adc4e937d788a50`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:34:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:20 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:34:20 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 15 Apr 2026 20:34:25 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='159099235c536b152f86111a694a8a03392948924736f354c79e95532dcfc1f8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='2cbb356c6923f89814b892561e6f0377ecf035ab0577e3162d2cf4e202d38ee7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Wed, 15 Apr 2026 20:34:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:56:59 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:56:59 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Wed, 15 Apr 2026 21:56:59 GMT
WORKDIR /usr/local/tomee
# Wed, 15 Apr 2026 21:57:00 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 21:57:09 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 15 Apr 2026 21:57:09 GMT
ENV TOMEE_VER=10.1.4
# Wed, 15 Apr 2026 21:57:09 GMT
ENV TOMEE_BUILD=microprofile
# Wed, 15 Apr 2026 21:57:11 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Wed, 15 Apr 2026 21:57:11 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 21:57:11 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af76732d1c87ea83d225c5f6a2bf4fa407c04df7ac0d6690f5edd0cebf5d443`  
		Last Modified: Wed, 15 Apr 2026 20:34:38 GMT  
		Size: 9.4 MB (9437820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3300773eb3533c39a390c3a79a3507cbfce58fff5b2830599b1b2777e3e6b03`  
		Last Modified: Wed, 15 Apr 2026 20:34:40 GMT  
		Size: 62.0 MB (61989231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e724d96c5cee4b750a12171be14e0977a7b52bd4f65b0a2fafc4c3511d445e40`  
		Last Modified: Wed, 15 Apr 2026 20:34:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a087e3676bef7e9b9fca18be80126326e794d2eeb53107f3540f62cbfd2e90`  
		Last Modified: Wed, 15 Apr 2026 20:34:38 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580764e983b8bf5cfa3862991f83c04334d61af806e0105ebac27add096623c4`  
		Last Modified: Wed, 15 Apr 2026 21:57:20 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8004cfb981abd95b12925965d6629ffc3e96fc31c224589e0fb7bf93ef8164`  
		Last Modified: Wed, 15 Apr 2026 21:57:20 GMT  
		Size: 7.2 MB (7238018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8d5764866c7ec34bcab8125bc28e6e2055651c666a10fa6892a930faed9b9d`  
		Last Modified: Wed, 15 Apr 2026 21:57:20 GMT  
		Size: 75.6 KB (75629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280c0eb4428ca733385903046f9e21fd8e3f3dd2fd402e1b5c6acdd7b038b409`  
		Last Modified: Wed, 15 Apr 2026 21:57:22 GMT  
		Size: 70.5 MB (70506949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre25-alpine` - unknown; unknown

```console
$ docker pull tomee@sha256:5fb2d8273740e83c1f77b00efc55de2849402e851ad720dd98377c1a0597fe3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560258c6cda4259b4ac6b157ef21591a2cb92f398f99f79a101115a769b959d1`

```dockerfile
```

-	Layers:
	-	`sha256:8bc534e259ba0191a08159eed86cf13af068bac59ac2e3fb44a7fc9ea185d747`  
		Last Modified: Wed, 15 Apr 2026 21:57:20 GMT  
		Size: 1.3 MB (1293266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:483915047b178b960a20e0f17863a3a79440a9c10c0346ae4361e9028f4099c8`  
		Last Modified: Wed, 15 Apr 2026 21:57:20 GMT  
		Size: 35.5 KB (35475 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:jre25-alpine` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:f0af4341a5e7c5add43afff233df96c6422ccdce40db9593a1d911aed9777a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.3 MB (152315152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20dff02895f0d8cd8b6d2b83068c0a32a005d26de9c8b6c871b3b8aec1d4fdcb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:34:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:33 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:34:33 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 15 Apr 2026 20:34:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='159099235c536b152f86111a694a8a03392948924736f354c79e95532dcfc1f8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='2cbb356c6923f89814b892561e6f0377ecf035ab0577e3162d2cf4e202d38ee7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Wed, 15 Apr 2026 20:34:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:09:09 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:09:09 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Wed, 15 Apr 2026 22:09:09 GMT
WORKDIR /usr/local/tomee
# Wed, 15 Apr 2026 22:09:10 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 22:09:20 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 15 Apr 2026 22:09:20 GMT
ENV TOMEE_VER=10.1.4
# Wed, 15 Apr 2026 22:09:20 GMT
ENV TOMEE_BUILD=microprofile
# Wed, 15 Apr 2026 22:09:26 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Wed, 15 Apr 2026 22:09:26 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 22:09:26 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1721e585ff7394a90749cf70f35830f448534661f41eb945960585b2fd5d0b1`  
		Last Modified: Wed, 15 Apr 2026 20:34:51 GMT  
		Size: 9.5 MB (9468125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1f8d58c780fffee51756ee51526a6329798791dc37276a7f10128a26a66a6b`  
		Last Modified: Wed, 15 Apr 2026 20:34:53 GMT  
		Size: 60.9 MB (60914745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d01df8ebfebd818effaec3310e5faee3b390a936d6670702afb6c5f1c87e4e6`  
		Last Modified: Wed, 15 Apr 2026 20:34:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd11c3578ad86b8955bafd222fdd1765fdde6d844fdd5900c668bd796af3ac26`  
		Last Modified: Wed, 15 Apr 2026 20:34:51 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef3806a8b5ae60b4053a060da0ac1ef7977ab495c19bd5b8ba6d9f1c10e677d`  
		Last Modified: Wed, 15 Apr 2026 22:09:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4440655332f06389ad9f115d1d2819d80fdc31b5ccf0c3ad651bb93ca6cf4715`  
		Last Modified: Wed, 15 Apr 2026 22:09:37 GMT  
		Size: 7.1 MB (7147160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2ce2a342d3305b3da90bb93fe379ffeebcaa8282ed6354eed7a0b98760881e`  
		Last Modified: Wed, 15 Apr 2026 22:09:37 GMT  
		Size: 75.7 KB (75650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d97e38c9623d798b06439802a3c204164f9b801e879aaee4beffdf0e0bcd028`  
		Last Modified: Wed, 15 Apr 2026 22:09:40 GMT  
		Size: 70.5 MB (70506990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre25-alpine` - unknown; unknown

```console
$ docker pull tomee@sha256:f4892c4bb086b30c84e9b0019b12f58198e502f4c0ab50202c997c81cdbcee29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba51c2bd1e13e5007ea1855f6c6d15ef49de5a59f9656607bc2ebb21db386bf4`

```dockerfile
```

-	Layers:
	-	`sha256:b6f682d74216dc2495fdd998290007b87967552029e77fc5ec49f13ecb1e7c30`  
		Last Modified: Wed, 15 Apr 2026 22:09:37 GMT  
		Size: 1.3 MB (1292387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5d800ad71611ccf337ce294c0e342741cc88b893234d81a98667aba3f91532b`  
		Last Modified: Wed, 15 Apr 2026 22:09:37 GMT  
		Size: 36.0 KB (35960 bytes)  
		MIME: application/vnd.in-toto+json
