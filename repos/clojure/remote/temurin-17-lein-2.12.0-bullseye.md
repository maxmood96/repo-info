## `clojure:temurin-17-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:130e0031627b47503abfd770fdcc7a3faa997edd3c0f6ccd94c00e11297e7b13
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
$ docker pull clojure@sha256:e1f470d55967fd74d74a27afc9d1bcd6aee8e7f410cba21da29958559e515382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217818463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81736ca1078c959a5b52793afef7d85ad3efeb38542329fb96c5d7c91f91eff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:14:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:14:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:14:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:14:53 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:14:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:14:53 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:15:07 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:15:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:15:07 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:15:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:15:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:15:09 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:15:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784c49115287550ea7b3bc7425362fe05072367e0729bbabed73e05dafa8369c`  
		Last Modified: Wed, 15 Apr 2026 22:15:29 GMT  
		Size: 144.4 MB (144436187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04f88b0bf127aeda4a6387bd32137e63df54456ac7cbc0182881c986ada7f0d`  
		Last Modified: Wed, 15 Apr 2026 22:15:26 GMT  
		Size: 16.6 MB (16616495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f691229e50b7d44e31fe56c9261fa7c632699121682dba6cc584caa2be0dfb`  
		Last Modified: Wed, 15 Apr 2026 22:15:26 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9041e4aee9361acac0dc1191f8c573b237a62515a7469e6628d1c3bdc39ad22`  
		Last Modified: Wed, 15 Apr 2026 22:15:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:eaa8555e434dce74ae04bb7c69ebdfe34963d3619428c8cc336cf10236eeb102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4503325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda40482022d60433454a80890801456f9f4f20416ee673f60d4b5e7d60ae8ab`

```dockerfile
```

-	Layers:
	-	`sha256:ef0faac8c6bffec182693a038ef7fd9378ec88fceff35d0b72938177731ff659`  
		Last Modified: Wed, 15 Apr 2026 22:15:25 GMT  
		Size: 4.5 MB (4484836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d9e391005a7f82cd590eeda7a7d7cc8cdb4647b20648928bc69589c3100c5ab`  
		Last Modified: Wed, 15 Apr 2026 22:15:25 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json
