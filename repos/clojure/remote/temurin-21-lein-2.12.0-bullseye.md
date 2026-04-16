## `clojure:temurin-21-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:129f1e5eb9b4da640a615a077d94ff3ad0f944cc2941f1e8f6d82f1f33745233
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f3d84ebf709c358927014e161aebd7d33e280209fef6a6be61c7b9342387d704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232767668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c21c29e3d4585640405f7e60290b4ece7ff54964596a18cb5adeea314a1096`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:04:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:04:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:04:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:04:56 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:04:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:04:56 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:05:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:05:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:05:11 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:05:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:05:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:05:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:05:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f7e20462fde802c8cbab4efa0d314780c8c8ed30a2848822b0f09005814319`  
		Last Modified: Wed, 15 Apr 2026 22:05:33 GMT  
		Size: 157.9 MB (157857054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d088376c9e081be426cf974a7000c0a9bdad343723cad90e4aca256444b65a1a`  
		Last Modified: Wed, 15 Apr 2026 22:05:30 GMT  
		Size: 16.6 MB (16629659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c88e8f62be9d52242cf31a1ecd8e5ce9d2086062e116226758ab71ef7d26019`  
		Last Modified: Wed, 15 Apr 2026 22:05:30 GMT  
		Size: 4.5 MB (4517733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c4f4b0de84eef849ac151aef8332a8ef993d8fc54c482fb32acfbf6f8d477a`  
		Last Modified: Wed, 15 Apr 2026 22:05:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:369f3a15b5721d913e987bfe2d92c787e02edec707d29253e6d1965877f2c78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463c69145d002064fbaebffc58fa3028a3b80d35fc812f6776dbbeaababe15e8`

```dockerfile
```

-	Layers:
	-	`sha256:9206d956c8fc235ead9fdf707ad0fc2127fe1bf1e0461474d140e87f7d7ca89a`  
		Last Modified: Wed, 15 Apr 2026 22:05:30 GMT  
		Size: 4.5 MB (4487714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f9577723bd705d8d5dfc998ba6c48e21736f0c6f63b0098389a370873be0f84`  
		Last Modified: Wed, 15 Apr 2026 22:05:29 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5f86dc1b7e8ab502d3f502ffca07741d760785da37ceb6a969939453cc83a0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229515194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f9ff88b1c353849c43cf48fd88d0a57d058a4902322ecf94b69251878a3fbf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:16:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:16:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:16:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:16:30 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:16:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:16:31 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:16:45 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:16:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:16:45 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:16:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:16:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:16:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:16:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd3f78301febca1f602dcc4b43c8e2b888f6975af822a4048be100adbbb17e1`  
		Last Modified: Wed, 15 Apr 2026 22:17:09 GMT  
		Size: 156.1 MB (156133057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabf11a4264faaab9d83ab56ba66a040bc2559e5847923827c75b5eddf281283`  
		Last Modified: Wed, 15 Apr 2026 22:17:06 GMT  
		Size: 16.6 MB (16616383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb275413772e04793c97151660d9794bf95d1f48a4eba80ee9060f7714e74c0`  
		Last Modified: Wed, 15 Apr 2026 22:17:05 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a642db59c916aad91cf702f09d230e7a5d8fbb1a5fe818523e1e21f0c2f4d8af`  
		Last Modified: Wed, 15 Apr 2026 22:17:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cd591d1f4d984d861ac709e1ebe2ac5c44df5e2ce4fd9fe5d54f83731d60ffbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4505177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d21f12f229a3b8c7fe543a03e2b5d7d6c0f16b90b5d241128dd21c8e37147d`

```dockerfile
```

-	Layers:
	-	`sha256:23e202bc2fefc76a2fd4001a9fecf1a94a2d6480ba035e239ecef714a293242b`  
		Last Modified: Wed, 15 Apr 2026 22:17:05 GMT  
		Size: 4.5 MB (4486688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de9c2a7f6becd9e5ef6b5be428ef02401306db410c67452de6422b2675c75869`  
		Last Modified: Wed, 15 Apr 2026 22:17:04 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json
