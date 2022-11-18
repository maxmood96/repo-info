## `clojure:tools-deps-1.11.1.1200-alpine`

```console
$ docker pull clojure@sha256:62808e2d710737e53206eedc7bbae3911318c19ac681a0cea0048113d3955b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:tools-deps-1.11.1.1200-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:d537df138133cd3f143b4917b0af4889b1f49f16839cdbc302cca02df16f0149
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236669888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f3c2bfcb6cf7a2644f2f749c96e06f820a73806503e33d40039984ffe9478ab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:12:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 12 Nov 2022 05:12:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 05:12:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 12 Nov 2022 05:12:06 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Sat, 12 Nov 2022 05:13:30 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Sat, 12 Nov 2022 05:13:49 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='cb154396ff3bfb6a9082e3640c564643d31ecae1792fab0956149ed5258ad84b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.5_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Sat, 12 Nov 2022 05:13:51 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 12 Nov 2022 05:13:51 GMT
CMD ["jshell"]
# Fri, 18 Nov 2022 22:25:37 GMT
ENV CLOJURE_VERSION=1.11.1.1200
# Fri, 18 Nov 2022 22:25:37 GMT
WORKDIR /tmp
# Fri, 18 Nov 2022 22:25:43 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "694381cb78d44f143bdcc38657507f012ebac4009bc57cec67abef1675447878 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Fri, 18 Nov 2022 22:25:43 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 18 Nov 2022 22:25:43 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 18 Nov 2022 22:25:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 18 Nov 2022 22:25:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9822f87bb1185b1d8f81aa09fc8a20796bb3db4c90da28c6177e0fd8a3d8d3`  
		Last Modified: Sat, 12 Nov 2022 05:16:37 GMT  
		Size: 12.0 MB (12030631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dd5a4c9d9b66950c491bf46b0fa319e048043eee4d4f74a473b0f27cd70589`  
		Last Modified: Sat, 12 Nov 2022 05:18:22 GMT  
		Size: 191.7 MB (191737252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5b1b0a2ab2f3efa0b93fa43b3aa8d8ea84d62cf5dc6bd850464f5c14e2cef3`  
		Last Modified: Sat, 12 Nov 2022 05:18:07 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987f2cdba77601c1e5f62ccb1bc57fdd739f42c22551663823826e7f4875e74d`  
		Last Modified: Fri, 18 Nov 2022 22:35:26 GMT  
		Size: 30.1 MB (30094530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd96367e49fde313f495736e17e14b20abaada5d362c93ee8409a91a5eccfe1b`  
		Last Modified: Fri, 18 Nov 2022 22:35:23 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d8d63ef37f01177c4d2343a4c599e591fbac0415173857346a56f4e431276b`  
		Last Modified: Fri, 18 Nov 2022 22:35:23 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
