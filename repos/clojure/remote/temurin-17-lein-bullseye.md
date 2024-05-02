## `clojure:temurin-17-lein-bullseye`

```console
$ docker pull clojure@sha256:bc4100c60b421cd7a4726e7ed143986c696d428c7086d23ec980afb19f98a38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c70a7a33107f0c2c43f3ac138d2faa0602e2da4d4f9d54b955e6b7a2d0a4040c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220947608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17577a37a8c67c2f3cf20d39a83830c95a098886b358a051d97101f7a2f5e60`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:37:27 GMT
COPY dir:d78c0cec90816231fd61ebcd7c27b07c1af0064b89c255fd2a157e0b344541d4 in /opt/java/openjdk 
# Thu, 02 May 2024 05:37:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:37:28 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 02 May 2024 05:37:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 02 May 2024 05:37:29 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:37:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 02 May 2024 05:37:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 May 2024 05:37:44 GMT
ENV LEIN_ROOT=1
# Thu, 02 May 2024 05:37:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Thu, 02 May 2024 05:37:46 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 02 May 2024 05:37:46 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 02 May 2024 05:37:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391faf0b4445debf40a16e0a0eabc23775d085761aa0ab4ced5a2239d961aaf7`  
		Last Modified: Thu, 02 May 2024 05:50:42 GMT  
		Size: 145.1 MB (145095180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b520387eebac267e4bc011d074faa0dccb2cdd23e44ac171cb3b02ff980ec182`  
		Last Modified: Thu, 02 May 2024 05:50:32 GMT  
		Size: 16.4 MB (16354995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add7fe86f1ed41322b99979f0608bd72562fbcbe508cc882904c097ce7274664`  
		Last Modified: Thu, 02 May 2024 05:50:31 GMT  
		Size: 4.4 MB (4398162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a578c101cd6d9315a3e4e0f683af6eebd1b67291449704954278d243f41136`  
		Last Modified: Thu, 02 May 2024 05:50:30 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:432ec98b3609c245a418b096b5c16e2ab0596a4a5ff5d6ead7c9018df8d4fe2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218374345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac29ac808bc4ab88c939af6629b1cb4410e24bbcb626951fb7c00456b636a43`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:34:49 GMT
COPY dir:317487729b1812635c51c5f305bd9178bd957a141903eab756a1683874b5752b in /opt/java/openjdk 
# Thu, 02 May 2024 05:34:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:34:52 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 02 May 2024 05:34:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 02 May 2024 05:34:52 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:35:06 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 02 May 2024 05:35:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 May 2024 05:35:06 GMT
ENV LEIN_ROOT=1
# Thu, 02 May 2024 05:35:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Thu, 02 May 2024 05:35:08 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 02 May 2024 05:35:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 02 May 2024 05:35:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c72cc73ccc61231ef93582824dc792a5a36e2ce7cddcdeafe99bff48bd71e4`  
		Last Modified: Thu, 02 May 2024 05:46:01 GMT  
		Size: 143.9 MB (143891839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e699f2fce28557d471047553032d30fe58831eb61e104a1712c1259fa5a2c7f0`  
		Last Modified: Thu, 02 May 2024 05:45:53 GMT  
		Size: 16.3 MB (16344048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3493b939bef3c83e8848f6e9145483aec7e1ae2d4e63abf7d0127982a63a1280`  
		Last Modified: Thu, 02 May 2024 05:45:53 GMT  
		Size: 4.4 MB (4398096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b6e6773c01de45d0cdcad78aeb62c43e0aaf03369f5ce18dadfaf71c55ea49`  
		Last Modified: Thu, 02 May 2024 05:45:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
