## `tomee:jre21-alpine-plus`

```console
$ docker pull tomee@sha256:fbb1be818c4eb698bb04b6f876c5ab7ad691c409eecb7285985c02e14d6f86b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:jre21-alpine-plus` - linux; amd64

```console
$ docker pull tomee@sha256:0124aa0cb1fd2792d4ecd3d4f10536b4196b178ff9c0ff3c05e7d5615917f7d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151779846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbb8ce70866d7d5daccaab13c0057f8470e5abd6c8bc0805075cbdb0ce4adae`
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
# Fri, 08 May 2026 00:25:28 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Fri, 08 May 2026 00:25:38 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Fri, 08 May 2026 00:25:38 GMT
ENV TOMEE_VER=10.1.5
# Fri, 08 May 2026 00:25:38 GMT
ENV TOMEE_BUILD=plus
# Fri, 08 May 2026 00:25:40 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Fri, 08 May 2026 00:25:40 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 08 May 2026 00:25:40 GMT
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
	-	`sha256:05a924ff2f6f4b3f431f7f0490da4100170d90737f73f5da4ffba8c070c44eda`  
		Last Modified: Fri, 08 May 2026 00:25:50 GMT  
		Size: 888.1 KB (888147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cadca8ec22a75b0812ac1ea4af380ac9b84c63b348d7e64485c27823e0f12f`  
		Last Modified: Fri, 08 May 2026 00:25:50 GMT  
		Size: 75.7 KB (75689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013920a95c36e8a946a5e9855be8451d65df6e9ab5b255adc70cd95b68e6a8f1`  
		Last Modified: Fri, 08 May 2026 00:25:52 GMT  
		Size: 76.8 MB (76790223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre21-alpine-plus` - unknown; unknown

```console
$ docker pull tomee@sha256:7b877c4b5e209d89c9ece247994e298b7dcc92891345315a94fb17de86b58f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1335951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2cbafcf84760f784e07f2c90c0e32eca12d2bcb6b86b8b196a0b779db2a5e7`

```dockerfile
```

-	Layers:
	-	`sha256:bac94806c979fe74338c60f02a93b6271931bcf2482357806eabfa35b800b1dc`  
		Last Modified: Fri, 08 May 2026 00:25:50 GMT  
		Size: 1.3 MB (1308413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9034c3b1bfbf97d435dc374b022ed1c8b1dcd4b95d75afd5f941a4647a89d7ce`  
		Last Modified: Fri, 08 May 2026 00:25:50 GMT  
		Size: 27.5 KB (27538 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:jre21-alpine-plus` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:79ad7dd3beeae5386e79eefee814192eb8774fdf21dc509825704c0de6060b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151139193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766eec6a2a5e9530f2924d984f316a71290699459606feb7e0fb4c571f8ec18c`
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
# Fri, 08 May 2026 00:25:27 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:25:27 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Fri, 08 May 2026 00:25:27 GMT
WORKDIR /usr/local/tomee
# Fri, 08 May 2026 00:25:28 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Fri, 08 May 2026 00:25:39 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Fri, 08 May 2026 00:25:39 GMT
ENV TOMEE_VER=10.1.5
# Fri, 08 May 2026 00:25:39 GMT
ENV TOMEE_BUILD=plus
# Fri, 08 May 2026 00:25:40 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Fri, 08 May 2026 00:25:40 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 08 May 2026 00:25:40 GMT
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
	-	`sha256:87745bb38d668d4fbdb2c23313b68bef310f27f37f1ee36a003895aa9c8470f6`  
		Last Modified: Fri, 08 May 2026 00:25:50 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1643e2298794fd09b814f260375f37de3019eb70fdcb9338aa9c10c42a77ef8f`  
		Last Modified: Fri, 08 May 2026 00:25:50 GMT  
		Size: 894.0 KB (893960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6130443e5b037ea53c1411467540efa847aba39af02537694374ae09f19eeb88`  
		Last Modified: Fri, 08 May 2026 00:25:50 GMT  
		Size: 75.6 KB (75634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccb38be13aa2069d9531ed836e45f02aa3782228f20328d45583b79b0b16a30`  
		Last Modified: Fri, 08 May 2026 00:25:54 GMT  
		Size: 76.8 MB (76790327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre21-alpine-plus` - unknown; unknown

```console
$ docker pull tomee@sha256:d477317996b505f591b52d7c412aff10b5bf65ba4842123d5c40c7233619b9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1334984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa401ad344217d09faac6f8cf22cef5ae6a18999d11149c3cd6d71af0a1d8ab4`

```dockerfile
```

-	Layers:
	-	`sha256:8a5c8417054932a4824a595a7577f79dced25e154c2bb6d20c4df58f4e30dcf0`  
		Last Modified: Fri, 08 May 2026 00:25:50 GMT  
		Size: 1.3 MB (1307249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb0b5413e279468b11e5fce534f732f13f8ae11d381027ae7f1316a543d61632`  
		Last Modified: Fri, 08 May 2026 00:25:50 GMT  
		Size: 27.7 KB (27735 bytes)  
		MIME: application/vnd.in-toto+json
