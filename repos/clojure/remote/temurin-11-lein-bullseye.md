## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:f2fa5a780f16ec82d2f310fbe5312ffa6c949c6c2c66000520d5a25436911be5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:631100bb54187dd8163c284c11564b2f1476a1c0d5f764232b5687fb57b451ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220716957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d08da936b6075d7b8b70f7253e5abdb107906a2ea14793eba7cb8024d8b47c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:02:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:02:24 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:02:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:02:24 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:02:39 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:02:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:02:39 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:02:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:02:40 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39fb37449e696f5b6785eb959876bb7b56e795d6b22296a84cffff34e2e14c2`  
		Last Modified: Wed, 15 Apr 2026 22:03:01 GMT  
		Size: 145.8 MB (145806793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d69ea13037d2702c1e177576abfa7f4a4eb97a6502422cf0983b7094e596f70`  
		Last Modified: Wed, 15 Apr 2026 22:02:57 GMT  
		Size: 16.6 MB (16629645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b23ff2a5ae64b2b9e5231edd2892406a660dd8f2011c5624560ee4c15283fc`  
		Last Modified: Wed, 15 Apr 2026 22:02:57 GMT  
		Size: 4.5 MB (4517694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3c60f9b65380efcc6ebb3ebfd33b450f1650984e80b44ca37dc4c84705f9d812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a5050bc8437617df1b2b669d7eaed11e8c07e388f3f395572ff8ca55628b05`

```dockerfile
```

-	Layers:
	-	`sha256:7e0fb3a973d837d95b2e5cd95d01308bae3e3e3574cafd0f5f43bdea18458ae0`  
		Last Modified: Wed, 15 Apr 2026 22:02:56 GMT  
		Size: 4.5 MB (4506003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfa78201d7cb314b8e5db249fe3d6941103ece00efe099300fa221bbdf591fc7`  
		Last Modified: Wed, 15 Apr 2026 22:02:56 GMT  
		Size: 16.4 KB (16381 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0269b56e30ad5e85f3e28234bd7d2c2f89a149514e0a33a362b2be7047e77461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215882695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fc0167f76ea8d5697bf775bd2783f91a08b97a307c4ae5166ce16d5e972fd4`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:13:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:13:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:13:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:13:30 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:13:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:13:30 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:13:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:13:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:13:44 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:13:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:13:45 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca110c84f751b3f67a74459d3952144bf4b419f2d11cd8d620f4df8bfbf8611`  
		Last Modified: Wed, 15 Apr 2026 22:14:06 GMT  
		Size: 142.5 MB (142500804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1fa946b3e66a1bde29ae05a7cea4893b97227132bce391d3ed2eaf46ba890b`  
		Last Modified: Wed, 15 Apr 2026 22:14:03 GMT  
		Size: 16.6 MB (16616530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0055108baf6dc7cb6699c50b269a634bf1ff581f046a52495090a4c830ffa5`  
		Last Modified: Wed, 15 Apr 2026 22:14:02 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:85dcd2174502bf52c3ae0b06b20cdd29f28c2754dafe2e389248b2b248927b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656ae5111dd2b4bec1df959e9bd733a2c4083a64628b65d5fb2f7ca820fe7b39`

```dockerfile
```

-	Layers:
	-	`sha256:b1ecd8703ef852b87c94c8eba5a77ed7f7fbaf441582a5b825f70974879a6d67`  
		Last Modified: Wed, 15 Apr 2026 22:14:02 GMT  
		Size: 4.5 MB (4505595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:265c326fedd8746e99d5e504246e5f34dab4bb716e2d1ba2bdbc49c51ddef41e`  
		Last Modified: Wed, 15 Apr 2026 22:14:02 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json
