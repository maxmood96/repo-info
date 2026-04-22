## `clojure:temurin-17-lein-bullseye`

```console
$ docker pull clojure@sha256:10d4828b729bf670aaf30951db634f06066b9c8cfb990da847d2e376330dab4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:601398e39059e08e3d07b7d49ed3979d1d40e39fba3c17bc2f7049d46fa51555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220539359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c26403a3d81ed9efec08a241396fa124dc138b6ce18e8801a954a2a6e6a411`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:03:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:03:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:03:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:03:36 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:03:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:03:36 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:03:51 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:03:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:03:51 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:03:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:03:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:03:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:03:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eaee25846334ad9ad669d2755afbe2807a29fcf3074a7da96353284382dfada`  
		Last Modified: Wed, 15 Apr 2026 22:04:13 GMT  
		Size: 145.6 MB (145628761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994583d75350042c35237464b8bfd63f4caf3fd51ca66a8f0553f5a9ee722ffb`  
		Last Modified: Wed, 15 Apr 2026 22:04:10 GMT  
		Size: 16.6 MB (16629630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7110e978596ca08db6a94f7162e5cd40c2f21a04ffd71497744e1f01d3052df4`  
		Last Modified: Wed, 15 Apr 2026 22:04:09 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3da28cc7b4e8b63808463f7985bc5166271321d11ff2e9a281f1270542f421`  
		Last Modified: Wed, 15 Apr 2026 22:04:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4ee272ab1c4cb49f33564ded8924c190db4957c448fcbe0206033a896d83de04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4504230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca46471a8564a5a196b4d62389ef13ac506577329ae4a1714e767e45a4bd84e9`

```dockerfile
```

-	Layers:
	-	`sha256:ca74534ca1ba9eefd1ea43ebaab4909c5dff78011b28727fcd79d9c0e71b24e8`  
		Last Modified: Wed, 15 Apr 2026 22:04:09 GMT  
		Size: 4.5 MB (4485862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4369800df6d4c0a0ddc503e23635c273d8342604e45e473aa926124140d74a69`  
		Last Modified: Wed, 15 Apr 2026 22:04:09 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:94ede4ccb66a0dec22612b20e31c631491782dbf3dab99942fded0f91a164834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217823893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb232afc1e6e0cb08d2248b145fa61e282d137b0e974b5331017ea3eaaeb6048`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:21:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:30 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:21:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:21:30 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:43 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:21:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:21:43 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:21:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:21:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:21:45 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:21:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9b73b39422eed403216bc8b2b019cefc6dd1c13ee305c8335f530dd9c7b891`  
		Last Modified: Wed, 22 Apr 2026 02:22:06 GMT  
		Size: 144.4 MB (144436212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc18891850b5025168b7f66787febe6970c4332c651f861a259a8bf92cb6728b`  
		Last Modified: Wed, 22 Apr 2026 02:22:03 GMT  
		Size: 16.6 MB (16616504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d8a3d0a0ae84de4e7e23f90bebf7ca3ab44dbc3667c51a50099ea7357e602f`  
		Last Modified: Wed, 22 Apr 2026 02:22:03 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517e11f89c114e07a06f71188ec543f394833c22489e72506019d8a50fb5e496`  
		Last Modified: Wed, 22 Apr 2026 02:22:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:282eb2b1c9aed566c33f09dbcfabf3d0bc440653425fad61f10352410d6d8a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4503325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6004e60e7167079478e03be9f656bc60acd8c3cb4121e5167e376a5fadc1936c`

```dockerfile
```

-	Layers:
	-	`sha256:3b163626b3ee4dfaf3fa0bf3e6da5022cddac920cb27da1de81d30697e8d708f`  
		Last Modified: Wed, 22 Apr 2026 02:22:03 GMT  
		Size: 4.5 MB (4484836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f003fdcd84188af607b0b08abd56876081d3d2917441b6db939306c690db8b91`  
		Last Modified: Wed, 22 Apr 2026 02:22:02 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json
