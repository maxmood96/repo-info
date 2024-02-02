## `clojure:temurin-17-lein-2.11.1-bookworm-slim`

```console
$ docker pull clojure@sha256:9808c98884623026fb167b07ff27dc062c660343786bce4295b9d0b2d87265c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-2.11.1-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6b83266eaa4974405170431454bbe1989f7d8f76ddfbd2f602c76dbd82b5e5bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195929785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73576f6d5265d96b8a8423dd0663085103803d178ef927b50a9be384d91388bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:43:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 17:18:40 GMT
COPY dir:2765b9c6732dde1d622a6314ea7119038a6031d832e1ec655de4889b7fd05a2e in /opt/java/openjdk 
# Fri, 02 Feb 2024 17:18:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 17:21:51 GMT
ENV LEIN_VERSION=2.11.1
# Fri, 02 Feb 2024 17:21:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 17:21:51 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:22:06 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 02 Feb 2024 17:22:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 17:22:07 GMT
ENV LEIN_ROOT=1
# Fri, 02 Feb 2024 17:22:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 02 Feb 2024 17:22:09 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 17:22:09 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 17:22:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d7efeba6e82ed6b263a3a20620e986ed4521adda8da2894ddc213ef6994c1f`  
		Last Modified: Fri, 02 Feb 2024 17:36:17 GMT  
		Size: 144.9 MB (144893201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7740ae13c221a98e38f4233073eb49440534ae239072b824c3bea4988ad49e81`  
		Last Modified: Fri, 02 Feb 2024 17:37:53 GMT  
		Size: 17.5 MB (17486554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bf14fd5aa749ea29fd5eb014e4dfbb87c7191db2a6a992b17a2923cafe6200`  
		Last Modified: Fri, 02 Feb 2024 17:37:53 GMT  
		Size: 4.4 MB (4399163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cb3dcd70cb3b8c1bbb7ae5778864f896d55dd1d7c3b91764bfde53899ac2a3`  
		Last Modified: Fri, 02 Feb 2024 17:37:52 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-2.11.1-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b4edd6c50d3c8a13220179d55316985d2bc5a6a6dd7be76d2bf4f922fb37a0c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194611246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed4e90444820353b89b2ad12efba6cf68a153f29d8ceeee2653f3829dad56ba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 08:27:34 GMT
COPY dir:1e33e1b9b4d5ff1fcafcf70a5b147d046ddd08f2a0ffd21b97536e3a6e636c5f in /opt/java/openjdk 
# Fri, 02 Feb 2024 08:27:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:30:29 GMT
ENV LEIN_VERSION=2.11.1
# Fri, 02 Feb 2024 08:30:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 08:30:29 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:30:43 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 02 Feb 2024 08:30:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 08:30:44 GMT
ENV LEIN_ROOT=1
# Fri, 02 Feb 2024 08:30:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 02 Feb 2024 08:30:46 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 08:30:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 08:30:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a2971378842cba2355c934edd4fe1c223f5b855eb23918cd0885b86957c0ae`  
		Last Modified: Fri, 02 Feb 2024 08:43:54 GMT  
		Size: 143.7 MB (143720893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93e75351834e11ba14b99afef599295ca0ad6946ac6f7fd45ce3eda5a688463`  
		Last Modified: Fri, 02 Feb 2024 08:45:20 GMT  
		Size: 17.3 MB (17309956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7416a097b73df408956af134a475de5e8a6d7e0d24d2f2e31f06088e489d5e`  
		Last Modified: Fri, 02 Feb 2024 08:45:19 GMT  
		Size: 4.4 MB (4399164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf59901f435f68b6ec9de761766f48fc80295b84a36cc317403b4751884e6a1`  
		Last Modified: Fri, 02 Feb 2024 08:45:19 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
