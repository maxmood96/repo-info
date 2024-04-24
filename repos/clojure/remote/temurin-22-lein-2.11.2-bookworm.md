## `clojure:temurin-22-lein-2.11.2-bookworm`

```console
$ docker pull clojure@sha256:0a46551b17b7b66401f6502148dc192ed1ade6d1916f2c801a7e003196b499c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-22-lein-2.11.2-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:c4e586523cc369822f157dd475991afb04267776de92b281b34214f054ccf0af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230209204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f5a6252ca6fbca1a17718274dfe8126d1b83b89847d3c2f8da514e7610922d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:33:25 GMT
COPY dir:26aa9b736de249ab67b8c50e579c4c188c999c32408e8bbdcde37c30c2d0e7d3 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:33:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:33:27 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 21:33:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 21:33:27 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:33:43 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 21:33:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 21:33:43 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 21:33:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 21:33:46 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:33:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:33:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:522be7a11b3bc6b464f347d214d53851eff99fc537af85604fa527600fc33d48`  
		Last Modified: Wed, 24 Apr 2024 21:55:51 GMT  
		Size: 156.7 MB (156714950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37da2128b5c5e99474d0110f7ea29a16bb543aecd1c5be9e3788ecc24f61cac`  
		Last Modified: Wed, 24 Apr 2024 21:55:42 GMT  
		Size: 19.5 MB (19518412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b4a207f6e6e7497e3a6bfb24f52be63a00e5ef99cbb7dcff72fcbb65102994`  
		Last Modified: Wed, 24 Apr 2024 21:55:39 GMT  
		Size: 4.4 MB (4399160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84517417d4f2b22c30357d533534f24b48cbe755353083741b1ab30f576e7433`  
		Last Modified: Wed, 24 Apr 2024 21:55:38 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-22-lein-2.11.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4ddd81a467546d653b37e647c49cf1397b782a0455cce0b3a6ffc997a7af5453
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 MB (228090386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a94866734163a054954f82363acfada82ba9ad7cc8f7e3b9fd34be6c8bebcb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:42:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:15:58 GMT
COPY dir:8db4aa7d00469f3c784932412aa95caf68b05146a02559362a91df21ce463ad4 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:16:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:16:02 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 19:16:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 19:16:02 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:16:17 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 19:16:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 19:16:17 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 19:16:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 19:16:19 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:16:20 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:16:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76692e349ab3fc28939969feb219a1adc5237e5df9daf81b4b08faa0c3cc5ea`  
		Last Modified: Wed, 24 Apr 2024 19:35:07 GMT  
		Size: 154.7 MB (154737723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb9908bad0b34bab64d97f5ee91bd713c5903a0b18951c024a20d098243757e`  
		Last Modified: Wed, 24 Apr 2024 19:34:58 GMT  
		Size: 19.3 MB (19339737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb9b3447f41cd2c7c880d295ee8f258dee5d860e93296d54273641a40431b58`  
		Last Modified: Wed, 24 Apr 2024 19:34:57 GMT  
		Size: 4.4 MB (4399184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac938718997299ca8b99ec300b99c4adcbf331bc666693ec09759cf1e9e5107`  
		Last Modified: Wed, 24 Apr 2024 19:34:56 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
