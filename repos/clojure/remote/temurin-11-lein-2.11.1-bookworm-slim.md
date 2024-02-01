## `clojure:temurin-11-lein-2.11.1-bookworm-slim`

```console
$ docker pull clojure@sha256:9bb068626049e35c2eb83947dd78412c6a249beccd2cd8fb618083427d8ba2c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.11.1-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:86beec3d11cd3235f7358d4e1c58f756489b05fc0a4f995ab656582f8d7b3049
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196307166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2605baa24a33a9faff20996be612dc6c26dcf218e1fe9fdea01ed9f4ff1cd86`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:43:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:49:05 GMT
COPY dir:e1ce96bca1c423a1c79b84eacb7ae69429353a37485cc24af4161ce4b9d3ee2a in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:49:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:51:18 GMT
ENV LEIN_VERSION=2.11.1
# Wed, 31 Jan 2024 23:51:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:51:19 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:51:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 31 Jan 2024 23:51:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:51:34 GMT
ENV LEIN_ROOT=1
# Wed, 31 Jan 2024 23:51:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 31 Jan 2024 23:51:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5064ff6b6cb70868d3b2861016a4e99a9515996a6839bad68a869ad30eb6f8ff`  
		Last Modified: Thu, 01 Feb 2024 00:08:51 GMT  
		Size: 145.3 MB (145270941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26616751d2a9040d40b013396128c27e0966a88d80fbf482c81b3394f3f0fc2c`  
		Last Modified: Thu, 01 Feb 2024 00:09:58 GMT  
		Size: 17.5 MB (17486540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393f5ca7d9b3938191666624f78eaf81b3b032ff5bb7da72a9bf86517be58298`  
		Last Modified: Thu, 01 Feb 2024 00:09:57 GMT  
		Size: 4.4 MB (4399220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.11.1-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:78d4c7dbc8103dabfca3395c698c8c73721dccbb9e85ec6d975cc17c70c25c64
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192896433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62802d6fbd355497088d9e887cf75691dfe60b8ff9d82ce547421f3a89e0004`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:25:03 GMT
COPY dir:454699b64b949edd3264b234e72a891ace37d538f2726c5ec754e17e6fb3fb19 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:25:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:27:06 GMT
ENV LEIN_VERSION=2.11.1
# Thu, 01 Feb 2024 06:27:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Feb 2024 06:27:06 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:27:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 01 Feb 2024 06:27:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Feb 2024 06:27:20 GMT
ENV LEIN_ROOT=1
# Thu, 01 Feb 2024 06:27:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 01 Feb 2024 06:27:22 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c45e79333257621ebdb964760990997f3a264d1e457e0bfb0ba6e5b5865a5b`  
		Last Modified: Thu, 01 Feb 2024 06:42:36 GMT  
		Size: 142.0 MB (142006518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a805346bb250b262a0b43e632667164f855294af3ab60fcb138437645ec7dc4`  
		Last Modified: Thu, 01 Feb 2024 06:43:31 GMT  
		Size: 17.3 MB (17309911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd1725e86a01ffcc7e8b2271210c22fab2e81c7c25beb29cc9cddef8ca202bb`  
		Last Modified: Thu, 01 Feb 2024 06:43:30 GMT  
		Size: 4.4 MB (4399172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
