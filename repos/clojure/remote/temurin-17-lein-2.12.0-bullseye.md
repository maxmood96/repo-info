## `clojure:temurin-17-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:943f76ee1cd60140b4f576cb11498a3bfe74bf9589a6145e03dc84dda3ff54aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.12.0-bullseye` - linux; amd64

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

### `clojure:temurin-17-lein-2.12.0-bullseye` - unknown; unknown

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

### `clojure:temurin-17-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4ccb87428a0b4db43ce99b9e1a8b082635d57b07818a2312c690f54a36558bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217818580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c26a391283f156fcf906ab6be6647f94173e72ab50dbc5e467fd8b60edd244`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:25:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:25:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:25:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:25:05 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:25:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:25:05 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:25:19 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:25:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:25:19 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:25:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:25:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:25:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:25:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028c8e3df7a31205969e81f0a1cf5c58c19aefc586846fd5f53e663b1976e97d`  
		Last Modified: Tue, 07 Apr 2026 03:25:43 GMT  
		Size: 144.4 MB (144436223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d32777f4da907ccee62ffcba3a086c46194cc1780c4f29e5d67f720f1de275`  
		Last Modified: Tue, 07 Apr 2026 03:25:40 GMT  
		Size: 16.6 MB (16616571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c6d209ac62600987c25ccc77e867a8a2b8b9c394bbf7e85c31269149f876b6`  
		Last Modified: Tue, 07 Apr 2026 03:25:40 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576e69e6848ac8aaf8ba8efae3739c09509a5bddd6c9dd046c57c5d982635270`  
		Last Modified: Tue, 07 Apr 2026 03:25:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:510ebc506cdf90c9ae2167635066b18d4273ce5caebc56dc7e69ec3998c97b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4503324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b038a8fe909e35b608180c637166a4377bf5bc8051f8adc2bc0205a13e06383b`

```dockerfile
```

-	Layers:
	-	`sha256:b612858ff726f916994516ac88148114941502a771dfe725ca3cc6b4b6a41a71`  
		Last Modified: Tue, 07 Apr 2026 03:25:39 GMT  
		Size: 4.5 MB (4484836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc4843162946619ee571ffb6c9aa358c380f075467a9513a911205fd28ceba97`  
		Last Modified: Tue, 07 Apr 2026 03:25:39 GMT  
		Size: 18.5 KB (18488 bytes)  
		MIME: application/vnd.in-toto+json
