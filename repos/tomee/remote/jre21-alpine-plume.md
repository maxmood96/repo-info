## `tomee:jre21-alpine-plume`

```console
$ docker pull tomee@sha256:b6c7046e70e25155d52d51df2b18d10e49ec9760ba26981b91bbf25b42c6082f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:jre21-alpine-plume` - linux; amd64

```console
$ docker pull tomee@sha256:b4790cb329ad3850cb814219af0d89da7d9583fee287d4ce0c09071e9f14275a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157548946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b887a798473c5e9038d5e9c94cf771bdcfd8570f32c4abc5baae419e91ae4e8d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:59:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:35 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:59:35 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7f8c230ba505b418e4288e2b34758a6e4da32470944740e5ba0cfaae02271c22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='17aca4ecc1600f70ec88ea0f8bf3a06ba6806bdae8c96d03c07683c800f0d4e8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sat, 08 Nov 2025 17:59:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:39:11 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:39:11 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Sat, 08 Nov 2025 18:39:11 GMT
WORKDIR /usr/local/tomee
# Sat, 08 Nov 2025 18:39:11 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl  && rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 18:39:21 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Sat, 08 Nov 2025 18:39:21 GMT
ENV TOMEE_VER=10.1.2
# Sat, 08 Nov 2025 18:39:21 GMT
ENV TOMEE_BUILD=plume
# Sat, 08 Nov 2025 18:39:23 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Sat, 08 Nov 2025 18:39:23 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 18:39:23 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93902f35c01693819c190c354786cbb573f4ef49a5b865d6c34f2197839cc3e4`  
		Last Modified: Sat, 08 Nov 2025 17:59:59 GMT  
		Size: 16.3 MB (16289711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a857bcc1a1505748a54fef25bb81f303468a26d3de127b6b0044b1ffde6275a`  
		Last Modified: Sat, 08 Nov 2025 18:00:03 GMT  
		Size: 53.2 MB (53169034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a75c308165465141d861c1b7f7ec799b18fc84d5d8b87396dc29c3aa4894ff`  
		Last Modified: Sat, 08 Nov 2025 17:59:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d1cf1d02f064d13d647e4816e26b17678a634769ec583b4eb29d5a68d415f7`  
		Last Modified: Sat, 08 Nov 2025 17:59:56 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e6747da71effe4aa65f2b6888443cf76ea4d15b08ea21b2faeca4957668804`  
		Last Modified: Sat, 08 Nov 2025 18:39:57 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9a1791131c1b27f06c75b9f35bb48c5da9862b3c3321ebb5148d6aaf6617b7`  
		Last Modified: Sat, 08 Nov 2025 18:39:57 GMT  
		Size: 1.2 MB (1175966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb0bfea7fdabe8970ff9aa5e38db26f0f8ea5f4adc194b36fecfa7b226d6955`  
		Last Modified: Sat, 08 Nov 2025 18:39:57 GMT  
		Size: 75.6 KB (75620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72be87d9fc59cebfb238a3bbe094cc83f695cc3748a384c2dfe77c6634c70c9`  
		Last Modified: Sat, 08 Nov 2025 18:40:08 GMT  
		Size: 83.0 MB (83033557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre21-alpine-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:5127a3496fc6e4fdbb1482aec8b264eb64bf2e6636dbfd929ca63c780a79bd29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1353462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad45b2c1edefc4570ecc1ad2bfa538c6d6ca2509a0b71ab76d1a8ec2d634a94`

```dockerfile
```

-	Layers:
	-	`sha256:557d9e61e04f443ae5be7b43a9201d60ebc2aeced76395bc9c634daaa1279847`  
		Last Modified: Sat, 08 Nov 2025 23:13:58 GMT  
		Size: 1.3 MB (1325907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d62107ffc8725c06d1e8cbdd1a586288278e81b9be652d19d442b7b41b71227`  
		Last Modified: Sat, 08 Nov 2025 23:13:59 GMT  
		Size: 27.6 KB (27555 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:jre21-alpine-plume` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:b5de8989a8b5424128245933be26bddaf8ec1211b1d561a0613682965d7ea7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156900894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ac9a71074df3aec03965bf0cbf01e39cd853e10bf80512dd8c661ac0445a38`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:58:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:58 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:58:58 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:01 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7f8c230ba505b418e4288e2b34758a6e4da32470944740e5ba0cfaae02271c22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='17aca4ecc1600f70ec88ea0f8bf3a06ba6806bdae8c96d03c07683c800f0d4e8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sat, 08 Nov 2025 17:59:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:39:00 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:39:00 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Sat, 08 Nov 2025 18:39:00 GMT
WORKDIR /usr/local/tomee
# Sat, 08 Nov 2025 18:39:01 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl  && rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 18:39:11 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Sat, 08 Nov 2025 18:39:11 GMT
ENV TOMEE_VER=10.1.2
# Sat, 08 Nov 2025 18:39:11 GMT
ENV TOMEE_BUILD=plume
# Sat, 08 Nov 2025 18:39:13 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Sat, 08 Nov 2025 18:39:13 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 18:39:13 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9b9ccbec66a68ab16d44064cb6d5b3237fae5cc9357c0aa358b9dcdadbd9a6`  
		Last Modified: Sat, 08 Nov 2025 17:59:20 GMT  
		Size: 16.3 MB (16253675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d029414ffab73c2cdc0ed11f28215fa32c6e67035a81da529c1cfadeae1de11f`  
		Last Modified: Sat, 08 Nov 2025 17:59:24 GMT  
		Size: 52.2 MB (52226475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae04221b2e584a4e0a67d1d535900a5eb9c049d2a2051d0b66d4d2af68f77ac`  
		Last Modified: Sat, 08 Nov 2025 17:59:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ada9f9a574189d8e20095927344850458cfffc58029c0e6d5d292c6f568c419`  
		Last Modified: Sat, 08 Nov 2025 17:59:17 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28610a32448e2335428493f915f1c7615d94569ab8aa3997c3d7b66e30735326`  
		Last Modified: Sat, 08 Nov 2025 18:39:30 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e293be3bff7f3624ebd956c104f465561fddb41e34445b7b54f1ec426523a3`  
		Last Modified: Sat, 08 Nov 2025 18:39:30 GMT  
		Size: 1.2 MB (1170839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd1eb948bddd2dbf4d0ebc7f3bfaf2f209f2e24da20cbb86b2dd8def805b3a8`  
		Last Modified: Sat, 08 Nov 2025 18:39:30 GMT  
		Size: 75.7 KB (75679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18d9303ea5ee927e277889730084602b7eb9b4224170d42ac60d23cc3d3f763`  
		Last Modified: Sat, 08 Nov 2025 18:39:37 GMT  
		Size: 83.0 MB (83033552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre21-alpine-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:830a5ac24b27de050bb8c1be4da9466e154244d18f76c5c198f3ea82d6f83b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1353144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca44c4913e82864c3f8ffdfe0e37bbe7aabfeb740cb55a016aadf6d03405c279`

```dockerfile
```

-	Layers:
	-	`sha256:bffaa58aa2f0445026b7cff44b3f0251d343d057a9ae82e11168d980a4c33069`  
		Last Modified: Sat, 08 Nov 2025 20:14:15 GMT  
		Size: 1.3 MB (1325393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f74cb6b64e13009c90d755f4423f9238bcfb90eac57a94e4605bd46c9a4b8807`  
		Last Modified: Sat, 08 Nov 2025 20:14:16 GMT  
		Size: 27.8 KB (27751 bytes)  
		MIME: application/vnd.in-toto+json
