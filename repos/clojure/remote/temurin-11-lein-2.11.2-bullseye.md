## `clojure:temurin-11-lein-2.11.2-bullseye`

```console
$ docker pull clojure@sha256:8c07a6b61be8c087e40b6d0d4d4679c83189cee4d568645170410facad6bb328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.11.2-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:eee88f52d65e04c3963bba0cb3c92ee4fffe1747d8bec6668037d82cd80bee5f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221108749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cac04c2899dc699f5a1bb676dc1595aa9b8180d1e58ba24258e1a96b06c0d90`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:11 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Tue, 12 Mar 2024 01:21:11 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:12:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:59:10 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:59:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 03:02:20 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 28 Mar 2024 03:02:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 03:02:20 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:02:36 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 28 Mar 2024 03:02:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 03:02:37 GMT
ENV LEIN_ROOT=1
# Thu, 28 Mar 2024 03:02:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 28 Mar 2024 03:02:39 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda920a039665a5015c5cb162e10882e5997cc683456c339212c7aa546a6ebd7`  
		Last Modified: Thu, 28 Mar 2024 03:19:51 GMT  
		Size: 145.3 MB (145271223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df58e33b3a4f6fad6c7ee57d46f421c0b90ac42cdee95f3550cfd7d4bf1a07ad`  
		Last Modified: Thu, 28 Mar 2024 03:21:22 GMT  
		Size: 16.4 MB (16353401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50cf9d64d7da8a88c2ffba1452f5c680286890604100c33bda3dfbce1adffa6`  
		Last Modified: Thu, 28 Mar 2024 03:21:21 GMT  
		Size: 4.4 MB (4399156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:561d11fb92957ff1c6edc1d637cc9d65bf5cdcf5598a6763308dbbceddd7c1d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216470153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cc64919fbf2ed5d6e4a56e9b6ccf1e4b89bb3cd01dbd62d259dce98039f40e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:44:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:33:19 GMT
COPY dir:d5fb8d9a38dea7496f2aff176bc9a34bbca80551c2dc57109d2dae5907a339ee in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:33:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:35:50 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 28 Mar 2024 02:35:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:35:50 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:36:04 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 28 Mar 2024 02:36:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:36:05 GMT
ENV LEIN_ROOT=1
# Thu, 28 Mar 2024 02:36:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 28 Mar 2024 02:36:07 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1fdda8e4da6bde8ae6730609d8d2464cbd336e3514cb984622194caa155ea73`  
		Last Modified: Thu, 28 Mar 2024 02:50:00 GMT  
		Size: 142.0 MB (142006317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff28292244a45259b15a857740ddb79a768efa5aa771fb417814fc48289a196`  
		Last Modified: Thu, 28 Mar 2024 02:51:13 GMT  
		Size: 16.3 MB (16342580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b0a65d57f58de1176ee0d60ea19878aad68da4a3d99ccef7c3e441e8ff7f32`  
		Last Modified: Thu, 28 Mar 2024 02:51:12 GMT  
		Size: 4.4 MB (4399157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
