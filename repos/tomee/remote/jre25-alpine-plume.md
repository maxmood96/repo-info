## `tomee:jre25-alpine-plume`

```console
$ docker pull tomee@sha256:55f04af9c9813678ec90f054ec2619b5ca480edc3f602266a605804bf1e9b670
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:jre25-alpine-plume` - linux; amd64

```console
$ docker pull tomee@sha256:bf1d672330b14695d45c9010dbe5c52bba9434c5db9a0d4ed3fa0e9efe3f2b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167751191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654e157190ceef82ef1ba26072c41122b89a34c615cf6e5212f78e395c92b3ea`
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
RUN apk add --no-cache gpg gpg-agent dirmngr curl  && rm -rf /var/cache/apk/* # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
ENV TOMEE_VER=10.1.2
# Sun, 05 Oct 2025 18:19:29 GMT
ENV TOMEE_BUILD=plume
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
	-	`sha256:101c5240f3adb60d5f5a9c43564220a58080a7ad15ad181861d0f4768ae9ae86`  
		Last Modified: Mon, 06 Oct 2025 19:18:04 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35967d0d0c6a94ade95d1210a4386b9b7f40f63363f94e12210b3293c37338a2`  
		Last Modified: Mon, 06 Oct 2025 19:18:05 GMT  
		Size: 7.0 MB (6992331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ad05083c3484e04ba498097fe3aebfbac7259abc300d7b9a0b0cf2797e9e4d`  
		Last Modified: Mon, 06 Oct 2025 19:18:04 GMT  
		Size: 75.7 KB (75651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410d79b7cfe677b9ca790b3f2ed82fffb59b6a01d2266780a89cc58b0cfa989c`  
		Last Modified: Mon, 06 Oct 2025 19:18:16 GMT  
		Size: 83.0 MB (83033537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre25-alpine-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:95c39537f03761130e92f957a6282b20e4a628567e49eb36e21afeaaf4868643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1344051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b0bc02f5c14a4d8371b354d7b54baaf3b07421204e8510c3cb2e0bf9f2d333`

```dockerfile
```

-	Layers:
	-	`sha256:433551cc17bdd4594559e8b51e70cfe8782126498e2b581d061bf02e19faa78c`  
		Last Modified: Mon, 06 Oct 2025 22:12:33 GMT  
		Size: 1.3 MB (1313881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c09908a7ce9428617c6eb8109a1c9f25452af4393be103807ecc46c539ddad1`  
		Last Modified: Mon, 06 Oct 2025 22:12:34 GMT  
		Size: 30.2 KB (30170 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:jre25-alpine-plume` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:e4bd4c6623304c635325bd531476aeee7d579e264a02d99c4e0a9cdac7907a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167230095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1097dc0b9cc0b5f4c6d4f8f1f1f7ed4b3cf000c69c9f13817eed1a5417e98d3f`
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
RUN apk add --no-cache gpg gpg-agent dirmngr curl  && rm -rf /var/cache/apk/* # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
ENV TOMEE_VER=10.1.2
# Sun, 05 Oct 2025 18:19:29 GMT
ENV TOMEE_BUILD=plume
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
	-	`sha256:0f9d5d67dc3579f342a68f375fd37ed14b3a93414d5d873f48b17ad5baf591e1`  
		Last Modified: Mon, 06 Oct 2025 19:17:30 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118dccf2e51d1d92812f5a9a0d116e832fcf74c09e0bf98663d95dedff07f081`  
		Last Modified: Mon, 06 Oct 2025 19:17:30 GMT  
		Size: 6.9 MB (6920215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f334f998ca5c2ce17afcd4d4e540ef2305a37a025ec2d47c4f89ad38d913a4e8`  
		Last Modified: Mon, 06 Oct 2025 19:17:30 GMT  
		Size: 75.6 KB (75609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6173e63f104953b6f32cc74aa6676d1d31e02f0b64158acadd2eba804a0a0e8f`  
		Last Modified: Mon, 06 Oct 2025 19:17:36 GMT  
		Size: 83.0 MB (83033533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre25-alpine-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:ab5349d91708b6d5af427216ccdd3ecb5a8aa2342da7af51d218b5aa12032a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1343922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4438ebd27df203fed11d6209d1e5cc972dc130e00c8c71570df89d952d4a1176`

```dockerfile
```

-	Layers:
	-	`sha256:3484894033ab9535c592a1f8d02828e397fc8bcf8acf59b20f0559d572788bff`  
		Last Modified: Mon, 06 Oct 2025 22:12:38 GMT  
		Size: 1.3 MB (1313460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bb5fbe04c569ce08a7170dccbfd320ea0e7496272df58bf0b5e7e49ea1f112e`  
		Last Modified: Mon, 06 Oct 2025 22:12:38 GMT  
		Size: 30.5 KB (30462 bytes)  
		MIME: application/vnd.in-toto+json
