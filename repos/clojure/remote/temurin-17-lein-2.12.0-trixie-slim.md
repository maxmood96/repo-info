## `clojure:temurin-17-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:f6ceb8b4800520952d720909e13b10da315f193ab9f06e17569ff31aadcad65d
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

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:21ba5ac51366a9fb2fe1f8c18c8a1a4dd69794f0d21b88914abbb3eadc99fd5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196657204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31970127861752437ce9fed40360aba0057fa3012a0caaef921d2e0d18711ff5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:18:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:18:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:18:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:18:44 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:18:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:18:44 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:19:00 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:19:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:19:00 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:19:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:19:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:19:02 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:19:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c218ed03ec7171324179ef6495b62c61c21692fde82ac0e398781618297cc5`  
		Last Modified: Thu, 11 Jun 2026 01:19:20 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5106afb6311a3c2dd5e89364e61742fc3288a3f9a623cb3e36d705ed794106`  
		Last Modified: Thu, 11 Jun 2026 01:19:17 GMT  
		Size: 16.4 MB (16448156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7204dcbd24ee11355020b481c07794626515fa3d21833e421d0b4af3bf36b5b`  
		Last Modified: Thu, 11 Jun 2026 01:19:16 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b584167be41ca11df767fa8bba4fc7e199386d9d2d19446601ba253f0ebf38`  
		Last Modified: Thu, 11 Jun 2026 01:19:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:074cc4a007144c9633c011519ea5c778e61832b27188dca64c12c4ed27035e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f3d425ff10cd67f57978e32276f4082c1ceaa940c9b9b8a7a6b66774909c490`

```dockerfile
```

-	Layers:
	-	`sha256:677c743f79416b3f5c17ad8f8bd8e99d9097f00276a76dfda5dddb53021dd463`  
		Last Modified: Thu, 11 Jun 2026 01:19:16 GMT  
		Size: 2.4 MB (2365457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91bb4dc468cfa280334752ab13aeca58578590888de17ab9e9b24d404fc9362d`  
		Last Modified: Thu, 11 Jun 2026 01:19:16 GMT  
		Size: 18.5 KB (18540 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:acfb017e80750b1997dee88794834c52de6b74c10cf949000ef7d53efe3dc5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 MB (195805234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4fe75c84c75810f8522a67566be0020f77118e89812462695e291fe00966bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:22:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:22:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:22:36 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:22:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:22:36 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:22:57 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:22:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:22:57 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:22:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:22:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:22:58 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:22:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82aa397e9e943d575fd01a486228f206de6dfdec5a84a86f8e1eede56dfd99e`  
		Last Modified: Thu, 11 Jun 2026 01:23:19 GMT  
		Size: 144.7 MB (144724335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f21898b435ff7466c29946951c90b340de6a3f025b27b04ff39542b458747a1`  
		Last Modified: Thu, 11 Jun 2026 01:23:16 GMT  
		Size: 16.4 MB (16414218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c6eeb5e7903573a529fbe69fd1911ce7ce04bd457a14fdce42830092554e68`  
		Last Modified: Thu, 11 Jun 2026 01:23:15 GMT  
		Size: 4.5 MB (4517723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e58f440e7844216a88117c65dcb2321e6e0718505a2d0d61f45b8c09819ff9c`  
		Last Modified: Thu, 11 Jun 2026 01:23:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:77236764d409ca6bf8d1161289058f641df5dcf0b948c8842d57caa9e036958c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a05b4724da31057ca05619e7f40f7263d12ee6f5d66ffb466002769668fafb`

```dockerfile
```

-	Layers:
	-	`sha256:493ebebc1ac60b03558b9eede1e7c69bc3af0f0cc2d087c5d511142e7fa71da7`  
		Last Modified: Thu, 11 Jun 2026 01:23:15 GMT  
		Size: 2.4 MB (2365067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5416421b1789d6890cc4a70f290c64acf279383c37bf7cfe601aa3622cd7dcc`  
		Last Modified: Thu, 11 Jun 2026 01:23:15 GMT  
		Size: 18.7 KB (18661 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:5bc1c3cfb7cd6a095e29691050973212273aa196be27b61b9e1a474e53423552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.4 MB (200370793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38bc975115a4912b6d101fbbdc48385f9b7333f27b809c4850c50292a81596db`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 05:55:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:55:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:55:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:55:57 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 05:55:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 05:55:57 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:56:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 05:56:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 05:56:33 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 05:56:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 05:56:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 05:56:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 05:56:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fcaa63cfc3ea422959e06329a48ccd975c0ddbdd55ca19c3daa9d5e346bb47`  
		Last Modified: Wed, 20 May 2026 05:57:13 GMT  
		Size: 145.8 MB (145766113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36d84f1065dd706009ba2763463099d1764796f2443ee798b9a712bb7159089`  
		Last Modified: Wed, 20 May 2026 05:57:10 GMT  
		Size: 16.5 MB (16486089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59e3b08c8d53694ae8e223d22952639a8ce65d3b0e7e964e82b6ba7e0876bb2`  
		Last Modified: Wed, 20 May 2026 05:57:09 GMT  
		Size: 4.5 MB (4517708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91c10ede82036ff9e040831c3eb6ab93b326963f6241576a4e75a1612b602c8`  
		Last Modified: Wed, 20 May 2026 05:57:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b158e526fc27349ab2bf33ec7d82c54b4e9b7d614665de8ccf8e207cd6dfaea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6065b8470572e90c80d3733e27b7ca55fc9fb57fa443cb69039cf74238db127a`

```dockerfile
```

-	Layers:
	-	`sha256:a7f628dcc959dd961acea43906d35d2ce78141b4e3e638528e3a2212ec2515fb`  
		Last Modified: Wed, 20 May 2026 05:57:09 GMT  
		Size: 2.4 MB (2366437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05fa3312c9542915cade7d0a393482839a8c958ac093fac2aff6f51331870051`  
		Last Modified: Wed, 20 May 2026 05:57:09 GMT  
		Size: 18.6 KB (18585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:92f5f541f3dc31717963cd64686cf425a1175b16f319de74dcc417814217920c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186764254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e952f3fa3c91c2bbcc5bd87fdd140fc8d65b5751483425f02339d67a9d57ec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:09:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:09:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:09:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:09:52 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 03:09:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 03:09:52 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:10:06 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 03:10:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 03:10:06 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 03:10:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 03:10:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:10:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:10:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5215dd65ae5f167140650aad18f5f586cafd155179ec2d0dbc151ca090b6ce61`  
		Last Modified: Thu, 11 Jun 2026 03:10:35 GMT  
		Size: 135.9 MB (135910420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ec15fff9afb0739144635163c316543b0a1b8a9e9a109060c5f0db57cb2e24`  
		Last Modified: Thu, 11 Jun 2026 03:10:33 GMT  
		Size: 16.5 MB (16484302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f56df0a0251916a6f3ff02bfc2222d9fcb067f6814dda17595ed1ff8282177`  
		Last Modified: Thu, 11 Jun 2026 03:10:33 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8135a7d521bf8adf94e0f96ab46d26bb3b256f08f37a457aaf602e9297ff90b`  
		Last Modified: Thu, 11 Jun 2026 03:10:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3e9c48437274fdd472f6e64c2a8a6aa3e57f3a055eddb76a9d3ac2e58502d86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79217d76e2cfbbe5c41ead45b14df6f1b6f4e917878d63d0a4e90aed3d44b2f`

```dockerfile
```

-	Layers:
	-	`sha256:82b04a56011b617ca040230cf8f226131212c6521e50cf67ec24c1547ebd84ee`  
		Last Modified: Thu, 11 Jun 2026 03:10:32 GMT  
		Size: 2.4 MB (2361884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31a529202ec23024540e9db9633e8c1f345dc6c92f352b0f7314117ac0291e38`  
		Last Modified: Thu, 11 Jun 2026 03:10:32 GMT  
		Size: 18.5 KB (18541 bytes)  
		MIME: application/vnd.in-toto+json
