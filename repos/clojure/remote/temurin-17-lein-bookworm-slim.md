## `clojure:temurin-17-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:e3219496376285c872372922d453e849954bc6f2315f6aa1a0da545c3220181f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:189896d3f99a0db6384f1fa6673a6de0442431e85d8679c045e1129af16a5f4c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196132677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4431934be196ebc5b64cd22b2fe23d42f04d1b3206f40ac9cbf4401d288ff4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:37:03 GMT
COPY dir:d78c0cec90816231fd61ebcd7c27b07c1af0064b89c255fd2a157e0b344541d4 in /opt/java/openjdk 
# Thu, 02 May 2024 05:37:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:37:04 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 02 May 2024 05:37:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 02 May 2024 05:37:04 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:37:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 02 May 2024 05:37:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 May 2024 05:37:20 GMT
ENV LEIN_ROOT=1
# Thu, 02 May 2024 05:37:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Thu, 02 May 2024 05:37:22 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 02 May 2024 05:37:22 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 02 May 2024 05:37:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002e2ebb10873bf6b0fa0a37e950a94f94204d5baf185501b3c19be56f8d879f`  
		Last Modified: Thu, 02 May 2024 05:50:22 GMT  
		Size: 145.1 MB (145095178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d641932204c27948fcc22f854518046cb1dfdfc771e18d4acebd13dc41e1087`  
		Last Modified: Thu, 02 May 2024 05:50:12 GMT  
		Size: 17.5 MB (17488460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242394d14469abc65e2f4bb902427083124fe92fbf9d2d406b0b52b940fe7e54`  
		Last Modified: Thu, 02 May 2024 05:50:11 GMT  
		Size: 4.4 MB (4398159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31c0b7042a3681a975d8fa5e1eed2c55bb00e49d6086b70bd3154cb438b224f`  
		Last Modified: Thu, 02 May 2024 05:50:11 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2454fab173cc90db0ab34998641f0399d2ab62c4601c9dbac7e69e89675aade2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194781609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9274e974238d5d0d4e9dd86e71682fc95ad4bb040bc5134825d62970941b8aae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:43:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:34:25 GMT
COPY dir:317487729b1812635c51c5f305bd9178bd957a141903eab756a1683874b5752b in /opt/java/openjdk 
# Thu, 02 May 2024 05:34:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:34:29 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 02 May 2024 05:34:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 02 May 2024 05:34:29 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:34:42 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 02 May 2024 05:34:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 May 2024 05:34:43 GMT
ENV LEIN_ROOT=1
# Thu, 02 May 2024 05:34:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Thu, 02 May 2024 05:34:45 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 02 May 2024 05:34:45 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 02 May 2024 05:34:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff240f07bd7ec84db24ba936652a43f9d5b27137063d0553db4e078bc72c5a3`  
		Last Modified: Thu, 02 May 2024 05:45:43 GMT  
		Size: 143.9 MB (143891839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c8ec651e1adfa8d740badaff87d9ed3154c37588b52a0af8954c988624654d`  
		Last Modified: Thu, 02 May 2024 05:45:35 GMT  
		Size: 17.3 MB (17311324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0d336a75bdb0465c2a308beee9d1fc3cfec94cf51b825ad5d1faa93b626e9d`  
		Last Modified: Thu, 02 May 2024 05:45:34 GMT  
		Size: 4.4 MB (4398110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f298c77c695f1de2af74a431d9aa2ab227ed59b347a6c856b668ec81d7c81f6c`  
		Last Modified: Thu, 02 May 2024 05:45:34 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
