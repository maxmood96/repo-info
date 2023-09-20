## `clojure:temurin-17-lein-bullseye`

```console
$ docker pull clojure@sha256:9766eb8e87cb0d02739417f8e5e6a0006ad353ba874dd7334a433c6193236353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ab5ea616f6c053e92e7c25b0a78268ae36f1783b4f53c4f55503081d0b25c22f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218093408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3869acff5da98e0c083b7ee514c1403ce8e3b43430c2b85513bc621cd22b236a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:51 GMT
ADD file:85db4f4c5016f51f7112a5d09cb7d4620f565a1379ae4b8a03c5ffc23886a876 in / 
# Wed, 20 Sep 2023 04:55:51 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:21:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Sep 2023 07:27:45 GMT
COPY dir:61bbef45bd137d5078f6a6f774d9bc49d275ae5fe27274294232d075ae1a5bf2 in /opt/java/openjdk 
# Wed, 20 Sep 2023 07:27:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 07:28:58 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 20 Sep 2023 07:28:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 Sep 2023 07:28:59 GMT
WORKDIR /tmp
# Wed, 20 Sep 2023 07:29:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 20 Sep 2023 07:29:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 Sep 2023 07:29:13 GMT
ENV LEIN_ROOT=1
# Wed, 20 Sep 2023 07:29:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 20 Sep 2023 07:29:15 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 20 Sep 2023 07:29:16 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 Sep 2023 07:29:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ddf874abf16cc990e0fd75a154a34ca0a03ee310ad895a18fb62ae15bf4171fb`  
		Last Modified: Wed, 20 Sep 2023 05:00:41 GMT  
		Size: 55.1 MB (55056714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf4a672ed9955378a963316cbf18411e8a03dfdf04af1c6124a50daf2a46955`  
		Last Modified: Wed, 20 Sep 2023 07:37:17 GMT  
		Size: 144.8 MB (144775739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db09a69157fbf46dbd4c084690c8acf309f59f2986ab676c3583e1f494ffdffa`  
		Last Modified: Wed, 20 Sep 2023 07:37:51 GMT  
		Size: 13.9 MB (13861275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa0c08c10b877cf17874086df70f382235a65470ca1dfd9043aca4c7478abd6`  
		Last Modified: Wed, 20 Sep 2023 07:37:51 GMT  
		Size: 4.4 MB (4399280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e43878cfea9d401baad7aa1ceee61ee507a772df04c523345c9b2d46c69b0d`  
		Last Modified: Wed, 20 Sep 2023 07:37:50 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0931e3b338d97a0403b4c45762dc533c3ee79145984898a8380422e992019548
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.5 MB (215497288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db5b7aed11e888ce915fcb4666c847e16d63c68eb95e5253a88f348cdc0200b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:45 GMT
ADD file:6bc001e951ef1280f566a92e65fcff57aefb8a280aa3510b7cd4b4e0a54c5cff in / 
# Thu, 07 Sep 2023 00:39:46 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 09:03:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 09:09:15 GMT
COPY dir:ffc7dc4725a3524e0b294e59a90d1e58e69ec448374b50aef6bef0cfa219cb0f in /opt/java/openjdk 
# Thu, 07 Sep 2023 09:09:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:10:17 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 07 Sep 2023 09:10:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 07 Sep 2023 09:10:17 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 09:10:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 07 Sep 2023 09:10:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Sep 2023 09:10:31 GMT
ENV LEIN_ROOT=1
# Thu, 07 Sep 2023 09:10:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 07 Sep 2023 09:10:34 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 07 Sep 2023 09:10:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 07 Sep 2023 09:10:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:61c16b7975697b00760ff9536c09eed29b6a76923d4d98be38e9cdc749506417`  
		Last Modified: Thu, 07 Sep 2023 00:43:21 GMT  
		Size: 53.7 MB (53704716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11abafe6bd868d46b7ee281876a4f1449b1024ece764bcbdf2e54191d6f14bf0`  
		Last Modified: Thu, 07 Sep 2023 09:17:33 GMT  
		Size: 143.5 MB (143543491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46fee1d4db9999460ebe720f01c8d07b81d07502e45a8850f84bb304e30d423`  
		Last Modified: Thu, 07 Sep 2023 09:18:00 GMT  
		Size: 13.8 MB (13849416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e0c6ea0053cf9cc62874d5e2ec21ab9eb502b25de102ffa8aba9508a99cc46`  
		Last Modified: Thu, 07 Sep 2023 09:17:59 GMT  
		Size: 4.4 MB (4399266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0c22c49612946319e2cde4332d97643aa49d419d64f4ac5977522d31678ea3`  
		Last Modified: Thu, 07 Sep 2023 09:17:58 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
