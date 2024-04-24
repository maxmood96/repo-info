## `clojure:temurin-11-lein-bookworm`

```console
$ docker pull clojure@sha256:e1e3f8b17c9fc96890b60f6fdebedc4d0d19a6ba166f9c8fa2668bfcf328a6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:210a5d2f4efa22502ba6d16861b684c551216fc952ebdfc09bba522d0d6a8382
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218998547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2383bf21da385ff2ed74c6d22e032cbf4c8b3efbe5ee38e1f59aec62f7cee4ba`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:19:18 GMT
COPY dir:27feef64ab9493a1c978ebf5ca0dc5d8ce2aa9d0441a77081243d3ab0f99637d in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:19:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:19:19 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 21:19:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 21:19:19 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:19:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 21:19:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 21:19:36 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 21:19:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 21:19:38 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2383bb2fba492f68230638def29657a1b193de16639ee31045aaa9ce717d0`  
		Last Modified: Wed, 24 Apr 2024 21:43:55 GMT  
		Size: 145.5 MB (145504714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1df44b4ac80ca845777e60b9e56df495bedff3b302acaed5120ae8c3cc76fc`  
		Last Modified: Wed, 24 Apr 2024 21:43:45 GMT  
		Size: 19.5 MB (19518353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2fdc50af47318e37bf886a7b3a157e2e5860d528e3ba0e97d254f7678a4882`  
		Last Modified: Wed, 24 Apr 2024 21:43:44 GMT  
		Size: 4.4 MB (4399197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:493a320a57bc9159b293a85256f2c0157800fc212d48e8f08643be822bbfdf4e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.7 MB (215656640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b672b36c0ce20cb0b108871982b85baa3c5c4a8c4589f843abeb6273e3ce8bfa`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:42:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:04:33 GMT
COPY dir:ed1d7b3eb6412a67cc5fb5f9ef1702ecc8bb34e5c226d446c2bffff7a9d8d2bc in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:04:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:04:37 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 19:04:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 19:04:37 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:04:51 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 19:04:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 19:04:51 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 19:04:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 19:04:54 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12591c55ea618c50d976c3e69782f55f21db7a3c276904b0b5228e94ac67b064`  
		Last Modified: Wed, 24 Apr 2024 19:24:42 GMT  
		Size: 142.3 MB (142304377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2a730f25c880c711bd0c481501303c539a3ec34823961bda2efcec8c28dea0`  
		Last Modified: Wed, 24 Apr 2024 19:24:35 GMT  
		Size: 19.3 MB (19339740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8401d6a31d924f05d874907fc0dc3b2c2e2b6ae0fae927db2a17169fb34b7e8a`  
		Last Modified: Wed, 24 Apr 2024 19:24:34 GMT  
		Size: 4.4 MB (4399182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
