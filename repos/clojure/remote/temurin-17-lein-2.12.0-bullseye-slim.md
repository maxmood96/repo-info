## `clojure:temurin-17-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:3cfc1071c742870b1958cb7a9cc290f863687bb9e89652c586a5370a235849fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5cd9ce813ae178544289b6eaea9066e26096094404fd73a69eab92e4e96f33c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196020082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e6920b017860fa66e5e4b41b349fe4160e55046c93940417b747412404244d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:58:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:58:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:58:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:58:37 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:58:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:58:37 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:58:50 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 19 May 2026 23:58:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 May 2026 23:58:50 GMT
ENV LEIN_ROOT=1
# Tue, 19 May 2026 23:58:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 19 May 2026 23:58:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 19 May 2026 23:58:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 May 2026 23:58:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e8fd17ad2e1b98c46ef6b321ca3d58f50bd64cddf86fa631d7324443723f5`  
		Last Modified: Tue, 19 May 2026 23:59:12 GMT  
		Size: 145.9 MB (145905467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7545bc103c5d42e3758d301d829e7f262f4c10c3f037bebb0de81ec0ecc76bac`  
		Last Modified: Tue, 19 May 2026 23:59:09 GMT  
		Size: 15.3 MB (15338868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea73de70e5c9ecc4d53d3fbd5fc48a42170f4d9c8325a2a3011f740973095114`  
		Last Modified: Tue, 19 May 2026 23:59:09 GMT  
		Size: 4.5 MB (4517721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11da91a76d8d6fb7e3a41afaff0b84cfc2220f87c73e1577213a86fcf624faf1`  
		Last Modified: Tue, 19 May 2026 23:59:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:69e0edd184b840acf857aaa6e7cee2d123da320d2d4e7f0deb77c249d34625cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1caea402572392054cd9bdb6600ca3b3da4c591be07d0fa0778ca96acd73595f`

```dockerfile
```

-	Layers:
	-	`sha256:5d18bd9ff1fef94c6952a087e867cc201c35d859d41ce0b47be392387b12d947`  
		Last Modified: Tue, 19 May 2026 23:59:08 GMT  
		Size: 3.0 MB (3028209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38abaddfa4dbe3c25e619c80e85199b8af22956be6f620926dd0afc91d5b5211`  
		Last Modified: Tue, 19 May 2026 23:59:08 GMT  
		Size: 18.6 KB (18557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:af0158974a1b89924a2f69b464d92bd69695ee4f3606f2c043982b55b2c0bbc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193312692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3fabe926434756d4094bf99998ed56fa36abf0da9462750fcefed9213be5b2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:05:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:05:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:05:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:05:30 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:05:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:05:30 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:05:43 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:05:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:05:43 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:05:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:05:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:05:45 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:05:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbcc73e87c8c5bdbfc3c12a004cb25c4703867a7de1d00e1437d0a7f1ab6f92`  
		Last Modified: Wed, 20 May 2026 00:06:05 GMT  
		Size: 144.7 MB (144724334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c783c8c1c561ea5d7c4579accbaeabf5c2da6daaf87081d1d59f209bbdbbcb9`  
		Last Modified: Wed, 20 May 2026 00:06:02 GMT  
		Size: 15.3 MB (15327199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9297d5aa42cb8c1ea59335954c151e2feeb3aaa2c41d0372c8c2466fd41145ae`  
		Last Modified: Wed, 20 May 2026 00:06:02 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867bfd0621d12b6d34f9a5061ea0081f5e83d3b2af6743eca2dcca1841bdb9fd`  
		Last Modified: Wed, 20 May 2026 00:06:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d8fbea5bbf3616fe6ff0a447c8286ca9e0bae6c1685b2626f11e6c0fe4db9946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a1845dd5bb6fd4c3c3018f59b1140bcbd914195f6c8ce07bacd058cee4cbfb`

```dockerfile
```

-	Layers:
	-	`sha256:9f12200ce6bb77932f1fa8b272aa00d9f0980cb29eeee119e220bd13889bf372`  
		Last Modified: Wed, 20 May 2026 00:06:02 GMT  
		Size: 3.0 MB (3027818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4637dcfb90c6e81012a70cd3574d7c03d800e4cadfe9d66921c74da9c0768bce`  
		Last Modified: Wed, 20 May 2026 00:06:01 GMT  
		Size: 18.7 KB (18678 bytes)  
		MIME: application/vnd.in-toto+json
