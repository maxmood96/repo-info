## `tomee:10-jre21-alpine-microprofile`

```console
$ docker pull tomee@sha256:2a59ae2c9104233603bc07a71200855d57a7b5250a0d9f4dedd2b82b95ec6c58
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:10-jre21-alpine-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:a5923a70652758b15979c445a443b298fc7918f5eb06d20e53c993334b399fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147301013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf9d5a0de38cfd626e7734299ccb0e31d868117b26d7d2b6983179d6d635aa2`
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
# Fri, 08 May 2026 00:25:27 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:25:27 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Fri, 08 May 2026 00:25:27 GMT
WORKDIR /usr/local/tomee
# Fri, 08 May 2026 00:25:27 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Fri, 08 May 2026 00:25:38 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Fri, 08 May 2026 00:25:38 GMT
ENV TOMEE_VER=10.1.5
# Fri, 08 May 2026 00:25:38 GMT
ENV TOMEE_BUILD=microprofile
# Fri, 08 May 2026 00:25:39 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Fri, 08 May 2026 00:25:39 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 08 May 2026 00:25:39 GMT
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
	-	`sha256:d50a622e0c48255ec9936f0dec15e78ee92a9a1f398f2f79ee2bb5869a7171b8`  
		Last Modified: Fri, 08 May 2026 00:25:50 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7418dc90a44f231d32e55a5e7b8594e7ed37ed6c099c8aa0a0be77be87b1da`  
		Last Modified: Fri, 08 May 2026 00:25:50 GMT  
		Size: 888.1 KB (888136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ce3ecf0e0bf6cea82c12bf83d4b47e0c8cfc31737a7be71bf770aa5f4d32f6`  
		Last Modified: Fri, 08 May 2026 00:25:50 GMT  
		Size: 75.7 KB (75696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555c3c777181736c3a73c1a306801e3488bfda5faafb405729f4a51de1f6436f`  
		Last Modified: Fri, 08 May 2026 00:25:52 GMT  
		Size: 72.3 MB (72311394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre21-alpine-microprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:fe146b9ac0d69a9946320a0c425201d6b80c23d18b75a54f9eb1b044cd1a94ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1330960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7904454e2fd7dccf83d4f1dd05ac6f7e101bd23fd34483e3768c4e3ebe08bab`

```dockerfile
```

-	Layers:
	-	`sha256:120a44bcfd6ddee3fd85aead494a5a9ba9c3e8c5e45077d95401a407281a15e5`  
		Last Modified: Fri, 08 May 2026 00:25:50 GMT  
		Size: 1.3 MB (1300670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9518a7e031fbf9c558bb33e42e17021ae8ef812f4c4434716ef6ec3a1bf0aa2`  
		Last Modified: Fri, 08 May 2026 00:25:50 GMT  
		Size: 30.3 KB (30290 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:10-jre21-alpine-microprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:ae74d740692c9682cb96918e32b60a05ea55ffd86e7e5ce0d4b9b6194cf7a96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146660262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c833270ecad4ff3cfd5c33a5bced523028c72c9e45bb97c9127798654e8eead8`
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
# Fri, 08 May 2026 00:25:24 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:25:24 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Fri, 08 May 2026 00:25:24 GMT
WORKDIR /usr/local/tomee
# Fri, 08 May 2026 00:25:25 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Fri, 08 May 2026 00:25:36 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Fri, 08 May 2026 00:25:36 GMT
ENV TOMEE_VER=10.1.5
# Fri, 08 May 2026 00:25:36 GMT
ENV TOMEE_BUILD=microprofile
# Fri, 08 May 2026 00:25:38 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Fri, 08 May 2026 00:25:38 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 08 May 2026 00:25:38 GMT
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
	-	`sha256:6fe12edf6e39fb59c4bfbe1f43678ec5f200cacd3ad76247825a183ed0d6e5c6`  
		Last Modified: Fri, 08 May 2026 00:25:48 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57e0a7827f7b3958c7af1676b717e1ef6f08a935ed7430bdde525a15ec32e06`  
		Last Modified: Fri, 08 May 2026 00:25:48 GMT  
		Size: 894.0 KB (893952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae78afb2b5676f20c2268a4819f3cf607f269590befb2749d8d13cbfba3d3a0b`  
		Last Modified: Fri, 08 May 2026 00:25:48 GMT  
		Size: 75.6 KB (75636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba1c60f116884dd7de10411d99b3292d1601d586d083e5f0d9e4ea73778ad88`  
		Last Modified: Fri, 08 May 2026 00:25:52 GMT  
		Size: 72.3 MB (72311403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre21-alpine-microprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:815603aa3d72177bf9cb3d188bdfa32be867682ec0ab023eb070e70f9df91db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1330184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d15e3c784856d82d23f4730463c1ad911112e3015879e1b905863a506b66866`

```dockerfile
```

-	Layers:
	-	`sha256:59130920b5920d95d1380440457500138f1fc35907eb975fff0645d1679e6507`  
		Last Modified: Fri, 08 May 2026 00:25:48 GMT  
		Size: 1.3 MB (1299602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:538064827d396792503c155ecd567f93520bf45105a4d2d3eb0dc9d14242d909`  
		Last Modified: Fri, 08 May 2026 00:25:48 GMT  
		Size: 30.6 KB (30582 bytes)  
		MIME: application/vnd.in-toto+json
