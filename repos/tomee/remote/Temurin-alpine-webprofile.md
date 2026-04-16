## `tomee:Temurin-alpine-webprofile`

```console
$ docker pull tomee@sha256:e3ccd4c12a58d726cded0f2293b75a3defe8105df5a3e620f3a675e7358bd7a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:Temurin-alpine-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:d554fdbdc1ccffa4536c31ae354335ea4e5650c34d1091b4a695627e85db4e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142472645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4218c6b67566137f339649cd903621c9e0fe905dce4ff6d4e26641b70909575d`
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
# Wed, 15 Apr 2026 21:57:13 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:57:13 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Wed, 15 Apr 2026 21:57:13 GMT
WORKDIR /usr/local/tomee
# Wed, 15 Apr 2026 21:57:13 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 21:57:23 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 15 Apr 2026 21:57:23 GMT
ENV TOMEE_VER=10.1.4
# Wed, 15 Apr 2026 21:57:23 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 15 Apr 2026 21:57:24 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Wed, 15 Apr 2026 21:57:24 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 21:57:24 GMT
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
	-	`sha256:f0cbed98d107c7884d059eb49db91f4bf76f6499f1d9b598c1358261e9d60eab`  
		Last Modified: Wed, 15 Apr 2026 21:57:32 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f998fd9f1bc3741820bcfefc7df7484030d5895bce362267a8fe89a6a789d5`  
		Last Modified: Wed, 15 Apr 2026 21:57:33 GMT  
		Size: 7.2 MB (7238020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec061765abfc2976c03ba235190357bbe632d7c6190611b2d7aa9d215e7fa16a`  
		Last Modified: Wed, 15 Apr 2026 21:57:33 GMT  
		Size: 75.7 KB (75650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f818f37d9c441441f5beba3c9cb7df67244d00c5c18b678088afd783070a653b`  
		Last Modified: Wed, 15 Apr 2026 21:57:34 GMT  
		Size: 59.9 MB (59865124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:Temurin-alpine-webprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:d45986dc284957071bf381594d9f5eed3a3aee8bbb9f43c8eba1e6b76e4e9e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1201996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344ffeaffcd8ab6f91de805b57dc9d29ff05ce1121e2a22ba7c404f7187f359d`

```dockerfile
```

-	Layers:
	-	`sha256:2cb3a6b085ca1088f69d9d6d50847309e2516a96fcb2034374b1ac73ca098ac9`  
		Last Modified: Wed, 15 Apr 2026 21:57:32 GMT  
		Size: 1.2 MB (1171675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bb582bff058a065203df414157bd4a430e09b386c5dbf62b1a4af7f030dd446`  
		Last Modified: Wed, 15 Apr 2026 21:57:32 GMT  
		Size: 30.3 KB (30321 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:Temurin-alpine-webprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:b0ddba1025d708e851d96ee6f6092aec4c1b10ce45a98c90bea27a6a56dc3910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141673316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9baceaa2ebd337e4ebb8b9d5753bc30ce1e1707266b4577e9bcea9f1beeb0150`
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
# Wed, 15 Apr 2026 22:09:19 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:09:19 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Wed, 15 Apr 2026 22:09:19 GMT
WORKDIR /usr/local/tomee
# Wed, 15 Apr 2026 22:09:20 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 22:09:30 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 15 Apr 2026 22:09:30 GMT
ENV TOMEE_VER=10.1.4
# Wed, 15 Apr 2026 22:09:30 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 15 Apr 2026 22:09:31 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Wed, 15 Apr 2026 22:09:31 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 22:09:31 GMT
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
	-	`sha256:7326d9baaaefdac13fc8ef73f51c062961188f02456a2781e444c3cee1c29dc4`  
		Last Modified: Wed, 15 Apr 2026 22:09:40 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ead4998c9567634cb5863e0dd3012ad16e9108dcca3f9df3b73d749a31c3a80`  
		Last Modified: Wed, 15 Apr 2026 22:09:40 GMT  
		Size: 7.1 MB (7147184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1623dc68870d11f96a07ae281aac405904670bdef8bfcb2b04a0531cf5d13079`  
		Last Modified: Wed, 15 Apr 2026 22:09:40 GMT  
		Size: 75.7 KB (75655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12707b4e7a799b189d831e5861fb66dacefecbdf2755ac5155663c4fb402a9c9`  
		Last Modified: Wed, 15 Apr 2026 22:09:42 GMT  
		Size: 59.9 MB (59865126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:Temurin-alpine-webprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:f56754a9e0025dab5e9cda7aa303eba49ff3ae351e8711807540427d269e071b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1201218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a6abb2d15062b939939165d3bcfb59fd5145520722d67f67e0f40d016bffeb`

```dockerfile
```

-	Layers:
	-	`sha256:9e524b827ab817f6fce9f338c3b4d02fef27b86ad9caf33fd6045ca7543a0251`  
		Last Modified: Wed, 15 Apr 2026 22:09:40 GMT  
		Size: 1.2 MB (1170604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffe5dec2ed7c27201d361f8e93654e184fb6e4ef7a25e128b226484545a4fb33`  
		Last Modified: Wed, 15 Apr 2026 22:09:40 GMT  
		Size: 30.6 KB (30614 bytes)  
		MIME: application/vnd.in-toto+json
