## `clojure:temurin-8-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:0316fd9e4d3f99d818ff9778709c4b95eba80f62e839c64c8a987196d6ba1739
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:34b630bf66e7b27315cebdbb0281f588aaa6bdb5e8fd28ab54c57d58ccb46e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130080300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e6daafb16d666bf2c3f9c465dbb9377a7ce931c8af9b45429e42be153909930`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:00:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:00:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:00:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:00:27 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:00:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:00:27 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:00:42 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:00:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:00:42 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:00:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:00:44 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9afda9ebd4ab8afb8310bd64ba97823c2ab9ae04ad2bb766c5dbfbb3a71ed0a`  
		Last Modified: Wed, 15 Apr 2026 22:00:59 GMT  
		Size: 55.2 MB (55170109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74674cae508b564743d69d672d1e7da40d07bf4e3984ed6fbd92e9092e4fe858`  
		Last Modified: Wed, 15 Apr 2026 22:00:58 GMT  
		Size: 16.6 MB (16629650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93812053b4adae59089508083a1975f3249d8fa24502d24b76edf70fb47dc065`  
		Last Modified: Wed, 15 Apr 2026 22:00:59 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6cde5b97794e2bea0639dc4b70681c2ac291e57ffbc85935dd46df12b400c6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4623221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f732afa86e8c5be1a4d7c191e4170c810fac027bece4e0e7427a0681556ecf9a`

```dockerfile
```

-	Layers:
	-	`sha256:6cf9e39292d351ef40315fa0db9927d752c7a48ca26737451438bd439183099f`  
		Last Modified: Wed, 15 Apr 2026 22:00:57 GMT  
		Size: 4.6 MB (4606851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbbd196b6cb7316f3848d27366a95599c0a38293068799ddfeeaba03390e654c`  
		Last Modified: Wed, 15 Apr 2026 22:00:57 GMT  
		Size: 16.4 KB (16370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f4aac2bcb3a180ae562d17d8846867587a2f3c960925fd435359fe04a1ebe1e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127633488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a6bb094fbe6557102f5f46fe34ef57b1be83551a4d2a539fb2c884dfcd3c8b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:12:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:12:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:12:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:12:08 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:12:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:12:08 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:12:22 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:12:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:12:22 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:12:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:12:24 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979a44f6b41a94c270eb987165ecfea5988684298cc964ff19c8773ccffa6873`  
		Last Modified: Wed, 15 Apr 2026 22:12:39 GMT  
		Size: 54.3 MB (54251620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df141a2ee9afe22b0536b8f9d8903acc36af7edd658376f14076d6f82329665f`  
		Last Modified: Wed, 15 Apr 2026 22:12:38 GMT  
		Size: 16.6 MB (16616501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af4cb87f8bfb78b46b8fd00195cf95ae317a346a404270fb74484e2516c9090`  
		Last Modified: Wed, 15 Apr 2026 22:12:38 GMT  
		Size: 4.5 MB (4517720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:476c28d51bbf59db9932be8e82f75193cbdc5351d7a0222ec59924a4a4375c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4623015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c794b04ea708070b0e626d65b7a248affffdc1e61768897d3a65494b29619c`

```dockerfile
```

-	Layers:
	-	`sha256:357d6eda1e6d153cf2697db817c9080c7ffa74caf2af5fffbb7fbfc266e038c8`  
		Last Modified: Wed, 15 Apr 2026 22:12:38 GMT  
		Size: 4.6 MB (4606525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14155f733edbeab650bc24219acba086301458edd231d7810460d606c7841d89`  
		Last Modified: Wed, 15 Apr 2026 22:12:37 GMT  
		Size: 16.5 KB (16490 bytes)  
		MIME: application/vnd.in-toto+json
