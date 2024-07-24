## `clojure:temurin-11-tools-deps-1.11.3.1456-alpine`

```console
$ docker pull clojure@sha256:9379fa698cda1ef6cd55b3e3da702606a80538e18ddad3a72aaf9e3ee14335ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.11.3.1456-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:2c5602ae14f1f66c03c009f784955e7e4f796c5b7bcc8f5eecdae61a19d326a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178473149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8a34ead048e972f30ccdf1b8657a2838877c7e41f5f1e7fa5b1c3aa8c83f0b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sat, 20 Jul 2024 21:06:39 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='ae988c72eeb2d78bb729a3387601ce0ea84305734ebdbe95d276f39952a8e019';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b502c76566e71337b4737a25ae762dd54193bc78dba7f7474ea005c07de9efc`  
		Last Modified: Tue, 23 Jul 2024 01:08:16 GMT  
		Size: 8.4 MB (8371901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b385df864585b78915877316205cb3db2f799121531a5b9ef0a5d3be3b9ad4d`  
		Last Modified: Wed, 24 Jul 2024 01:26:25 GMT  
		Size: 140.7 MB (140723469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc6876caaa094de9bc2be784ba085f5b032565c209919eda08c5556b21c7992`  
		Last Modified: Wed, 24 Jul 2024 01:26:14 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f669f0607d0b48e33e36400177b61a6ea6b8071450e76c7fb5c6f9d82c3ddbb`  
		Last Modified: Wed, 24 Jul 2024 01:26:14 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff0c5f209db712fdda86987cc54e8a77a7c0331d7b87e00380b1c3a699ae6b4`  
		Last Modified: Wed, 24 Jul 2024 02:03:46 GMT  
		Size: 25.8 MB (25752642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35af69508205fac672854ebecbce401a998c32a17d173ddfe014445a0eb14d25`  
		Last Modified: Wed, 24 Jul 2024 02:03:47 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.3.1456-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:8c6de0cbdd8dd7f6f82dd9aaf089b8c1d6f64e82b3e5de89373c944f1210aa83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **900.0 KB (899973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443e6cfcacf8f4671e7f3d502eec4e3925c9d48244982cd5719b84c49536d20f`

```dockerfile
```

-	Layers:
	-	`sha256:c461c26c2395fabafa5140d8f0e82fb483f5296007c5b24c27ecb620e28598b5`  
		Last Modified: Wed, 24 Jul 2024 02:03:46 GMT  
		Size: 886.6 KB (886637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73debb3dee9b16cad01c49dc0963ac6a03766045a9ba5e45531a98111d1f1889`  
		Last Modified: Wed, 24 Jul 2024 02:03:46 GMT  
		Size: 13.3 KB (13336 bytes)  
		MIME: application/vnd.in-toto+json
