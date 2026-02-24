## `clojure:temurin-11-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:4251b88b468fbf7cf79a2f832a7734cd5d8c8ebc79877b2c37a636e94c5a7a35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ac1a0eb8b3be410cc94f4cce3d0c0899b9ac9cf52e7d4d62bae1e2fcbc6fd929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220710466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e723e2cc4cfafe20ae30e479bc90d5d33073fa8a7ded0321480a66a188aa7c47`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:53:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:53:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:53:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:53:51 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:53:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:53:51 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:54:04 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:54:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:54:04 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:54:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:54:06 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bb0273b39ed9f306b154332a7a8948f2899d6b8cf06d5f26aaa2393003daed`  
		Last Modified: Tue, 24 Feb 2026 19:54:26 GMT  
		Size: 145.8 MB (145806701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624d945891424f4b2db77dea6a4517c40aa839f8ea723c95fa0af824734185f4`  
		Last Modified: Tue, 24 Feb 2026 19:54:22 GMT  
		Size: 16.6 MB (16629552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1300b7e6a1f29863d3acdccab207543df7f63be4ffc87f9f4a30d43f4c43b349`  
		Last Modified: Tue, 24 Feb 2026 19:54:22 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:594ea7da869eb6b25ff173bd8d04caac2d156515f8539794788993468de89c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4524009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10768a431ad1118fcc18f0d710af11e61862a1f3078b7f2f4bffeec0e942b4c`

```dockerfile
```

-	Layers:
	-	`sha256:993a12998c7bf79fe61a680ed4343d33fc557d3037863895c33847bf9dbbe160`  
		Last Modified: Tue, 24 Feb 2026 19:54:21 GMT  
		Size: 4.5 MB (4507627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0473d8af5345b04037dcdba2bc1404b73fe392b8a9f3bbda1f3752ea2f41026c`  
		Last Modified: Tue, 24 Feb 2026 19:54:21 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8e3fb1d246852492d848dced80c40c6d4d999ffd6d76a9b9e573de2e76225861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215894046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb3e2f91739fdbaba4039e516e3d85c0fa9c16b21c75fa47acf991e92ada811`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:04:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:04:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:04:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:04:14 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:04:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:04:14 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:04:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:04:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:04:28 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:04:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:04:29 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2640af19aa6f1d4357dd92dfe2ff171cad48ace966763c1767b48f4e6463b8aa`  
		Last Modified: Tue, 24 Feb 2026 20:04:50 GMT  
		Size: 142.5 MB (142501442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c15f2ebdb2ec06da2d7607aacd368bf3cbda327cf3bb2fa20c96d92e52b18ea`  
		Last Modified: Tue, 24 Feb 2026 20:04:47 GMT  
		Size: 16.6 MB (16616462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159f1231ddf382e77fb321a7cacd4b5c73593f384ee97defcfe80f61ac977445`  
		Last Modified: Tue, 24 Feb 2026 20:04:47 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e226ba0a807a6030c6e5b8b6c4f405f39f5d5f5c315fbd22091086ad67fa5bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4523722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eea1970984f76339937a6288be5047b96b5d8c9ed25a911429f71a9d09db328`

```dockerfile
```

-	Layers:
	-	`sha256:36f24c730b553ae148428d16a92608f78325273f8863651197e5709ab655063f`  
		Last Modified: Tue, 24 Feb 2026 20:04:47 GMT  
		Size: 4.5 MB (4507219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de23d9e5174737defa961321933c50b4f5fddb09226c6c2327545e8dcebda27b`  
		Last Modified: Tue, 24 Feb 2026 20:04:46 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json
