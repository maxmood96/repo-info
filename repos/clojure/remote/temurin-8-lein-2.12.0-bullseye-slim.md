## `clojure:temurin-8-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:b635a43bdd4cd4e40479b2ff02828b65001f40512a4a05968da59b6b18b17030
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a72fdd653d8771e2888dba93f3b12821abb9e5d8fb4d2e180919b4ed4a77b954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105284709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ed70932183f1ca93f3491030811701938046edc2b2017725ffb4a7de7ad73f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:12:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:12:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:12:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:12:23 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:12:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:12:23 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:12:37 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:12:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:12:37 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:12:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:12:39 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d9bdd7ba138ea81884f26ccc2ad40e0b9601ad853815931562e3968c2561a5`  
		Last Modified: Tue, 07 Apr 2026 03:12:54 GMT  
		Size: 55.2 MB (55170110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e1c82773827339e686a8ebf18142fb2bf488f96d625325235eee000728cb6f`  
		Last Modified: Tue, 07 Apr 2026 03:12:53 GMT  
		Size: 15.3 MB (15338788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774ab8ca526c5f17e2582186cc7e99d4481d48395a571c981d19450a60cfd43c`  
		Last Modified: Tue, 07 Apr 2026 03:12:52 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3998ab6853c49b05772acacf00a4bd264a9674bea8ae427a0bed5ae15716cca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3164971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712f14ae37bc79efe932cb37397cdf85f9d5f401c7a3fa6780e8687f48e6fe1c`

```dockerfile
```

-	Layers:
	-	`sha256:f031751fa09fa1f0c8287b38dcaecbe4ada2fd48087eecd5f47d009e2afc2793`  
		Last Modified: Tue, 07 Apr 2026 03:12:52 GMT  
		Size: 3.1 MB (3148571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b863618291c1bec17651984aadf3942dfeb94f8bd236e84e0580d03c6ac30820`  
		Last Modified: Tue, 07 Apr 2026 03:12:52 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7fbe37dcb0a654addbf3b4386d2b26e41637f6034984fa0338618948953ec87c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102841298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804d038556a0e844d2776e56293abbca32ace26b5b3a2d3c4f7a53d5e0c1c53d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:23:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:23:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:23:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:23:07 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:23:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:23:07 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:23:21 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:23:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:23:21 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:23:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:23:23 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1277e3d7b6735bffe828f835ee9bc9a1d0583cf7f2708e0c90270cf47f21f283`  
		Last Modified: Tue, 07 Apr 2026 03:23:37 GMT  
		Size: 54.3 MB (54251611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15376b6c1ed7dc4241d30d0cceddeddfd7ab90725f1f37262510f258eddca30`  
		Last Modified: Tue, 07 Apr 2026 03:23:36 GMT  
		Size: 15.3 MB (15327237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d627b019ce90ae3960b7e0aa34836d634ff9c4e75402688917d8b22b5924388d`  
		Last Modified: Tue, 07 Apr 2026 03:23:36 GMT  
		Size: 4.5 MB (4517730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c02414b0c2d9e297b43f3db9773b3fc19078e7811253c7413c9ae2bf05c95909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3165401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e153f937c82b87e2b4de5291f2234314a9ab455448ad0697d1ae1c6f5df49ed`

```dockerfile
```

-	Layers:
	-	`sha256:2fcd34093fc8568408769e4b588aca8274a9f0b6e97a625dd25c81754e6875dc`  
		Last Modified: Tue, 07 Apr 2026 03:23:36 GMT  
		Size: 3.1 MB (3148880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81544bb6dbc15761b701c7769ec4624d8cfcdd0f3316f9e4d4293be7c2802d78`  
		Last Modified: Tue, 07 Apr 2026 03:23:35 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json
