## `eclipse-temurin:21-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:611529cce1e8840fb46d8f7f6d942d1951282b71bdc8dde0a454a008ea9cc081
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9d583aab76db86497a0223430ec6a86be97b3d6cdc9ac902b75155ceba116116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72693258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ffde9bf6fcc7086285f08d084f03f47ad4380587b7a9ed0ec3d0d4083bf97c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f7071e890eb7d0dff77491e391c11e2ed75e3e604948c55dc10a98c0971a79`  
		Last Modified: Tue, 04 Feb 2025 13:59:37 GMT  
		Size: 16.0 MB (16022006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff3482d37c2e398094813391c0c21119d516497d7a99c82305ab5b5a78474bf`  
		Last Modified: Wed, 05 Feb 2025 11:53:50 GMT  
		Size: 53.0 MB (53042586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bd8c3f867bc4d149ed55723d6add09d99da630af22b6ae779ecb10f865c3de`  
		Last Modified: Wed, 05 Feb 2025 09:30:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b264232eaba27c5507eaf4380be776895249a55726c570009bebba5ce0417406`  
		Last Modified: Tue, 04 Feb 2025 13:59:37 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:13966a112b64ab6653e56e2c525edf0420dea8775b09fa911ec5a5d12f2964c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **904.9 KB (904903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c60440ed85a4a6d95e7aa336588e2d8455f22743858f7f1f30d22605d9510e7`

```dockerfile
```

-	Layers:
	-	`sha256:4dd7454e82af98e89291f0d1c4fd0f4b01cd35052d3aff73d62e15e25235ebee`  
		Last Modified: Fri, 31 Jan 2025 01:30:57 GMT  
		Size: 885.8 KB (885847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:644f7c9614b4ad6856a891a31949a88c1e76579cb367966059221bafde23b8ca`  
		Last Modified: Fri, 31 Jan 2025 01:30:57 GMT  
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
		Last Modified: Fri, 31 Jan 2025 01:47:41 GMT  
		Size: 885.3 KB (885261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c64c4d324a4fb0509e43a03527f407899263253cdf7d8b0db775fada3bb554f5`  
		Last Modified: Fri, 31 Jan 2025 01:47:41 GMT  
		Size: 19.2 KB (19166 bytes)  
		MIME: application/vnd.in-toto+json
