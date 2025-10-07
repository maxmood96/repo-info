## `tomee:jre25-alpine-webprofile`

```console
$ docker pull tomee@sha256:33a68ff07d6c50345975cb5e448fff3e45e7685ea1dbfb45cf10b82b6966a456
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:jre25-alpine-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:407948f941ddceded01948dca5358f4973eca427d5eb19289dd840a9836b5685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144578755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dc04922b03aa0174722bc4e71a773fa3d575a3679dcfad97e01055396dcfe9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e88496ca31d2e0a0cdeeba385ab4ea668bbb53a03018f30c8933e97f4f9fda47';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25_36.tar.gz';          ;;        x86_64)          ESUM='aa5160aa130f0f0b4379fc62a0d5198c065815224e01318272864e56f260de34';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_alpine-linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 05 Oct 2025 18:19:29 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 05 Oct 2025 18:19:29 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
WORKDIR /usr/local/tomee
# Sun, 05 Oct 2025 18:19:29 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
ENV TOMEE_VER=10.1.2
# Sun, 05 Oct 2025 18:19:29 GMT
ENV TOMEE_BUILD=webprofile
# Sun, 05 Oct 2025 18:19:29 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
EXPOSE map[8080/tcp:{}]
# Sun, 05 Oct 2025 18:19:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65066cd35e5f01df9fe74f660a91505081cf739f77f0d1dd53519a0d3963d84f`  
		Last Modified: Thu, 25 Sep 2025 21:19:16 GMT  
		Size: 11.9 MB (11885118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a2e4a061fb5ed029cf666382a1f5d4f4d0ce091ef3ed940c07608537bf0a2a`  
		Last Modified: Thu, 25 Sep 2025 21:19:19 GMT  
		Size: 62.0 MB (61962252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a8c05ea020bdd95f264437cf34ce32c499b0c1b7bba16221fa1c05b358436`  
		Last Modified: Thu, 25 Sep 2025 21:16:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5985a25118832520d34d02284ff25511ec9dc5a354d050b92285465023b87af6`  
		Last Modified: Thu, 25 Sep 2025 21:16:52 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fa9521d2338470fa75dba07df8eded194ac0c9a9307adf7c2c904dd60b52bb`  
		Last Modified: Mon, 06 Oct 2025 20:12:26 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c62486c945912ecd512944adfde34ee2f389738683a1847b821586f93c63a7`  
		Last Modified: Mon, 06 Oct 2025 19:17:26 GMT  
		Size: 7.0 MB (6992351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659ffd98264268c7ecea5f00669cf9d26e0158ed91bbd533453f4a513eeeadec`  
		Last Modified: Mon, 06 Oct 2025 20:12:25 GMT  
		Size: 75.7 KB (75663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899162f965b0bbba8605885b3ec4011f754c8b7d495592fc42af38fe1cf5812d`  
		Last Modified: Mon, 06 Oct 2025 19:17:28 GMT  
		Size: 59.9 MB (59861069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre25-alpine-webprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:208786894fe9462e3434be738a8fb817610b1bc01b770bc0fb177942bf93d2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1198674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b22e1ec4d2ba7c73c8274950b7eb54541e4a99d8e7e0a46cd80bbbacf369e7`

```dockerfile
```

-	Layers:
	-	`sha256:ca20b67736730ad59160ebb7122fde1ded93937b0b7fd77755932a16b8c09b33`  
		Last Modified: Mon, 06 Oct 2025 22:12:48 GMT  
		Size: 1.2 MB (1168320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4606b59a2ca717c4958e9527fdd3653649c60d8fbd720ba6f9540918c2a6c6ff`  
		Last Modified: Mon, 06 Oct 2025 22:12:49 GMT  
		Size: 30.4 KB (30354 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:jre25-alpine-webprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:47f7bf97995812670a71d5ca84188594b01681d74fbef65fb409e634b4068d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144057572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83045344379fd023f61ff58530ec526f5d46b3b1e0e974882c493d8d013da1d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e88496ca31d2e0a0cdeeba385ab4ea668bbb53a03018f30c8933e97f4f9fda47';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25_36.tar.gz';          ;;        x86_64)          ESUM='aa5160aa130f0f0b4379fc62a0d5198c065815224e01318272864e56f260de34';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_alpine-linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 05 Oct 2025 18:19:29 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 05 Oct 2025 18:19:29 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
WORKDIR /usr/local/tomee
# Sun, 05 Oct 2025 18:19:29 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
ENV TOMEE_VER=10.1.2
# Sun, 05 Oct 2025 18:19:29 GMT
ENV TOMEE_BUILD=webprofile
# Sun, 05 Oct 2025 18:19:29 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
EXPOSE map[8080/tcp:{}]
# Sun, 05 Oct 2025 18:19:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d761e29959db912783f2230e5873f772b9571ab3f8c560320af9dab4acea15b`  
		Last Modified: Thu, 25 Sep 2025 21:43:58 GMT  
		Size: 12.2 MB (12198528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95d40354e82e9785368c707d244482a30ba62c997569b8d298eef14d18b6e52`  
		Last Modified: Thu, 25 Sep 2025 21:44:15 GMT  
		Size: 60.9 MB (60868848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff334854b95c17d48f838cb488af4f42cdc576eee70c71db57cc8ab49acabd97`  
		Last Modified: Thu, 25 Sep 2025 21:16:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951c4054e070def6124dde5f5e46b2bcb7dd2a88e7acd5e86cd6e2b27c131ff4`  
		Last Modified: Thu, 25 Sep 2025 21:17:01 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90061a0e04f1f7763def97a6dab369179fdde058657f6c26092be1d3bb70ac0`  
		Last Modified: Mon, 06 Oct 2025 19:18:05 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed38ca36ebf77b6b60e0025e994bf0a1a940b0df619f13e36cac8b40e22f7dd`  
		Last Modified: Mon, 06 Oct 2025 19:18:06 GMT  
		Size: 6.9 MB (6920216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da194c9f70dcfe0deb390d4cedb97ab3b08367ec944c4a34267e55d7e088459`  
		Last Modified: Mon, 06 Oct 2025 19:18:05 GMT  
		Size: 75.6 KB (75625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb492503b4c595f1a1be35335983b64f58b23713d594f3f60e622b320cae4e5`  
		Last Modified: Mon, 06 Oct 2025 19:18:11 GMT  
		Size: 59.9 MB (59860993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre25-alpine-webprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:062ffec4b350f9193c7c434134d2b499932c558357d790418f2f1c37eb281acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1198546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912ff78bc1dbbac2c006f151a4de8ddda200f3cf1f5f6f5a14c7dcda7f7b077b`

```dockerfile
```

-	Layers:
	-	`sha256:87e05a3b30d6880f4eef54e4de8a7c5363f427d4134012f9891ce936f16c64cc`  
		Last Modified: Mon, 06 Oct 2025 22:12:53 GMT  
		Size: 1.2 MB (1167899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb720879e6d6c062b46d0c3bf2c0d52780fa5cb6a23d49b14cabf751315bd35d`  
		Last Modified: Mon, 06 Oct 2025 22:12:54 GMT  
		Size: 30.6 KB (30647 bytes)  
		MIME: application/vnd.in-toto+json
