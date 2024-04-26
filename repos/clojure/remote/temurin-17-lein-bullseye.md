## `clojure:temurin-17-lein-bullseye`

```console
$ docker pull clojure@sha256:3e61cda77663e014b331d2fe5ad411a4a3be128549a19c0a25daf95e60f2538d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:63d8a690c6331eb5a8917dfbf4df519db8d82cb03418e295b1cf40aa18eb20b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220947737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0643882b3e45e959f8892c9e7c96fee8ea92614825fda6b7c111943ef6acb733`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Apr 2024 04:49:06 GMT
COPY dir:36f5164517b1d083643fb66b5ce80f151a1fd45f701835f30c768c906e72895e in /opt/java/openjdk 
# Fri, 26 Apr 2024 04:49:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 04:49:07 GMT
ENV LEIN_VERSION=2.11.2
# Fri, 26 Apr 2024 04:49:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Apr 2024 04:49:08 GMT
WORKDIR /tmp
# Fri, 26 Apr 2024 04:49:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 26 Apr 2024 04:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Apr 2024 04:49:23 GMT
ENV LEIN_ROOT=1
# Fri, 26 Apr 2024 04:49:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Fri, 26 Apr 2024 04:49:25 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 26 Apr 2024 04:49:25 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Apr 2024 04:49:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b56a069e7c2cce602b3c97a35f6b51d9429de11e3d7b2b47ebdaf03792986fc`  
		Last Modified: Fri, 26 Apr 2024 05:02:27 GMT  
		Size: 145.1 MB (145095338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28e2da38d1db18d87ad3a786a8122ec53031b775e64e0044215c25a89dfe40`  
		Last Modified: Fri, 26 Apr 2024 05:02:16 GMT  
		Size: 16.4 MB (16354983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b020baccfd5564d8401b944640078a1b36cf1c2d993efd5b46e92e231afab2b`  
		Last Modified: Fri, 26 Apr 2024 05:02:15 GMT  
		Size: 4.4 MB (4398146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb8a3e6a26737cf38f824d15b930af3805673cc8954b3dc2ad8f30baf42d9ea`  
		Last Modified: Fri, 26 Apr 2024 05:02:15 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b7fc94e571d533a614f418b8053a9ccb60088e86071bb0abdd62e8d1654fee1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218374317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01ac5926460a8c051e7c57d6bf9549a06b3c019f6024984989b4bbfedd1d06b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Apr 2024 01:31:04 GMT
COPY dir:c133644f5c07e30ba622e3ac6570b28080cd19be78bf4af55cfe492de2f59b24 in /opt/java/openjdk 
# Fri, 26 Apr 2024 01:31:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 01:31:07 GMT
ENV LEIN_VERSION=2.11.2
# Fri, 26 Apr 2024 01:31:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Apr 2024 01:31:07 GMT
WORKDIR /tmp
# Fri, 26 Apr 2024 01:31:21 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 26 Apr 2024 01:31:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Apr 2024 01:31:22 GMT
ENV LEIN_ROOT=1
# Fri, 26 Apr 2024 01:31:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Fri, 26 Apr 2024 01:31:24 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 26 Apr 2024 01:31:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Apr 2024 01:31:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdec292b58e2b3144d6224079475782e80323512307f657853dcbef336a1ce35`  
		Last Modified: Fri, 26 Apr 2024 01:42:30 GMT  
		Size: 143.9 MB (143891890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf7449b45a665a8407fe0b816edd8ac5a0d355d00c0b4286e18373b8c2879ab`  
		Last Modified: Fri, 26 Apr 2024 01:42:21 GMT  
		Size: 16.3 MB (16343967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259015eb4da3ba64acc8574749aa6e58fb029cac195c31c9c0c34bce0c6a9a11`  
		Last Modified: Fri, 26 Apr 2024 01:42:20 GMT  
		Size: 4.4 MB (4398100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94b859f7f37cc956dfc78436a183aee67d42556b4f54f36a91a841be394938d`  
		Last Modified: Fri, 26 Apr 2024 01:42:20 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
