## `eclipse-temurin:25_36-jre-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:bf9c91071c4f90afebb31d735f111735975d6fe2b668a82339f8204202203621
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:25_36-jre-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:0c7880c8870e0753309bbe2ea8d789139d793ba0d11e3b2d9f5defdf7f3345be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75188082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64df8effbdba88e161711367bb2149e766dea9525cd4b856d0c50121a5eabd21`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 19:59:06 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87a5950d3a781d7cbae82ee449d1f2772e44fa3170d3aefd5a87f1f67f6996f`  
		Last Modified: Wed, 08 Oct 2025 23:33:07 GMT  
		Size: 9.4 MB (9420424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1577ea4e72642e6f4238fede21f347e9498e879261e989b4a2192a390f6c7672`  
		Last Modified: Wed, 08 Oct 2025 23:33:14 GMT  
		Size: 62.0 MB (61962796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c27339c34800a4155bbe75d31255745a05aec62afc2b93a678514990e2bdf3`  
		Last Modified: Wed, 08 Oct 2025 23:33:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4484b284405b11f788e71ff9c3c7a32d6c4805a75f969016f2a105cec1c4160d`  
		Last Modified: Wed, 08 Oct 2025 23:33:07 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25_36-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ddcf3589570aed53c01f4f738e54cdfbd3915f23857df1fd0a92d2a0678c229d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **820.2 KB (820242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f71dcca9f27bacf56cec68d0d3aef02a3656b4a6e325c5319f9ff643782ec6`

```dockerfile
```

-	Layers:
	-	`sha256:0e58d09ad5eebf7b9df3e7c0f88e3d82d57f533fa0037ef99009488bf429f262`  
		Last Modified: Thu, 09 Oct 2025 00:17:27 GMT  
		Size: 800.5 KB (800456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7714f8f6e06ac3aa23aca59b128bc85581c19f2241f1e1cfbd9972d830cd44e`  
		Last Modified: Thu, 09 Oct 2025 00:17:28 GMT  
		Size: 19.8 KB (19786 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25_36-jre-alpine-3.22` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:8e51b7782d3fcbad1271a1cfb97d8ad8c78d1501d8522c49447a90545050ab98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74443869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97d116129124f0ad388e465929386e0af7fb02e128bd1cdc2c956b2595b4174`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 19:59:06 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15626b9510e505ea847755b0f875e21ac709daa693aa60a0448f5a1c9b96a5d4`  
		Last Modified: Wed, 08 Oct 2025 21:49:06 GMT  
		Size: 9.4 MB (9434841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e9e130d8575f0b4944c57df7b25e9ed42f3263b5654c9307b9cf230f7800c7`  
		Last Modified: Wed, 08 Oct 2025 21:49:13 GMT  
		Size: 60.9 MB (60868551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8ec74a6484006af784aecd922412e0fe32e7e4eda10e225f6496fc82bce0db`  
		Last Modified: Wed, 08 Oct 2025 21:49:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61bbe768428636816f4a086d5689aa4510f9bc9c44ef5ee4a4cdaf531fd526b`  
		Last Modified: Wed, 08 Oct 2025 21:49:05 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25_36-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f1102e0a67598763a6ae3a9b91c51543bf0eb3c002e8921e3266f9aca459c666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **819.8 KB (819811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c73396cac61c1e87e086d9d9da96c5775ea479ff1ceea76b9126d2de9551baf`

```dockerfile
```

-	Layers:
	-	`sha256:35fc5b1d312e6cff7dcb7f7bc41a0c4d57fdd42b000726a154179e844c6f0d35`  
		Last Modified: Thu, 09 Oct 2025 00:17:32 GMT  
		Size: 799.9 KB (799891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6a3e1f78e0951b6c08dd6fe4283676d4c18d6526c5f43a3f40edd0d8610ed8f`  
		Last Modified: Thu, 09 Oct 2025 00:17:33 GMT  
		Size: 19.9 KB (19920 bytes)  
		MIME: application/vnd.in-toto+json
