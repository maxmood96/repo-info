## `clojure:temurin-8-tools-deps-1.11.1.1435-alpine`

```console
$ docker pull clojure@sha256:6f0057a5f5ef5c6bd0d0ff57a225ebb81e8e3354e385e1725d49670282e4c724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-8-tools-deps-1.11.1.1435-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:acad8bbc7dab304c312692a015cd6b6a9617bc1c290e4878b52d4a03e1cb6d9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138476117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65b334435059b5367436024a40c9482c7d6e792d27dbda5b2f59752580e7d03`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
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
# Wed, 24 Apr 2024 21:16:13 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:16:13 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:16:19 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Wed, 24 Apr 2024 21:16:19 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:16:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21a63612cbe8d148f75173be90696fbe03e2a6e9c901e2c039bcf1bcdeec0b9`  
		Last Modified: Thu, 28 Mar 2024 02:02:51 GMT  
		Size: 8.5 MB (8537401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55c1055a2ad6292da34c7007392014a7a5a8939d32d297c43fa65f0faaec5bb`  
		Last Modified: Wed, 24 Apr 2024 19:06:44 GMT  
		Size: 101.5 MB (101520753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22a846daf1a23fd92d6d59d3dba57bda463e910cd200bb9914603682a117fd8`  
		Last Modified: Wed, 24 Apr 2024 19:06:36 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3546951364d504cdce98ebf79d8e5f55edd67fe2ac6b83e4c6e13afbfed84ba0`  
		Last Modified: Wed, 24 Apr 2024 19:06:36 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7749d4597790a6972f97bff4f100065890db04d458b74c0dbbedda82be5dd60d`  
		Last Modified: Wed, 24 Apr 2024 21:41:27 GMT  
		Size: 25.0 MB (25007718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e8b94b5c6139f4a9a78f6cf660b677874465abaa4948f9982343c2620a0beb`  
		Last Modified: Wed, 24 Apr 2024 21:41:25 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
