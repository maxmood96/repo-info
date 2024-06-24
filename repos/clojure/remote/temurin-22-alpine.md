## `clojure:temurin-22-alpine`

```console
$ docker pull clojure@sha256:2474b710096863cb5d5f931be796af27c35e5d0108890a2436bbf897a6f75110
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-22-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:6c7c9db4b7e5b58e3f809850d2018a996ebeb7df164560d0689318888a4b0a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198506843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d190c0a6c568604214780233bd1ffbbe8f45a98b1e2d5451f64747be175bd06`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='86a7b47c9277f2fd063ec910616b3676d86553ab7d23aa3bd365e51a57be1dc5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_alpine-linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|x86_64)          ESUM='d226e44b3513942db855df9a8737d848f64069848970d4cfd35ee3c38f2525c1';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_alpine-linux_hotspot_22.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60acd7138d3e0a8e35e097d75b62e0b1cfd99cdad83e29656157ec622e1c51e2`  
		Last Modified: Mon, 24 Jun 2024 16:42:45 GMT  
		Size: 13.1 MB (13142550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5527a619aa80834ec27b7385ccfab9e813cd457497b97479cdec2826e62dfa62`  
		Last Modified: Mon, 24 Jun 2024 16:44:17 GMT  
		Size: 156.9 MB (156934764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c126c6df6080cc84c31effa92413e24655866a8450e9dc44e1749998dec1c00`  
		Last Modified: Mon, 24 Jun 2024 16:44:04 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48e2799fd549f5e211e628fc1acc4bd10b1562ec648dc1ebaeaf28a1bc5baff`  
		Last Modified: Mon, 24 Jun 2024 16:44:04 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc77d8c88e358e34a6dc928d94f984356e837dd7782e2b13826373721b92a22c`  
		Last Modified: Mon, 24 Jun 2024 17:55:54 GMT  
		Size: 25.0 MB (25010259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b78bf88f85a862403ed70f8172d8bd2442f12aad138558a9321648e800f3af`  
		Last Modified: Mon, 24 Jun 2024 17:55:54 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60690239698c056bc5ee4757a1a1f05e8121a8b0dd1c54398e01778ec5286b7`  
		Last Modified: Mon, 24 Jun 2024 17:55:54 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:ea23ccec4f67f3962f492b90a8182360319677308bc731d8bd9d1877f83d9a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1348785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0ec07c1a4971c0ed5b7afbfc3156c58ea372b6dd50bcbafb013e98b5a65bac`

```dockerfile
```

-	Layers:
	-	`sha256:4713a7d4d9467ad2036e3b4ad9f8a1427aa7eb05703ae74489e62cbdc02c3746`  
		Last Modified: Mon, 24 Jun 2024 17:55:53 GMT  
		Size: 1.3 MB (1333386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5f3985f0733b70d2dc544a5d021c491e22239e45f594be68544c6f3734fa856`  
		Last Modified: Mon, 24 Jun 2024 17:55:53 GMT  
		Size: 15.4 KB (15399 bytes)  
		MIME: application/vnd.in-toto+json
