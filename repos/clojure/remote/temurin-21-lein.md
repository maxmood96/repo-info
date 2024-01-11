## `clojure:temurin-21-lein`

```console
$ docker pull clojure@sha256:1519c042bd30deae6e945a461eabe83018045edfee152e9d309681bdc408035f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-lein` - linux; amd64

```console
$ docker pull clojure@sha256:119fe8093d4afbcd4671ff5bfa1dd53640c3dffe52202b08b4ddca61782530f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229618103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ea1a674285059f98bf1251aae51a9fb2bd2f53169bf08073fe932048997d91`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:50:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:50:54 GMT
COPY dir:e6025cb107ac582823e7222bca84438ae7fa7384431777ac5a68b80c2a5b3d9d in /opt/java/openjdk 
# Thu, 11 Jan 2024 04:50:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 04:50:56 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 11 Jan 2024 04:50:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 04:50:56 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 04:51:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 11 Jan 2024 04:51:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 04:51:11 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jan 2024 04:51:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 11 Jan 2024 05:09:18 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 11 Jan 2024 05:09:18 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jan 2024 05:09:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0947ab7912f8799797e21af4061c1079778e5c670b12a389b27dcc7df0e78a3`  
		Last Modified: Thu, 11 Jan 2024 05:14:04 GMT  
		Size: 158.6 MB (158630584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb95350e4e0cfb0f3f4ff3ffd1fac3444d71733f1e2c634b879ff33833051dab`  
		Last Modified: Thu, 11 Jan 2024 05:13:50 GMT  
		Size: 17.0 MB (17026353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e4dbb04caae61fd988d47dfda7a1789b07c1d2e3610a19de8bf79ebf0860dc`  
		Last Modified: Thu, 11 Jan 2024 05:13:49 GMT  
		Size: 4.4 MB (4399280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfd25f2b8fed8ce286cf336d910de0b6ecaa62713fcbaf348d5dc2ae8f72bf2`  
		Last Modified: Thu, 11 Jan 2024 05:24:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:475ead181591ff0d51988e04e16566514e656f48f2b80f6208dd08b7859f82d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227712654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317c0e521f52c4ac9d452fd29e2323544e5991a6debcf1707a6316e8e72d11d4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:02 GMT
ADD file:412f80f75ed3e520f767e70b6b27fc81807f62fc5c6e5adf756507e33af9fa6b in / 
# Tue, 19 Dec 2023 01:41:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:53:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:53:37 GMT
COPY dir:6c09b6d38e0ce748c3ef1f9f172525f08b1f5fa7d2d583b56755ceb9d38b6e61 in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:53:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 06:53:41 GMT
ENV LEIN_VERSION=2.10.0
# Tue, 19 Dec 2023 06:53:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 06:53:41 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 06:53:55 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 19 Dec 2023 06:53:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 06:53:55 GMT
ENV LEIN_ROOT=1
# Tue, 19 Dec 2023 06:53:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 19 Dec 2023 07:08:13 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 19 Dec 2023 07:08:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Dec 2023 07:08:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b66b4ecd3ecfb67b3b7a2a44b0199cbdfc94965c8bd3fefab75cd2e612799740`  
		Last Modified: Tue, 19 Dec 2023 01:44:14 GMT  
		Size: 49.6 MB (49592259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1808780032a4c7370b9064c00f6989f956dde542d1e7d624e90bca73cae8b224`  
		Last Modified: Tue, 19 Dec 2023 07:12:31 GMT  
		Size: 156.9 MB (156872127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01879dfdb10e25dab6d00d4971bc334230de40c5be7c188ed298fd4204a3a32`  
		Last Modified: Tue, 19 Dec 2023 07:12:20 GMT  
		Size: 16.8 MB (16848636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a407c92141e3592db6794d1300cb24d8d0ad1c7f7bcaeaaa377659b266b891ec`  
		Last Modified: Tue, 19 Dec 2023 07:12:18 GMT  
		Size: 4.4 MB (4399235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56476f0e3ccbc77e117866259c2c0953ed5ba0e547956c4180887e0785d9701`  
		Last Modified: Tue, 19 Dec 2023 07:21:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
