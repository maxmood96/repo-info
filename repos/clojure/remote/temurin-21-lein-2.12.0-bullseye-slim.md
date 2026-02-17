## `clojure:temurin-21-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:777d5e823906b4d46309a9dc5a25ca4f7fcc1a8dfbf8d9b599c947d66da8e260
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b9910cc7e10b0de41f438491d2fa5b91e5bce562f526dcf23c420825b5fe3aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (207952258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a9042ce2289925a93d69699a6a9257234eb0c4668e567534e74c73dc174cd4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:44:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:44:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:44:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:44:13 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:44:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:44:14 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:44:29 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:44:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:44:29 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:44:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:44:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:44:31 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:44:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d38432d3db690e1340d6939e5c55fb91373140e12a768f1066ba6dada8e53b`  
		Last Modified: Tue, 17 Feb 2026 21:44:51 GMT  
		Size: 157.9 MB (157857099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770e4fe8e99878be83feede83377cfb26d300df1b601f6479d9b566ab3640683`  
		Last Modified: Tue, 17 Feb 2026 21:44:48 GMT  
		Size: 15.3 MB (15318689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475eea9c16ac605c8a814c0e914e427e6ddb7fdd59557dd0c2de0ff1d1df0151`  
		Last Modified: Tue, 17 Feb 2026 21:44:48 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d9f7fd69651e60500fc2ac47d3b508f0e92e8d11f0ed06b464a16db1030d85`  
		Last Modified: Tue, 17 Feb 2026 21:44:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1d02474d996a39e9a3f55df2d308a7a2963d73ad17dcf667cfcd3775cfd6cb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3039417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475965724fcf200378872486f70769d5d3190f09fae085a3e3c07939f78817c3`

```dockerfile
```

-	Layers:
	-	`sha256:92de8bff970792eb01c7c8002399a8cec5ad596b4fdf757e446197f569a39e0f`  
		Last Modified: Tue, 17 Feb 2026 21:44:48 GMT  
		Size: 3.0 MB (3021014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c658fb19cd0765d9af1fa6c99b90be9aa71e58ebdcd5ce42e46abe170e135151`  
		Last Modified: Tue, 17 Feb 2026 21:44:47 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:392784a640c5ab211cdb52fc59d80de6f311db13b6c8dcdf69b98866f5d5e510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204701525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508280a4649d68b5f2eeb80ac768fe09cd5b3d50d2a214d510b2af31828be802`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:24:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:24:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:24:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:24:48 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:24:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:43:52 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:44:08 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:44:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:44:08 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:44:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:44:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:44:10 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:44:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f3fd07dcf6f5c8ade45bfc94dfefdf7bc529a2fd1f12b4164c36ffc1db4bbe`  
		Last Modified: Tue, 17 Feb 2026 21:25:43 GMT  
		Size: 156.1 MB (156133080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec8b7d8f6de9b850148b6c3c8aeba41fa78c7b753d733a7c2ef42919deda463`  
		Last Modified: Tue, 17 Feb 2026 21:44:20 GMT  
		Size: 15.3 MB (15305821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d0d7ad6861f860d53c79aee520d61942c881f1219d186353cb75e141b108fa`  
		Last Modified: Tue, 17 Feb 2026 21:44:20 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037ea107db2bc0719c778f2a9f19cde3fff4d9c560322681fd971dbb9ee0a374`  
		Last Modified: Tue, 17 Feb 2026 21:44:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:84fc1aa94333adf8fee2c986f0353c4556cd2407be0ad8ef1b0064a220bef24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3038345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26ec56e9879f35718afb1a0dd596ee3be31f940fc74b5bc00eb93472b1eee21`

```dockerfile
```

-	Layers:
	-	`sha256:facae239b108b28a8654a6b4f48a16308d82fb10bcaed32c61cea0064bbf6f1b`  
		Last Modified: Tue, 17 Feb 2026 21:44:20 GMT  
		Size: 3.0 MB (3020623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76e6bd516a116a17e80d965d271687076a23ee43c5a1c34663e33704abc4faa0`  
		Last Modified: Tue, 17 Feb 2026 21:44:20 GMT  
		Size: 17.7 KB (17722 bytes)  
		MIME: application/vnd.in-toto+json
