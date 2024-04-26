## `clojure:temurin-17-lein-2.11.2-bullseye-slim`

```console
$ docker pull clojure@sha256:ff4feed0b2f62458f88e1c8d2be94199ec300468f9e8f5303b28697169ba4279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-2.11.2-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1e9578b577036c9331e1fe72d5856a586671e5bc06945f6df17b5a7e1cc148cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (195992914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff4eeb9c1eba3fbb83b3068f6cae75d1310c5031f5a9107a9da4f5b2af72344`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Apr 2024 04:49:30 GMT
COPY dir:36f5164517b1d083643fb66b5ce80f151a1fd45f701835f30c768c906e72895e in /opt/java/openjdk 
# Fri, 26 Apr 2024 04:49:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 04:49:32 GMT
ENV LEIN_VERSION=2.11.2
# Fri, 26 Apr 2024 04:49:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Apr 2024 04:49:32 GMT
WORKDIR /tmp
# Fri, 26 Apr 2024 04:49:47 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 26 Apr 2024 04:49:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Apr 2024 04:49:48 GMT
ENV LEIN_ROOT=1
# Fri, 26 Apr 2024 04:49:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Fri, 26 Apr 2024 04:49:50 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 26 Apr 2024 04:49:50 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Apr 2024 04:49:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4c830d8c95074e2e782fdd6ee82347a20a742e20df24cc7c47ec44a99030ab`  
		Last Modified: Fri, 26 Apr 2024 05:02:46 GMT  
		Size: 145.1 MB (145095347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7c27a2af504ac8c52d8f905f58b2c9e39e483aac354983675254755fcf1d47`  
		Last Modified: Fri, 26 Apr 2024 05:02:36 GMT  
		Size: 15.1 MB (15064798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a473824e6177b40de0f30594f18d1f73148594cd4ff2d842b2b0cf7d6d2d224`  
		Last Modified: Fri, 26 Apr 2024 05:02:35 GMT  
		Size: 4.4 MB (4398105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2874c5daa9c00129532fae63fc121660d388f64a6172ef9a7e4ee6e8cf86a5`  
		Last Modified: Fri, 26 Apr 2024 05:02:34 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-2.11.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dce26467e98a0be74f63acb4260f8f29fc83c09b01c1a6c7cbb134597279967b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193430341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5eb5b985f8188d557654ab6d674f830a4cbed4bf5d9abcd253085f27b2c80f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Apr 2024 01:31:27 GMT
COPY dir:c133644f5c07e30ba622e3ac6570b28080cd19be78bf4af55cfe492de2f59b24 in /opt/java/openjdk 
# Fri, 26 Apr 2024 01:31:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 01:31:31 GMT
ENV LEIN_VERSION=2.11.2
# Fri, 26 Apr 2024 01:31:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Apr 2024 01:31:31 GMT
WORKDIR /tmp
# Fri, 26 Apr 2024 01:31:45 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 26 Apr 2024 01:31:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Apr 2024 01:31:45 GMT
ENV LEIN_ROOT=1
# Fri, 26 Apr 2024 01:31:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Fri, 26 Apr 2024 01:31:47 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 26 Apr 2024 01:31:47 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Apr 2024 01:31:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc4434c9bf51b4918beda568d65ee3c738207f5504aea294c573555eac94f5c`  
		Last Modified: Fri, 26 Apr 2024 01:42:50 GMT  
		Size: 143.9 MB (143891889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4113c9dcd831b7f598b96595cc03ff7b42c922cdfde4cb76ca5042818b3fb0c3`  
		Last Modified: Fri, 26 Apr 2024 01:42:39 GMT  
		Size: 15.1 MB (15052554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ada1bdb8b44cf00e1e54f46bd2d4e2fedff57ba0966833e46998d789be12d4`  
		Last Modified: Fri, 26 Apr 2024 01:42:39 GMT  
		Size: 4.4 MB (4398159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d39b24ac17ea060e344c68b7cfeac27b918f8ce9c771341e4a809e03bf563f5`  
		Last Modified: Fri, 26 Apr 2024 01:42:38 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
