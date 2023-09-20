## `clojure:temurin-8-lein-2.10.0-bullseye-slim`

```console
$ docker pull clojure@sha256:029fc56700727b07c3b6369ba4fc1f05872b88496578a1829df23b68327df000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-lein-2.10.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:593ffef8a82a8cdb04a461db0f3702a603e4de7a3cac93392a6d128e5ad59335
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151978311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294b9b61691057fb9b88af8d1ed5127e058b355bdab406bb20ad0ec040a2de8f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:22:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Sep 2023 07:22:28 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Wed, 20 Sep 2023 07:22:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 07:23:33 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 20 Sep 2023 07:23:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 Sep 2023 07:23:33 GMT
WORKDIR /tmp
# Wed, 20 Sep 2023 07:23:47 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 20 Sep 2023 07:23:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 Sep 2023 07:23:47 GMT
ENV LEIN_ROOT=1
# Wed, 20 Sep 2023 07:23:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 20 Sep 2023 07:23:50 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d904e0e0acb14ab36621cdb61a83d87d553b53cafbe8016f9cc443e19e4ff9`  
		Last Modified: Wed, 20 Sep 2023 07:34:08 GMT  
		Size: 103.6 MB (103585017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3eccc6903ca032ef7450314bdc70a092678f78fa795ed855b9bf87bebb2b173`  
		Last Modified: Wed, 20 Sep 2023 07:34:34 GMT  
		Size: 12.6 MB (12576350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110be2504c8891f57c566d1b69e3cb0282f4a46cd8bae9d9f7e54f58bfde5441`  
		Last Modified: Wed, 20 Sep 2023 07:34:33 GMT  
		Size: 4.4 MB (4399233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-lein-2.10.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0c0a4acca9c1451509c861aac28faecd4737960787de1077135a20b1d14b5815
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.7 MB (149716304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99f3cfa101fcafb3987ea7c224e7f09c502ed6401f4ca569a469018515ae967`
-	Default Command: `["lein","repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:46:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 09:04:32 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Thu, 07 Sep 2023 09:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:05:27 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 07 Sep 2023 09:05:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 07 Sep 2023 09:05:27 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 09:05:41 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 07 Sep 2023 09:05:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Sep 2023 09:05:41 GMT
ENV LEIN_ROOT=1
# Thu, 07 Sep 2023 09:05:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 07 Sep 2023 09:05:43 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256b28be577c49d6f216cda63c69699c76582076b787ffcf77067af08f7f0490`  
		Last Modified: Thu, 07 Sep 2023 09:14:43 GMT  
		Size: 102.7 MB (102690458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b4b4005a8abc8a26c98dbd59d759fba23833c26ddef28a01edbc72c56f97941`  
		Last Modified: Thu, 07 Sep 2023 09:15:07 GMT  
		Size: 12.6 MB (12563664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b39fbf09d7b92927017f3b93b0362a2369f33e630753baa3d477049f9cd0ac8`  
		Last Modified: Thu, 07 Sep 2023 09:15:06 GMT  
		Size: 4.4 MB (4399279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
