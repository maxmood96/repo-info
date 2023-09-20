## `clojure:temurin-20-lein-2.10.0-bullseye`

```console
$ docker pull clojure@sha256:3ab065d76422361fbd020448f507de4151f9650d7714d0a82a48734f0d906a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-lein-2.10.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:68bdc2e48d0363bbd47426cb88a65254c092c69fd97e777ce3545479d0194e7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227109435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26cf9ea36678148fb81a3fecb3162222b2ec5d5f14b8f25302d2e8762b1de020`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:51 GMT
ADD file:85db4f4c5016f51f7112a5d09cb7d4620f565a1379ae4b8a03c5ffc23886a876 in / 
# Wed, 20 Sep 2023 04:55:51 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:21:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Sep 2023 07:30:40 GMT
COPY dir:6a540db71f2a37db361084aee8addd6817cd7c4f18237e6f852a38e98bdb4182 in /opt/java/openjdk 
# Wed, 20 Sep 2023 07:30:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 07:30:42 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 20 Sep 2023 07:30:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 Sep 2023 07:30:42 GMT
WORKDIR /tmp
# Wed, 20 Sep 2023 07:30:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 20 Sep 2023 07:30:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 Sep 2023 07:30:56 GMT
ENV LEIN_ROOT=1
# Wed, 20 Sep 2023 07:31:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 20 Sep 2023 07:31:00 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 20 Sep 2023 07:31:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 Sep 2023 07:31:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ddf874abf16cc990e0fd75a154a34ca0a03ee310ad895a18fb62ae15bf4171fb`  
		Last Modified: Wed, 20 Sep 2023 05:00:41 GMT  
		Size: 55.1 MB (55056714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a007c5ad34070f89dbff4bf982cc317cb01a9169574dbff83d366a9de54c350b`  
		Last Modified: Wed, 20 Sep 2023 07:39:09 GMT  
		Size: 153.8 MB (153791726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802b8a3214de946ff49a3267eec629651c36a0fbf56d452dc8fbf26dc201482d`  
		Last Modified: Wed, 20 Sep 2023 07:38:57 GMT  
		Size: 13.9 MB (13861296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f081d14279c61c4d77387ed083cc7ec4677782dd918f3e38a7f46d57619447d`  
		Last Modified: Wed, 20 Sep 2023 07:38:56 GMT  
		Size: 4.4 MB (4399299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bd288bc9d858c18f3b7dd59cd85414f0c334a980bcd10747d683697b3dd18b`  
		Last Modified: Wed, 20 Sep 2023 07:38:56 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-lein-2.10.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fbff2930867e71633406afb765260a88e298cc21aa55425a9bb150df22bc075d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224073793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec17005c87d08e91a2b58aeb7c7d0a79aa5f90ee16203d043035333b1f9b80d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:45 GMT
ADD file:6bc001e951ef1280f566a92e65fcff57aefb8a280aa3510b7cd4b4e0a54c5cff in / 
# Thu, 07 Sep 2023 00:39:46 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 09:03:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 09:11:44 GMT
COPY dir:d35c6357dd030960bb6081f48b2bc10afb3da11efc1525ff916214b03be70ddf in /opt/java/openjdk 
# Thu, 07 Sep 2023 09:11:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:11:48 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 07 Sep 2023 09:11:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 07 Sep 2023 09:11:48 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 09:12:01 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 07 Sep 2023 09:12:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Sep 2023 09:12:02 GMT
ENV LEIN_ROOT=1
# Thu, 07 Sep 2023 09:12:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 07 Sep 2023 09:12:04 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 07 Sep 2023 09:12:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 07 Sep 2023 09:12:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:61c16b7975697b00760ff9536c09eed29b6a76923d4d98be38e9cdc749506417`  
		Last Modified: Thu, 07 Sep 2023 00:43:21 GMT  
		Size: 53.7 MB (53704716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc354c706869eba40a152aca0c1d130fcc77393eba6caeec4c0c4b6b5a1cb1b8`  
		Last Modified: Thu, 07 Sep 2023 09:19:09 GMT  
		Size: 152.1 MB (152120013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4158df1c8d9375e418051ef9c797ba0bc1ca2fbc79c08691dbe40ee61951f5`  
		Last Modified: Thu, 07 Sep 2023 09:19:00 GMT  
		Size: 13.8 MB (13849397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee2e1ba838dd99a4def865122822232b9b626745b0a0136433acd95789332e0`  
		Last Modified: Thu, 07 Sep 2023 09:18:59 GMT  
		Size: 4.4 MB (4399267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c440be4a733098d5598c40b7f5761192119e69283afe0ae014e1c1a99d0466a`  
		Last Modified: Thu, 07 Sep 2023 09:18:58 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
