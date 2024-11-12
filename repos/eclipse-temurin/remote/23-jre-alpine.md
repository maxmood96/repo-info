## `eclipse-temurin:23-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:f0330e8c0d4c1850bae45e040f929ab75d8daf08b72c15840e9059b87db71cae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:23-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:7cae1b94f9bf48580ccc04262faef7bc80a8a26c3628ebc861f2edf499ba5584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75058310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116b89359bf1c0d9955c6ab30064043fba8bb84ab3442634a0011a1957f5bf0d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='b56eaedc094cb9107be2d5be9ad34c3dd9492c45aa671d102b5829a488cfc744';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='38a1b20b5ee8869b20e9f9aefdc91eedf245584d35287842a66540f0745dd3d0';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031dc3da24c32d543ef3d1dc74909b5c73f41b2b00887a61155556829603fbc4`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 18.3 MB (18307509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb22fe02bfc680b619b183c5de032b8cad8cfca2c7c308e9dd42419a4357019`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 53.1 MB (53124488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417fc8c2adaa4903fcf9747fcf908b9c01c0c5295fd184c9bbc66513893041e4`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78fe47fe453af682fad0d120e9e4f2a5c05f85ebe5e3bdec8014fc7020c9c7d`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e52bb0b36837dd94892eae3d7d3250f7cad359aab44ca5adbb96c8151d10dd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **906.3 KB (906294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c03ae83fe42647ab7a1378355595123ccec220180646be8997be1f7371b457`

```dockerfile
```

-	Layers:
	-	`sha256:6ffef7ff297c43c51b55d1c467f80ab7f9b9b252141725cffdf9e3c98a045048`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 887.2 KB (887205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee2c8ac3082241c5ace68ce637bd2a79b2ae06e4666b09253c78bf840abffdc`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.1 KB (19089 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:0a174a47f2b058a12aba5757e9264304546bb34ca784bacb54b01d16d4e06ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75042929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd09529cd562a95682ed8ad1de4d9fd3bc64d4feb8292c25008da8a8a743512`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
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
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='b56eaedc094cb9107be2d5be9ad34c3dd9492c45aa671d102b5829a488cfc744';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='38a1b20b5ee8869b20e9f9aefdc91eedf245584d35287842a66540f0745dd3d0';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690c1c3c12311099b849c7ad59a80f61f93631107a83ac61ee77c9d267e42913`  
		Last Modified: Thu, 24 Oct 2024 01:17:10 GMT  
		Size: 18.9 MB (18876774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc87b0d40598477f553b2c76c15a47d1049deb5dd86655ad7503cd935f0ececf`  
		Last Modified: Thu, 24 Oct 2024 01:22:14 GMT  
		Size: 52.1 MB (52076102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9aa2ade209641ae6dd4cd944d6cef79bd4dfc32b0fd9ca8e00619a699b10a3b`  
		Last Modified: Thu, 24 Oct 2024 01:22:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22305b7c26b1b0d7bce41e501fa68e65f2c9510bd6ae6aace101449072ffc3c0`  
		Last Modified: Thu, 24 Oct 2024 01:22:13 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:11aefaaf37576d7c27ee2d35a6db828a2506938a5e92c6efda2bdc617681144c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **905.0 KB (904995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339cbce5ae1ab47bd9602262d6a3fe0b6fb2d6cfc4089f3978459b30d84de049`

```dockerfile
```

-	Layers:
	-	`sha256:4aa20e89e7ddf7e4d24768e87ce57595cfdfc41562eb65f85cd503d51d89c5ab`  
		Last Modified: Thu, 24 Oct 2024 01:22:13 GMT  
		Size: 886.0 KB (885995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87b24d2b4caeaaab1d8818b2140334c9333f4c5372750b4b3a56ea2506bdbcd7`  
		Last Modified: Thu, 24 Oct 2024 01:22:13 GMT  
		Size: 19.0 KB (19000 bytes)  
		MIME: application/vnd.in-toto+json
