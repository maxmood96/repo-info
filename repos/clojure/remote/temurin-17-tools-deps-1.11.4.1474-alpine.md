## `clojure:temurin-17-tools-deps-1.11.4.1474-alpine`

```console
$ docker pull clojure@sha256:52fcf215eb6129779fc5b90763f183603e0d597f0586b0833d11a191cb8a0271
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.11.4.1474-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:81ccebde712ff26b069f16f141535c68e9f2774aa31c99ebbd4bd3cf5d8e6132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187390977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1913a2d6f97bae1d5f97306d219183166f5126c7c28354122cf28a8c3c033a9a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='6d274a292a717a6f8d00a3ed0695497405c5c634c27fec1692dd13784f6ff6fa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["jshell"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
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
	-	`sha256:7beb93379603195c1cd0e0fa2dfd4b31ab5a9580ed4dd4cc301f4ca12c31c1ff`  
		Last Modified: Fri, 23 Aug 2024 19:26:45 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a6c182636b41535f5fb41af1aeb69ad4bb5ef8dade46231a2945f153aea626`  
		Last Modified: Fri, 23 Aug 2024 20:02:04 GMT  
		Size: 25.3 MB (25331079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af1daa294fed47d261c213a3fcc800f44a459f326c3911fb261b28e83d5f327`  
		Last Modified: Fri, 23 Aug 2024 20:02:02 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f95cfe390788545fde58f6511aec451756eca8ba1fdb190fd5955c95bf38179`  
		Last Modified: Fri, 23 Aug 2024 20:02:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.4.1474-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:ac6864b5ab5033f82d9d1693926420a8a57d67a7a0e8fe49f1abc80c551a4a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf67b7f36d7bd52ed303239acf5f1406f6fd640c53a2a9c489c07d51233af61d`

```dockerfile
```

-	Layers:
	-	`sha256:d422b3a47c47810975809869e790ba647db84dbd483fd370ab370221cc3d92a7`  
		Last Modified: Fri, 23 Aug 2024 20:02:03 GMT  
		Size: 998.7 KB (998741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d705a58ea4594c1a25ca987a968dd93df8e8263b9ae884e0b7c89bf833b1c0af`  
		Last Modified: Fri, 23 Aug 2024 20:02:02 GMT  
		Size: 15.4 KB (15406 bytes)  
		MIME: application/vnd.in-toto+json
