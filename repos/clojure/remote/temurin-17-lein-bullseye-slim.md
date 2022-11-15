## `clojure:temurin-17-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:2aa23f1d7be3b23244edaf0c1c7ab081b783bd2c95fb9b953751a14aff15ecca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5717e0b9ebc74ab1b8194cf42eb42b7a2c04907166fd67231ca9997ea6b83749
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241226067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7ab62b5843a10c52de032a07a7403fce910c20cc027cd140f159408867fb36`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:05:21 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Tue, 15 Nov 2022 17:57:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 17:58:51 GMT
ENV LEIN_VERSION=2.9.10
# Tue, 15 Nov 2022 17:58:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 17:58:51 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 17:59:07 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 15 Nov 2022 17:59:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 17:59:08 GMT
ENV LEIN_ROOT=1
# Tue, 15 Nov 2022 17:59:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 15 Nov 2022 17:59:11 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 15 Nov 2022 17:59:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 15 Nov 2022 17:59:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1e2f15985394be21a4e4a010fbea73bcb4ac9c162a40582171119a45451824`  
		Last Modified: Tue, 15 Nov 2022 13:08:12 GMT  
		Size: 192.4 MB (192431277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1024347174b4b986e0e194e4410107adca1f1a0737846c1e0f57540ea5f15d4a`  
		Last Modified: Tue, 15 Nov 2022 18:11:07 GMT  
		Size: 13.0 MB (12983060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e303f7c512d13375c201766ecdc9ba24f5e0b0f76e8267bac71e06af4463b61d`  
		Last Modified: Tue, 15 Nov 2022 18:11:09 GMT  
		Size: 4.4 MB (4398701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d7efb46a2a2a9cb810a95ba6dd9f629854385bee7a2b14147ce0ab143c0644`  
		Last Modified: Tue, 15 Nov 2022 18:11:06 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e02c9e9805d803dc40f9caa73b5b1679824a7c1c4c4039111b30b989bf336174
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.6 MB (238645173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b221d4b1f066f607e6469c0f8fc6ea6d61ef045305a2f86313887c9f73d64aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:49:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:54:33 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:54:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 05:55:32 GMT
ENV LEIN_VERSION=2.9.10
# Tue, 15 Nov 2022 05:55:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 05:55:32 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 05:55:45 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 15 Nov 2022 05:55:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 05:55:45 GMT
ENV LEIN_ROOT=1
# Tue, 15 Nov 2022 05:55:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 15 Nov 2022 05:55:47 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 15 Nov 2022 05:55:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 15 Nov 2022 05:55:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0032fd948a5495fec37e26e9d086c7c0fa24d0623f43f8ad0471aac3350e5f61`  
		Last Modified: Tue, 15 Nov 2022 06:05:10 GMT  
		Size: 191.2 MB (191215234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1799269531987cb3cba632e6c1a9cde859bbda94811c815fc96e4618093d63f1`  
		Last Modified: Tue, 15 Nov 2022 06:05:34 GMT  
		Size: 13.0 MB (12970251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0a17b541071e9aaed04c55d7a7e4c0439f83a43cc852ab2603a34df84b4403`  
		Last Modified: Tue, 15 Nov 2022 06:05:33 GMT  
		Size: 4.4 MB (4398685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff328b1be761c01610011285950d67df7238cfb65be56cbb6f731f3cf5871a2e`  
		Last Modified: Tue, 15 Nov 2022 06:05:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
