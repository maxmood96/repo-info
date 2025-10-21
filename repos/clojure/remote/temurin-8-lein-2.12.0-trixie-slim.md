## `clojure:temurin-8-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:9b8e983bb1d3c7ded35e198fc2d40e98b20c8e640f64850df03a7a8af0175c9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d6402fd4f8639dc2f2875e38bf2380ec5c1856d44b6286cff0e3cfe3e15e858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105474464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917f75dc76e781949be6c150cdd28e192e3437f360266e7420ac49be235dcf56`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f79012317a853855f0a23ac4c31c725972d927c279e3934aa8e87c1957c6dbc`  
		Last Modified: Tue, 21 Oct 2025 02:19:04 GMT  
		Size: 54.7 MB (54731336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42089fd9533d76cc75e90e2670148311cd780ec21f1d6c3c2e6c47ead38cd473`  
		Last Modified: Tue, 21 Oct 2025 02:19:00 GMT  
		Size: 16.4 MB (16447417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29797a201aa486f6dd48ac8db81821fc6390c141bec6c684a01fdc2de2ef3521`  
		Last Modified: Tue, 21 Oct 2025 02:19:00 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:387e36da84d72bc676df1c0e532732b9ac89074010bc928e29739c05ace1d61f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7421e749b7977bb85fc8900dfaab80e43c26a13b0dd37a8add7329efdb1108c5`

```dockerfile
```

-	Layers:
	-	`sha256:0272fca2412a23eaa57ef642f7f260db12c2fb36bf074c480903cc51982eda95`  
		Last Modified: Tue, 21 Oct 2025 09:47:22 GMT  
		Size: 2.5 MB (2485054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fbff32e890673b2e35a548ddbc2b4e26700db7169308c3ead0cba1934a10343`  
		Last Modified: Tue, 21 Oct 2025 09:47:23 GMT  
		Size: 16.4 KB (16423 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4f1c5d8062a410d8c74611ab679da4715672c2f62d50abfa8809491f08d0c12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104908990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c859abe3e3a5c990853707ad2cb5754858c3f72a3409d33153ae49cd52dc872`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bca21515bd3733244cca6de7a301d65b5d5851e980d67367c85aa74b1bdb309`  
		Last Modified: Tue, 21 Oct 2025 02:25:06 GMT  
		Size: 53.8 MB (53835607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960bbdc0aa40bcd4cfae4a8a504767382069e7193289cd705443cb486ae01008`  
		Last Modified: Tue, 21 Oct 2025 02:25:00 GMT  
		Size: 16.4 MB (16413509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9421c28a3ea55408a8b1c0df7303eec82db292b7a591a658d496882daf4706c2`  
		Last Modified: Tue, 21 Oct 2025 02:25:00 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0c85be360c2d0563abd9b957f58734ef131535ee6050efa8a8f52aa1e452ecfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3770f5397a2253173458849934f9f36775b4180bfa385a6a34c6062ec56eb0b0`

```dockerfile
```

-	Layers:
	-	`sha256:b99f0b91d7e2e378579a3c9e9c455c324dd2fc6cce423edef1c73b88e79dc511`  
		Last Modified: Tue, 21 Oct 2025 09:47:27 GMT  
		Size: 2.5 MB (2485370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c61272ec5b5508a7eac3800b1f9758ab7496e902ef09cfcd37f67019630bc8f`  
		Last Modified: Tue, 21 Oct 2025 09:47:27 GMT  
		Size: 16.5 KB (16546 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:96ab6131a6e903be8db730f4b38198ea77246e16599f73c6a88b2f4a5a7206b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109961022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47add8957861c2a8af2163dae33daef4f31fad5f4924972ef726d8488d8202d2`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8850f6bfd7c5a8dd3875f0dbd8746815ac97b4f412c114102fd1d99799526a2c`  
		Last Modified: Fri, 10 Oct 2025 04:47:10 GMT  
		Size: 52.2 MB (52165392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d72e3bb0a5b6c7454846a7e7f992dce72db09fd311f9ffc68daa8bcec3828a`  
		Last Modified: Fri, 10 Oct 2025 04:47:09 GMT  
		Size: 19.7 MB (19679383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b2b3c88455df642287045db16f683752417fadff7355ae1956b59f6d4637f5`  
		Last Modified: Fri, 10 Oct 2025 04:47:07 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7583d11aa16203b28fa5e2f7ed15bf22547ea5a074e98b220ea62cf90d1ccbb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49edfb907eefdfb95fec00146fb79d7828e98a91660f4eec2fd9c906af99848f`

```dockerfile
```

-	Layers:
	-	`sha256:edf73f46cb7b62157a3398f2ad575336ed59674bc3a4bc6aa619c76a91c91010`  
		Last Modified: Fri, 10 Oct 2025 06:51:54 GMT  
		Size: 2.5 MB (2486627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0def6e5c79065749e93ee0b33e293d498952eeb808624daa9298c40ad73a779d`  
		Last Modified: Fri, 10 Oct 2025 06:51:55 GMT  
		Size: 16.5 KB (16469 bytes)  
		MIME: application/vnd.in-toto+json
