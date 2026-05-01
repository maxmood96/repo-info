## `tomee:10-jre25-alpine-plume`

```console
$ docker pull tomee@sha256:81fc524010bca4529ad585209393f3e77ad62324ec4183f2d9505c0ae35c751b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:10-jre25-alpine-plume` - linux; amd64

```console
$ docker pull tomee@sha256:45049567550b1f28ff6815d62837aff6668c31f64e43ce03210af40c0c59b6db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165876442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b280e63a8dd46b20c05b1d79872414e8fe30f184904c86135744cb5bf52db6`
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
# Thu, 30 Apr 2026 23:52:35 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:52:35 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Thu, 30 Apr 2026 23:52:35 GMT
WORKDIR /usr/local/tomee
# Thu, 30 Apr 2026 23:52:36 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl  && rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Apr 2026 23:52:45 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Thu, 30 Apr 2026 23:52:45 GMT
ENV TOMEE_VER=10.1.4
# Thu, 30 Apr 2026 23:52:45 GMT
ENV TOMEE_BUILD=plume
# Thu, 30 Apr 2026 23:52:47 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Thu, 30 Apr 2026 23:52:47 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 30 Apr 2026 23:52:47 GMT
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
	-	`sha256:e89d0f026093729dd3a900eaacf784a675a777ab6bc70a0f9de64979d904319a`  
		Last Modified: Thu, 30 Apr 2026 23:52:54 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d062c0662f0d217851cded8f8cb8585281adabc830a49c494d16db5031bf3f`  
		Last Modified: Thu, 30 Apr 2026 23:52:57 GMT  
		Size: 7.2 MB (7237985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef193c4a62568e53ae8d96a5d113d3aeba9e9e2bafb703b88b5f291ebfb13a7`  
		Last Modified: Thu, 30 Apr 2026 23:52:57 GMT  
		Size: 75.6 KB (75629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0665a1153eb61dce69e1a0833b748dc5248014ad243fcfe5d171af91a0c4582`  
		Last Modified: Thu, 30 Apr 2026 23:52:59 GMT  
		Size: 83.1 MB (83138538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre25-alpine-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:3af39ce0c71faf542082a86d2572754e7ae3b851614096cea19ab83d953d320d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1347991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db373dcf5c075bb555b1c2ffc35370070b066f8a848e3b0cb2dc5ddd61973aaa`

```dockerfile
```

-	Layers:
	-	`sha256:82392db0a5a5271c447f1e91478ceab401e19fdeb9dbbc5b1c8ece0e6de842f3`  
		Last Modified: Thu, 30 Apr 2026 23:52:57 GMT  
		Size: 1.3 MB (1317859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66446a2d184feb3d1da4961adc47e541fa6aafb80dc22657c190636828f24a00`  
		Last Modified: Thu, 30 Apr 2026 23:52:57 GMT  
		Size: 30.1 KB (30132 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:10-jre25-alpine-plume` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:d76702a9ce0301652adeae5807a8333c7620ebaf23a6c662757201d32e19f8ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.1 MB (165081810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3231080326c7e653ceb64727e42688271e08e3a4aca4531714429e4c2e4e8b0`
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
RUN apk add --no-cache gpg gpg-agent dirmngr curl  && rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Apr 2026 23:52:08 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Thu, 30 Apr 2026 23:52:08 GMT
ENV TOMEE_VER=10.1.4
# Thu, 30 Apr 2026 23:52:08 GMT
ENV TOMEE_BUILD=plume
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
	-	`sha256:8e6072ea2593703691baf53a298ce84df26333ef7493e281a12427e5c4f9e420`  
		Last Modified: Thu, 30 Apr 2026 23:52:20 GMT  
		Size: 7.1 MB (7147726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0578b711f5cfe38bb8cbebee70f9377937f5bbe75ddbef0eeff0d6af08f8c241`  
		Last Modified: Thu, 30 Apr 2026 23:52:20 GMT  
		Size: 75.7 KB (75666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e03edfaf844c9ac5e8867bf5ea18697bfa3f6ac711f2603e3dd1367e3ae786`  
		Last Modified: Thu, 30 Apr 2026 23:52:23 GMT  
		Size: 83.1 MB (83138583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre25-alpine-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:d8b12b16f05d3686d72b53a0dcaf648265c7cc591b28f1afeac64ba354f16510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1347214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98596c82d20b577627859c6b147a0b181b632bf81b7efa69b6d536d60543ebf2`

```dockerfile
```

-	Layers:
	-	`sha256:e359e32a7b8a1d4fbccef0bd6e023dab2ae84f08654f9b70a52272d81df171e4`  
		Last Modified: Thu, 30 Apr 2026 23:52:20 GMT  
		Size: 1.3 MB (1316788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:941b125dbb91a50937e9b52651de80f0274362d3e9928d40a2e66643ac9152ef`  
		Last Modified: Thu, 30 Apr 2026 23:52:20 GMT  
		Size: 30.4 KB (30426 bytes)  
		MIME: application/vnd.in-toto+json
