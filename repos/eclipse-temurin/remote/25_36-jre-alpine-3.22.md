## `eclipse-temurin:25_36-jre-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:0be0f9b8c4c9c55bd97194ed84f0751f639f5712d9e99a45a0d65bf49f57bd08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:25_36-jre-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:a1420b2a50a5f4664e0c38e56e9a2a39f68ff8b5dfca58c1c369e54a1135854d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77649467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b946315746301aae243df0a5e9aafdfbe531a47a41d77e78498ac50dd48683`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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

### `eclipse-temurin:25_36-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0adcb41aebbc5d4a79c07c2c51e45de013bb27d6e42fae7d4beec325eaeefadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **817.6 KB (817633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc4cb4addb6cdbd60c0867092f81db86512775bb6acb739b8950d1dc07f900c`

```dockerfile
```

-	Layers:
	-	`sha256:83ed6bc1f8a59d1131f3fc1857e7dfdfcb0d2f27801b13562e9cc93753a1424a`  
		Last Modified: Thu, 25 Sep 2025 21:15:19 GMT  
		Size: 797.8 KB (797843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89d641bbc2d386fe16976c84b1f83512c46024363e2f976ff03d0d21a7a43c9d`  
		Last Modified: Thu, 25 Sep 2025 21:15:19 GMT  
		Size: 19.8 KB (19790 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25_36-jre-alpine-3.22` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:48fadff941b5ee2f6cf65a63a4efe431b9eb8158568527a3804942bdf377aca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77200534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc528ba3b74b33caa95afe412e6c7980a0159b0597dfd9e117e1133a24bd091`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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

### `eclipse-temurin:25_36-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:bb438bbf9f00c469f684832d998c521ff3588a8afb1b9dd56da54360e8c29987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **817.2 KB (817202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511467df01f94049c95c24d01bd010d5c4c78b9b82a1a35f1c7990b239ea622c`

```dockerfile
```

-	Layers:
	-	`sha256:7d1eade8ecfb01f81c055abb422d123bf7bcac5aed9539cef2f259bb644a7df1`  
		Last Modified: Thu, 25 Sep 2025 21:15:24 GMT  
		Size: 797.3 KB (797278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e16bd8fb8d8fa74a16cda6d547cac946d331d057a09f05d1563322e89e960581`  
		Last Modified: Thu, 25 Sep 2025 21:15:24 GMT  
		Size: 19.9 KB (19924 bytes)  
		MIME: application/vnd.in-toto+json
