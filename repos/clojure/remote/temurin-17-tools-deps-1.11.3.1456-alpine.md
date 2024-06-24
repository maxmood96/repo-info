## `clojure:temurin-17-tools-deps-1.11.3.1456-alpine`

```console
$ docker pull clojure@sha256:2a49c43efa40829ec1ae81fc9c0ceda20429601a92237e234016fe30e6549410
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.11.3.1456-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:2d905b7b3c5eb1edf964c77d72865b72584740974bceba6a86980f8a4c1e2742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185904076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62583d7f0a75c52174780d7d2c0613947c912147ad4343f51c6e1de7401a84d2`
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
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='839326b5b4b3e4ac2edc3b685c8ab550f9b6d267eddf966323c801cb21e3e018';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:f1b5e1235bfbe173503864b0745991f6acbc1cb3cc585db25db55cc975d8c4a2`  
		Last Modified: Mon, 24 Jun 2024 16:42:55 GMT  
		Size: 144.3 MB (144332006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b1cd3263773d4ffacbc48e3c623670d0f823ddab3860cd77eb3e012e2c02a`  
		Last Modified: Mon, 24 Jun 2024 16:42:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48fadb2170d58cb6bea4140e5d4cad7173488b82a2763a9f56369fe59647a1b`  
		Last Modified: Mon, 24 Jun 2024 16:42:43 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f14873a5cb651b7d08bc498ee0f1081b5195fa8bd20f98683836e35348666dc`  
		Last Modified: Mon, 24 Jun 2024 17:55:51 GMT  
		Size: 25.0 MB (25010252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e430e47dbe8fc56e408af1fe5618f42dbf4dda9d9a4f44ed53a394421349294`  
		Last Modified: Mon, 24 Jun 2024 17:55:51 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477f9f066421f7da9aee904f5e8ea31bbe56b6ac77eb36fd441d14c04ed3270a`  
		Last Modified: Mon, 24 Jun 2024 17:55:51 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.3.1456-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:a507b0f44a908cdf3276c88c93f7dbc7cfc556b9e10e10654598ec206f913db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1348793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bab5f9f114a7a5a84fb766a360201750452990f126af134deadfd49304fd28`

```dockerfile
```

-	Layers:
	-	`sha256:bbb8ef7f3c0b84f242f3779ea4d2bbcfab2ecd4cfdbbdc935ff6b9b30c0f4917`  
		Last Modified: Mon, 24 Jun 2024 17:55:50 GMT  
		Size: 1.3 MB (1333392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8956f5dd376254a1dc615100facdfa822a1e9e7128b9ae478ca97895030c1228`  
		Last Modified: Mon, 24 Jun 2024 17:55:50 GMT  
		Size: 15.4 KB (15401 bytes)  
		MIME: application/vnd.in-toto+json
