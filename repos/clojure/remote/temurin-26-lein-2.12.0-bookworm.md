## `clojure:temurin-26-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:f61ada52e39809e6c949e2e6969c60d96d7b9cc2bc9a4ab37acfa380860e93db
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

### `clojure:temurin-26-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:207d38e1cce1ebe039d4c25e80c95ed40d948d37d4cc668d090ccf8bab55f892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167357623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff7727643932e9a165e3b832a7d22a228190f8d0b00c7578156fed1036701bc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:21:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:21:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:21:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:21:31 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:21:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:21:31 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:21:46 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:21:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:21:46 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:21:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:21:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:21:47 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:21:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3800082801c401b0011ce0548b4912250ce92ea12a037d1448c6a09de21cd3`  
		Last Modified: Thu, 11 Jun 2026 01:22:06 GMT  
		Size: 94.5 MB (94524373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d846aa7e41f8ba21e8367e1cfc13f022f15358537829640f9a6b786657af537d`  
		Last Modified: Thu, 11 Jun 2026 01:22:05 GMT  
		Size: 19.8 MB (19813072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9832740a6ef2b435d33e35b3f74cadd4df13143586a8078f83efa77797abe22c`  
		Last Modified: Thu, 11 Jun 2026 01:22:04 GMT  
		Size: 4.5 MB (4517709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed591f2cd17d9fbee01650c4cf89c82de19188a839574c704d0f106fbe549b8`  
		Last Modified: Thu, 11 Jun 2026 01:22:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:036e3faba6274be10aba2e0d0f7e58f4c54910710d3f274afe7af895ac0a5e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4267100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4b975646e6e6a968e8f957328e43176beda4699f64033280662daf1a533993`

```dockerfile
```

-	Layers:
	-	`sha256:57a17db9b5b18d6454a33b89def1e53531c3f35cacb1088e7580f8bb8821b457`  
		Last Modified: Thu, 11 Jun 2026 01:22:04 GMT  
		Size: 4.2 MB (4247935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0204bc47c89c98d7943d22ad641e6ceafbdd43d3f50b8b9b93a5e68586955715`  
		Last Modified: Thu, 11 Jun 2026 01:22:03 GMT  
		Size: 19.2 KB (19165 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c633db0d0c28686fdeb14fdc9d7e99505dfb25b6bae55b4783f1e870bdacb1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.1 MB (166054337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28061ddf89dc1db34fe2d0defd16bf74ae8120a2ba06fdd80b40d3e1a974610`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:25:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:25:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:25:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:25:33 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:25:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:25:33 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:25:51 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:25:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:25:51 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:25:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:25:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:25:53 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:25:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cc6083f22e83393bdbca6111b8dbc2e1227aedb7d681a21944dda434bbc957`  
		Last Modified: Thu, 11 Jun 2026 01:26:13 GMT  
		Size: 93.5 MB (93504334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521a753ad9f7315fb4c425524f964b78e758518ae734b38089e55b2236d90927`  
		Last Modified: Thu, 11 Jun 2026 01:26:10 GMT  
		Size: 19.6 MB (19642850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c62be2565a71ace8a2470ad02d70aaa5ee2497baa0458356603f84f5f7fb213`  
		Last Modified: Thu, 11 Jun 2026 01:26:09 GMT  
		Size: 4.5 MB (4517709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4401150381f983bc5931e98e6ace01e8b82934200fd0e91b5335c05c3123982`  
		Last Modified: Thu, 11 Jun 2026 01:26:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8ed55a163e94e9cdf381a53d6f60fca296cb73f7ef5f5623091d73462f2a5706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4512bf6fac2a4d760d7f03575a71b0df8b5073e29673c932bfd4eb2e950f9aa6`

```dockerfile
```

-	Layers:
	-	`sha256:4fe83bbe3fc3b16ce0634f510047f0b4cd26cf47023d746aaafd078a1562054d`  
		Last Modified: Thu, 11 Jun 2026 01:26:09 GMT  
		Size: 4.2 MB (4247571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bec0826de72aa66cde4396540a5689523fe14c8be77251a9780f1880676b67c`  
		Last Modified: Thu, 11 Jun 2026 01:26:09 GMT  
		Size: 19.3 KB (19310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:3665fff8505950da0ce4ce3008b68bd04658b975ef0d429757f38faa47b3cc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 MB (170793603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308b6062f2bff7311c3f1ee9be219d82f1eaf601d5c0a12952dc226bf68b7d36`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 06:10:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 06:10:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 06:10:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:10:17 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 06:10:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 06:10:17 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:10:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 06:10:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 06:10:44 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 06:10:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 06:10:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:10:48 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:10:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a250708f248a2296e18311b56818c5d5e6477c5552cb0d7df7a8d16b02343c`  
		Last Modified: Wed, 20 May 2026 06:11:23 GMT  
		Size: 93.9 MB (93902016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae4802a941d155bc247f6d5010d75d997eb6708384e59cede900b863e68270b`  
		Last Modified: Wed, 20 May 2026 06:11:21 GMT  
		Size: 20.0 MB (20033249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbb17d6b75892e1d15a89b30899e6fc4ed9ebab00e7fa164251b7d7e7b5d32d`  
		Last Modified: Wed, 20 May 2026 06:11:20 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bafdb9cedb0aa77767d9b285cdbb9436e21b2092ac9a3c20b972a66bfb71a6`  
		Last Modified: Wed, 20 May 2026 06:11:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a55dc4eab3104926a5681bda84e2e8c29f065fe342fc221ea64765c20b793534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2577a9e3cdfeae0858e2668a4bbe01742490a051d950f7e4dc1c6ff785598eca`

```dockerfile
```

-	Layers:
	-	`sha256:573d161421455f3fdaa58bd1b475e7f4599cc3c48bf7c2ea54877269d6f03332`  
		Last Modified: Wed, 20 May 2026 06:11:20 GMT  
		Size: 4.2 MB (4233726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9a363fcb21df311811263b7b377bbba25c7549d1e070862c9e36772cb177231`  
		Last Modified: Wed, 20 May 2026 06:11:20 GMT  
		Size: 19.2 KB (19221 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:0688872330344ea01f53066ae2e2bc759e2fddf56ce97c9ae298a9de57d1d213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161691642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0038dac06445a33f4283f84c9a721f04009d609e99128c450620ce1a5678cb50`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 03:15:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:15:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:15:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:15:20 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 03:15:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 03:15:21 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:15:36 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 03:15:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 03:15:36 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 03:15:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 03:15:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:15:38 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:15:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9599dc914187bd0773e9a9bfca693b301ec556e0366d3639bd6b7023bafb8e5`  
		Last Modified: Thu, 11 Jun 2026 03:16:07 GMT  
		Size: 90.5 MB (90536968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8df513fa7be9243009fbb0dbc8edac8a0697a33f8b03c4488b1fd0847499021`  
		Last Modified: Thu, 11 Jun 2026 03:16:05 GMT  
		Size: 19.5 MB (19475008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c601038e9f738e25ea812a1381288ef2426d3f35f111b74dd8bff39b513090b4`  
		Last Modified: Thu, 11 Jun 2026 03:16:04 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d0e28d97dcfe869ae79b9ac7fd991ae2e3490e950b5d3070247b2481e42f8d`  
		Last Modified: Thu, 11 Jun 2026 03:16:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5f164d710f5e331c677bb739340725ae7e22d1bbb65147496d0a7d05ce3bf916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4244100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1951aa0768be8ffe5f0f65a740f11aa72a4296b5800bbe78c44d1e5b04874e8`

```dockerfile
```

-	Layers:
	-	`sha256:0dcca3b84f84a4be94ea3eb4618a94482f390f8fc018481ee2fc955f9784e0cd`  
		Last Modified: Thu, 11 Jun 2026 03:16:04 GMT  
		Size: 4.2 MB (4224935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:830b9c2e182e1c5c3e7c0c7a567e485df8aac5c9d3f531cce2baad368aa64386`  
		Last Modified: Thu, 11 Jun 2026 03:16:04 GMT  
		Size: 19.2 KB (19165 bytes)  
		MIME: application/vnd.in-toto+json
