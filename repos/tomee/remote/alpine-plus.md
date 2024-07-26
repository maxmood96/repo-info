## `tomee:alpine-plus`

```console
$ docker pull tomee@sha256:1114ce2e287c60bfa83edb8e2129fd7328e363403190502f44f94ebdb40947b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `tomee:alpine-plus` - linux; amd64

```console
$ docker pull tomee@sha256:ab0f4ab1bed0cc6d03b42ce50015c7bda19381067c53066d06c66c913223bd9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136866977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f15ca80651ba6be7d6fd4304fafb2933c6d6e3738a811148901779b5a96a5e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 18:18:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Jul 2024 18:18:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 18:18:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Jul 2024 18:18:20 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 23 Jul 2024 18:18:20 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='0ac795729cc11f47323a71713eac2a5b22d4615fd9b66c8766f964c03fb6e160';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Jul 2024 18:18:20 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 18:18:20 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
WORKDIR /usr/local/tomee
# Tue, 23 Jul 2024 18:18:20 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
ENV TOMEE_VER=9.1.3
# Tue, 23 Jul 2024 18:18:20 GMT
ENV TOMEE_BUILD=plus
# Tue, 23 Jul 2024 18:18:20 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 23 Jul 2024 18:18:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dff7dc6fc2858af0a16833a15a63741d58d895a9d1a9a2de411e9921a0de0dd`  
		Last Modified: Thu, 25 Jul 2024 17:25:18 GMT  
		Size: 9.4 MB (9394889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f8a9a7eca8da1b2932de2c5fa1eb4007ddf65fa392396f72c70563b8c7949d`  
		Last Modified: Thu, 25 Jul 2024 17:28:51 GMT  
		Size: 43.6 MB (43555987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7704bfc5cc02cf7405989987e6a665316ff35d8e70c951331104f3e2fc7d073`  
		Last Modified: Thu, 25 Jul 2024 17:28:46 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabee84202d486cb813bb1655e65bfaa0607816e36aa61d673e89b51669e9d4f`  
		Last Modified: Thu, 25 Jul 2024 17:28:46 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ebc0296fa4cd5cb3c4524bf1198397a47111a39f31720cf9675b9cee408949`  
		Last Modified: Thu, 25 Jul 2024 19:06:17 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83afc05457d57fe89f79f389eec557cfee84d993d96142dae63ac084adaf3b56`  
		Last Modified: Thu, 25 Jul 2024 19:06:17 GMT  
		Size: 6.7 MB (6739731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99bf572ffe5d9b9681b0ad924b520edce60ebcaad48028c5748a763a2f8241b`  
		Last Modified: Thu, 25 Jul 2024 19:06:17 GMT  
		Size: 69.2 KB (69223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23f8002136c7ec2ae473e78f0eed390a17dc758ff9cb29766a5926d44916b38`  
		Last Modified: Thu, 25 Jul 2024 19:06:18 GMT  
		Size: 73.5 MB (73482050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:alpine-plus` - unknown; unknown

```console
$ docker pull tomee@sha256:8a24782b2c8378a51b9a094a3a0ec59c43969d61fea1aac8b60b9d0efc7fa022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d091fb123b10d8c3ebf5b660adc3a5e753b03e09ffd8ff73d9c014c235821f`

```dockerfile
```

-	Layers:
	-	`sha256:e4c3b07aa326c016a010016ac3a94fa5795d683215718cce89b41751e0dff93d`  
		Last Modified: Thu, 25 Jul 2024 19:06:17 GMT  
		Size: 1.2 MB (1166710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d4fda1751ae95a5876e42697436d9c420941878a558cff1e1b9c5e2a83a09a7`  
		Last Modified: Thu, 25 Jul 2024 19:06:16 GMT  
		Size: 28.7 KB (28709 bytes)  
		MIME: application/vnd.in-toto+json
