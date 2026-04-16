## `tomee:10-Temurin-alpine-plume`

```console
$ docker pull tomee@sha256:c292bb53bdc65b6f030bd36e9c6816018e4434c806801d447b711d6b0a3f8208
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:10-Temurin-alpine-plume` - linux; amd64

```console
$ docker pull tomee@sha256:43067a0ca9ffda23c519f64f6b12d05e748b43f19cdbdfa0abb0c8ab4c41e202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165746208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be25243d3a318dfce9707965d869d745fe26ef70ed89a93c0c6018be558dd071`
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
# Wed, 15 Apr 2026 21:57:08 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:57:08 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Wed, 15 Apr 2026 21:57:08 GMT
WORKDIR /usr/local/tomee
# Wed, 15 Apr 2026 21:57:09 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl  && rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 21:57:18 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 15 Apr 2026 21:57:18 GMT
ENV TOMEE_VER=10.1.4
# Wed, 15 Apr 2026 21:57:18 GMT
ENV TOMEE_BUILD=plume
# Wed, 15 Apr 2026 21:57:20 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Wed, 15 Apr 2026 21:57:20 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 21:57:20 GMT
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
	-	`sha256:d422aa0f64d9951aee7c1f7a95776232fe346021d535d14bbfc8417a75f349a4`  
		Last Modified: Wed, 15 Apr 2026 21:57:30 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a435361a659183cbb89aaa366249c5625de2217f880bf2d95b378ef27791a5be`  
		Last Modified: Wed, 15 Apr 2026 21:57:30 GMT  
		Size: 7.2 MB (7238029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3173986a55227c8cf955fee84ac002f7a79e4652ecf9e3970e1a749315eca406`  
		Last Modified: Wed, 15 Apr 2026 21:57:30 GMT  
		Size: 75.6 KB (75630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e1a55c9ae16bc82b00545c5e8eaa0d3c295187cefb5a1c6b88ea76eb6a3292`  
		Last Modified: Wed, 15 Apr 2026 21:57:32 GMT  
		Size: 83.1 MB (83138698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-Temurin-alpine-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:ae99789f3ccef7e416a695ccbd8f701b4155c4461718aa50d00cc13d6e10217a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1347373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650bbeedf3266d22c6575088225db5c72d12de61eeba4567b26b054d7c3fcc18`

```dockerfile
```

-	Layers:
	-	`sha256:f8e743f57d73fe4a00affb5894a7f2ac076743a5c145218bcbab2f138234fb13`  
		Last Modified: Wed, 15 Apr 2026 21:57:30 GMT  
		Size: 1.3 MB (1317236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26783af1725556a737a7d9be32a3160a80c119dd1a19db10731216f0d6d08a41`  
		Last Modified: Wed, 15 Apr 2026 21:57:30 GMT  
		Size: 30.1 KB (30137 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:10-Temurin-alpine-plume` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:9be8b1c827210e0c324034d286cdfdc0317e0d2dad383be905660e7b1a6a407d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.9 MB (164946745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6ed5a7c0c6432a34c4d9a43a2a67366a345f439849d8e51242aabb5bf6c923`
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
# Wed, 15 Apr 2026 22:09:05 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:09:05 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Wed, 15 Apr 2026 22:09:05 GMT
WORKDIR /usr/local/tomee
# Wed, 15 Apr 2026 22:09:05 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl  && rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 22:09:15 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 15 Apr 2026 22:09:15 GMT
ENV TOMEE_VER=10.1.4
# Wed, 15 Apr 2026 22:09:15 GMT
ENV TOMEE_BUILD=plume
# Wed, 15 Apr 2026 22:09:18 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Wed, 15 Apr 2026 22:09:18 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 22:09:18 GMT
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
	-	`sha256:6f78b5fe9dc63964ef4bc4ab3c4c5a086048158e1b42bfc7e59dddfa805e852b`  
		Last Modified: Wed, 15 Apr 2026 22:09:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6b925ec8eab0b98af5e01019ce3e33871c266cae3501d382c1504b8369af87`  
		Last Modified: Wed, 15 Apr 2026 22:09:28 GMT  
		Size: 7.1 MB (7147184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c298c8d2c80a3d97b842e48dab9c7cfacfcf61319351811d3079f6d202d36d5`  
		Last Modified: Wed, 15 Apr 2026 22:09:28 GMT  
		Size: 75.6 KB (75649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc4372f8f42f950f19ca99933ad4039f25b72aade7ddf8c128ebd23685d5fab`  
		Last Modified: Wed, 15 Apr 2026 22:09:30 GMT  
		Size: 83.1 MB (83138561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-Temurin-alpine-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:b60376899179b44296f98341848f8afc672108c2d044b75a4031ea86923dbebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1346595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628a6bac03699c28c3f1992990705a7807607cbc0778b6ea8d0941600c05bc4f`

```dockerfile
```

-	Layers:
	-	`sha256:8ad5205d07526cc32117cbc3eb98f5c4ff695d9302ce40f71dc8da6b05df507a`  
		Last Modified: Wed, 15 Apr 2026 22:09:28 GMT  
		Size: 1.3 MB (1316165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:745d7bda88b9fc3376c4a3a9adec3deaf6dace07d916b9dfa12273cf988a5b8a`  
		Last Modified: Wed, 15 Apr 2026 22:09:27 GMT  
		Size: 30.4 KB (30430 bytes)  
		MIME: application/vnd.in-toto+json
