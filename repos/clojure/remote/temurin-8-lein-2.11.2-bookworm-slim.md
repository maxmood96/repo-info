## `clojure:temurin-8-lein-2.11.2-bookworm-slim`

```console
$ docker pull clojure@sha256:315f73e87a2b7152b5c9f9efaf264e0f89e16007bd7f4d51fa6f967b2768a129
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-2.11.2-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:060afb2cf2f92b872ea59eae7b05ec4daf752212bedc2a733585c9cff7e63733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 MB (188357120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71aa022eacab6008a96aafe4506204d9749e3698236689e142a3f4142a39f8fc`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0363768455b327256b65e9a3e1595be5f2d3d3b7701184d8de667c1ff8e1da60`  
		Last Modified: Fri, 23 Aug 2024 20:02:12 GMT  
		Size: 103.6 MB (103611892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcb9c8d3ed2fdeb551eda46f5a6959aeb1ed960b48c5a0a608dcbcdac82aa0e`  
		Last Modified: Fri, 23 Aug 2024 20:02:10 GMT  
		Size: 51.2 MB (51220875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9523b9bfd81f099fce2e286780f1f5d24325165f3568a2c28450a1d228bff35`  
		Last Modified: Fri, 23 Aug 2024 20:02:08 GMT  
		Size: 4.4 MB (4398089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.11.2-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d29f13a67d5878ae634816f2babfb23a9eaecf464e207b05fa1c1ed208d94cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4194583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb47108f030b6d10423139af0eb04a27455166136e5f834eebb3f28b33c871e7`

```dockerfile
```

-	Layers:
	-	`sha256:7fd2ac164e66abc27bd5b08876524cbec9dccaa7feb8aeb1960b26eb73aed699`  
		Last Modified: Fri, 23 Aug 2024 20:02:08 GMT  
		Size: 4.2 MB (4178502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb22969206557ce71a3f63ed33ad25fb6c4ed6636dea42ec690c8648fc0b18af`  
		Last Modified: Fri, 23 Aug 2024 20:02:07 GMT  
		Size: 16.1 KB (16081 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.11.2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ac35dd36fbc7b7cac6348230c9b1f7206d7f20882152e3ee6f810d091191b8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187379145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffee39514f87112eab13bbb310d1b682ce30f868cad97d08645d1ef4e96ef035`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edcc7a7af68400eeaf570c17969676510119f264dd0e3c2e9727f01574ef515`  
		Last Modified: Sat, 17 Aug 2024 05:51:40 GMT  
		Size: 102.7 MB (102729220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64189ea1143bf814af994d39d25035588833ac7c0c5fe5a8084d8ad3c3436553`  
		Last Modified: Sat, 17 Aug 2024 05:51:38 GMT  
		Size: 51.1 MB (51095283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62151d0c3ae95390b62f312615d5cbeb0911591a06e1633c21732926a0ddaa6a`  
		Last Modified: Sat, 17 Aug 2024 05:51:37 GMT  
		Size: 4.4 MB (4398082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.11.2-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:38631ee336d3640d9b00530074bf85333fd950de831c6ecf8597caf570f1c44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4201427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72175c00312dc4970d123025fe2d2f41ad206e604f86c9579a1cb14b96562d3f`

```dockerfile
```

-	Layers:
	-	`sha256:6d15ac4efbf133995cc24500615efd0937874c32337814f1b12eb750730a7b57`  
		Last Modified: Fri, 23 Aug 2024 20:43:10 GMT  
		Size: 4.2 MB (4184818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c9378a207e28f33c9b740b8fa3e0a82481789bd1ef16acef6554a1f8bb2f8ac`  
		Last Modified: Fri, 23 Aug 2024 20:43:09 GMT  
		Size: 16.6 KB (16609 bytes)  
		MIME: application/vnd.in-toto+json
