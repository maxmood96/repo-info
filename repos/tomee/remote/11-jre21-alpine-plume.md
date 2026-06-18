## `tomee:11-jre21-alpine-plume`

```console
$ docker pull tomee@sha256:af1eb658e7a869cb25b2a70a4f20d744c2fe889d3afab6f879b94f8ba844872a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:11-jre21-alpine-plume` - linux; amd64

```console
$ docker pull tomee@sha256:bd677872499669f195ebfc5270f61af5cc0783a12fd9e0a3c5a55ae50421c627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159828386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb706e1650a4494b784af60d6d7bb7891da6e794d5475d61f94308fcdcbd2cd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 00:00:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:00:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:00:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:00:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 08 May 2026 00:00:05 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:00:11 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='33399db5fb4f542df36a706d6642a3ba1fab3d247da707273a11ef29e39f0705';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='b75c9f0dd052adfd213f0c2c1cc0c8a6d4539a8de9f7947d2b8fc45d18289975';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 08 May 2026 00:00:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:00:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:00:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Jun 2026 20:44:37 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jun 2026 20:44:37 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Thu, 18 Jun 2026 20:44:37 GMT
WORKDIR /usr/local/tomee
# Thu, 18 Jun 2026 20:44:37 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl  && rm -rf /var/cache/apk/* # buildkit
# Thu, 18 Jun 2026 20:44:47 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Thu, 18 Jun 2026 20:44:47 GMT
ENV TOMEE_VER=11.0.0-M1
# Thu, 18 Jun 2026 20:44:47 GMT
ENV TOMEE_BUILD=plume
# Thu, 18 Jun 2026 20:44:49 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Thu, 18 Jun 2026 20:44:49 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 18 Jun 2026 20:44:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef4bf1bda3522f6b64c24ee154ed6739c8ab26c1be19e7b9e564bf0f39cbf22`  
		Last Modified: Fri, 08 May 2026 00:00:23 GMT  
		Size: 16.9 MB (16857117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e338134b21e530c8c101d288f216594c45a122a53f0d095568b2d0e943d8fec`  
		Last Modified: Fri, 08 May 2026 00:00:24 GMT  
		Size: 53.3 MB (53301871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42516208460b63f47d0044aef98b70571ce7765cc9108b0a3d14ae7fa16d7566`  
		Last Modified: Fri, 08 May 2026 00:00:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1a277377d10ae29a58277bdefa13f3a1cfffb295a5b7bce5ad0b0d82661629`  
		Last Modified: Fri, 08 May 2026 00:00:22 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110d45ddffcb3daa0ceff320a73b642df3030bfd131674bb4cd9a494c28a530e`  
		Last Modified: Thu, 18 Jun 2026 20:44:58 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d688f3b2fdf1ad2c6fc3e203415ad5ca0100ca4a9c4f38f34760f80f9a1367`  
		Last Modified: Thu, 18 Jun 2026 20:44:59 GMT  
		Size: 809.3 KB (809348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2224855f99be89e47e5b78fe66d5b333c371499239380a40c44bfd37cc19a208`  
		Last Modified: Thu, 18 Jun 2026 20:44:59 GMT  
		Size: 75.7 KB (75651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea67587165c885ad130f7e2588fc5eacdf9f1cdda334b0676e93a40f2610f308`  
		Last Modified: Thu, 18 Jun 2026 20:45:01 GMT  
		Size: 84.9 MB (84917596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:11-jre21-alpine-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:185d7970d02410138050d809e645686255be800cefbc2398440bec7d2204eaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1345865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d2ddb8369a4912754ef87fc8d7c14214aa5066694b8c1dda9a071731c01b79`

```dockerfile
```

-	Layers:
	-	`sha256:193e45fc3d1dc7aa917181291cec78066464c16c2cb58b766f8429b000baf85e`  
		Last Modified: Thu, 18 Jun 2026 20:44:59 GMT  
		Size: 1.3 MB (1318946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:401ea0bed862aee48913448b194681ac27e882c8ef53638c96771f1f78e7190a`  
		Last Modified: Thu, 18 Jun 2026 20:44:58 GMT  
		Size: 26.9 KB (26919 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:11-jre21-alpine-plume` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:f167583041e04af045d004e03a6d744b8738d3a0a47c9a48467ba873aad06b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159186211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f463cbd4cf04ffa69b3fc2b34366cf5a322d6e2f225e12d7f4697da68b0eba`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 23:59:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:59:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:59:20 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 07 May 2026 23:59:20 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Thu, 07 May 2026 23:59:24 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='33399db5fb4f542df36a706d6642a3ba1fab3d247da707273a11ef29e39f0705';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='b75c9f0dd052adfd213f0c2c1cc0c8a6d4539a8de9f7947d2b8fc45d18289975';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 07 May 2026 23:59:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:59:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:59:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Jun 2026 20:44:32 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jun 2026 20:44:32 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Thu, 18 Jun 2026 20:44:32 GMT
WORKDIR /usr/local/tomee
# Thu, 18 Jun 2026 20:44:32 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl  && rm -rf /var/cache/apk/* # buildkit
# Thu, 18 Jun 2026 20:44:42 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Thu, 18 Jun 2026 20:44:42 GMT
ENV TOMEE_VER=11.0.0-M1
# Thu, 18 Jun 2026 20:44:42 GMT
ENV TOMEE_BUILD=plume
# Thu, 18 Jun 2026 20:44:44 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Thu, 18 Jun 2026 20:44:44 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 18 Jun 2026 20:44:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf450a430f283e30e1c40224be86cafae4f423e0521eb9ba2e8799bef6b81f96`  
		Last Modified: Thu, 07 May 2026 23:59:36 GMT  
		Size: 16.8 MB (16808915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4bddb7f46e4f78e2ad4312982140fa4df3f2fabe062b83836c8fb58e949ccc`  
		Last Modified: Thu, 07 May 2026 23:59:37 GMT  
		Size: 52.4 MB (52367876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff48e0031f1e3b1efe1e77813f0dafa06ee81a76c884d23e8a2bfd5113592585`  
		Last Modified: Thu, 07 May 2026 23:59:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab8d09dd6da961016c94e5c1d602e23b7d50b9cf3de06d915601c48c4ac160a`  
		Last Modified: Thu, 07 May 2026 23:59:35 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18be47dd23171efe17263724959abe93c998d5b8d34cb316bcdab7423ddc5aa9`  
		Last Modified: Thu, 18 Jun 2026 20:44:54 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69a8c7ae2155ea04106f22299b3de396321c98b251856d713e541292f4a1b1`  
		Last Modified: Thu, 18 Jun 2026 20:44:54 GMT  
		Size: 813.7 KB (813672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e0502780279339042bf5e78bf545cb11ad402e2f5a388967f2600c84c4b34e`  
		Last Modified: Thu, 18 Jun 2026 20:44:54 GMT  
		Size: 75.6 KB (75642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71aebb2989a2177c4fd30c827cd8b6862a7eed17359ec189204e3918fadfcfac`  
		Last Modified: Thu, 18 Jun 2026 20:44:56 GMT  
		Size: 84.9 MB (84917624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:11-jre21-alpine-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:c9905379a0b980b6b11ade66120e417c3e4fdc94aab97a6a06b495b258898fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1344850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d269f44de0c19494e3f460e9a69ab99e75eaa2ff04f359efa2bc13fb368353`

```dockerfile
```

-	Layers:
	-	`sha256:9aab003eedf83640d42a82bf9df33d3ca23d6cbd5e83bcb830824e6425fc4c8c`  
		Last Modified: Thu, 18 Jun 2026 20:44:54 GMT  
		Size: 1.3 MB (1317758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d8637c60b0b80c6b6d823e341644ba436bb9698fa10c51b8d6df5e5f402fd17`  
		Last Modified: Thu, 18 Jun 2026 20:44:54 GMT  
		Size: 27.1 KB (27092 bytes)  
		MIME: application/vnd.in-toto+json
