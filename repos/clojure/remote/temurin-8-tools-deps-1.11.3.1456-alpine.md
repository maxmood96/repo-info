## `clojure:temurin-8-tools-deps-1.11.3.1456-alpine`

```console
$ docker pull clojure@sha256:cdde6cae75120dbc3298c259d074d8dac861f211d0cb66df00c36219af865189
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.11.3.1456-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:d2b87f915d65372286947ba064f339c35d1ac980797e7dec69163048ec5540ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138488700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc55224608a2e10ee883ed25cc9671d74facd657059c332bc0344b44a46f1449`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='409091665e5f8cf678938bbbc0d377122ef8bad7b1c97a0f809da054db956e51';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d23e9cf3a3a50104650ef5ced46aaea90097d347ea2de4ac6d383c714d6fe4`  
		Last Modified: Mon, 24 Jun 2024 16:41:30 GMT  
		Size: 8.5 MB (8537069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc6adfa5160bd12e83b59556783ab9eabc84aa2760d4c7a4823c2e95f75b288`  
		Last Modified: Mon, 24 Jun 2024 16:41:36 GMT  
		Size: 101.5 MB (101520834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47088dc4b5e1c76206ce81c2c850479e9725a3401136522f20580e79b3502f0`  
		Last Modified: Mon, 24 Jun 2024 16:41:28 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030d7df500581b0e06a747613d5976dd0a4dc43c7fd50ca6863a3dd8f3bb42f5`  
		Last Modified: Mon, 24 Jun 2024 16:41:28 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222097bdea79b7daf3c76fc76f7036415abe375d4740c8ec473631cddfa1f4e9`  
		Last Modified: Mon, 24 Jun 2024 17:55:49 GMT  
		Size: 25.0 MB (25011952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7704cbea6e1d3590b8048ed31f1bbe8e0af3a75f2adf2dedcc1ed3e023d061ff`  
		Last Modified: Mon, 24 Jun 2024 17:55:49 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.3.1456-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:918caad266743a030127a886d4c931b9dc8f2b16e427b07a1e7e6f9321458625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1273323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e1f0184d6f1e509f6e722e2f1e8cad98b6cf70f95f012a13a5e8e1459dc056f`

```dockerfile
```

-	Layers:
	-	`sha256:d9b9dc96498686e2df696bb0e59c4b275b0930ed81a7f712225c832c085cca3a`  
		Last Modified: Mon, 24 Jun 2024 17:55:48 GMT  
		Size: 1.3 MB (1260006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec822685290719545d437443c12f4760d81b6cb4f4e8a4aecbe9990e0463ca31`  
		Last Modified: Mon, 24 Jun 2024 17:55:48 GMT  
		Size: 13.3 KB (13317 bytes)  
		MIME: application/vnd.in-toto+json
