## `tomee:11-jre25-alpine-plus`

```console
$ docker pull tomee@sha256:9687a372e3018e8c50c1c4a92da8026382059b8b92763edb687a9c8102a481f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:11-jre25-alpine-plus` - linux; amd64

```console
$ docker pull tomee@sha256:ff65aec54781f3e7635fd8ed12610be40ec1a3b205e0d545ebfb51072deb440f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159286381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856233ac7bddfd540ca3e65b989ee253d058815c4b77994e9565236aef4793f1`
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
# Thu, 18 Jun 2026 20:43:51 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jun 2026 20:43:51 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Thu, 18 Jun 2026 20:43:51 GMT
WORKDIR /usr/local/tomee
# Thu, 18 Jun 2026 20:43:52 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Thu, 18 Jun 2026 20:44:02 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Thu, 18 Jun 2026 20:44:02 GMT
ENV TOMEE_VER=11.0.0-M1
# Thu, 18 Jun 2026 20:44:02 GMT
ENV TOMEE_BUILD=plus
# Thu, 18 Jun 2026 20:44:03 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Thu, 18 Jun 2026 20:44:03 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 18 Jun 2026 20:44:03 GMT
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
	-	`sha256:152ff53521e44fdbb367f6f840f2d52c7b9b07453985d68a0e9f9e34e76bea44`  
		Last Modified: Thu, 18 Jun 2026 20:44:13 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348b97131c35a36e080cd70c5c9899ed79cc99f0643d8551f3e47941e6538b80`  
		Last Modified: Thu, 18 Jun 2026 20:44:14 GMT  
		Size: 7.2 MB (7184508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf84f87d63f43f67400365acb90664980da8f290c49f6f42c40f6773438cc0ca`  
		Last Modified: Thu, 18 Jun 2026 20:44:13 GMT  
		Size: 75.6 KB (75626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1164e1ee50f3053027294520289939b8dd058edc4155092bf772c42a94e3c320`  
		Last Modified: Thu, 18 Jun 2026 20:44:15 GMT  
		Size: 76.6 MB (76601953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:11-jre25-alpine-plus` - unknown; unknown

```console
$ docker pull tomee@sha256:ae990364e77f1c952c3f5363137d804ad4cbb6464d5890eee06d79e349e2d4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1315406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683d6a1a1b0a862208911106c1b4acc5bf55d74f7ef358145757a5bf246662c4`

```dockerfile
```

-	Layers:
	-	`sha256:ff5328150dce9076e9c834a9716b82a2b28cfa8c933a77f924f8098fe8dfda82`  
		Last Modified: Thu, 18 Jun 2026 20:44:13 GMT  
		Size: 1.3 MB (1286556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:335885f6928da23b44c448896f43305c4ba0ad8701e1d1721a57bab22ef93840`  
		Last Modified: Thu, 18 Jun 2026 20:44:13 GMT  
		Size: 28.9 KB (28850 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:11-jre25-alpine-plus` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:2a94223a93cf719bc8eb735239c624ef9c426a47ae9880917bef0f97f4f2ac6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158488801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b526096e036339eed578ecd224414c8558c7a7c3399deb0303aba69c39bf83ab`
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
# Thu, 18 Jun 2026 20:43:52 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jun 2026 20:43:52 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Thu, 18 Jun 2026 20:43:52 GMT
WORKDIR /usr/local/tomee
# Thu, 18 Jun 2026 20:43:53 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Thu, 18 Jun 2026 20:44:02 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Thu, 18 Jun 2026 20:44:02 GMT
ENV TOMEE_VER=11.0.0-M1
# Thu, 18 Jun 2026 20:44:02 GMT
ENV TOMEE_BUILD=plus
# Thu, 18 Jun 2026 20:44:04 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Thu, 18 Jun 2026 20:44:04 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 18 Jun 2026 20:44:04 GMT
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
	-	`sha256:8c8c9ac6b25a9755e8f16de310564617b80f4b10d9ecb15c8e181ce20300303c`  
		Last Modified: Thu, 18 Jun 2026 20:44:14 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3ae4ec9a7e3f75877b3c437830a0c18338f7be5ce450b8279271d17d323b75`  
		Last Modified: Thu, 18 Jun 2026 20:44:15 GMT  
		Size: 7.1 MB (7091377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65571645106544aefd379faf56d16514988c4d181a9504e8ff696068a09c7833`  
		Last Modified: Thu, 18 Jun 2026 20:44:15 GMT  
		Size: 75.6 KB (75632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b1584efa737be1e2f4e5055fe77eeb570e66f383559a6a1c9f2c5c37ef0b0d`  
		Last Modified: Thu, 18 Jun 2026 20:44:16 GMT  
		Size: 76.6 MB (76601953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:11-jre25-alpine-plus` - unknown; unknown

```console
$ docker pull tomee@sha256:1fcc1cc1d2d693df357f2ce8714240a372bd5c96e429d5d8a11ed1bf3e8257c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1314532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c17961e9d87bacf9cae7327f2e2ca841ebeff57b9e9d1bc42c01d81418f9148`

```dockerfile
```

-	Layers:
	-	`sha256:43003dc4022d32e905cfa7a7247f74685efdba875da51bae7e44693a701e0389`  
		Last Modified: Thu, 18 Jun 2026 20:44:14 GMT  
		Size: 1.3 MB (1285437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2164b1432cef49bf92dc768cd7c1875c8cfa0c002108eda2f92bb536dc460bc`  
		Last Modified: Thu, 18 Jun 2026 20:44:14 GMT  
		Size: 29.1 KB (29095 bytes)  
		MIME: application/vnd.in-toto+json
