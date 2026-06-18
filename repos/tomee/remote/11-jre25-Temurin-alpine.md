## `tomee:11-jre25-Temurin-alpine`

```console
$ docker pull tomee@sha256:6262fca669c8070dd53f3ea6738bb1b60ebf63af5b236312317d36a938312536
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:11-jre25-Temurin-alpine` - linux; amd64

```console
$ docker pull tomee@sha256:15067e09ca9e52cfff90e50bc2dd6af92cf02197a9d3b4e38c64674ba7affef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154788294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c3916ba691748afd0315b5cdbce96e5690e2c5c2963e223404f865c0acf83e`
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
# Thu, 18 Jun 2026 20:43:38 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jun 2026 20:43:38 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Thu, 18 Jun 2026 20:43:39 GMT
WORKDIR /usr/local/tomee
# Thu, 18 Jun 2026 20:43:39 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Thu, 18 Jun 2026 20:43:49 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Thu, 18 Jun 2026 20:43:49 GMT
ENV TOMEE_VER=11.0.0-M1
# Thu, 18 Jun 2026 20:43:49 GMT
ENV TOMEE_BUILD=microprofile
# Thu, 18 Jun 2026 20:43:51 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Thu, 18 Jun 2026 20:43:51 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 18 Jun 2026 20:43:51 GMT
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
	-	`sha256:1a4a7a213d896f1fe5b94dae849e16e718dd2b998343f8b89c6b1c44011612a5`  
		Last Modified: Thu, 18 Jun 2026 20:44:01 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cfb40f0fd24d640700597cab5c14cb01209376165398d9f047cb1437ca8424`  
		Last Modified: Thu, 18 Jun 2026 20:44:01 GMT  
		Size: 7.2 MB (7184491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7120146586840b42c94e2ce63900065df8ab0e701f5e7b72f524b03d4d8d3f45`  
		Last Modified: Thu, 18 Jun 2026 20:44:01 GMT  
		Size: 75.7 KB (75665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dc158e63ec45fb19d4c2ec3915fcc749cd63d015be0f1b50550bea1cce6bbf`  
		Last Modified: Thu, 18 Jun 2026 20:44:03 GMT  
		Size: 72.1 MB (72103844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:11-jre25-Temurin-alpine` - unknown; unknown

```console
$ docker pull tomee@sha256:1de151433554fd215b23ccefbe7eb07eb15145a27643e6179d6e8c5c8841c60f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1311841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493bb3b1adc94b7ce579f50324f23497b95293cdda576b4fe07456d3c0e38ef0`

```dockerfile
```

-	Layers:
	-	`sha256:9a58ee127398060bd010b0f3027cf80d89107f837d6001a7918ddc9d6d595146`  
		Last Modified: Thu, 18 Jun 2026 20:44:01 GMT  
		Size: 1.3 MB (1278899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbfbf5be485f3a1126564783cd37c2e42a2010193e97f1be9dc139d4d013fe04`  
		Last Modified: Thu, 18 Jun 2026 20:44:01 GMT  
		Size: 32.9 KB (32942 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:11-jre25-Temurin-alpine` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:dc911f09661a8c14e4bd528c9c5e0a739f74f791fcf81a114f5600970b4743ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153990702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8fac7624ab863dc146f68155c0484628aaa666fa6e24c9b4ffac46807d11272`
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
# Thu, 18 Jun 2026 20:43:46 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jun 2026 20:43:46 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Thu, 18 Jun 2026 20:43:46 GMT
WORKDIR /usr/local/tomee
# Thu, 18 Jun 2026 20:43:47 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Thu, 18 Jun 2026 20:43:56 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Thu, 18 Jun 2026 20:43:56 GMT
ENV TOMEE_VER=11.0.0-M1
# Thu, 18 Jun 2026 20:43:56 GMT
ENV TOMEE_BUILD=microprofile
# Thu, 18 Jun 2026 20:43:58 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Thu, 18 Jun 2026 20:43:58 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 18 Jun 2026 20:43:58 GMT
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
	-	`sha256:b1fac4d1720ed41318ec4bdc541870311676610078c1baba986d6dabfb3ce8ea`  
		Last Modified: Thu, 18 Jun 2026 20:44:08 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fae05daba3dbfc211ebc9403461c78efa121e734e5035e85bc8b5fe8179a100`  
		Last Modified: Thu, 18 Jun 2026 20:44:08 GMT  
		Size: 7.1 MB (7091375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177a41cf795841cdc06f61e0807d72d7533c39b134b59ce349efe5eabc19a0e5`  
		Last Modified: Thu, 18 Jun 2026 20:44:08 GMT  
		Size: 75.6 KB (75648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be840da9f8f3086c3b63e9908402e0b3859c6550210f59865df02361fbf6f852`  
		Last Modified: Thu, 18 Jun 2026 20:44:09 GMT  
		Size: 72.1 MB (72103841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:11-jre25-Temurin-alpine` - unknown; unknown

```console
$ docker pull tomee@sha256:a9251288d8d7a9f4fcf679d97abf2f0d11f7ab8aa3b5575fe3f80034af3e0f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1311255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e51b66239e46315d4a605e9fad79af24196a46acc51897bed163213b99764c0`

```dockerfile
```

-	Layers:
	-	`sha256:bb3ae888e8564a60347910e1007ab1c09b25e277788c014f1e21d2fb31146921`  
		Last Modified: Thu, 18 Jun 2026 20:44:07 GMT  
		Size: 1.3 MB (1277924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5db9387b439c89e82ce6a5e4b17ada0e6de9a4f87a41997938c5d38df9b51c0a`  
		Last Modified: Thu, 18 Jun 2026 20:44:07 GMT  
		Size: 33.3 KB (33331 bytes)  
		MIME: application/vnd.in-toto+json
