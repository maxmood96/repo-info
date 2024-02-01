## `clojure:temurin-11-lein-2.11.1-bookworm`

```console
$ docker pull clojure@sha256:b3c5d643809d326c396938ab6bee381f8a3dcd4444fb04f984160a82943528b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.11.1-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:27f281719102e48b31fcff750309caf8d022a01d7096b829dbd97eadddb785fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218771181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42930d39f64f7a1538efab3e02faef27c110665978f566e9381caa534757954d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:41:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:48:31 GMT
COPY dir:e1ce96bca1c423a1c79b84eacb7ae69429353a37485cc24af4161ce4b9d3ee2a in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:48:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:50:54 GMT
ENV LEIN_VERSION=2.11.1
# Wed, 31 Jan 2024 23:50:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:50:54 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:51:09 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 31 Jan 2024 23:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:51:10 GMT
ENV LEIN_ROOT=1
# Wed, 31 Jan 2024 23:51:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 31 Jan 2024 23:51:12 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afe2d1272b0c5e9161314942fa02036caab8b5f924665169595a113d2b85488`  
		Last Modified: Thu, 01 Feb 2024 00:08:30 GMT  
		Size: 145.3 MB (145271031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59bc6d944bfb8fbf8f2393439e715b5b747f571cc539ec1ef210cf7e156c05c`  
		Last Modified: Thu, 01 Feb 2024 00:09:48 GMT  
		Size: 19.5 MB (19517200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2357df59c6906011d7d73ebad5245e12873289d0631fa82b8dee049a5eef2a7`  
		Last Modified: Thu, 01 Feb 2024 00:09:47 GMT  
		Size: 4.4 MB (4399196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.11.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b1a451bf9e04e1e67d1a02175e7038b483963ff49ee0bb04c67eeb1a4205ba4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215358886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601aa9751fa137614cbb48a8fa3f820b7ca672c6bd1a3b9a5e321ebfdf8a9fe3`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:18:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:24:31 GMT
COPY dir:454699b64b949edd3264b234e72a891ace37d538f2726c5ec754e17e6fb3fb19 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:24:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:26:46 GMT
ENV LEIN_VERSION=2.11.1
# Thu, 01 Feb 2024 06:26:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Feb 2024 06:26:47 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:27:01 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 01 Feb 2024 06:27:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Feb 2024 06:27:01 GMT
ENV LEIN_ROOT=1
# Thu, 01 Feb 2024 06:27:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 01 Feb 2024 06:27:03 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e0ac421e55bb8543ff3500ddf65c130f2d08b742a21b53522bcaa47b27c222`  
		Last Modified: Thu, 01 Feb 2024 06:42:18 GMT  
		Size: 142.0 MB (142006502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c4e5160692f83bdd9073d405029c4542845fdcc569e6191f87aa0e6b41e0ea`  
		Last Modified: Thu, 01 Feb 2024 06:43:22 GMT  
		Size: 19.3 MB (19337873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35186c756faa0f7a86c08430688e1d008c5775a3bdcf0bb8d16f963bec6dcd5`  
		Last Modified: Thu, 01 Feb 2024 06:43:21 GMT  
		Size: 4.4 MB (4399215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
