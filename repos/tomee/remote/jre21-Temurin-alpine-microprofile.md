## `tomee:jre21-Temurin-alpine-microprofile`

```console
$ docker pull tomee@sha256:1de8d52f13e09d1722a04ea91b5cc4eea01779161dcc2ed9f24812e65910c0f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:jre21-Temurin-alpine-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:d8c4f5acaf05259744409f7732a1a028a8e8086b6e6e227bce35744805e6d013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145344004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7bd76bbc2316e86bdb7eaac9810690581c2671dee481048197e3bd5dba362bd`
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
# Wed, 15 Apr 2026 21:57:42 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:57:42 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Wed, 15 Apr 2026 21:57:42 GMT
WORKDIR /usr/local/tomee
# Wed, 15 Apr 2026 21:57:43 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 21:57:52 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 15 Apr 2026 21:57:52 GMT
ENV TOMEE_VER=10.1.4
# Wed, 15 Apr 2026 21:57:52 GMT
ENV TOMEE_BUILD=microprofile
# Wed, 15 Apr 2026 21:57:53 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Wed, 15 Apr 2026 21:57:53 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 21:57:53 GMT
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
	-	`sha256:ba9ddef140822d208df892ab8e0045da81b64c3604f30b7f73f91f4934ea7541`  
		Last Modified: Wed, 15 Apr 2026 21:58:02 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea11d418b534d479b9d091d1939c594bb7c41baad00e5ef36d154926bc4d86a4`  
		Last Modified: Wed, 15 Apr 2026 21:58:02 GMT  
		Size: 888.1 KB (888065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe244472a743f8364b5352dccd21daa01130ddc942cd65ae1bc4fe7799c3bc1`  
		Last Modified: Wed, 15 Apr 2026 21:58:02 GMT  
		Size: 75.6 KB (75639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381e6af68cb76346f12f705746fb36b29cf1a9ea78eb2db78d87a3dda56bd6e9`  
		Last Modified: Wed, 15 Apr 2026 21:58:05 GMT  
		Size: 70.5 MB (70506976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre21-Temurin-alpine-microprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:f483a621756105978390a818574daea8fff5d0702e451e240e7a9a9f7d4b4658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1330345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394c54a784de4bdf16d629ec11299f240e67b90368bc070666fa943e59d64a28`

```dockerfile
```

-	Layers:
	-	`sha256:95dc468548b2ca812eb80d5d48e52f3b6a5616a80e08c8de59ecd1cfa7d31155`  
		Last Modified: Wed, 15 Apr 2026 21:58:02 GMT  
		Size: 1.3 MB (1300061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5140c15295f3a3feffff0be5e3bb7db8b3c4b5210d5625bcc213ecffe0df2bad`  
		Last Modified: Wed, 15 Apr 2026 21:58:02 GMT  
		Size: 30.3 KB (30284 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:jre21-Temurin-alpine-microprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:8b5c375f15cacf7349b495bda3009e389fae170e1fcbaa11d46824936d066d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144709307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3f080908ad7c7728591d45ae9e6ed533745d29074280d9d0a67d27775b874d`
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
# Wed, 15 Apr 2026 22:10:03 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:10:03 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Wed, 15 Apr 2026 22:10:03 GMT
WORKDIR /usr/local/tomee
# Wed, 15 Apr 2026 22:10:03 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 22:10:13 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 15 Apr 2026 22:10:13 GMT
ENV TOMEE_VER=10.1.4
# Wed, 15 Apr 2026 22:10:13 GMT
ENV TOMEE_BUILD=microprofile
# Wed, 15 Apr 2026 22:10:14 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Wed, 15 Apr 2026 22:10:14 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 22:10:14 GMT
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
	-	`sha256:30b7641249a92e213720d02034bdcb78027eee96fa1283e870f4f631f01fc6ae`  
		Last Modified: Wed, 15 Apr 2026 22:10:24 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d39c4c55523f5c65810947a6cbf6cc3997addbd740a5ad681767977fbbc39b`  
		Last Modified: Wed, 15 Apr 2026 22:10:24 GMT  
		Size: 893.4 KB (893361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0b43668199c8a719ed6dea0e4e5ad2f7f4e623e65f7bb94d78f11d90973fd6`  
		Last Modified: Wed, 15 Apr 2026 22:10:25 GMT  
		Size: 75.7 KB (75650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55c6d09efafc9338bb19394c2505ff4d1f23cafacde5ba34c9b3d871d2f6162`  
		Last Modified: Wed, 15 Apr 2026 22:10:26 GMT  
		Size: 70.5 MB (70506918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre21-Temurin-alpine-microprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:c645a331efb7fe4704c9c49e11f5113b6e0b4b4b3e5423f18d9f347bbc87544c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1329571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1304301f50bd3219704c4d757d937c57f6f891bd8b96c58a0d8ff74d7de47ee2`

```dockerfile
```

-	Layers:
	-	`sha256:ca3eb791fc69b42e62dc7e7c8aca7c89595bcc1db75d88f0d31316353d7fa4b8`  
		Last Modified: Wed, 15 Apr 2026 22:10:25 GMT  
		Size: 1.3 MB (1298993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40a66e75a4f6f18defbfa31f8194380422e010993803fae56a6337ce44a797e9`  
		Last Modified: Wed, 15 Apr 2026 22:10:24 GMT  
		Size: 30.6 KB (30578 bytes)  
		MIME: application/vnd.in-toto+json
