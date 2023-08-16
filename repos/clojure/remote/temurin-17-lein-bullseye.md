## `clojure:temurin-17-lein-bullseye`

```console
$ docker pull clojure@sha256:723873a70f8c423c6f07e649e11f5a6cb7185963395ea293067bacff42f4ccdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f7b346c21dd61f395453dcfb8eaf60c0600f49c82e86dc3dd6092d05ff279d60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218091250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b37a6daa5bdd2be1fbf9152aca323aeb92e5fdf824bf509ff06ae5ec908578`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:57 GMT
ADD file:20f89ff93bfbd6c9fb1a97058a1f3de4485a8974e8a83892072c511fbd2e4134 in / 
# Wed, 16 Aug 2023 00:59:58 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 18:08:24 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Wed, 16 Aug 2023 18:08:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 18:09:59 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 16 Aug 2023 18:09:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 16 Aug 2023 18:10:00 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 18:10:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 16 Aug 2023 18:10:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 16 Aug 2023 18:10:14 GMT
ENV LEIN_ROOT=1
# Wed, 16 Aug 2023 18:10:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 16 Aug 2023 18:10:16 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 16 Aug 2023 18:10:16 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 16 Aug 2023 18:10:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a70103cc499a199e10e379794c60aa524d9598587cc2bdfe2995642c2da8df7`  
		Last Modified: Wed, 16 Aug 2023 01:04:50 GMT  
		Size: 55.1 MB (55056621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fbbfc9003ff6a7a7db701f4c4c225eecdff24e8d91f37e9d447417a6e458b2`  
		Last Modified: Wed, 16 Aug 2023 18:17:54 GMT  
		Size: 144.8 MB (144773721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2b93f2ef9120804198cd07f8881e58b6a74eb6aa53abdfa8d8bbe396960097`  
		Last Modified: Wed, 16 Aug 2023 18:18:45 GMT  
		Size: 13.9 MB (13861220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a040b5f15f40354e416d9981d076f48357567d0b319d2a564692d208d11919`  
		Last Modified: Wed, 16 Aug 2023 18:18:44 GMT  
		Size: 4.4 MB (4399289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7405564f7d7f30ad1ddd6d80a73fdf7a5366dafd37002fbfba22587d3e838e`  
		Last Modified: Wed, 16 Aug 2023 18:18:43 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b99093f9111a707f74f817d0d860cf2e92124dc547abffea1a4cfec8ed5e1f13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.5 MB (215491978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38c2a9cc4d447383bdd92d517fb15fb72f016288759a42bf646ce795a14e561`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:20 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Wed, 16 Aug 2023 17:25:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 17:26:50 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 16 Aug 2023 17:26:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 16 Aug 2023 17:26:50 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 17:27:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 16 Aug 2023 17:27:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 16 Aug 2023 17:27:03 GMT
ENV LEIN_ROOT=1
# Wed, 16 Aug 2023 17:27:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 16 Aug 2023 17:27:05 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 16 Aug 2023 17:27:05 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 16 Aug 2023 17:27:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407f1b0394be128a63af2359d89c3282164b67cd2fac29716c6f2f5e348ec07a`  
		Last Modified: Wed, 16 Aug 2023 17:34:01 GMT  
		Size: 143.5 MB (143538089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fd784527041494e468446a9c7ea366ce063c2380147b0033a3672ac3a76abc`  
		Last Modified: Wed, 16 Aug 2023 17:34:57 GMT  
		Size: 13.8 MB (13849444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d2cdc01e6ceb90a93c14159585e020057bfa8ec373ac7ddbd54c03fc0386ce`  
		Last Modified: Wed, 16 Aug 2023 17:34:56 GMT  
		Size: 4.4 MB (4399265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad3e42e54921f61037651a82e39aeabf6e5ce6b4e7aadf0d1c33d6ec4aa9649`  
		Last Modified: Wed, 16 Aug 2023 17:34:55 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
