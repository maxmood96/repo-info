## `clojure:temurin-11-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:e53295df613482da1c3f23e9325f6e7a94ac62af0b07035fd77ccf1cc792e773
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c2074b20c31d4e9ce45492b12eea8d1e58ec5b60c2c6a8e8bf374cdcfb71c658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220717089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f142c5e17496964fc8e5c25e7031b2be5b62df182fd831b8f276391c989f39a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:13:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:13:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:13:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:13:23 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:13:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:13:23 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:13:38 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:13:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:13:38 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:13:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:13:39 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd136dea5ceb1572e4065658646c8b834e86b82b1dc98f34cc77d2b9ef334c21`  
		Last Modified: Tue, 07 Apr 2026 03:14:04 GMT  
		Size: 145.8 MB (145806914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7cca59f800a299c9991a723cfd5cb8ae2e93a52b901e75c906cd1f5ddfd440`  
		Last Modified: Tue, 07 Apr 2026 03:14:01 GMT  
		Size: 16.6 MB (16629617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5b60dd9db07d330c05a873986bc215f9ff7caffc77961a4f5d0b7d66504355`  
		Last Modified: Tue, 07 Apr 2026 03:14:00 GMT  
		Size: 4.5 MB (4517733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c2593c58a3a2e3b72e5b5d3daffdae6221e5cf22e01828882d9f972e5301682d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d025d720b6c3a5952cb7e545fab012e6e726a06c6885e13df77c212302365e`

```dockerfile
```

-	Layers:
	-	`sha256:876c5441166e6b1b639a4352ba6968a9bbb04de35ee2c5c826b7a890691ec569`  
		Last Modified: Tue, 07 Apr 2026 03:14:00 GMT  
		Size: 4.5 MB (4506003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2d21018844585ca092c6011d1d300c3d0567849dfe0a8b5e79a311157af4ed7`  
		Last Modified: Tue, 07 Apr 2026 03:14:00 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eaa2de7f49e33dc1b017fb1cfd901e534ded2707789c6462c0e338e65a5b0737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215881989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3294a61d15a7e47bb56749e8bbd9f2fedc20cc73938f0a73803445c1bc46260`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:24:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:24:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:24:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:24:10 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:24:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:24:10 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:24:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:24:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:24:24 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:24:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:24:26 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104f952f18f5fe766f2da4d65a5d35c7b8dc353091cccad99835a2141b7e130c`  
		Last Modified: Tue, 07 Apr 2026 03:24:49 GMT  
		Size: 142.5 MB (142500070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6730a3d0ed2d62ede9f8929eb8f23dd9535d2447e9ef5e73c45ff7ca8a978b70`  
		Last Modified: Tue, 07 Apr 2026 03:24:46 GMT  
		Size: 16.6 MB (16616529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd960e27e8e75d502656a9ad57736da2ebf9d57b37b93fb52f4643927c0d027`  
		Last Modified: Tue, 07 Apr 2026 03:24:46 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a39096ff50897d1a73405e2b0582728ec75a66814323bd566ec75c3ca3eae1a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9d6218696ed62d8628d1826dec8babe9a2c94f6d7f3e6a38a303b27ba45e23`

```dockerfile
```

-	Layers:
	-	`sha256:10c614cd308a2b94caa049f27ab7d1cc30bbf0193313e35c7083bc475644a1ee`  
		Last Modified: Tue, 07 Apr 2026 03:24:46 GMT  
		Size: 4.5 MB (4505595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2359ffc863639e182809652c5c64411c5721330cd1857f67a946224b23e6d99f`  
		Last Modified: Tue, 07 Apr 2026 03:24:45 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json
