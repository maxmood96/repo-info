## `clojure:temurin-11-lein-2.11.2-bookworm-slim`

```console
$ docker pull clojure@sha256:c0d3a6b832d9ad33badff8a5a3792b3db4294b1dac6e9c7719aff9b355fd7601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.11.2-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:75dfba4bdd21f6dea58d5b6e6af633c5473d7a8464e66c13c59549c9b5d38f01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196286811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c72e627a23de99365ec976a3d3249d6f62931122bf575a8bf4e70c1c913972`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:17:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:23:14 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:23:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:25:29 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 10 Apr 2024 06:25:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 06:25:29 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 06:25:44 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 10 Apr 2024 06:25:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 06:25:45 GMT
ENV LEIN_ROOT=1
# Wed, 10 Apr 2024 06:25:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 10 Apr 2024 06:25:47 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed28721d3594017943f3547d57bc37d04bfc57a97f0bce49df19ccea514aace`  
		Last Modified: Wed, 10 Apr 2024 06:42:39 GMT  
		Size: 145.3 MB (145271203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54a78e4571ea36df8d792ddb3ccdba3bc210ac8a556cb1476907bc6fce48b04`  
		Last Modified: Wed, 10 Apr 2024 06:43:45 GMT  
		Size: 17.5 MB (17485034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7d19be396f8a11f5a2d626322f3972fc238f5216b6a4e0bdee46d8c834f93f`  
		Last Modified: Wed, 10 Apr 2024 06:43:44 GMT  
		Size: 4.4 MB (4399216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.11.2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6f4a5ba32312ed39683fef3e1cae5c51980d02e7c6bdeb055b9c6b0d993ca18f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192876911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:279096269f40603d930fdebfbb6f29f5ea71f1aacffb46f6e967a56c1180bc13`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:38:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 06:33:11 GMT
COPY dir:337eb37873e2fe424b3d62c18ff2640cf50898156a884981e9e10924759441c3 in /opt/java/openjdk 
# Tue, 16 Apr 2024 06:33:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 06:36:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 16 Apr 2024 06:36:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Apr 2024 06:36:12 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 06:36:25 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 16 Apr 2024 06:36:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Apr 2024 06:36:25 GMT
ENV LEIN_ROOT=1
# Tue, 16 Apr 2024 06:36:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 16 Apr 2024 06:36:27 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf40e293c383aa322b6672363da730a85aaf0687fcd3e1c421634beaf9fd7e0`  
		Last Modified: Tue, 16 Apr 2024 06:52:31 GMT  
		Size: 142.0 MB (142006379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88392d588700c70555165ebfe86182bf3032e448926fce0ce58ee1e66fb2f4a`  
		Last Modified: Tue, 16 Apr 2024 06:53:51 GMT  
		Size: 17.3 MB (17309210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae40219c7e75f0739c8f3597dfc300a706a4e940a4e9761cb4f4d5d39bb1ec94`  
		Last Modified: Tue, 16 Apr 2024 06:53:50 GMT  
		Size: 4.4 MB (4399165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
