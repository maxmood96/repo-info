## `clojure:temurin-11-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:13cdb6692f98ad9e19067c50a2af7137d5cfdd42f93dd641c0c15de61ad07795
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fc991988b4c4efcf1c2e6c9234cf4f8b5adda7148f2030076af2a0b5a20dfeef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195061534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a91250d1561ffd7892cc4dfdef4ca49c66fd19ed4544f465f60d04dd1c4ace2`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:51:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:51:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:51:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:51:31 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:51:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:51:31 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:51:45 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:51:45 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:51:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:51:47 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44215fbb720784ee7e4c70a55deafac3d6a8dfd3b4f8bfff785df78242878915`  
		Last Modified: Mon, 08 Dec 2025 23:52:25 GMT  
		Size: 145.0 MB (144966590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3af1e0474b0751f2e1c0763f4e3498afea31ff75d8ebbde5a7b1e70065b3858`  
		Last Modified: Mon, 08 Dec 2025 23:52:13 GMT  
		Size: 15.3 MB (15318724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8102eb3ba60b4be88ff115e4bb5d2aab9ba32826f63e02f4d4c9852bed7c669b`  
		Last Modified: Mon, 08 Dec 2025 23:52:12 GMT  
		Size: 4.5 MB (4517723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:02bebb4047a909bf967041b3c76218e01e690cacf0a0c81d4b9e35300999be78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e122d04dccaf5960c013c12a168b921832fe4047dddf306b8a0ae7c0cf22d9c`

```dockerfile
```

-	Layers:
	-	`sha256:a84a1991dfca4c596979b089879628278af5f75b7ba4a57fc11f8bf6797a1731`  
		Last Modified: Tue, 09 Dec 2025 04:37:10 GMT  
		Size: 3.0 MB (3038049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd4285e20b1a83efa498ef2f89887ed5f9af9a38f1d938ed7d76a3c82b317c9`  
		Last Modified: Tue, 09 Dec 2025 04:37:11 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:62b8a17db015a9262d68783738a7d7a99358ab529ff401f153e6413749c629be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190303646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8925ac433dbea15abe9f0e084d68543e6005fac07912ca09fede4b197650c2f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:58:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:58:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:58:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:58:53 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:58:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:58:53 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:59:06 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:59:06 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:59:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:59:08 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6399b8ff1b2d58592129a52c77f56c11e37699a3778a6d4f3914c9c53b6b345`  
		Last Modified: Mon, 08 Dec 2025 23:59:27 GMT  
		Size: 141.7 MB (141731575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695c7a380f042ef0398168e50382cedc18b22d4b35866622f8fac89990493dbb`  
		Last Modified: Mon, 08 Dec 2025 23:59:33 GMT  
		Size: 15.3 MB (15305811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ed3e138ed62163eac6f57802beada923bbe76997855c55ed240e934b30002f`  
		Last Modified: Mon, 08 Dec 2025 23:59:33 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:79285b637960c62412045deab244576834c998944c3de4b6b8b68c34af141b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47b92791fba229ffce1764eeffdcf1f5cda3e94ad8cd281a694226799803fb7`

```dockerfile
```

-	Layers:
	-	`sha256:e11812f223adb5f175a1ec948ac906153a95f94daf48b31e746a007839ae471d`  
		Last Modified: Tue, 09 Dec 2025 04:37:16 GMT  
		Size: 3.0 MB (3038276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cfce8a07237663c729209e262e7c0c3ee39184554b31e739b956c8479560777`  
		Last Modified: Tue, 09 Dec 2025 04:37:17 GMT  
		Size: 16.5 KB (16533 bytes)  
		MIME: application/vnd.in-toto+json
