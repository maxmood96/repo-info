## `clojure:temurin-17-lein-2.11.1-bullseye-slim`

```console
$ docker pull clojure@sha256:e01930f58c3e5b67f6775c2a0c1b7650c4de51f90fab57d467bde02aa93f16b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-2.11.1-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7a7a1790ee5b9568be324a916e5154caf75edbd55dbc8c784cfb54666902351e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 MB (195774140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3372308788528f28ac3018150c16f060a2e583d1b683281e3e229d02d03bbbbd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 17:19:49 GMT
COPY dir:2765b9c6732dde1d622a6314ea7119038a6031d832e1ec655de4889b7fd05a2e in /opt/java/openjdk 
# Fri, 02 Feb 2024 17:19:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 17:22:36 GMT
ENV LEIN_VERSION=2.11.1
# Fri, 02 Feb 2024 17:22:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 17:22:36 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:22:51 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 02 Feb 2024 17:22:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 17:22:51 GMT
ENV LEIN_ROOT=1
# Fri, 02 Feb 2024 17:22:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 02 Feb 2024 17:22:53 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 17:22:53 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 17:22:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b6457fcb8b0261583156367d4c0b9e3b3d6e192b2ea1b69ebb7fdca7dcfc12`  
		Last Modified: Fri, 02 Feb 2024 17:37:00 GMT  
		Size: 144.9 MB (144893181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5b37865a81c5af4241cf0fe6474b790b45b0c75d4ee2f3c24cd18db3cb50ca`  
		Last Modified: Fri, 02 Feb 2024 17:38:13 GMT  
		Size: 15.1 MB (15063547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b7b72962c3c2eea3e08b7e0ae96767c1d27e875ebda5c06e9ee55a91d704ad`  
		Last Modified: Fri, 02 Feb 2024 17:38:12 GMT  
		Size: 4.4 MB (4399184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e9fce56bdc7532daa04267d31e879401c26565889ad4561d542dfa135762a8`  
		Last Modified: Fri, 02 Feb 2024 17:38:12 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-2.11.1-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4605befe47ce3df7db29316421b72cc669369e9a504c024e00be378b1171c3a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 MB (193235839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862b884761d34045335ab2479f73a1fab14a2698d78ad3ecd774aa399a1b28b7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:21:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 08:28:41 GMT
COPY dir:1e33e1b9b4d5ff1fcafcf70a5b147d046ddd08f2a0ffd21b97536e3a6e636c5f in /opt/java/openjdk 
# Fri, 02 Feb 2024 08:28:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:31:08 GMT
ENV LEIN_VERSION=2.11.1
# Fri, 02 Feb 2024 08:31:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 08:31:08 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:31:22 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 02 Feb 2024 08:31:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 08:31:22 GMT
ENV LEIN_ROOT=1
# Fri, 02 Feb 2024 08:31:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 02 Feb 2024 08:31:24 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 08:31:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 08:31:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88be844818cddfb9d70282106952cd5c045d860ee8c5e21a6db93d7361155140`  
		Last Modified: Fri, 02 Feb 2024 08:44:30 GMT  
		Size: 143.7 MB (143720879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7711445643bebcbe1fd61b7fb6296b231462ef6c136f41dec13106bb61130c1f`  
		Last Modified: Fri, 02 Feb 2024 08:45:40 GMT  
		Size: 15.1 MB (15051023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67064cf8129d4f0f1e6ffe53169604527f1236d06d6743bc9944134fcbba6b9`  
		Last Modified: Fri, 02 Feb 2024 08:45:39 GMT  
		Size: 4.4 MB (4399203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ade79bf44e447294e6a2ca2c7b5dbd9799f0ac2550d515ccbfc6b7be6ce6bf5`  
		Last Modified: Fri, 02 Feb 2024 08:45:39 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
