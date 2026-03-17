## `clojure:temurin-21-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:d3172c406404080a730c5522f27e3a718b2ac60c50613052cf564ae1369c7ad1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5eeadc89dc84c296e8d21d42bf1d6918074b6d81f3bf84807911899144e44617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (207971857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0d72b76bdb9bd9e62413c09332479bc8173bee3f60898450be8f89170bf1bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 02:59:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:15 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 02:59:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 02:59:15 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:59:29 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 02:59:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 02:59:29 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 02:59:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 02:59:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:59:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:59:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d7905f77ed7a7183e2669447f35db5a753f56f747af9e16b372641bd5e5163`  
		Last Modified: Tue, 17 Mar 2026 02:59:50 GMT  
		Size: 157.9 MB (157857092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fed34591874d36539f373cfd53486430c215ed4f786fcf5364ae5725918ebe4`  
		Last Modified: Tue, 17 Mar 2026 02:59:47 GMT  
		Size: 15.3 MB (15338811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43656bc96aa7354820a48feecff21649e678cf97b3a0420480995c34c3dcc3e5`  
		Last Modified: Tue, 17 Mar 2026 02:59:47 GMT  
		Size: 4.5 MB (4517700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423fd46ac61cb76fcb61d30f1d9a34c6a259bd8af521124e565a35c314cb1c1a`  
		Last Modified: Tue, 17 Mar 2026 02:59:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9784a19d454a4727e2da10c9c5cfe6376db8cd11f082c2c112f27a2b9b3b7c8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120c6ef70d295a94e1b57b609e55f8a46724d7e901bcc50359c7bb1d738b53a1`

```dockerfile
```

-	Layers:
	-	`sha256:b4b76c39009468efef1c8924b0cf24c8057cc8af46c9aaaf8a633ef9520dcdbe`  
		Last Modified: Tue, 17 Mar 2026 02:59:47 GMT  
		Size: 3.0 MB (3029434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dfa7c7a0ab97a31854198ab494ebd4baefa2244ca29f47331884a959033fb24`  
		Last Modified: Tue, 17 Mar 2026 02:59:47 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f1b5c46feee10cfb12445f062398fb896fbae30911f6d9ecaec788579a0d21d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204723036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e58e9c33a54514ff74a34fc6eda0f526f69c7a4fb4e6054d95408bc963a23d5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:04:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:04:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:04:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:04:02 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:04:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:04:02 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:04:17 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:04:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:04:17 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:04:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:04:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:04:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:04:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48751576bad0dec218ac56d778963af33bd1b5c1a3e88e4dd072ab454b5a074e`  
		Last Modified: Tue, 17 Mar 2026 03:04:42 GMT  
		Size: 156.1 MB (156133067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7669391b80d11c2049c34dcf289e44a7a1769b4d265908e5e17a61aad6b041`  
		Last Modified: Tue, 17 Mar 2026 03:04:39 GMT  
		Size: 15.3 MB (15327263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71c4655fa1fb303b27c6272088ccc1f08c44571f2154ec2d5b5d2f866503486`  
		Last Modified: Tue, 17 Mar 2026 03:04:39 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552c8b4b3f2613fa8e9ae3d083d38ef574e265440ad51ca3e56a4484cb6af65d`  
		Last Modified: Tue, 17 Mar 2026 03:04:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:897612a51e84d73af38139cbb3aa42970cdf80bc891d4ebfd40b76b02827a0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489972055b7ccd437dce43027ce376cba03fc62436b7b30fa1c7b77564149d31`

```dockerfile
```

-	Layers:
	-	`sha256:88f3ea1be5c429cfbd47e295b12364147c5509a5d9d5af18ed6ae43339718d89`  
		Last Modified: Tue, 17 Mar 2026 03:04:39 GMT  
		Size: 3.0 MB (3029043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26887900e57c1c8a2788a1d34c08be7b418fc8290c500c2f37bf430739a51a24`  
		Last Modified: Tue, 17 Mar 2026 03:04:38 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json
