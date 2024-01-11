## `clojure:temurin-21-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:e0a73ca68f95bdcbb622cfd6ccd74ab41f5d7ecb11d29ce9b5d59aab2e8ef574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:70f0be00f25e450b8261792647112e854e7896dce024fb2cf3882f859869d362
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 MB (207026491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de676ef6ac281a4d25e900d0c2d3438ccdef09434c3a9be100b3dcc555df590`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:10:11 GMT
COPY dir:e6025cb107ac582823e7222bca84438ae7fa7384431777ac5a68b80c2a5b3d9d in /opt/java/openjdk 
# Thu, 11 Jan 2024 05:10:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:10:13 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 11 Jan 2024 05:10:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 05:10:13 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 05:10:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 11 Jan 2024 05:10:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 05:10:28 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jan 2024 05:10:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 11 Jan 2024 05:10:31 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 11 Jan 2024 05:10:31 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jan 2024 05:10:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef36e12111e37e575e53c3a23687c816ab06002dbb25a2a5abaeab9e64b9362`  
		Last Modified: Thu, 11 Jan 2024 05:25:51 GMT  
		Size: 158.6 MB (158630540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad18f7fb7eaf36f5333508aee7812a2008551f3790a340c3471682555ce44518`  
		Last Modified: Thu, 11 Jan 2024 05:25:39 GMT  
		Size: 12.6 MB (12578356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cb0e4a8fd5c34266cf9dcf187de599d5e8c082ce78cbd32df6390c263c6bdb`  
		Last Modified: Thu, 11 Jan 2024 05:25:38 GMT  
		Size: 4.4 MB (4399240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfad3f3c52a2b9ea9e71b87bedac68dc31632aead5fff4639181d4fa08a3864`  
		Last Modified: Thu, 11 Jan 2024 05:25:38 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:96ff9df67d1bfae77ef0b30935f59c94648c037604fae1896bc165cd8e04979f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203901488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53924cca86dc84ee6573bce9e5320846157c8c5a8945209af62800c437656458`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:00:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 07:09:07 GMT
COPY dir:6c09b6d38e0ce748c3ef1f9f172525f08b1f5fa7d2d583b56755ceb9d38b6e61 in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:09:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:09:11 GMT
ENV LEIN_VERSION=2.10.0
# Tue, 19 Dec 2023 07:09:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 07:09:11 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:09:24 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 19 Dec 2023 07:09:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 07:09:24 GMT
ENV LEIN_ROOT=1
# Tue, 19 Dec 2023 07:09:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 19 Dec 2023 07:09:27 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 19 Dec 2023 07:09:27 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Dec 2023 07:09:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c125c1ca87fdf704a7b920d25350427184a9cfec1b320aa3f11cdac7f0540885`  
		Last Modified: Tue, 19 Dec 2023 07:22:59 GMT  
		Size: 156.9 MB (156872108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d226259fadde06a86d4972c852ce5ee3bf23b3d32eb7480b153d2c63e5c8c8b`  
		Last Modified: Tue, 19 Dec 2023 07:22:49 GMT  
		Size: 12.6 MB (12565709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89da70c9495fadf943298c3b4541832834b082a5f0e66938938878d4c03b39ef`  
		Last Modified: Tue, 19 Dec 2023 07:22:49 GMT  
		Size: 4.4 MB (4399219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977999b6aeb07fd014b2a98efca754dc9329708db31da8dcfbe69e2d41d498b3`  
		Last Modified: Tue, 19 Dec 2023 07:22:48 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
