## `clojure:temurin-8-alpine`

```console
$ docker pull clojure@sha256:1392a9a06ef6034adbe059bb4f7902fb6bc3fac7e6f4126764251757aeee854d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-8-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:02c16f7e733b0c181dde7e0344cde9e25ed378c7b90167babc2fb855420c8ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140284048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6834203bfb7eff333273ddae9896973bd387ed35deab33f17467b590093d1953`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='525a7731331cad502b9293ccb4ac2b13e85516736e98a57cb27c2767005188e1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
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
	-	`sha256:83a5b4e8863d905ec4a9cf899ab58456bbf5e69c77c880195237b730f54b1ec3`  
		Last Modified: Thu, 25 Jul 2024 17:25:28 GMT  
		Size: 101.6 MB (101550154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7fb9bd12016294f8b7643104b6af5b98398ca45d4f000a0492f82f5b017db9`  
		Last Modified: Thu, 25 Jul 2024 17:25:17 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b196e5c22826b2e8a8b0eea7dc9ff9697a5aba3c119d627499ba7285ec46698d`  
		Last Modified: Fri, 23 Aug 2024 19:24:23 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae467486410207e4922458581319da11e9f6382d4eb0f60c00b0a2eea0545c4`  
		Last Modified: Fri, 23 Aug 2024 20:01:42 GMT  
		Size: 25.7 MB (25713191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd7716ad2c277bb25ed18e2e891dd05e3bf4d70710d9dfe975bf361a364cebb`  
		Last Modified: Fri, 23 Aug 2024 20:01:41 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:216b65c75cc60541e5fc2bdcd7d734b3a5814be38080da7b9367a4c22e1c49d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **942.9 KB (942864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03d4fdc5e79c82357e2f855bc90a7f4527ae529721ed2120352d44d06f51f0a`

```dockerfile
```

-	Layers:
	-	`sha256:b1fef10fb20a39015ba5d6ef2140591370e14e4b4c3daa83a3db2560ff8901ca`  
		Last Modified: Fri, 23 Aug 2024 20:01:41 GMT  
		Size: 929.5 KB (929542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89ca1fdc6332e61e7cece65a437d5bded2b891b92df60b3e4541d105a942738a`  
		Last Modified: Fri, 23 Aug 2024 20:01:41 GMT  
		Size: 13.3 KB (13322 bytes)  
		MIME: application/vnd.in-toto+json
