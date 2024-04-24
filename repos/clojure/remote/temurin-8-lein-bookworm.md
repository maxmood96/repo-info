## `clojure:temurin-8-lein-bookworm`

```console
$ docker pull clojure@sha256:601851f823c8fa2ae348f14cd52e284e2e287c01c2b915d3e26fdbf38d8903ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:6d1e64c3107af6f4c96fb532e1640f3bb9f3b926b03c25269106abeacb7b57af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177094029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312e6a6ec47b1cc11aa465de466aed3893a1fc3aaf0bd433054f14c7a2c5c834`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:13:39 GMT
COPY dir:54f5f76f9b290ecbafc047cf196165b69f1cb32e49c8748c35e250f5e316fcc0 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:13:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:13:40 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 21:13:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 21:13:40 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:13:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 21:13:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 21:13:56 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 21:13:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 21:13:59 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c0852faaab04d655f913386e0af6c14a4412d28e791543c7cdd1d53c23bf06`  
		Last Modified: Wed, 24 Apr 2024 21:40:04 GMT  
		Size: 103.6 MB (103600140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cc2b5753532343d44a4a6cb292f8f502888c693353feacbdd3cd51683789c9`  
		Last Modified: Wed, 24 Apr 2024 21:39:58 GMT  
		Size: 19.5 MB (19518389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95b69a583f8ac1102a41c589b5a4a3b74267ee2602e43d1c1e1ab52722b10a0`  
		Last Modified: Wed, 24 Apr 2024 21:39:57 GMT  
		Size: 4.4 MB (4399217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a09e5e6cd76921dbeb62bb085f51ef0f9e75b83ee127043ce438ee041ade91a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176052404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9daec05ae845ed9491af2f5dacf55b865d1d190b081f80884116df7bd2d946b3`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:42:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 18:59:42 GMT
COPY dir:f816a852ac21a5e29532918ac40e44b27f618ca8c5c539e334f114f460fe4b51 in /opt/java/openjdk 
# Wed, 24 Apr 2024 18:59:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 18:59:45 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 18:59:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 18:59:45 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 18:59:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 18:59:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 18:59:59 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 19:00:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 19:00:01 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a326c3125dc8673964b82d25ba8518ec98242bdf3b9b32ce6bc1024a14e290b`  
		Last Modified: Wed, 24 Apr 2024 19:21:24 GMT  
		Size: 102.7 MB (102700132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7264e0a80c45f10ca261036c3603958c5b90d9aefda7654e657b85d526e9cb`  
		Last Modified: Wed, 24 Apr 2024 19:21:18 GMT  
		Size: 19.3 MB (19339748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826e39dc0a30c5ec9adec6f390dddba629df5d131d54ca6f72fba5ea13465c46`  
		Last Modified: Wed, 24 Apr 2024 19:21:17 GMT  
		Size: 4.4 MB (4399183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
