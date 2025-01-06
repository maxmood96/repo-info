## `tomee:10-jre17-alpine-plus`

```console
$ docker pull tomee@sha256:b9f79e18fe112ca94acdae3e256c2f26e03d8129eb8b72cc8453905760e5bd9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `tomee:10-jre17-alpine-plus` - linux; amd64

```console
$ docker pull tomee@sha256:75d62f6a392bd6b47d87bc19ed3a856a89d3fc5c19aa0187ea32af0561cc59a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142086544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9770760562ad6c08ec67ad71217f45df7f7a0d8fbacc15b0696d7b363163532e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 23:15:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Oct 2024 23:15:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 23:15:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Oct 2024 23:15:53 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 16 Oct 2024 23:15:53 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7a2df4e2f86eca649af1e17d990ab8e354cb6dee389606025b9d05f75623c388';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 16 Oct 2024 23:15:53 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 23:15:53 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
WORKDIR /usr/local/tomee
# Wed, 16 Oct 2024 23:15:53 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
ENV TOMEE_VER=10.0.0-M3
# Wed, 16 Oct 2024 23:15:53 GMT
ENV TOMEE_BUILD=plus
# Wed, 16 Oct 2024 23:15:53 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 16 Oct 2024 23:15:53 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb8a593a4b7726f83576628ca6aa70220bcdcbef9651d003ba88727ce34d9d1`  
		Size: 18.3 MB (18307356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441f37ea86bb2ebd3f2d928c64e6d4c39686f25618e8847e957fee5ff58da0e6`  
		Last Modified: Tue, 12 Nov 2024 02:38:49 GMT  
		Size: 46.6 MB (46615858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44818f47c6831f333e1b9a5947c85124e4a12ca670bea7043d4b11beeb3a780b`  
		Last Modified: Tue, 12 Nov 2024 02:38:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cfa7e9b065bacf6029c8a0af5b63bb0e86ef13e828cb645d914da3480fbbfb`  
		Last Modified: Tue, 12 Nov 2024 02:38:48 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c5844fb40787dd403e81530c50de845d72508efd9c40bf667137b3fccac062`  
		Last Modified: Tue, 12 Nov 2024 03:11:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1296664e519f764a8039b803343a27749359e4f50ad626c2b69234db32a5d2`  
		Last Modified: Tue, 12 Nov 2024 03:11:29 GMT  
		Size: 1.1 MB (1113463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4487e671ca4e0b72739ace97b0edd8559e2110665fde4a62518bce2e3e45c0ca`  
		Last Modified: Tue, 12 Nov 2024 03:11:29 GMT  
		Size: 75.6 KB (75588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f7a0ef5502a6df7cff3f8fe59707d065c9bdcc16908cf5906eaa46b5ba0d52`  
		Last Modified: Tue, 12 Nov 2024 03:11:30 GMT  
		Size: 72.3 MB (72347765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre17-alpine-plus` - unknown; unknown

```console
$ docker pull tomee@sha256:82006884195a1bfe11daab1c58f62a0fe54f4455c236de0246ce9651c10ee303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1296988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8a7253bc2984082361e9674f9bbb5c9942edbb452965682414f5bb5fa9e6aa`

```dockerfile
```

-	Layers:
	-	`sha256:99a7c5dc2f25e3d10a0f8cb739a0d0ad5cb7574e233119959681553b8ca5ff08`  
		Last Modified: Tue, 12 Nov 2024 03:11:29 GMT  
		Size: 1.3 MB (1269210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5011f704c98e18565dfc1140552454e2eb51f64e86ecaf19f64e6af900d6ee2`  
		Last Modified: Tue, 12 Nov 2024 03:11:29 GMT  
		Size: 27.8 KB (27778 bytes)  
		MIME: application/vnd.in-toto+json
