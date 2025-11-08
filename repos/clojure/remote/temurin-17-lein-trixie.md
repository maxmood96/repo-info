## `clojure:temurin-17-lein-trixie`

```console
$ docker pull clojure@sha256:c1d5bbcf79a72027a9f9ca08a3a2a6d79e249b2a3ba61f291667ec79dd4bbb14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:a6cb258971a6a5307224a372236ecc25292363a4b7bdfaa711196072e968a942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.1 MB (217076305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ccd5b637510eaeb16c4960af0b8b2f12147b5e225dbc4d827bdd1ef6235f74f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:30:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 04:30:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 04:30:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:30:47 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 04:30:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 04:30:47 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 04:31:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 04:31:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 04:31:03 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 04:31:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 04:31:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 04:31:05 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 04:31:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e5fcf26a03206838a32e1ef420dab8416818472bf1244f436c8c7f297bfc67`  
		Last Modified: Wed, 05 Nov 2025 13:28:56 GMT  
		Size: 144.7 MB (144693305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df3b23166fd7fad21ee8c8b71dba4562cb20f19f05fb2b244ef89cf96fa4b0c`  
		Last Modified: Tue, 04 Nov 2025 04:31:34 GMT  
		Size: 18.6 MB (18579193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae4a206592cad52597171f775cb09a96b73627b20c972f5ce4c16e308f6b3eb`  
		Last Modified: Tue, 04 Nov 2025 04:31:32 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9868d5984b87f9e75c253e8db6fe11741ecd323d297775df1c0374d04dcebd7`  
		Last Modified: Tue, 04 Nov 2025 04:31:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8376816a9b9cf6b7d439a2db0cad691640ce88ebf8811e95e0ddfc10e6a0eb0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b60c27b6711507ad6d9d3d217e7adea7d945a754c5dbf8371eed44d66b666a6`

```dockerfile
```

-	Layers:
	-	`sha256:f0d1b045765cccbe4fe9350cd47b82618f1c4e02fd588d648b35d356dd7f4693`  
		Last Modified: Tue, 04 Nov 2025 10:40:29 GMT  
		Size: 3.8 MB (3813384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2cdcbe284766cd66ff5583cfd79775b502befefd9b1df74fe6597e01dacc8c8`  
		Last Modified: Tue, 04 Nov 2025 10:40:30 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9d5dfcf61bfdab709466f5623e5972c03b826be5598d6b269f034bfca67e3dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216250612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65eabeab644e3e4b7432a97f514570f31459cdd6d7130b928480a2892090dbdb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:44:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 01:44:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 01:44:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:44:26 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 01:44:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 01:44:26 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 01:44:42 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 01:44:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 01:44:42 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 01:44:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 01:44:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 01:44:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 01:44:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4a0f13e67f368d18098ee9ec8c0610e5e508727009de2f49717a990d7498db`  
		Last Modified: Tue, 04 Nov 2025 22:42:18 GMT  
		Size: 143.5 MB (143542093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce80f382b220a94b54c7b790bdce62cf122379fb1cf649e792bcbe37e122a21b`  
		Last Modified: Tue, 04 Nov 2025 01:45:10 GMT  
		Size: 18.5 MB (18539906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2c153f01057e9321c95fdf1902766393f0ee6e826248095f11e852d7210212`  
		Last Modified: Tue, 04 Nov 2025 01:45:09 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c494f6fc432f9a25cdd007e709f127021758eafe46ed52840b9fbf54487ebe62`  
		Last Modified: Tue, 04 Nov 2025 01:45:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:038c847cc27b49bbb29e60762d8d933113d93b0029f13e24635ab43305cb8b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab4f136e1c2d8f1f7c5da0850845001f7711c0f8a9117d978787f6158d207db`

```dockerfile
```

-	Layers:
	-	`sha256:e0b1dbbf0e491720f5181cbe841ad7778263971c7d3db58031c723319fc8e58c`  
		Last Modified: Tue, 04 Nov 2025 10:40:34 GMT  
		Size: 3.8 MB (3814261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:219f15f054c3cd07ced8319974a1ab9f4210d3075c1a647bfb1145f100ba3807`  
		Last Modified: Tue, 04 Nov 2025 10:40:35 GMT  
		Size: 18.5 KB (18472 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:5a8ecf69ccc1f2d2b1e23518b301146328b18840c7522d086c33bd874880ee65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220637810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab7416cf300989c73ac2be2ebdf0820b04eaf34823744cfdbe3054693c9a89a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 13:24:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:24:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:24:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:24:19 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 13:24:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 13:24:19 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:25:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 13:25:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 13:25:03 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 13:25:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 13:25:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 13:25:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 13:25:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb09d1935d5dcfb59c2b828f8730e2e0cc1200d9a83398904ff45bff51cda4b`  
		Last Modified: Tue, 04 Nov 2025 22:42:40 GMT  
		Size: 144.4 MB (144372909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4754195a70540376763c7eee40b5a2bb4e9fcefcfdd9da2bb4537904e3d4586`  
		Last Modified: Tue, 04 Nov 2025 13:25:59 GMT  
		Size: 18.6 MB (18636628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe715847c91e5b25fd17c2ac8728c4a2c4eed9ac3eeb18644e320c31106ac8c`  
		Last Modified: Tue, 04 Nov 2025 13:25:57 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764b5b0ff1585ba2eff1b796bb5151e8b5950a8c270279b518ed94d7a58c9a98`  
		Last Modified: Tue, 04 Nov 2025 13:25:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f008c33ea97e54fa8e55b0d7f952acccedcce01fcc806b8d9d24edabc69ce9cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b79195afad5b035794f7657dffa2ac0241459aca15cd3c9f44154b508fcaaff`

```dockerfile
```

-	Layers:
	-	`sha256:d1bb534caafe53b48b1e0b072a1d98855bb298cef66978bfaef65670f4caa6ee`  
		Last Modified: Tue, 04 Nov 2025 16:36:53 GMT  
		Size: 3.8 MB (3814382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecb125d0805b2f6b9c1a9c73dc7de3ae2354387e430c8f534acf3d05df5151b0`  
		Last Modified: Tue, 04 Nov 2025 16:36:54 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:44639b65f1af989e2b487b4e43d4073197e80f5af5fc83b98594d485c31eb1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.4 MB (209395897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be821e273d1c432f440357c40df7a813e1514e79f7915e2ae01f76fc5f974e7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Fri, 07 Nov 2025 06:05:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 07 Nov 2025 06:05:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 07 Nov 2025 06:05:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Nov 2025 06:05:53 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 07 Nov 2025 06:05:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 07 Nov 2025 06:05:54 GMT
WORKDIR /tmp
# Fri, 07 Nov 2025 06:07:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 07 Nov 2025 06:07:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 07 Nov 2025 06:07:24 GMT
ENV LEIN_ROOT=1
# Fri, 07 Nov 2025 06:07:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 07 Nov 2025 06:07:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 07 Nov 2025 06:07:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 07 Nov 2025 06:07:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c954b8170eabf573a80b99d49dd9da69985111271e239b9f7af18ceb6ef66d`  
		Last Modified: Fri, 07 Nov 2025 22:58:29 GMT  
		Size: 138.6 MB (138575651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f6f4eb3058ef92c4da1b26dffddb803e20ce4ddbb8758e0477c3a88b5f8826`  
		Last Modified: Fri, 07 Nov 2025 06:11:58 GMT  
		Size: 18.5 MB (18531104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b42ce8933ba23c8c2522b51719998b7750d75a45e42d8b9d895bc5f6bc14529`  
		Last Modified: Fri, 07 Nov 2025 06:11:54 GMT  
		Size: 4.5 MB (4517788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfbefc8c391096bcc88ea00b941e23af27e2e230ec4c192459ddfb6c2f2c95d`  
		Last Modified: Fri, 07 Nov 2025 06:11:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:54d20f6ee05fd27aef569916f93d3e559876da6766343935079cafec05659d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3820336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324c0f8de2410aaba97494ba06b3ff7980a7d38632f0be9cc3a7d42d755ef275`

```dockerfile
```

-	Layers:
	-	`sha256:ffb47c7044816d59e523b8a6e364fc44109c2b26f8f8c95ca68b8f74f6e38603`  
		Last Modified: Fri, 07 Nov 2025 10:35:41 GMT  
		Size: 3.8 MB (3801940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3328b7abe7e4d083f327c70f1d5685bcec54fb0603f76ea80e2da2df3e3d4862`  
		Last Modified: Fri, 07 Nov 2025 10:35:41 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:d824227c11f56569366b6572214eb9c34e7314ad995f1b34ed073e9f85693d99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207214246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7421dd4e0b643942fe07da661c1bca62b4b2df860c8a3999e531e1c6c7c5c63b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 12:59:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 12:59:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 12:59:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:59:31 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 12:59:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 12:59:31 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 12:59:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 12:59:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 12:59:44 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 12:59:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 12:59:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 12:59:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 12:59:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8caae96ef3e33780620b5029c31906f23b6496c68aac3becdf6358b74de74a`  
		Last Modified: Tue, 04 Nov 2025 23:01:24 GMT  
		Size: 134.7 MB (134723624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203ceced0f77127059d7a2b1116e170a9ec9d80fa254ed965fcf6ce5eaecc537`  
		Last Modified: Tue, 04 Nov 2025 13:00:27 GMT  
		Size: 18.6 MB (18620169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e90cfe119558e5ea7becef156051dd40d78da6607c53c997da2a0437d92c70d`  
		Last Modified: Tue, 04 Nov 2025 13:00:27 GMT  
		Size: 4.5 MB (4517725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3c9f607295c691e6b1bafbe975377875732d6637c7ba716bc6bfd19e3ee03f`  
		Last Modified: Tue, 04 Nov 2025 13:00:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8a8e3763fbfa0dd48ff5acc9d7ba81eebbed13a91fdcaf904ed37df05a6c9be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3828163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b6266bc1821f5c84d7d963e7dfd4355b9e53206a865019122636123cd89f5d`

```dockerfile
```

-	Layers:
	-	`sha256:ebb2939771c01323a724271e716ddc55846e775ccd5fedf25e36fa214040f306`  
		Last Modified: Tue, 04 Nov 2025 13:35:55 GMT  
		Size: 3.8 MB (3809811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdfa5d8cba28e34c7146219cb77e8567110f31361d09cee6288a33b6d7c70107`  
		Last Modified: Tue, 04 Nov 2025 13:35:56 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
