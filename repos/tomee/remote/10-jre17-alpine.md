## `tomee:10-jre17-alpine`

```console
$ docker pull tomee@sha256:76a2cdffd5367e05d4d32b89fa9c512e17ad41bd54b544dd09da9d0cf2969bca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `tomee:10-jre17-alpine` - linux; amd64

```console
$ docker pull tomee@sha256:13c8ae04b9993fdd5d1681ce4de9890222ab78d822e24ca980c387648b983ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139274437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7492ddba972cdb6ff72bf4e94a17e458c3c00e1120f2cd1073f29206833d16`
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
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:33:39 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='3226a10cf4f7ef8f835148ce8737490f0cf63e38a1e3ba26cf1e05d9e28adf5c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 15 Apr 2026 20:33:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:58:34 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:58:34 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Wed, 15 Apr 2026 21:58:34 GMT
WORKDIR /usr/local/tomee
# Wed, 15 Apr 2026 21:58:35 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 21:58:44 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 15 Apr 2026 21:58:44 GMT
ENV TOMEE_VER=10.1.4
# Wed, 15 Apr 2026 21:58:44 GMT
ENV TOMEE_BUILD=microprofile
# Wed, 15 Apr 2026 21:58:46 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Wed, 15 Apr 2026 21:58:46 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 21:58:46 GMT
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
	-	`sha256:09f01c4101f54c4f60c1510e1916b7a6584953ff1b5229b617996da7fd40e272`  
		Last Modified: Wed, 15 Apr 2026 20:33:50 GMT  
		Size: 47.1 MB (47099174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070a7b9fef9143a36d5ef71a6027ecbbd0d5fcc76c2375b8d5909ab429c37134`  
		Last Modified: Wed, 15 Apr 2026 20:33:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0f9a83cd259d675ee9277fabad86bfa2ccb5d95a10d34657c764360c4b65c2`  
		Last Modified: Wed, 15 Apr 2026 20:33:48 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75c0efe95ac465c072be04afef79c71c0ef4eb110c94dfb7f49ea06ca0f39bf`  
		Last Modified: Wed, 15 Apr 2026 21:58:55 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f226d2b6c2c6268c231f8e5171e0d59a2e420bbe9ec173df05312b65a158391`  
		Last Modified: Wed, 15 Apr 2026 21:58:55 GMT  
		Size: 888.1 KB (888073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648dd141862adb2917d0c7c29f7407857c9036833078f082b15e7437ae147399`  
		Last Modified: Wed, 15 Apr 2026 21:58:55 GMT  
		Size: 75.6 KB (75645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a87f3e59120260547bf26036acc0e0082301e7abb8a343de790cac8e850828b`  
		Last Modified: Wed, 15 Apr 2026 21:58:57 GMT  
		Size: 70.5 MB (70506975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre17-alpine` - unknown; unknown

```console
$ docker pull tomee@sha256:b6f94b280c9b842f83f1beeacf6704b95393c2ceb889e2c7f3a30a440f2bc102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1329098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff58819296b54350eec28e286d27545aad3cad4017de130a19e499f9a6835aa`

```dockerfile
```

-	Layers:
	-	`sha256:0ec80011f1025c153a0f54e1e5bace33ce8fccf9aa5b335980b09aacab32c162`  
		Last Modified: Wed, 15 Apr 2026 21:58:55 GMT  
		Size: 1.3 MB (1298813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6a9422c15d25c1195b79d9646c73a9f51c7034c1d18f7c2badb3a70fde21551`  
		Last Modified: Wed, 15 Apr 2026 21:58:55 GMT  
		Size: 30.3 KB (30285 bytes)  
		MIME: application/vnd.in-toto+json
