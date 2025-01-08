## `tomee:alpine-webprofile`

```console
$ docker pull tomee@sha256:3b33dd08505cdfd3062203fab7d3f8b23a21afb67f4079a9c08a90f4c53bb7d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `tomee:alpine-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:d91e08f45f2e7db42d8089476af292633145a534a02c74afec44ebbc36d8d65e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132871123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b40bd425c9d610ca46e09e8f1ee1f699c29790eb7ceb72ba8420d66e9ffd114`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='12b988a3d934e3eb89c6a981a93f8e2adf0a62cc9030487dee76c0c29b93714d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        x86_64)          ESUM='2dfa33fb8e9474e6967c6cf17964abb5ddce9c17fa6a9f8d7aa221a0ae295df9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 29 Dec 2024 01:38:24 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 29 Dec 2024 01:38:24 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
WORKDIR /usr/local/tomee
# Sun, 29 Dec 2024 01:38:24 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
ENV TOMEE_VER=10.0.0
# Sun, 29 Dec 2024 01:38:24 GMT
ENV TOMEE_BUILD=webprofile
# Sun, 29 Dec 2024 01:38:24 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Sun, 29 Dec 2024 01:38:24 GMT
EXPOSE map[8080/tcp:{}]
# Sun, 29 Dec 2024 01:38:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 23:53:52 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc442151d2c70db4810e987819a87bcc66ea2b637ca5678e865d5b76b8e5312`  
		Last Modified: Tue, 07 Jan 2025 03:31:18 GMT  
		Size: 16.0 MB (16005491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561de8b096d4deabdaa687f9cc13e926407ae5b7c47ba9fb818606f9f3629344`  
		Last Modified: Tue, 07 Jan 2025 03:31:19 GMT  
		Size: 53.0 MB (53039424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fdc4c445f81fc2c82c81d2f687928774de7a42244b72327631f45301ab66de`  
		Last Modified: Tue, 07 Jan 2025 23:38:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32599ff3ca8cf029c2dccbdda0ac4f8fb115d5ec94b4f4abe92b852da1f19982`  
		Last Modified: Tue, 07 Jan 2025 03:31:18 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8388e395e8539ca7c497841e49895234425e7e3a7c364c997cd78dcf1aaa15c8`  
		Last Modified: Tue, 07 Jan 2025 04:22:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fd16c93433ee87ad77c188c8056cd1cba243fa6c0e96a9bae8ae7660d647a8`  
		Last Modified: Tue, 07 Jan 2025 04:22:42 GMT  
		Size: 1.1 MB (1113723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cd150334ef78952e00eb121ae5359dba072bb1d63f6fa9c53c6c6f6b17224a`  
		Last Modified: Tue, 07 Jan 2025 04:22:42 GMT  
		Size: 75.6 KB (75626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ef841446c78825023144f0650409b69c88663d4db344edea6f310ae707759c`  
		Last Modified: Tue, 07 Jan 2025 04:22:43 GMT  
		Size: 59.0 MB (59020252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:alpine-webprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:0ae519c7374a2e8d90c119fbcb4c48d663fb4644d50aec1c2c0ca1088f91bbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1186122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3918883310fbc9775210ff5b3a01acc4efe1ede5a4fc407a93917341482f5d5`

```dockerfile
```

-	Layers:
	-	`sha256:eea789a82f27c547810cbd46b572768e9932965a1cf3447fd2b06728c01587d8`  
		Last Modified: Tue, 07 Jan 2025 04:22:42 GMT  
		Size: 1.2 MB (1156880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ce01347a7c07f5375826b2e8ae30c1e00ae01ced40e6d63a1123145ab2073fa`  
		Last Modified: Tue, 07 Jan 2025 04:22:41 GMT  
		Size: 29.2 KB (29242 bytes)  
		MIME: application/vnd.in-toto+json
