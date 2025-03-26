## `eclipse-temurin:24-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:2b88976851406a7f185e9636656e578c8284a498dacaf77e1203a575e43cf84d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:24-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:636966f0f27f16e222c53831e4b48f2d89d9248e13c30d9bd4a6ad542743bfae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.8 MB (80838614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535718a1c6810038128e49f2da6039274d4052b075ec87d25eda421b02b13099`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='0bc8181c7e85d55bba652503db62e60846439f279271d583b740ac70f9f5ae87';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_aarch64_alpine-linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='0f738719d0483d6fe7f08a1371d1c696d68dcfe39f073b4241673f35ffc8d655';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_alpine-linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f58dde68648321dd7b7e908dbd6cf5af75338262a80dbe218289fe7500fb67`  
		Last Modified: Tue, 25 Mar 2025 21:57:42 GMT  
		Size: 16.2 MB (16176295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723935d86ab46519f740d3348af94a989ced0e5b61f52297223cdbf8bbc9e661`  
		Last Modified: Tue, 25 Mar 2025 21:57:44 GMT  
		Size: 61.0 MB (61017664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d260acd0c1e84493fd1d3942cfea2b25b0f76f1bf071ef645a3f037778998f02`  
		Last Modified: Tue, 25 Mar 2025 21:57:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881f81a442e62a473c053e65d790b33bcc2b7c09329a02ade1cff8918fa0284f`  
		Last Modified: Tue, 25 Mar 2025 21:57:42 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:fad26f387e7c7e1d9ccbb9e0831680656092af4823e75cd73c7b89f1a6699e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.6 KB (920635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8827a8a8851cac843382d06b696a51420638ab513e7b3ec9e91f609aec1ec2fe`

```dockerfile
```

-	Layers:
	-	`sha256:7e19391cdcd11f31817af54ad70f7aa17335c46cd050bf6936776ef628099137`  
		Last Modified: Tue, 25 Mar 2025 21:57:42 GMT  
		Size: 901.0 KB (900957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:246f224fdf59f60cdda5f449073151c4699123d87d861c6913338a220e3769fc`  
		Last Modified: Tue, 25 Mar 2025 21:57:42 GMT  
		Size: 19.7 KB (19678 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:3ed9c9764adea80d3d2c986a09ac76854203f74fd1a9b745ba484fe19baf4aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80139346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ea497d730913d7e4a8cdc7028607f1ff9f2c237e9b4472b1b8d58d4950e883`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='0bc8181c7e85d55bba652503db62e60846439f279271d583b740ac70f9f5ae87';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_aarch64_alpine-linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='0f738719d0483d6fe7f08a1371d1c696d68dcfe39f073b4241673f35ffc8d655';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_alpine-linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126be689628518e8e17412d8b07297eb9bf2ffefb790eac9852dbb57a3b139eb`  
		Last Modified: Tue, 25 Mar 2025 22:05:40 GMT  
		Size: 16.1 MB (16138902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4813982b458786e66f7b3aefff82ba7d4a1b6f8bc7b0bb966571916953afebda`  
		Last Modified: Tue, 25 Mar 2025 22:05:41 GMT  
		Size: 60.0 MB (60005008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4d24309f919493251bff9154f7aee82ab950ec60516e465e0d03761d6e4fcf`  
		Last Modified: Tue, 25 Mar 2025 22:05:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96880898a26da0a93d10dac075d8cbba6a7d080020bd88993a1cda6041ef135`  
		Last Modified: Tue, 25 Mar 2025 22:05:39 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1c0e76eae2216d9da422defe1dd16a5ec66cd970f1a465fa09155162ce5344cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.2 KB (920204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa0ccfdf15ca78af56e8f21700dddd642ef5ff8a1301ed4d6d20ec18458e697`

```dockerfile
```

-	Layers:
	-	`sha256:a914f928deb5ba2f2936f53f890964fe4cc9b328e1dab97fedecf3950749b2e7`  
		Last Modified: Tue, 25 Mar 2025 22:05:40 GMT  
		Size: 900.4 KB (900392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c01a8572e1d0b2a306c9a8aac14effb8a5fc1f30c7bf97bdc92dfa4a32b110b4`  
		Last Modified: Tue, 25 Mar 2025 22:05:39 GMT  
		Size: 19.8 KB (19812 bytes)  
		MIME: application/vnd.in-toto+json
