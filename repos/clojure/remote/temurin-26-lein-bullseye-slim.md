## `clojure:temurin-26-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:a975358e4e045f8b25d2850609835d134ae076deb2641b4f203b3089cd354e11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a717a981edcb1f6af189cc5e055d0867e3b6d29a54e8232b84236f1587d4969a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144639008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becd647ad8cc72c46e90dc0b18db53a9742eb73439a82356aa2dcb46e688763d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:01:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:01:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:01:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:01:56 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:01:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:01:56 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:02:09 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:02:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:02:09 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:02:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:02:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:02:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:02:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd55796c251472a0c6bc627c62f658b41539a2f4282fe2077d391f62238978a2`  
		Last Modified: Wed, 20 May 2026 00:02:29 GMT  
		Size: 94.5 MB (94524374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfb848b6a5e983c19e20f6aa1154071423c783e8c567b150d23e6a11a634358`  
		Last Modified: Wed, 20 May 2026 00:02:27 GMT  
		Size: 15.3 MB (15338862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1851de5785409ce25a3a89cbf983850cfb22809188cb57188452648ed4944d2`  
		Last Modified: Wed, 20 May 2026 00:02:26 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151b00fc41b600dfbff61172f28430701977f26f9ab02b8c763fcb32a7edaefd`  
		Last Modified: Wed, 20 May 2026 00:02:26 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b92aa3ad59bfe9561ffb15f3731bb796aeba2a11f8eaec2480c7bfae4ae947e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06aebb6c2c0ac76e888bfe990b1e702c23facf6935cb9f1bb4ec72b3481e6121`

```dockerfile
```

-	Layers:
	-	`sha256:b7a1f986e22e0f9d5d24575c493367756b1c6706a2058677f5b88e2b774bcf25`  
		Last Modified: Wed, 20 May 2026 00:02:26 GMT  
		Size: 3.0 MB (2993100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5450713b77ec8160b033add8f758482f62957757afa748d5450bf2bc1dc85ded`  
		Last Modified: Wed, 20 May 2026 00:02:26 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a6feecb4cb502fdf0c27523af59ff0f477d8eb687a2d5a360247e5c440cbc7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142092737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413036d427c4d3b229182dd73b5675b6de7c17fe4aabc31e84055b0735f33bd6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:09:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:09:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:09:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:09:00 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:09:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:09:00 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:09:12 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:09:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:09:12 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:09:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:09:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:09:14 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:09:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b63000e058b244a465007df0adcf70b48b0f8270ead5af5cd11c23937e5a25`  
		Last Modified: Wed, 20 May 2026 00:09:33 GMT  
		Size: 93.5 MB (93504334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1255aa7c2eb84a29951d5322163e28b7d1580dfbb7fc3ee01ad361bfb9a53289`  
		Last Modified: Wed, 20 May 2026 00:09:31 GMT  
		Size: 15.3 MB (15327260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf86e697d24f215e3da0105f3782ecd60fb5807f40939fbc4fe892b437e345d9`  
		Last Modified: Wed, 20 May 2026 00:09:30 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5253f0ddbdddf85720e3fb862abbb8d0ce4c7b52ac32dedbce94634bb171f4f`  
		Last Modified: Wed, 20 May 2026 00:09:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c7ac63ef43ac0968c222eb1410840f573f1f16af1a3328412eaab831ed541fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dfd7876ffc3a7937278f161d47531d83d91ab8222e1a0542f7d43d414ba26f`

```dockerfile
```

-	Layers:
	-	`sha256:22e8e49d0b4a7283429c6570ceba92072302bf9554bf550d273b8af704acb334`  
		Last Modified: Wed, 20 May 2026 00:09:30 GMT  
		Size: 3.0 MB (2992706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef01948b94fdd31710dac1eacd7c0362f4ba10970a38b373a53e7a29f2720e05`  
		Last Modified: Wed, 20 May 2026 00:09:30 GMT  
		Size: 18.7 KB (18671 bytes)  
		MIME: application/vnd.in-toto+json
