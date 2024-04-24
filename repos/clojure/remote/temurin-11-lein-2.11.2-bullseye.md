## `clojure:temurin-11-lein-2.11.2-bullseye`

```console
$ docker pull clojure@sha256:1ffbbe195d8f98d5139545931b12bd182a95907a3c4f5f609a12cf2abeb58bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.11.2-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d60037f90796e706b9c6a62ae44200ca68767031022d13ee8f838048fbc4e9c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221357760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d191c73f1ae20237007fb6fc3327c81ffbbe993a522ec2fdb0a5450d8ad7f9`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:20:10 GMT
COPY dir:27feef64ab9493a1c978ebf5ca0dc5d8ce2aa9d0441a77081243d3ab0f99637d in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:20:12 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 21:20:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 21:20:12 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:20:27 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 21:20:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 21:20:27 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 21:20:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 21:20:30 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb84145e720ef12c948dfb02c9cce9a91b0f285a5139c63fb5df70da7603db33`  
		Last Modified: Wed, 24 Apr 2024 21:44:35 GMT  
		Size: 145.5 MB (145504683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267f62edc38ccbbf8857a46dec3658bd04836e3949a0ef3be8eb12f07eee16cf`  
		Last Modified: Wed, 24 Apr 2024 21:44:24 GMT  
		Size: 16.4 MB (16355029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce9c2131a651c7f08e7b6ac7a55671ea1f3046d116143ebc8062aa607324014`  
		Last Modified: Wed, 24 Apr 2024 21:44:23 GMT  
		Size: 4.4 MB (4399178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3f01b4637f34ac907362c9e2eb74eaad6c39fe1f5b2173dd04f01cac352aedda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 MB (216787607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89010046ca6b8c1b25ae6858adc962256c069abdab5de1aaca57928335db71dd`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:05:23 GMT
COPY dir:ed1d7b3eb6412a67cc5fb5f9ef1702ecc8bb34e5c226d446c2bffff7a9d8d2bc in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:05:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:05:27 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 19:05:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 19:05:27 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:05:41 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 19:05:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 19:05:41 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 19:05:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 19:05:43 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c103559d9a51b5c973652ab0b7b7056114129f4061944495b13f05cd0ed1ec`  
		Last Modified: Wed, 24 Apr 2024 19:25:24 GMT  
		Size: 142.3 MB (142304379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9332b236658b07b9f459b035e909087002f622040104bf6d1c0fd30172d771`  
		Last Modified: Wed, 24 Apr 2024 19:25:16 GMT  
		Size: 16.3 MB (16344043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c6266fce22e734090c796c4cc0ab0588dfcde19ef32c50d64df51f8b8923ab`  
		Last Modified: Wed, 24 Apr 2024 19:25:15 GMT  
		Size: 4.4 MB (4399226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
