## `eclipse-temurin:21-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:c66fa42d953a423c50a66284ab88989f4761a5bbed4cc0fd38c7e84f30164cbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:8f44829b456f0185dbc21b3f76bd8798cd6721eacf886fe2881d58326a9e487f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72695309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7f2a5e8076511cb61a9359be677e08ebd0fa74895df412d32fae0ab4522b6e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952e47caa173372e8d1fb746202867277967eb946e2d93b27acdb17e7ceba791`  
		Last Modified: Fri, 14 Feb 2025 19:25:45 GMT  
		Size: 16.0 MB (16023419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0b517f93b451f989f06377bdb3cdae2e789a3001ca4c353d297e8e770d9da6`  
		Last Modified: Fri, 14 Feb 2025 19:25:46 GMT  
		Size: 53.0 MB (53042584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994d61579febcac2124b7793e99401cf4dfaffc2d5b2c467dafb6e2c629ce2a6`  
		Last Modified: Fri, 14 Feb 2025 19:25:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028bdb4ba1d30ce07296f6ff11888a3572f586ef2f31f0f2c33f91352f0ae214`  
		Last Modified: Fri, 14 Feb 2025 19:25:44 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0cedaea455e6d0aabfbda6082888c0d63924b8720beb3ec213d1e19846c7c4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **904.9 KB (904903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46dadd5b15a6392936b5abc11cfc4034fe97d60ce2e526786637db8f4604a3e`

```dockerfile
```

-	Layers:
	-	`sha256:8689840964fc67790914ce2f6890eb22b86b835555de0d81a2a5b2a8b1cccf6e`  
		Last Modified: Fri, 14 Feb 2025 22:14:39 GMT  
		Size: 885.8 KB (885847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd8659523b22ba5dad2e9eed0c61327eb8113970e41bab5b0a744df316885764`  
		Last Modified: Fri, 14 Feb 2025 22:14:39 GMT  
		Size: 19.1 KB (19056 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-alpine-3.20` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:1c90f578fd4abc1b7c9dc589e710acca6d2e4507d7726d20b2aa13f16e608662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72396016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd310df107750cae09fe7b73351dffaace1a5af32ea771ab17f4c15369f03fa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
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
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539ef939d4f3419215ec7a0fb03915a0ee2eae3cc91741b20cdc867be6436ac8`  
		Last Modified: Thu, 06 Feb 2025 23:38:29 GMT  
		Size: 16.2 MB (16187864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffdd12de503a425f2b2d1ee2dc7ab8ab9832cfe606b7568329c721fedd316dd`  
		Last Modified: Thu, 06 Feb 2025 23:38:31 GMT  
		Size: 52.1 MB (52114975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8725a8dc5fdc7bb1759e5321d865027830a86834385ff61838bbdcc3d5b81d0`  
		Last Modified: Thu, 06 Feb 2025 23:38:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04b5f47f9bfec0be30d3a3d0eb737886ad1ea3a40602dd6bc4945da3edb6a42`  
		Last Modified: Thu, 06 Feb 2025 23:38:28 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a3720a8e7a481f930e8e1b3fa8e8c0d62abfd775b9ac12144fd752e9cf0b06f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **904.4 KB (904427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194827f5ff254729345ccd25299c80e56fa6c81dbb39856c8995dd937827ce03`

```dockerfile
```

-	Layers:
	-	`sha256:7ca1cd7d44ca730cdf406989cf7b51fd1e60542a5edde9964cd8b0069b9d8a56`  
		Last Modified: Fri, 14 Feb 2025 22:14:40 GMT  
		Size: 885.3 KB (885261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c64c4d324a4fb0509e43a03527f407899263253cdf7d8b0db775fada3bb554f5`  
		Last Modified: Fri, 14 Feb 2025 22:14:41 GMT  
		Size: 19.2 KB (19166 bytes)  
		MIME: application/vnd.in-toto+json
