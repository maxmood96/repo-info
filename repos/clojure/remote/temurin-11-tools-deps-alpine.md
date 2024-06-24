## `clojure:temurin-11-tools-deps-alpine`

```console
$ docker pull clojure@sha256:73219aadb60531933764957eaffe63d36a7d0ec97dcd5728ddf140e675843571
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:02a51cba56b12f237a75a3053943619e2c283f9db3798b940749dd32a61e7495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.7 MB (177653852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce97e64ebfa8e4c7d9fbc376a81c70c16dd51e4c9ed8952d0c187ce3c291fe4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b45c467be52fe11ffd9bf69b3a035068134b305053874de4f3b3c5e5e1419659';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d23e9cf3a3a50104650ef5ced46aaea90097d347ea2de4ac6d383c714d6fe4`  
		Last Modified: Mon, 24 Jun 2024 16:41:30 GMT  
		Size: 8.5 MB (8537069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e3336067725637c55fdbcd20e8a64786177f18166b657a4676d9b8e378f1da`  
		Last Modified: Mon, 24 Jun 2024 16:42:15 GMT  
		Size: 140.7 MB (140685991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3014df4eef3d2e0ed43e1d03a3b79d6853c942a9b81cdc42d0614c9c1490d3fd`  
		Last Modified: Mon, 24 Jun 2024 16:42:04 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a87d9f826d1396dfa75d4d7283b254f05bf8100bdacaa3c4b005bfa774b79e4`  
		Last Modified: Mon, 24 Jun 2024 16:42:05 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de224d8f67fd9a5f15fa788638eec4191c9a55393a6cf993b02657859cecbfa5`  
		Last Modified: Mon, 24 Jun 2024 17:55:51 GMT  
		Size: 25.0 MB (25011930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e13afec7f469fa31770b84c8bdef250ebcdf8eaa258ee8e0a6b99c4a71f6ba8`  
		Last Modified: Mon, 24 Jun 2024 17:55:51 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:decda63aa29706e6c8e057d03b6886524887d99f22f3d05034aea6764f22d5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1251812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc11c78fdd99a654542dc33841032f33323fd2ba5e1a600d335ca8306ff60a5f`

```dockerfile
```

-	Layers:
	-	`sha256:96ef8ccc58d2296e452db0d12a0e9f2059f0aedee064917ba6ea8169808dade9`  
		Last Modified: Mon, 24 Jun 2024 17:55:51 GMT  
		Size: 1.2 MB (1238481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15281b7eda4302544494ab265bde48fdb9c60a0be94362eb6456c8ff7d75209e`  
		Last Modified: Mon, 24 Jun 2024 17:55:51 GMT  
		Size: 13.3 KB (13331 bytes)  
		MIME: application/vnd.in-toto+json
