## `clojure:temurin-22-tools-deps-1.11.3.1456-alpine`

```console
$ docker pull clojure@sha256:68908e98d9628503490681cb64b815895868c2d1c356c712b66ab852c7d68d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.11.3.1456-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:e1119e435ddb90a6cbc84f3de44d7afbb0b693a6b03fab84be96bbe28aaa8590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 MB (198696933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c655fb9e3d389ef4ee5600898763493486b2bd23d74637ca6cbdde2fb6cb8db7`
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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Sat, 20 Jul 2024 21:06:39 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='8ac93a2d5a55aabbc0f7156c2f9032026e87c185689d628ef8a4184b6e9ab006';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_alpine-linux_hotspot_22.0.2_9.tar.gz';          ;;        x86_64)          ESUM='49f73414824b1a7c268a611225fa4d7ce5e25600201e0f1cd59f94d1040b5264';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_alpine-linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:8e118bbc909a65083d314d2da5fe1f703619cf9810828b0d739ed6962de633f2`  
		Last Modified: Tue, 23 Jul 2024 01:06:33 GMT  
		Size: 13.0 MB (13019343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db286bb27ed845b0633219d49e3c9b81f2c8fe547e4c14a6d4e3e4b3333d774d`  
		Last Modified: Wed, 24 Jul 2024 01:29:38 GMT  
		Size: 156.7 MB (156688129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232e7a0d670b44b1232c37aa9614181f139acc22c1ed85392a2094dff3ad6c18`  
		Last Modified: Wed, 24 Jul 2024 01:29:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d13279157e3b042d431a8a47a3e50c7e6667569de4add5c886b94e82ffff35`  
		Last Modified: Wed, 24 Jul 2024 01:29:26 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c23d9749de9258b45885ea8169ab9f10b7e3803b695495fd94004b3106da433`  
		Last Modified: Wed, 24 Jul 2024 03:04:06 GMT  
		Size: 25.4 MB (25363922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ef294332fd8d7f1452decdb4a63bbf8895b2d914095945289c5a34868b1963`  
		Last Modified: Wed, 24 Jul 2024 03:04:06 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d7191b007eb39b3811fb540d2b267ff42271680135c1af4cb5fa2e2addc180`  
		Last Modified: Wed, 24 Jul 2024 03:04:06 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:dab01506f6c95565c34ae72d3483b9a6bf29a0dade7b05f225e7fc0fe566261a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **995.6 KB (995620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f333bfb73089a30bdd79b483101cee7f7fc4f0ac3c698b42c1e4e686b93a8f4`

```dockerfile
```

-	Layers:
	-	`sha256:60a0b580d4a458fd1f846abad213db692f4412f81e4511b4a93019e8f17bf484`  
		Last Modified: Wed, 24 Jul 2024 03:04:05 GMT  
		Size: 980.2 KB (980215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c06b9525363dd90889bed1571591a0e00ea1744fe4d584a04543bdf8897966ad`  
		Last Modified: Wed, 24 Jul 2024 03:04:05 GMT  
		Size: 15.4 KB (15405 bytes)  
		MIME: application/vnd.in-toto+json
