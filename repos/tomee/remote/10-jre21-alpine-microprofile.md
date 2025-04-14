## `tomee:10-jre21-alpine-microprofile`

```console
$ docker pull tomee@sha256:fdf39dc1656c4df40139686c40f2eda72ef48991fa75b5c2f4467e7e02f7470d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:10-jre21-alpine-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:ce7f8a788a7302a3a44eee540fe6cdb1f64d89195c338b49d1a30caed5ce7eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143840809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050cb763dd06e7304beebca6b0c80aebaa02088bba93549c315a1a24233f4c4f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='bcd459e70cdddaa6ada0d855ce944c592814042f1e12d53aa08fa89eedcdf893';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.6_7.tar.gz';          ;;        x86_64)          ESUM='2330f38feb59ab7af0e2fffc12d5500005d35f7f53f49dd8a9f9aa1ae68aee5f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 07 Apr 2025 14:29:55 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 14:29:55 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
WORKDIR /usr/local/tomee
# Mon, 07 Apr 2025 14:29:55 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
ENV TOMEE_VER=10.0.1
# Mon, 07 Apr 2025 14:29:55 GMT
ENV TOMEE_BUILD=microprofile
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 07 Apr 2025 14:29:55 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f73af09931e6a98f19eff15f289cbb5720aa61efbdcb756e1b1328c6a3029f`  
		Last Modified: Fri, 14 Feb 2025 19:25:33 GMT  
		Size: 16.2 MB (16175578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729fc64ae8c10531863e7742349517e1e33610a8cbe4504a9254c56eb71e3f54`  
		Last Modified: Fri, 14 Feb 2025 19:25:34 GMT  
		Size: 53.0 MB (53042588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28bd5515264539666818f51e15663ee3b05d92b9b81fa4e187ed9e3a6594bc53`  
		Last Modified: Fri, 14 Feb 2025 19:25:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa1f65d07a350139d7390033a591e07d865c082f4b458bb56ff38bc143349c8`  
		Last Modified: Fri, 14 Feb 2025 19:25:33 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a70fe3a13677e67253a2dc556ee1b04b86a3aa85c55acda4fa811ed633650ef`  
		Last Modified: Mon, 14 Apr 2025 17:27:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59b776b4df5242bb1e163f59524790e56d91f2a0f68e25757eac8cf9b83eda2`  
		Last Modified: Mon, 14 Apr 2025 17:27:20 GMT  
		Size: 1.1 MB (1148433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5233a90b68ab8a4f8aa7299b2c1b2668c37b1e7dd633673fb5863cef257329`  
		Last Modified: Mon, 14 Apr 2025 17:27:19 GMT  
		Size: 75.6 KB (75634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b5ecec07359196e3cacc493c2ca1ad791ff4732ef9c6fb2ca23d8f75aa700a`  
		Last Modified: Mon, 14 Apr 2025 17:27:22 GMT  
		Size: 69.8 MB (69753715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre21-alpine-microprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:0bb7771426c74e13ffb578c5e16f880a9c4f1e33d9fa0e66f696cc136065bcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1315046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be908ee35f4d050187fa4abbd20e648b993584f854a10e29f1b7e016563a7aca`

```dockerfile
```

-	Layers:
	-	`sha256:7aee5f505826556e578bca4ec45ff457c143ba7389f6070d082fc60423fc137f`  
		Last Modified: Mon, 14 Apr 2025 17:27:19 GMT  
		Size: 1.3 MB (1280658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1bc76f50724b45316c8245a31a1da71cdf6a50e25770efe54b05c63ae00ef83`  
		Last Modified: Mon, 14 Apr 2025 17:27:19 GMT  
		Size: 34.4 KB (34388 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:10-jre21-alpine-microprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:5fb3d20e037b2c390e9a20ef21ebb24c369db2fac53a674d0454dff71d249b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143216786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6117b4100d136811572142dce6764eb4dc24b29c2ee7231cfe845bdd69cc2fb4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='bcd459e70cdddaa6ada0d855ce944c592814042f1e12d53aa08fa89eedcdf893';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.6_7.tar.gz';          ;;        x86_64)          ESUM='2330f38feb59ab7af0e2fffc12d5500005d35f7f53f49dd8a9f9aa1ae68aee5f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 07 Apr 2025 14:29:55 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 14:29:55 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
WORKDIR /usr/local/tomee
# Mon, 07 Apr 2025 14:29:55 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
ENV TOMEE_VER=10.0.1
# Mon, 07 Apr 2025 14:29:55 GMT
ENV TOMEE_BUILD=microprofile
# Mon, 07 Apr 2025 14:29:55 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Mon, 07 Apr 2025 14:29:55 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 07 Apr 2025 14:29:55 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ef25395adf8ce8e3c308217ae1b2fe858832aa585adde8a15afea0afa6aab9`  
		Last Modified: Fri, 14 Feb 2025 22:44:20 GMT  
		Size: 16.1 MB (16138226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37e07d3395bb04692c5f3233b0fb5ea666aa598ec3d4e93a2d240cfaf8cdd43`  
		Last Modified: Fri, 14 Feb 2025 22:44:21 GMT  
		Size: 52.1 MB (52114973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cbc2927b00beab74b56e4304a3d2cb94ad9f5f9ed8c25b32ba91d076c09d5f`  
		Last Modified: Fri, 14 Feb 2025 22:44:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77801c78fa6251fcc2de0386b1fce0c9e6545711e9fcc3ba7e892bd4ff35760`  
		Last Modified: Fri, 14 Feb 2025 22:44:20 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baba81a443d75732d53b0635347fcedfbb9abeddc67a08717e01f3b0c28ca1d5`  
		Last Modified: Mon, 14 Apr 2025 17:28:52 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9f0c2bfe722b9e2018674730e6116929d878a8857db79dc57ef7a40b825c73`  
		Last Modified: Mon, 14 Apr 2025 17:28:52 GMT  
		Size: 1.1 MB (1138578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c42ea40982abc863eabd2b641311b98852a8bcb6836c12cc948ef559e5c34a`  
		Last Modified: Mon, 14 Apr 2025 17:28:52 GMT  
		Size: 75.7 KB (75655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8bd429a060a76fdcd4965ee822bb928758d3b7156790979a36d12df34d9b78`  
		Last Modified: Mon, 14 Apr 2025 17:28:54 GMT  
		Size: 69.8 MB (69753711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre21-alpine-microprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:d912c36c50e16139450c10f28805e87d96650f20f12cd03961b9bd52912d92a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1315305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c87d874bff86648e15055181ab8de7566c13353b2dd0791e94b6ab071c66c1`

```dockerfile
```

-	Layers:
	-	`sha256:8a13e95fa463c0ca4335556687ca488472e48f6633088c14bda81bf655142e1e`  
		Last Modified: Mon, 14 Apr 2025 17:28:52 GMT  
		Size: 1.3 MB (1280432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eaefe7b09283f1d0721574c334ec9548e1fd03f022ea7744d274d3c719df9c9`  
		Last Modified: Mon, 14 Apr 2025 17:28:52 GMT  
		Size: 34.9 KB (34873 bytes)  
		MIME: application/vnd.in-toto+json
