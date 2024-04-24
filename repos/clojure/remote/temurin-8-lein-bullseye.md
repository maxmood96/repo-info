## `clojure:temurin-8-lein-bullseye`

```console
$ docker pull clojure@sha256:b8e1a2066a054fbec6563ff56b7c55da0f8337903107ca2350d061d2a70a494c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:061b80a5dedac2bf16af402034f3bef85e7a689a151960615035baba23fb03d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179453243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3772b707c96db6a3fd8d265abe49cf06e1bc81db38f151bf18a4492e944ccd`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:14:32 GMT
COPY dir:54f5f76f9b290ecbafc047cf196165b69f1cb32e49c8748c35e250f5e316fcc0 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:14:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:14:33 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 21:14:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 21:14:33 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:14:51 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 21:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 21:14:51 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 21:14:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 21:14:53 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdc70d459841181e437388349fae966ee84cacccee8e9217b95eda3cf7bec02`  
		Last Modified: Wed, 24 Apr 2024 21:40:37 GMT  
		Size: 103.6 MB (103600134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb859fd2d48821b7534cec67a87763c82024c674a7ca2a6c1094c7ca95becbba`  
		Last Modified: Wed, 24 Apr 2024 21:40:30 GMT  
		Size: 16.4 MB (16355028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fbc092b8ecff895785efdca9539531249a82e990cbb4a270fd21ec5f33ee0a`  
		Last Modified: Wed, 24 Apr 2024 21:40:30 GMT  
		Size: 4.4 MB (4399211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c7c0629fdeaf2b3b664d10f9f152ee96b3d94a9657450b6d35ad69c178ddafb3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177183289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24144b653281aac155e8a50bdce544bcb17c7987da6b804256814a7dd64f621`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:00:28 GMT
COPY dir:f816a852ac21a5e29532918ac40e44b27f618ca8c5c539e334f114f460fe4b51 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:00:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:00:30 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 19:00:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 19:00:30 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:00:46 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 19:00:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 19:00:47 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 19:00:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 19:00:49 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b10ac2f49582813d917176fbb09495d94affa86eed578334d80898e8e861343`  
		Last Modified: Wed, 24 Apr 2024 19:21:54 GMT  
		Size: 102.7 MB (102700147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f444b010b4e264ce3da9f97811f98ac8797dbd8c2da729957995942468339f`  
		Last Modified: Wed, 24 Apr 2024 19:21:48 GMT  
		Size: 16.3 MB (16344024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac581de62290a5e745a608b3893708d239736e99c4a040529dd5d94a5cbbfcb2`  
		Last Modified: Wed, 24 Apr 2024 19:21:47 GMT  
		Size: 4.4 MB (4399159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
