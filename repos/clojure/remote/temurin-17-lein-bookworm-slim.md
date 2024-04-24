## `clojure:temurin-17-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:8a78d47388af1bfd95149ba4f9bd96f0d77bcbb2d310e2657f025224df66c9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d489ca5e4f2bb545bf943bd23a90d3359b4cf4450333faeefbd7ba73a7fbbca4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196133843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4514bfc5d0f590d09d73efa92e2c8f6df2715125782165bb584b8567a400fc34`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:24:45 GMT
COPY dir:61bea833528044db01491107d8c3fb583322243082c7798fd60ade98f7eb7613 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:24:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:24:46 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 21:24:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 21:24:46 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:25:02 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 21:25:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 21:25:02 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 21:25:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 21:25:05 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:25:05 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:25:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaf3a51e65fb5be60868458603f429cd0b008b781e06c9e52fbd6018557aac4`  
		Last Modified: Wed, 24 Apr 2024 21:48:20 GMT  
		Size: 145.1 MB (145095325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662fa3e36995676c24c1b9d01f98ea06ae5b4c3e5291c9b65351d5647879d865`  
		Last Modified: Wed, 24 Apr 2024 21:48:10 GMT  
		Size: 17.5 MB (17488468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890d89e32fd4398cb9978dd855367a44bd40304cac5d4484601cdf6c8a293f30`  
		Last Modified: Wed, 24 Apr 2024 21:48:09 GMT  
		Size: 4.4 MB (4399170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3564a9699a37fa511c885cef79f04726dd5f41c9edfc7089f0d89026eedbcb3a`  
		Last Modified: Wed, 24 Apr 2024 21:48:08 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c1ea1bd1a5a8dd848f078834215e12cda23f5fc34d6829312f48371e129a12a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194782660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05948a7e929de1b9903cd80b795cac840a61ddc73bc2756ede9e6ddb7d6ab41d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:43:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:09:10 GMT
COPY dir:894420f494a8d73ff0a7e5986ef0142218654b95343c81b2b9fc9a9d3ea0c174 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:09:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:09:13 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 19:09:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 19:09:13 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:09:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 19:09:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 19:09:27 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 19:09:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 19:09:29 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:09:30 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:09:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760600a5e2889343637bf277e65d485b109927b87e8fcdc44cb39ef52ec19dd1`  
		Last Modified: Wed, 24 Apr 2024 19:28:33 GMT  
		Size: 143.9 MB (143891815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e19d2d2b81d204045c8e1be2e45cc84a2e7d0f5b747f11f4cc9aa7efaa992c7`  
		Last Modified: Wed, 24 Apr 2024 19:28:25 GMT  
		Size: 17.3 MB (17311343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4769181dc1ec323737bd1a3c20cc48081e84cc3632d4ccd9a9aee16f28f4509`  
		Last Modified: Wed, 24 Apr 2024 19:28:24 GMT  
		Size: 4.4 MB (4399165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46065c6da30afee6af2df9d6d42d0979b5b5cf6f6ad9fab47cf3ee7eefa1f37c`  
		Last Modified: Wed, 24 Apr 2024 19:28:23 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
