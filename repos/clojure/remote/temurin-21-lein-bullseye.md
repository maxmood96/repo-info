## `clojure:temurin-21-lein-bullseye`

```console
$ docker pull clojure@sha256:64d0ce5fb3b2b594e49f93ac457f94b17d978f73a203515c2b7d68a06656e7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c7caa35704ab600265e583d747bddd0a9a9d9969583a535388220152f434b5ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235392842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8572dcda65f722f16f64272527e2375beb2cd6159ce581ce6e5168789947ae6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 00:00:14 GMT
COPY dir:64a8841762a9afbd2fb8b4cf497b2dee87765737d44ff0387ce1cfc51371c9a2 in /opt/java/openjdk 
# Thu, 01 Feb 2024 00:00:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 00:00:16 GMT
ENV LEIN_VERSION=2.11.1
# Thu, 01 Feb 2024 00:00:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Feb 2024 00:00:16 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 00:00:32 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 01 Feb 2024 00:00:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Feb 2024 00:00:33 GMT
ENV LEIN_ROOT=1
# Thu, 01 Feb 2024 00:00:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 01 Feb 2024 00:00:35 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 01 Feb 2024 00:00:35 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Feb 2024 00:00:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac4333b9c256cced06955a88cefbfd9b93fd1b42569f9c2ebda324bd77f6513`  
		Last Modified: Thu, 01 Feb 2024 00:16:25 GMT  
		Size: 159.6 MB (159582940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ea23be70cd8d789d147354e89828448af1f8e28c59f3a64e0c6512c7457fce`  
		Last Modified: Thu, 01 Feb 2024 00:16:14 GMT  
		Size: 16.4 MB (16353334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4f9c70051f4653488df943b23a9c6447b03d9055893fdf60467664d09c3515`  
		Last Modified: Thu, 01 Feb 2024 00:16:13 GMT  
		Size: 4.4 MB (4399205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a848f798902381f065b7a255a9ca05f60c842756bd990cc6c846b89fbbb0d27d`  
		Last Modified: Thu, 01 Feb 2024 00:16:13 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e25a392b8562dfcab72358ca8c5d2046a549bbf1e7138ea893af8a1372e71c69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232234411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d0e3c31b3da5fc91776e9a7e05f512b0ab50936e97e152cb7eec035b779e86`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:35:03 GMT
COPY dir:ab40534e435f9942975c0e8b5454d6b7a8d69c445f8e0758c1bd9c500e157fca in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:35:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:35:07 GMT
ENV LEIN_VERSION=2.11.1
# Thu, 01 Feb 2024 06:35:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Feb 2024 06:35:07 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:35:21 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 01 Feb 2024 06:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Feb 2024 06:35:21 GMT
ENV LEIN_ROOT=1
# Thu, 01 Feb 2024 06:35:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 01 Feb 2024 06:35:23 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 01 Feb 2024 06:35:24 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Feb 2024 06:35:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62cba91c04c8fb9fc51183c28a4bf7b61017854f51fbeceeb6d5042d36b85ab`  
		Last Modified: Thu, 01 Feb 2024 06:49:29 GMT  
		Size: 157.8 MB (157784601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ce7b8a6e16b6b9583d633c1daf87f890d00c1a8209774dc33f7b72c11bf763`  
		Last Modified: Thu, 01 Feb 2024 06:49:22 GMT  
		Size: 16.3 MB (16341962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1edfd79d0dcd09be11016989874da05ecde9b8b07c8ec639d030d320062fa86f`  
		Last Modified: Thu, 01 Feb 2024 06:49:19 GMT  
		Size: 4.4 MB (4399181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0247303798a14406df8bfdc3fd8b6fc3cf5901e66fad3200fa2ab26091f689`  
		Last Modified: Thu, 01 Feb 2024 06:49:19 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
