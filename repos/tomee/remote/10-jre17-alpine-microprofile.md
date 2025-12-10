## `tomee:10-jre17-alpine-microprofile`

```console
$ docker pull tomee@sha256:be34aa5de1f305af3465fd6cc2a4d143eaa8305de7a23e99448439b103ec4e49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `tomee:10-jre17-alpine-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:fa9f689d77770b400015ecd1d4ba971027b317249c7c09fe01653a65025d455a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138510534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab3153bc5bd81204c50196086f7321f8373abb353f871205dbb9d1b615523fa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:58:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:31 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:58:31 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:33 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='6c3047e8edd3878e8d2a1cee95c04606042c6a55954ad365d20b58f88cc9ecd5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sat, 08 Nov 2025 17:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:39:34 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:39:34 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Sat, 08 Nov 2025 18:39:34 GMT
WORKDIR /usr/local/tomee
# Sat, 08 Nov 2025 18:39:34 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 18:39:44 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Sat, 08 Nov 2025 18:39:44 GMT
ENV TOMEE_VER=10.1.2
# Sat, 08 Nov 2025 18:39:44 GMT
ENV TOMEE_BUILD=microprofile
# Sat, 08 Nov 2025 18:39:45 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Sat, 08 Nov 2025 18:39:45 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 18:39:45 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e1a9c5a7ff69b6a49186e081bc330d9572e229f2c818aa23374161f7a78611`  
		Last Modified: Sat, 08 Nov 2025 17:58:52 GMT  
		Size: 16.3 MB (16289678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8007edd66bab6d1c68463c2a313deb13b319de66422e9b16eaf4a14de89248`  
		Last Modified: Sat, 08 Nov 2025 17:58:52 GMT  
		Size: 46.7 MB (46718923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f0c913436040e8043051a25779be2670ee72a7efec25b6e4bbb08d54877db4`  
		Last Modified: Sat, 08 Nov 2025 17:58:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867c03b825a35a5db0249203ef051f7e12f2bc4c110f281f6de68072d3c55bab`  
		Last Modified: Sat, 08 Nov 2025 17:58:49 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7158a6b31c475e86b700365f8577dd93fdb8dce0c3facde71c67ba6770565e9`  
		Last Modified: Sat, 08 Nov 2025 18:40:16 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a38622811a196751b761038212db7a397ae1e05b7f2c3c30a4f874e9e328c0`  
		Last Modified: Sat, 08 Nov 2025 18:40:16 GMT  
		Size: 1.2 MB (1175965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc19e6e4af58af5fa5d038ebe0df8cc01ce14c7effc79ead61e307df76015eab`  
		Last Modified: Sat, 08 Nov 2025 18:40:16 GMT  
		Size: 75.7 KB (75650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b118f48fc96f293cd39b91b1d8f7c227345a856258bdffa9a77c66e84a5d111e`  
		Last Modified: Sat, 08 Nov 2025 18:40:25 GMT  
		Size: 70.4 MB (70445261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre17-alpine-microprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:f2a80f2e43be3f296080a819ceb3e9e59c530b50c6dd17fa3211d9d58e2e3729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1327128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c4870f847e48207e6a5f277a1556b2e69338bbc7d5b0afb21cb7b68804ac21`

```dockerfile
```

-	Layers:
	-	`sha256:9c108125862d2d1e75c783346b672d7add8ae21381ae9b3a0197a49ddcbf6aba`  
		Last Modified: Sat, 08 Nov 2025 23:12:29 GMT  
		Size: 1.3 MB (1296835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d30441abb7eb69dac5c6db636bf000f756352342df93ed86b1dd0d7de44811`  
		Last Modified: Sat, 08 Nov 2025 23:12:30 GMT  
		Size: 30.3 KB (30293 bytes)  
		MIME: application/vnd.in-toto+json
