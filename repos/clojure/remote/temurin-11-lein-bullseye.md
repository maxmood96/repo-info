## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:2f482deb3055dc6f3bdc4f03be7f9405268371e4cfd60d43c5b3d42aeb4ab128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c05212c585c9ca2115a5751c938a71c44e9908bd1273ff4b44a186fe70488f0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271781681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4664dd4c340fbbc3d47270033cd0b60af4a83cd42fbc665942b16f17050eb1`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:40:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 07:43:44 GMT
COPY dir:fdbc5e9dec2946fa124877176e92a68dd3fe3a70def5bb906a6040c4a1303a2d in /opt/java/openjdk 
# Wed, 01 Mar 2023 07:43:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 07:44:54 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 01 Mar 2023 07:44:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 07:44:55 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 07:45:10 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 01 Mar 2023 07:45:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 07:45:10 GMT
ENV LEIN_ROOT=1
# Wed, 01 Mar 2023 07:45:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 01 Mar 2023 07:45:13 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0b29cc6adaf6091151573ab5a4ba12f03dcfaea1402985879aea0d535da14c`  
		Last Modified: Wed, 01 Mar 2023 07:56:45 GMT  
		Size: 198.5 MB (198475588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c903815af794a40dc99a1a2199bd31a3470300bf58733ccd6fc313a5ca83f0`  
		Last Modified: Wed, 01 Mar 2023 07:57:19 GMT  
		Size: 13.9 MB (13860892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fc14edb7501e2648990cc7142a9221c7039821e1c3630b80cf83303af1fd9b`  
		Last Modified: Wed, 01 Mar 2023 07:57:19 GMT  
		Size: 4.4 MB (4399279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:35c9f6e2d89fa5e7183ecd854109d430bf321143c81ef016d085b97c714d213c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267191693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0c47ed87772f942384cd67a38c5d6f8665a925b901b03f35173d98dee85057`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:01:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:04:01 GMT
COPY dir:b661686bf8d434588756c45f2ef6e7f314f32f753cf180ef8fb45397388f098c in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:04:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:05:10 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 01 Mar 2023 03:05:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 03:05:10 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:05:25 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 01 Mar 2023 03:05:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 03:05:25 GMT
ENV LEIN_ROOT=1
# Wed, 01 Mar 2023 03:05:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 01 Mar 2023 03:05:27 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db5f99a046fb93d70e363d58ebe237b913e09a889f35b330f65e0bfa4627f3c`  
		Last Modified: Wed, 01 Mar 2023 03:15:41 GMT  
		Size: 195.2 MB (195240319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47979a7ae2a5961627b6047339ba9b3fb3e9251fb8e33fc93c4b90ae7c5b07b3`  
		Last Modified: Wed, 01 Mar 2023 03:16:12 GMT  
		Size: 13.8 MB (13848912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7635054355d0af37f096af1c35c1ff9bb855ec705002fc74bb8841408532fb0e`  
		Last Modified: Wed, 01 Mar 2023 03:16:12 GMT  
		Size: 4.4 MB (4399247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
