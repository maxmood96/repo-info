## `clojure:temurin-11-lein-2.11.2-bookworm-slim`

```console
$ docker pull clojure@sha256:4a5bf88b3283d14fc37ab638a4c05714c41c688f83a84467b4a04f1baba4ef3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.11.2-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:111e6df8abd332bd58eaa29acd374809a26ca99d873c4ddc2ed679f9f24902f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196542821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20387d4ccefbb102a4e149fa51feb297e9ca17c3caa98d6857a24a105237287`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:19:46 GMT
COPY dir:27feef64ab9493a1c978ebf5ca0dc5d8ce2aa9d0441a77081243d3ab0f99637d in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:19:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:19:47 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 21:19:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 21:19:47 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:20:03 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 21:20:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 21:20:03 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 21:20:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 21:20:06 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddf2af383d8c16576e07d89f5fcd3cb4ab9712395361a9c2ef60dae75ee8351`  
		Last Modified: Wed, 24 Apr 2024 21:44:15 GMT  
		Size: 145.5 MB (145504720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1003244b40e5eaac88744998268c6accb66a95de9928601dbc43b492f187012a`  
		Last Modified: Wed, 24 Apr 2024 21:44:05 GMT  
		Size: 17.5 MB (17488452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da67a6c28650359d1c7ba7bb3a8e753904b6b64961411df91f4d4cd22d1d7`  
		Last Modified: Wed, 24 Apr 2024 21:44:04 GMT  
		Size: 4.4 MB (4399170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.11.2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5269d79dc5c0ce3ed94177bfe900e93363f19ae9c4af2bd6c2ea0a465a515ea6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 MB (193194862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a9aaff586439b64ab608a892650fe2a6b9c624041cd2ca5bfb2f6d4625513d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:43:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:05:00 GMT
COPY dir:ed1d7b3eb6412a67cc5fb5f9ef1702ecc8bb34e5c226d446c2bffff7a9d8d2bc in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:05:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:05:03 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 19:05:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 19:05:03 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:05:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 19:05:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 19:05:18 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 19:05:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 19:05:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb109af8d78612293283226d5c08e06c120f7cdbbaa7c5a83526aa3bf398ff9`  
		Last Modified: Wed, 24 Apr 2024 19:25:02 GMT  
		Size: 142.3 MB (142304377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee2ad04413bd54dd124c999a4dc89c2447749f6c66d82d3ae7149cbd931338`  
		Last Modified: Wed, 24 Apr 2024 19:24:54 GMT  
		Size: 17.3 MB (17311349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a2e4e7f0e3f333e8e504667f73b3bc1c5982ae266364d88efd074921eaac5f`  
		Last Modified: Wed, 24 Apr 2024 19:24:53 GMT  
		Size: 4.4 MB (4399201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
