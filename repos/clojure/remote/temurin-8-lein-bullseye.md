## `clojure:temurin-8-lein-bullseye`

```console
$ docker pull clojure@sha256:3b5de45a3c4afbc474d03cf67106c50baf7e4384c66cf49d4671ecf127fed470
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:26c6f35f9768498a7ed4120951c9a361b547b1d0479cab97cc59a28c270dcc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130117958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4b2349dd80dd6593154749d7e249be2abc2f1e683496d40e22b67acf6cb334`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:15:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:15:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:15:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:15:38 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:15:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:15:38 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:15:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:15:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:15:52 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:15:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:15:53 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad41bbbd8855cd51d869142e12ac8fb77cfd5b1a58c5a21b30ee9f4da8b244fe`  
		Last Modified: Thu, 11 Jun 2026 01:16:07 GMT  
		Size: 55.2 MB (55198726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092eaf8d7f380912ed20b8072492e62c1677ce8ebad6f93732d1f32f51208ea4`  
		Last Modified: Thu, 11 Jun 2026 01:16:06 GMT  
		Size: 16.6 MB (16629730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1e888684e3de78ec967ebc549534c00af5e148b1aa31aa5e84ba1495b0a81e`  
		Last Modified: Thu, 11 Jun 2026 01:16:06 GMT  
		Size: 4.5 MB (4517701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a03231965fb05fd89f8dda8c782a7b3e98c139c0258070f4cb79845bb20c1c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4623378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f61da978d8f545c16390abf555591407b7b95f82d4f6ac98b209656492957e8`

```dockerfile
```

-	Layers:
	-	`sha256:c5dc7613452730480da77526f3eaae81173eca0c5f0b0b2506417ce37e7f369a`  
		Last Modified: Thu, 11 Jun 2026 01:16:06 GMT  
		Size: 4.6 MB (4606855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70543fc6fc23e282ce77800fa055785927dccf549a1c842c85db9b50de318ed2`  
		Last Modified: Thu, 11 Jun 2026 01:16:05 GMT  
		Size: 16.5 KB (16523 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:97e6969a8cc3b5365cffc8f11380987f8b5053e5c3e531813308eefe2f01756c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127671485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c1412b7f505df306b44099664ff971e37fc0baecd7d164abfa721e51688228`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:19:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:19:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:19:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:19:50 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:19:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:19:50 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:20:04 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:20:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:20:04 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:20:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:20:06 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704140f4ccc23cd95e72cae970d9693da982284a7d09474f18b92e1975ba9fbb`  
		Last Modified: Thu, 11 Jun 2026 01:20:20 GMT  
		Size: 54.3 MB (54272923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb90c2f5c14a0378ed5fc78f73c445e8019f0ffa792edad13f4c8fe0ad3e0e0`  
		Last Modified: Thu, 11 Jun 2026 01:20:19 GMT  
		Size: 16.6 MB (16616708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29b0b5658ba75617dac808a2122d62f893d4823b282bec177cb6fbbe86fc393`  
		Last Modified: Thu, 11 Jun 2026 01:20:19 GMT  
		Size: 4.5 MB (4517708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9c24e1839e662fb9c3dd08bee3d3dc52c81b76465e117bbea0ef4d6f9ab915e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4623174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051af40f28fb465c6796c83f2f5713131c92e50fe95e4fefd8366710a2c68e77`

```dockerfile
```

-	Layers:
	-	`sha256:bcba2f78d063946aad0c9e7fab29c60ac3324663a4937755ccc51f78dd3d64c1`  
		Last Modified: Thu, 11 Jun 2026 01:20:18 GMT  
		Size: 4.6 MB (4606529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:688cb0d016f6e3c56802ceba751c2bdf71c29d4bd843631752f30504be93492c`  
		Last Modified: Thu, 11 Jun 2026 01:20:18 GMT  
		Size: 16.6 KB (16645 bytes)  
		MIME: application/vnd.in-toto+json
