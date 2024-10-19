## `clojure:temurin-8-tools-deps-alpine`

```console
$ docker pull clojure@sha256:b0596dcfba27e96ce46de324b259843a8477ce2b8d6cc1ccbb2d6133c1b942d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:141b53eeab0f595f0315d2b5aa7e184c81b2d46064030522e5e8dde18a6a392e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140525896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cdaa55dc36876813fd48f2362c8de6ca128053849f4bd2e9e728ed85d910366`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='525a7731331cad502b9293ccb4ac2b13e85516736e98a57cb27c2767005188e1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0210391ff06386c858b74d27ffa9aa8216d62faff8a1a2b8cda5a7443bde9684`  
		Last Modified: Sat, 19 Oct 2024 00:54:56 GMT  
		Size: 9.4 MB (9389054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c493cdb4e467167231a52b19c3c347c1bad39ef0d36290b76197a57070523a3a`  
		Last Modified: Sat, 19 Oct 2024 00:54:58 GMT  
		Size: 101.6 MB (101550149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799853a821993f97b0bbe41959b5714f589bb3eba5b54f2ba9bc56ad9389e0e9`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1759b110d7b8c023033f17c4a086e83a7eb738d3df75b4be5aaddf1f34209387`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 2.1 KB (2129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39305d66b4c2cdec25e65218de7a2f5fa24d1646b0b4a90375e83cfb612b2d1`  
		Last Modified: Sat, 19 Oct 2024 02:07:45 GMT  
		Size: 26.0 MB (25959977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4a35713a21c246ec5e140971d80c6eb6344846c1f594bf201d97b246bd593f`  
		Last Modified: Sat, 19 Oct 2024 02:07:44 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:e879a0eef12d8952f201b8033fe3905f3848ab5d10076683e7d51f2a793d82da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1194903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1b84eac2e88af6e0bf8184b194d0450b00c327f7b2bf71711bf4a8378d6870`

```dockerfile
```

-	Layers:
	-	`sha256:f20b502391bd9dc4e3698985f5b3a187c13df67f4837334af6c958c21dd733d2`  
		Last Modified: Sat, 19 Oct 2024 02:07:44 GMT  
		Size: 1.2 MB (1181495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8890b45d8ad0bd67675fe16562584e1383e35031c12d65e47270bfcbdf220690`  
		Last Modified: Sat, 19 Oct 2024 02:07:44 GMT  
		Size: 13.4 KB (13408 bytes)  
		MIME: application/vnd.in-toto+json
