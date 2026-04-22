## `clojure:temurin-25-lein-2.12.0`

```console
$ docker pull clojure@sha256:54c38e965ad6e15169f6581c237a68e230984fe9b4435b6e7529c5bd3801a5b8
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

### `clojure:temurin-25-lein-2.12.0` - linux; amd64

```console
$ docker pull clojure@sha256:955274cacf591de362e0ecb83d9e7a2cf850e272e7fc46ced8012fa71f254412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.1 MB (165069620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204273e9d6552d5407156d877a91f80ca8d1f10269d81f487a900b1b71d8d6f0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:20:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:20:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:20:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:20:17 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:20:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:20:17 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:20:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:20:31 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:20:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:20:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:20:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:20:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fcd5632ffb072976212cd26eccc6c60a6649f888cef13182bc6694bad4d2a5`  
		Last Modified: Wed, 22 Apr 2026 02:20:51 GMT  
		Size: 92.3 MB (92256332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0348acb57c4faa5a6892b75bf01674fb4666a98054e963da9a841003ffa12657`  
		Last Modified: Wed, 22 Apr 2026 02:20:49 GMT  
		Size: 19.8 MB (19806526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d38b33f3781dd5e1ae579717c6b1186ad4bc1a17337bb11511996f5daec059`  
		Last Modified: Wed, 22 Apr 2026 02:20:49 GMT  
		Size: 4.5 MB (4517707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660a932cb729daa33a29a94fb93fb2bfa9e8b6bf690dd96e388c6cf3834d759b`  
		Last Modified: Wed, 22 Apr 2026 02:20:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:4ec370bbde2f471353233ed6823c7a5455d17abed8fbbb3cc035f29a24618290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7af6630c7149d2c31604d62b5aeb0e7adf80b331dc084581340ae13565f09c`

```dockerfile
```

-	Layers:
	-	`sha256:5dd94c1e28ac2e166269d102ea4ecd7068fffbff385ab2c07a47469d3b2187c8`  
		Last Modified: Wed, 22 Apr 2026 02:20:49 GMT  
		Size: 4.3 MB (4251027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fbeaa811c8b10ed53dbbde46f779f69e335871b84e39d041cc92c7380da5fb9`  
		Last Modified: Wed, 22 Apr 2026 02:20:48 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2317d2c7c924011c6e7a49902c87ce9cf944522f0b9c3e1fb77b3b248ea6f6df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163816436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32629f783abb076c06bf7ad007ade20c56f8548d26ffd368c231a7186d9c9d7e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:23:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:23:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:23:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:23:23 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:23:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:23:23 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:23:38 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:23:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:23:38 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:23:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:23:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:23:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:23:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0bc9378e90253f12c98c90f18c9739bf0e4bcdd4ba69bf7be02946a1b9077f`  
		Last Modified: Wed, 22 Apr 2026 02:23:58 GMT  
		Size: 91.3 MB (91288266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce05d4b87ecf3b3de9227ffb5152ef3443d669ed2b989713c4f05c55e3b0899b`  
		Last Modified: Wed, 22 Apr 2026 02:23:56 GMT  
		Size: 19.6 MB (19636957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab93d52f31846912e5b8343707f8efe22938f527ac6eb6faf73fd6993e1762f`  
		Last Modified: Wed, 22 Apr 2026 02:23:56 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91051fdd73aab55a85ec793bbb2acab863f10eadef6936eb87b11b44dbbc18ac`  
		Last Modified: Wed, 22 Apr 2026 02:23:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:f18624b792f4fec1d87b845694335760dbe6f3139c7ec6e029838d1cde84798c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecc479874bf41af2b020f9143aef89896e85c87a203557781ae11245d481373`

```dockerfile
```

-	Layers:
	-	`sha256:0a87218bd695599d8223936014918d4ff42b5884e28f758c2a9bfce0b904a54d`  
		Last Modified: Wed, 22 Apr 2026 02:23:56 GMT  
		Size: 4.3 MB (4250711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3323e3e0f5105ebbebdfee3ac78d1b5b835e33b871d39f28240fb3af16febd6f`  
		Last Modified: Wed, 22 Apr 2026 02:23:55 GMT  
		Size: 20.4 KB (20449 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0` - linux; ppc64le

```console
$ docker pull clojure@sha256:5719d21aacef8bed7e4991858ae6472c216427c4c255278f5ec42dec6012a3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168518642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a600695627deedf216056f441b4eae206a62b5a3c38afc9604226d1b638a7e21`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:29:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:29:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:29:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:29:27 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 02:29:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 02:29:27 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:29:58 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 02:29:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 02:29:58 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 02:30:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 03:08:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 03:08:38 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 03:08:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e921237880038077978485833f958f4cb6fe7cf35b55e5d3fcef9da28065c10`  
		Last Modified: Thu, 16 Apr 2026 02:31:28 GMT  
		Size: 91.6 MB (91632998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45cccf32f1e514d06337c765407fee36f0346212da4934180626a4d58c9e76e`  
		Last Modified: Thu, 16 Apr 2026 02:31:25 GMT  
		Size: 20.0 MB (20030552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c827a7ce8871e86eb0b97d7651119d8715a4774f01fe05aae7131d8d3e52e3`  
		Last Modified: Thu, 16 Apr 2026 02:31:24 GMT  
		Size: 4.5 MB (4517725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530af12e5bd66d0e5c43726dc0c553b1f5459b4da0d0356542f5233d29653e14`  
		Last Modified: Thu, 16 Apr 2026 03:09:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:91ded1ec424f78b23cb10a1fe529993e254d4fecad01cad13b9debe7be5ad25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4256575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e575059399b2c6ab26b3aeb8d7b2faa0d875ca0127ce1ab8e0f486672962be6`

```dockerfile
```

-	Layers:
	-	`sha256:642c2688902df832949b3cac6221becd1aa5d608c8f59e9c0992230dae23cf17`  
		Last Modified: Thu, 16 Apr 2026 03:09:01 GMT  
		Size: 4.2 MB (4236236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3a24930370b87fee266694a668d47be29eae88184ef707a8f0368f180c2a3ac`  
		Last Modified: Thu, 16 Apr 2026 03:09:01 GMT  
		Size: 20.3 KB (20339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0` - linux; s390x

```console
$ docker pull clojure@sha256:5a99a2bea534d35e1a2224cc37423e6aee77e3c082295093168d564696f7aad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.4 MB (159366856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34429a2b91c380ab1dbf65ed2ba4ef4b13d533ac325ef134181c08912a3d2ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:43:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:43:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:43:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:43:38 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 00:43:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 00:43:39 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:43:49 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:43:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:43:49 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:43:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:43:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:43:50 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:43:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45d52ff2ba34ed3445e056e0b205492ce1ce339a9079524daf5aea0d83bd473`  
		Last Modified: Thu, 16 Apr 2026 00:44:15 GMT  
		Size: 88.2 MB (88233835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f738945f077f3255539ba36125ea89d69709e925fda7f8ea6831c335dd1418`  
		Last Modified: Thu, 16 Apr 2026 00:44:14 GMT  
		Size: 19.5 MB (19466810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5630d80f1d62060d6f0ee1978593abed924a06cf693ffc02c36d1b47448a5a9`  
		Last Modified: Thu, 16 Apr 2026 00:44:13 GMT  
		Size: 4.5 MB (4517697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb751a5a278066c59265846af6e1f92538b61925c097dcd882a71a037b3e181`  
		Last Modified: Thu, 16 Apr 2026 00:44:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:ffd0f81542f4bf440edc27f92b2a797be9e79223a544942173c813ce3671f581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f228db9f3ab547fa94d09f998e5c2ed0186b6e0c875a4492c0d0dd02a00e9f`

```dockerfile
```

-	Layers:
	-	`sha256:ea9c92b68738570b3e5b4eb9c833309464a54fb4b7d2ba9b3e49c2bddcb8f233`  
		Last Modified: Thu, 16 Apr 2026 00:44:13 GMT  
		Size: 4.2 MB (4227403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f362c04e44b35ceb727f5f0bfd1e4fc964b89e21fbf3a96b03665557ee25d317`  
		Last Modified: Thu, 16 Apr 2026 00:44:13 GMT  
		Size: 20.3 KB (20258 bytes)  
		MIME: application/vnd.in-toto+json
