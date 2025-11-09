## `tomee:10-jre25-alpine-plus`

```console
$ docker pull tomee@sha256:bc99345ee09fe0b61d0de0a9be174ae30b1f15ca9240d17c620b5dde77b1b0d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:10-jre25-alpine-plus` - linux; amd64

```console
$ docker pull tomee@sha256:4300c57072ecfaf84a698113b67e370cdf6d207efb74d795625e12757a0d2f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157206562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e35331ae96109d8175c9393fcc867d0b75525484138ac50a2d3c0d569677ab9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 18:00:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:00:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:00:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:00:13 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 18:00:13 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 18:00:17 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='0176d4b18047ce6669c451e7293998961340a6720e979adfbfefb7356d21d597';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='46a7eca285957dadb0adacd96fe385bc5512f31b7f90a3dd01f04679d614a420';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Sat, 08 Nov 2025 18:00:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:00:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:00:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:38:32 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:38:32 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Sat, 08 Nov 2025 18:38:32 GMT
WORKDIR /usr/local/tomee
# Sat, 08 Nov 2025 18:38:33 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 18:38:43 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Sat, 08 Nov 2025 18:38:43 GMT
ENV TOMEE_VER=10.1.2
# Sat, 08 Nov 2025 18:38:43 GMT
ENV TOMEE_BUILD=plus
# Sat, 08 Nov 2025 18:38:44 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Sat, 08 Nov 2025 18:38:44 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 18:38:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbcbae383f82b131ce42d8dc9b73fce3ce6ef71ecb2d442f81c471da9477a28`  
		Last Modified: Sat, 08 Nov 2025 18:00:42 GMT  
		Size: 9.4 MB (9420506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8fdcab0dbb3c270d5f132aa2b7b2fa239dc548c6b6f3e403ccc5b22d8acb16`  
		Last Modified: Sat, 08 Nov 2025 18:00:44 GMT  
		Size: 62.0 MB (61974359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb469893871c044c8c730e2ab82cb428649adc3a9b3caaf47e54088fe98a4287`  
		Last Modified: Sat, 08 Nov 2025 18:00:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef1eda8b4815c38b023afce7b53d10407da1dacf82e780a961edf24c2dc33a5`  
		Last Modified: Sat, 08 Nov 2025 18:00:42 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b468156a6e9fdaa0e766eabb1467a1d129ec172411f3770b5e80b7c9844c25b5`  
		Last Modified: Sat, 08 Nov 2025 18:39:02 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0e1fa08eeb742103816abbb962fd25e99d7dc710bd80bc3f7e18b6a7849283`  
		Last Modified: Sat, 08 Nov 2025 18:39:03 GMT  
		Size: 7.0 MB (6992212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14daffdb864fdbf4a1a609ca533fc362f32e9f4b26b3213a6150e7dbcb7ee15`  
		Last Modified: Sat, 08 Nov 2025 18:39:00 GMT  
		Size: 75.7 KB (75655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ccec08f5214f6411ad8d336cd0b2afc99b243737b86c197527490ee0dac094`  
		Last Modified: Sat, 08 Nov 2025 18:39:07 GMT  
		Size: 74.9 MB (74938768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre25-alpine-plus` - unknown; unknown

```console
$ docker pull tomee@sha256:245cb7d71fecc0cade99968eee97a1d210c320b0234443214689158077a64f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1327760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25916429b2553e9df3304eb97000533d5963914f6ad21b3c807db8274d929bc`

```dockerfile
```

-	Layers:
	-	`sha256:05d501f36cddefd87010af2b41cc9fbfbc69567571d065283066e9e9fcbf673c`  
		Last Modified: Sat, 08 Nov 2025 20:24:36 GMT  
		Size: 1.3 MB (1297661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1377126d066700e94e23fb5a5726946304ecd5f3d854222b2ca5be6fc5bdb8ba`  
		Last Modified: Sat, 08 Nov 2025 20:24:37 GMT  
		Size: 30.1 KB (30099 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:10-jre25-alpine-plus` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:b1b126e2533173142533dea4de3e1367335df8feee4480d2afe8a905c310ef1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156384251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ae96614d237690101627bed64e0344081309ebe7b59c71541c39149c14a559`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:59:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:41 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:59:41 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 17:59:46 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='0176d4b18047ce6669c451e7293998961340a6720e979adfbfefb7356d21d597';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='46a7eca285957dadb0adacd96fe385bc5512f31b7f90a3dd01f04679d614a420';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Sat, 08 Nov 2025 17:59:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:38:10 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:38:10 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Sat, 08 Nov 2025 18:38:10 GMT
WORKDIR /usr/local/tomee
# Sat, 08 Nov 2025 18:38:11 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 18:38:21 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Sat, 08 Nov 2025 18:38:21 GMT
ENV TOMEE_VER=10.1.2
# Sat, 08 Nov 2025 18:38:21 GMT
ENV TOMEE_BUILD=plus
# Sat, 08 Nov 2025 18:38:23 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Sat, 08 Nov 2025 18:38:23 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 18:38:23 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5127811969c579c88a5357f4c5ad4c0537c80196c8d07ca805a145e533f893`  
		Last Modified: Sat, 08 Nov 2025 18:00:12 GMT  
		Size: 9.4 MB (9434836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bc56f5f939c88857f334409c355cf3185ef0cbd05a7a61f1b881382cba6407`  
		Last Modified: Sat, 08 Nov 2025 18:00:17 GMT  
		Size: 60.9 MB (60874383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d0239c7adb35ba880d05476593f6ebb6cc3334a5b2eb699d5e57bc5adb48b5`  
		Last Modified: Sat, 08 Nov 2025 18:00:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c966286306a34f2c98201f4736e4e54df9947a253cdd5cdbc3ea820a2cd51624`  
		Last Modified: Sat, 08 Nov 2025 18:00:18 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7b41b86e489df41375043a11717a70573d60a3881a076f478e30e63328ab08`  
		Last Modified: Sat, 08 Nov 2025 18:38:41 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2545b2e763ca0385ef0cd8567a90e877fa5ae0f61d8e32c93d1f7180b39b792`  
		Last Modified: Sat, 08 Nov 2025 18:38:41 GMT  
		Size: 6.9 MB (6920007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5117417ecbb3ad76d0313fc84cb164c5496874cb241f31b840537cd7fd76431c`  
		Last Modified: Sat, 08 Nov 2025 18:38:41 GMT  
		Size: 75.6 KB (75649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8d60a95af6289a1015da3c6131d07b6cb913d174a37b9c40f2e35796ec99c6`  
		Last Modified: Sat, 08 Nov 2025 18:38:46 GMT  
		Size: 74.9 MB (74938699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre25-alpine-plus` - unknown; unknown

```console
$ docker pull tomee@sha256:7319eef67fb99b51b047e4b970ec55ee83705d5f435977430e74df145091c58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1327631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89708f2e779c8ae901afcd69b54d9edf91094387f7bb68da95ae513d6d85450d`

```dockerfile
```

-	Layers:
	-	`sha256:aaf86de952242e6acd1f8b9014377b28307fe5a4486ce9ef1c6ca547292a9faf`  
		Last Modified: Sat, 08 Nov 2025 20:11:56 GMT  
		Size: 1.3 MB (1297240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af1b12d49abe6e680b42498c4ae22e8e42406c7abc4bc8e8c28e597cb1d72a43`  
		Last Modified: Sat, 08 Nov 2025 20:11:56 GMT  
		Size: 30.4 KB (30391 bytes)  
		MIME: application/vnd.in-toto+json
