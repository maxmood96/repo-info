## `clojure:lein`

```console
$ docker pull clojure@sha256:841c467d308e0444a090a22c8779f7caf8109dfacf231a92f3c8f33551f88c22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:lein` - linux; amd64

```console
$ docker pull clojure@sha256:22380b081bf5e68a4c63aa6afeccaa889d0eb6dfdcd38e368f85d7a0a8e16424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164847583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a771515b61518c35e8280a76dd3032fba6a95fd8f2112338eed495ec84e32377`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:37:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:37:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:37:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:37:18 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:37:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:37:19 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:37:34 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:37:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:37:34 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:37:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:37:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:37:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:37:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b956ddb8c3e6eb3cec91807cca3bde29781c24d90593bca494ae90b5b77f4`  
		Last Modified: Tue, 13 Jan 2026 03:38:19 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dccb4296a3a766680311105266c0f92cfc5a2deb8f69b1383fd5293af63ffe3`  
		Last Modified: Tue, 13 Jan 2026 03:38:05 GMT  
		Size: 19.8 MB (19802535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d536256ccd5c7f52692de26c23c7264c63343da6eb9f53ba1e6f4ee1e31fd04`  
		Last Modified: Tue, 13 Jan 2026 03:38:03 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0e19e4310654f87c428984efacd2c15a64a4e94f146e18f49a9e0020174f68`  
		Last Modified: Tue, 13 Jan 2026 03:38:03 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein` - unknown; unknown

```console
$ docker pull clojure@sha256:ba48511f67ed04a3a9c24c3e6a4eebd9da3ccf030f365092643556eefe7dbe4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4253298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30b49b9ed528eb933d85c9d5efc96292112eba4520b4824efff65a158e5550d`

```dockerfile
```

-	Layers:
	-	`sha256:93598538ad4a1bddc3539b1bb659fb5bcbe132c8a1048fa98609b8c4a0fdecf1`  
		Last Modified: Tue, 13 Jan 2026 07:35:37 GMT  
		Size: 4.2 MB (4233039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1a8d8469272c33e19419dbbf33995cf9d8227734216cdef567f33782bd20078`  
		Last Modified: Tue, 13 Jan 2026 07:35:38 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:40158cb7ac3be7628f47530444774d99a01e98a3989b7221c4ca7cb19df18a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163569431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb49e9e8a714dbf3b7bc09246c16907cd1a23647e0cfb3a4fffd3beb9716f04`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:41:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:41:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:41:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:41:13 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:41:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:41:13 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:41:27 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:41:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:41:27 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:41:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:41:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:41:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:41:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a623d413abc5000168dca711d85d1dc25981645490e7c4c47bdc47c58df0d0cb`  
		Last Modified: Tue, 13 Jan 2026 03:42:07 GMT  
		Size: 91.1 MB (91052501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5421d39a0da76df19f12486a7e326106edb113ea2c41f41564542f151c0232f`  
		Last Modified: Tue, 13 Jan 2026 03:41:57 GMT  
		Size: 19.6 MB (19632680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28292d6ec63aaf5df774b49b50c22d06beb25b04eff547bea861f336ed1fbc9e`  
		Last Modified: Tue, 13 Jan 2026 03:41:55 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba77a9e51fc38b2c6b491afc70646d885a0ffd2abb823527245d37c5c678e14`  
		Last Modified: Tue, 13 Jan 2026 03:41:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein` - unknown; unknown

```console
$ docker pull clojure@sha256:39155d9b0daf12644ab06145cdd0b5db1fae491378b97d7d4b3c9832be822518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4253175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a525affbc8286ccd89481995053c1855d598ebbf5ccef4d60028eec88543bee1`

```dockerfile
```

-	Layers:
	-	`sha256:8f2aef35a233d7a41f96acefdfe706500325480982e3f9d95d1872eb48ac0054`  
		Last Modified: Tue, 13 Jan 2026 07:35:43 GMT  
		Size: 4.2 MB (4232723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa9937eeef6818531a9838cb3fcf792ba7a9e00f4b50ced458a745c10aff2d1f`  
		Last Modified: Tue, 13 Jan 2026 07:35:43 GMT  
		Size: 20.5 KB (20452 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein` - linux; ppc64le

```console
$ docker pull clojure@sha256:ca85fcd76a43cc64fa40b893c6409d9d639662a09cc49129f7c738419824ba3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168478769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7fa7a1621ff784d5b51f9a0f016e5f0257dbc6a9b106d43d36a7d5f50ddd7a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 05:29:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 05:29:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 05:29:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:29:37 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 05:29:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 05:29:38 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 05:30:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 05:30:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 05:30:20 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 05:30:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 05:49:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 05:49:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 05:49:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:39 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b170658cc3480535e317472b552956a72545fa3b10ff67eeabf8ec9da0a276`  
		Last Modified: Tue, 13 Jan 2026 05:32:49 GMT  
		Size: 91.6 MB (91610769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7393adfb4e13837e196cfe7384060b5302448f32e49a09dc0528bcb7619fb9ff`  
		Last Modified: Tue, 13 Jan 2026 05:32:24 GMT  
		Size: 20.0 MB (20022437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64767704f764063c04d10d0f10b0a3be3e038704eaa19447c51250c891cdccb9`  
		Last Modified: Tue, 13 Jan 2026 05:32:21 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe5dca6141acc939fa128a9b55788567ed6ff37af45b6d6c81bfe1c7eaba448`  
		Last Modified: Tue, 13 Jan 2026 05:50:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein` - unknown; unknown

```console
$ docker pull clojure@sha256:7139867d301d3ea893b6e1783b8008e14a1eed9a41ccbf6043acb0891aff64e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4255774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a8913df4da9b5a3bd7f38b6ec7888f6de0bd304f5090ab94a7cc098c8e6542`

```dockerfile
```

-	Layers:
	-	`sha256:27e98b14bcbadf22e0e71dc8a1e8a5e152d3ee3924b8d041ad424d733463d3ae`  
		Last Modified: Tue, 13 Jan 2026 07:35:48 GMT  
		Size: 4.2 MB (4236234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:579ca664e501750185950bf42e7ab4bed852c3f856811b4c918b73bd31bde7db`  
		Last Modified: Tue, 13 Jan 2026 07:35:49 GMT  
		Size: 19.5 KB (19540 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein` - linux; s390x

```console
$ docker pull clojure@sha256:0ef33deac8993b2e930396bfce7c174880f4e6155e0d7fd6767a8726ec2985ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159329285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8497744d19a9eb4fc88c2641b8e613740beb16f1a5a53ef1b8a5160e80267be2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:06:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:06:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:06:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:06:49 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:06:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:06:49 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:06:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:06:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:06:59 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:07:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:07:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:07:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:07:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59357e56c5eabe42db724069fed8dafeb8cd07f5df0a3442d2e90ddf3c2420d6`  
		Last Modified: Tue, 13 Jan 2026 03:07:43 GMT  
		Size: 88.2 MB (88210715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411d89beacc1eab403def0f739ce5bb2ffe595713cf115a57fe38ee79d77a4d2`  
		Last Modified: Tue, 13 Jan 2026 03:07:35 GMT  
		Size: 19.5 MB (19461965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91719c9bbd000ff6bb1019da1267a2fe1c4a58a951960f94787ff9ab34ea56c`  
		Last Modified: Tue, 13 Jan 2026 03:07:33 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc130f3bb21f7630d99918a73895a6ec682c26d04e3be0539b3097b348f7b0f`  
		Last Modified: Tue, 13 Jan 2026 03:07:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein` - unknown; unknown

```console
$ docker pull clojure@sha256:4484bad6ab8a69ec41b2eabe452f3137634d36640e5c05a76611506efa3e22fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd190af098446bda19c412a95e19b60b4289cdfb63d4f283cb2ea93bcde6bc9`

```dockerfile
```

-	Layers:
	-	`sha256:654598804542b9b1cabe46f708c690a1c5924bf9618d2a1ec07974c584391e38`  
		Last Modified: Tue, 13 Jan 2026 04:35:17 GMT  
		Size: 4.2 MB (4227401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7de8cd0b345390fa23d33c07a9d273c83007aea6bcfffc3ef4784f7f9abc2c`  
		Last Modified: Tue, 13 Jan 2026 04:35:18 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json
