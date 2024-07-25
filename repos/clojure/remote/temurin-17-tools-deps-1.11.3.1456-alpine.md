## `clojure:temurin-17-tools-deps-1.11.3.1456-alpine`

```console
$ docker pull clojure@sha256:8586126e2de8864b477af0b445cddaa3099b19dc2df2c4c49fe2558a35a642bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.11.3.1456-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:075bbefdbbbabd330d1842421d10efc0ae2dca138c932a39a06261aa1d3f2b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187435518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1c04fe909af1412ec19d242a691ecf183ec758589535df0e3cf7c294906999`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["/bin/sh"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 20 Jul 2024 21:06:39 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Sat, 20 Jul 2024 21:06:39 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='6d274a292a717a6f8d00a3ed0695497405c5c634c27fec1692dd13784f6ff6fa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["jshell"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479e64820c602a6421582ff22341d66b5c6938bee2115d203f3d03147a89505e`  
		Last Modified: Thu, 25 Jul 2024 17:29:26 GMT  
		Size: 14.0 MB (14039136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e384a19a9b0cde9f53fc5c79a581f80b1606cb9b0c477b8019b1716ffe026fe`  
		Last Modified: Thu, 25 Jul 2024 17:29:36 GMT  
		Size: 144.4 MB (144394552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed71e81fa34c6c2e7902182aaf9da971d499b0e58d2dfcc2c789535bc6768e0`  
		Last Modified: Thu, 25 Jul 2024 17:29:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9ed14297063e3f9d673e7701f762b7d77112fe3f472e8b50399411d45457a`  
		Last Modified: Thu, 25 Jul 2024 17:29:24 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8a24e498b80220242b9387f6da5d390ab0d83c4bce977cf5cfc753b8c74573`  
		Last Modified: Thu, 25 Jul 2024 19:01:54 GMT  
		Size: 25.4 MB (25375857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be0f012433816ebaba2fb75be203c6438d2d55c16e9163c696e8f20397dc8b9`  
		Last Modified: Thu, 25 Jul 2024 19:01:53 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9402f69eed11a339fb5297bbc595e38047ada0ac8d91bd32c5d60e3a01dfa84d`  
		Last Modified: Thu, 25 Jul 2024 19:01:53 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.3.1456-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:5c28add26a9b4719dd565bc5782269a5f3cfe4bd64952fc0a1ff07c688775d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bde13889b8f2ba2ef33e01adc8586b85547fd2f1d390d2127b1740e5345968e`

```dockerfile
```

-	Layers:
	-	`sha256:57928ac87bfa4cfeb4cc8c877e01b355390051ee3dfc9da4a38c1fbd6ce8c351`  
		Last Modified: Thu, 25 Jul 2024 19:01:53 GMT  
		Size: 998.7 KB (998741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6e825fcec3d3ca7325a81a775fccfc242ed839bb23a282dd30e8b819556939a`  
		Last Modified: Thu, 25 Jul 2024 19:01:53 GMT  
		Size: 15.4 KB (15406 bytes)  
		MIME: application/vnd.in-toto+json
