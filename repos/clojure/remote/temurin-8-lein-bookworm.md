## `clojure:temurin-8-lein-bookworm`

```console
$ docker pull clojure@sha256:90130ee89ceb9ff8fbbc128cde74cd78bb9315453420f2930895a2c930479675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:2b9fd655b94d04a27d8294ccc304ab7f0a521d479d649c5d2011ebffad0c68f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177092099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83de2cc646a423faa1761d99496b4cb59d8bd6d803a60c569895f9a4b7d058d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:41:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:42:17 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:42:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:45:16 GMT
ENV LEIN_VERSION=2.11.1
# Wed, 31 Jan 2024 23:45:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:45:16 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:45:32 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 31 Jan 2024 23:45:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:45:32 GMT
ENV LEIN_ROOT=1
# Wed, 31 Jan 2024 23:45:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 31 Jan 2024 23:45:35 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638eb245e4649122c3cde175020b7b674960d80dc7cec3f2975ba51d86bc7a4d`  
		Last Modified: Thu, 01 Feb 2024 00:05:10 GMT  
		Size: 103.6 MB (103591896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f30b524112f0b0c0ae93972edd089725dc1cd0d235694dc58042bf867477e6`  
		Last Modified: Thu, 01 Feb 2024 00:06:18 GMT  
		Size: 19.5 MB (19517260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dc634e4f32f68b36974126bcdd0cf873a4d384f12604e4e99d8d441ad8c9eb`  
		Last Modified: Thu, 01 Feb 2024 00:06:17 GMT  
		Size: 4.4 MB (4399189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0a95f8da3c7728cadf1abd46bacf963b7db6f5da52e2e863a08673d7c4a8e55d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176055454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e0d3bc788cb946b1951467a0f1b5fbc96b8bdf85c03572bf5ff6bd6930f4803`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:18:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:19:09 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:19:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:21:49 GMT
ENV LEIN_VERSION=2.11.1
# Thu, 01 Feb 2024 06:21:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Feb 2024 06:21:49 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:22:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 01 Feb 2024 06:22:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Feb 2024 06:22:04 GMT
ENV LEIN_ROOT=1
# Thu, 01 Feb 2024 06:22:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 01 Feb 2024 06:22:06 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b427f51620767e3cfcd5376d7a199da31d4e087e65e7c8baa20d06efb81dd05d`  
		Last Modified: Thu, 01 Feb 2024 06:39:02 GMT  
		Size: 102.7 MB (102703057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea828c3b5d7bb551a4bb578112cc1aa7d87a1c5c597b9023a24aa2e2509afd80`  
		Last Modified: Thu, 01 Feb 2024 06:40:03 GMT  
		Size: 19.3 MB (19337943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1400f6b28d0cabddef87e77a440a842cf29d7ac8f6a9ad5ae8f575f25569edc3`  
		Last Modified: Thu, 01 Feb 2024 06:40:03 GMT  
		Size: 4.4 MB (4399158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
