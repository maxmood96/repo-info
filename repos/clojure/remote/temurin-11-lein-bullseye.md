## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:d2ea57d9feb6c50a365b3eb00cb08e3f2001bd3b1da82c7bf520d5f6ab7b1fe9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1496cea8f8f07c1e21f7a18a5d46a01eaaa97cfd01e9f7314a68640ff7f8836c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220688539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c9befab17930206f6e368e1660e650c32636195848078e00175225ee46e1d78`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:02:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:02:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:02:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:02:15 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:02:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:02:15 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:02:30 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:02:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:02:30 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:02:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:02:32 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac401906c708c6fd65f3e82904d2817667ec01dde0d4fe7e7316fc6de177f85`  
		Last Modified: Thu, 05 Feb 2026 23:02:52 GMT  
		Size: 145.8 MB (145806880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1de06db801f18cb619c5f818cb9f8ff9e15c68e4631ce3a0538013c88994d3`  
		Last Modified: Thu, 05 Feb 2026 23:02:49 GMT  
		Size: 16.6 MB (16607634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d57bc70f0cdf73f4d0998ab49030405fdc697984f063a535642884ac8e5c00`  
		Last Modified: Thu, 05 Feb 2026 23:02:48 GMT  
		Size: 4.5 MB (4517734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9690727817902e4526ead85a439ef602b4057ae87d3143af44ca5cd84c65c7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4513965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e4c875c5cbbb9861e53945986e36a5f44077114076bc5e05998211755e11a6`

```dockerfile
```

-	Layers:
	-	`sha256:1013a9aac3a0d5b7b14d0a365f69fd412b3e0eefc46dfc4a45d82991d13b0050`  
		Last Modified: Thu, 05 Feb 2026 23:02:48 GMT  
		Size: 4.5 MB (4497583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79169eea9268f89c824b26d4d467fc7867fac5a1e59c9d1b3f7c1ce44e9c783f`  
		Last Modified: Thu, 05 Feb 2026 23:02:48 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5afbf48f01b8b6daf27946506885e0a3cf5e51bdd97b36f5c478278b8b2b65ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215871914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6c1b157c91879bffdc478dafa2ee763fff74337a8c2e9789deb23548d86160`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:03:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:03:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:03:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:03:05 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:03:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:03:05 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:04:27 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:04:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:04:27 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:04:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:04:29 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20be37c65e18ef6adc2de144852e81c3a2de1212556e76b454ae1b2028b20b6b`  
		Last Modified: Thu, 05 Feb 2026 23:04:15 GMT  
		Size: 142.5 MB (142500849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5def177e16ff316dc6755aa975071356227a2d62c7c49207e013614c846980`  
		Last Modified: Thu, 05 Feb 2026 23:04:47 GMT  
		Size: 16.6 MB (16594967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524ceed072322f2498a34ebfd0dc8f925bbbb6b8330d7e6d69134134b1185b03`  
		Last Modified: Thu, 05 Feb 2026 23:04:47 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2ae699a8115d22508775ad8d22c2663a479bf3431954dce5c7b97c5f5e093b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4513678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac203f840052cd8ef3d31ddabe885136b0e5d535a4af5176c5030f4cff22c39`

```dockerfile
```

-	Layers:
	-	`sha256:7f998d8a5fb309f9e8b5b9818bfcecd5f6b51c64e606111fdc7bea35c4c9f69f`  
		Last Modified: Thu, 05 Feb 2026 23:04:46 GMT  
		Size: 4.5 MB (4497175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5ab4ac7aa0f2397970d1a8f65fb49b1a4935fc073a155636d35283f3e62e14`  
		Last Modified: Thu, 05 Feb 2026 23:04:46 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json
