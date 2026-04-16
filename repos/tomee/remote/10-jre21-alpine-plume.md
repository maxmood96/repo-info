## `tomee:10-jre21-alpine-plume`

```console
$ docker pull tomee@sha256:3df2f677e829b5bd2a0f37db21149cbc8d6b66ca49c0b955145ad97bb0c826f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:10-jre21-alpine-plume` - linux; amd64

```console
$ docker pull tomee@sha256:4ab3c1320b370549a59431a34803635547ea7c3ec11bbef8bbad896740df5722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (157975620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361910fabb88a4c34f912aee9e4cba1765f271b4735170c08278767e520b80c7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:31:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:31:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:31:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:31:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:31:59 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:33:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='d1cd7b33dcd81293b0b705f4d0e79adce092786be31736a63abe6a4b31841ae5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='4f6200277644afe6ad49218ae1dd45ab3d0d0b2ac4109163604e36156a93a306';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 15 Apr 2026 20:33:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:57:40 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:57:40 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Wed, 15 Apr 2026 21:57:41 GMT
WORKDIR /usr/local/tomee
# Wed, 15 Apr 2026 21:57:41 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl  && rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 21:57:50 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 15 Apr 2026 21:57:50 GMT
ENV TOMEE_VER=10.1.4
# Wed, 15 Apr 2026 21:57:50 GMT
ENV TOMEE_BUILD=plume
# Wed, 15 Apr 2026 21:57:52 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Wed, 15 Apr 2026 21:57:52 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 21:57:52 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775c53a23a895a8fdcb2534de50a64b420d676e982f81a1e72e88f6b283280fe`  
		Last Modified: Wed, 15 Apr 2026 20:32:15 GMT  
		Size: 16.8 MB (16837772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cc7558c41737fe273044d032b589323a9acd96790bbfd6cf2792647fb88e3b`  
		Last Modified: Wed, 15 Apr 2026 20:34:11 GMT  
		Size: 53.2 MB (53168753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7659027a798a9c8fca5bfcbae2d24bd6b7ec65dfe5285d4b7c30c75ca0965299`  
		Last Modified: Wed, 15 Apr 2026 20:34:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e51247e7df3167f00ff9972116a308eb551b96eac8382fbf88e82d5866971c`  
		Last Modified: Wed, 15 Apr 2026 20:34:09 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d362547df80b3f915474957a00e45d47dc7884d9b646fee9e762c497647812d`  
		Last Modified: Wed, 15 Apr 2026 21:58:02 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0617816e1b9c49dde3d9ca9a772792826e1bc2fa0010f0af9fb808627a80f58c`  
		Last Modified: Wed, 15 Apr 2026 21:58:02 GMT  
		Size: 888.1 KB (888071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02c8cc42aa94c4ec50451fe4ec48bcda24fecc12952e091c14fd2e6cb02fd2b`  
		Last Modified: Wed, 15 Apr 2026 21:58:02 GMT  
		Size: 75.6 KB (75636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c195c3c89744ac1181d1b86b62394ec14f486e93e1a4161034cc9771780fb9`  
		Last Modified: Wed, 15 Apr 2026 21:58:05 GMT  
		Size: 83.1 MB (83138587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre21-alpine-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:ebec5d87bc3446b3e5ca553cf27eb2ba06beab1946253df714ab2a867f5abaad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1354187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eeebda95f9fb90d0e218802e8d5ababf1feb0bed919b7ecd48e2d70a79f5647`

```dockerfile
```

-	Layers:
	-	`sha256:c77d3473a18b7bac90df09ee749003a29812376efbd0288de8492f97f0bb0db4`  
		Last Modified: Wed, 15 Apr 2026 21:58:02 GMT  
		Size: 1.3 MB (1326635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e00ad9c3b7e601c30a4e57167afdb30ca5e97202955c4a88f44e8eb506ba41f`  
		Last Modified: Wed, 15 Apr 2026 21:58:02 GMT  
		Size: 27.6 KB (27552 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:10-jre21-alpine-plume` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:65b503f78a16964d760cbf26c918341d290f3ddd10f26fff832261979c13f091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157340918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e98a12e10576858ddd93ab7b7eb31838379b01d1576e997588b44ab4759b597`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:34:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:03 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:34:03 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='d1cd7b33dcd81293b0b705f4d0e79adce092786be31736a63abe6a4b31841ae5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='4f6200277644afe6ad49218ae1dd45ab3d0d0b2ac4109163604e36156a93a306';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 15 Apr 2026 20:34:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:10:11 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:10:11 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Wed, 15 Apr 2026 22:10:11 GMT
WORKDIR /usr/local/tomee
# Wed, 15 Apr 2026 22:10:11 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl  && rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 22:10:21 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 15 Apr 2026 22:10:21 GMT
ENV TOMEE_VER=10.1.4
# Wed, 15 Apr 2026 22:10:21 GMT
ENV TOMEE_BUILD=plume
# Wed, 15 Apr 2026 22:10:23 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Wed, 15 Apr 2026 22:10:23 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 22:10:23 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ba8975f2870c67c471d5113538544d9738d4c24aa8d200334a8fdd33c2c8ab`  
		Last Modified: Wed, 15 Apr 2026 20:34:19 GMT  
		Size: 16.8 MB (16790279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572f4b22c15a1b48cdc98060318acd16ca95081af867ffb543dd069be0e86069`  
		Last Modified: Wed, 15 Apr 2026 20:34:19 GMT  
		Size: 52.2 MB (52240618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ff9bb4a5044737f5128b66c4d3157b01c64eb7119b6e48349f990918ded98b`  
		Last Modified: Wed, 15 Apr 2026 20:34:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1c2c760a3821e387ba9de59684b82e9c346c8cf115a56a9f2399b2b0ab3512`  
		Last Modified: Wed, 15 Apr 2026 20:34:18 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6ecd81dbcf89c1bb235ecd556efc7bc8ceaf17ee9eba5b265389568884b738`  
		Last Modified: Wed, 15 Apr 2026 22:10:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b35038ba5ed865a369c3a51364522f21e4257d2f5416438c688ff5569797a6`  
		Last Modified: Wed, 15 Apr 2026 22:10:33 GMT  
		Size: 893.4 KB (893359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac26ceea47d110232058b5b886e5de5cc8048e53b7f78b7c44af51a35a0fd955`  
		Last Modified: Wed, 15 Apr 2026 22:10:33 GMT  
		Size: 75.6 KB (75630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec08acc5a97f2454c050bf0b4d4b70b9ffcc26bc3a232750f23558985f96d88e`  
		Last Modified: Wed, 15 Apr 2026 22:10:36 GMT  
		Size: 83.1 MB (83138552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre21-alpine-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:b9b4b00214eff08eb4e01c73a7e3c6e67f1f3afe7c8b57ac6c8721d9c2dabffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1353220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13c8eb9fa37afdad5f21bc460aab4b73da91c5900984e9656274cc92322c2c7`

```dockerfile
```

-	Layers:
	-	`sha256:d85d618a472e25661f7d7935935adbbb9a0fadd169b51cb36c7222d44bfae691`  
		Last Modified: Wed, 15 Apr 2026 22:10:33 GMT  
		Size: 1.3 MB (1325471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b80dc1030647ed8236d441e2b4d0bc0ea19a3747a85cfe885ce462d86649c787`  
		Last Modified: Wed, 15 Apr 2026 22:10:33 GMT  
		Size: 27.7 KB (27749 bytes)  
		MIME: application/vnd.in-toto+json
