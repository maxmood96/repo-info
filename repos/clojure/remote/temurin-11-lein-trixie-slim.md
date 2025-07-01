## `clojure:temurin-11-lein-trixie-slim`

```console
$ docker pull clojure@sha256:d641759cd6169d33414ca8b75a60ae87d9a1b3ac4bfe7c2e531a75ed8ac9c9f0
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

### `clojure:temurin-11-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:59d6cb48b5781dbc6157a2164627e0a4fcc72b51ffd82827fe652149e00d86be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233807207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1edba50ad680193a1232b680ab1507b8bdfd95718a743e3c7118d176862fa392`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f7f88c6d7f710176d487a3ac59c7790f981832a06bfc197dbe4a74d73b1407b7`  
		Last Modified: Tue, 01 Jul 2025 01:14:56 GMT  
		Size: 29.8 MB (29761106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccc21893abe08f2b082aef4f1427009dbcf1d2a61e7e3b2424f330b6a8ddf3d`  
		Last Modified: Tue, 01 Jul 2025 06:56:11 GMT  
		Size: 145.6 MB (145635595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab8ae8adea52f35af3869d9e7364ef27d40e7104be1d2f15554810f423c8e8b`  
		Last Modified: Tue, 01 Jul 2025 02:39:40 GMT  
		Size: 53.9 MB (53896305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cca83fe695adae25f34944c1055c2e328ff37f2f2a55f64357ac66f11b2893`  
		Last Modified: Tue, 01 Jul 2025 02:39:36 GMT  
		Size: 4.5 MB (4514169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:faefd5f70deb0a56fd3addb2acdfa0f6795c1da8d983df75eccc01acd9e2ab37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df48370bd7492a2511f9683fa679661d208f95fadb6dd2fe515240bbc116042`

```dockerfile
```

-	Layers:
	-	`sha256:787e61c35b6f4d299f6e8c9d8926db8efd3cb57f2c30e2062600541d60951bb1`  
		Last Modified: Tue, 01 Jul 2025 06:36:05 GMT  
		Size: 4.3 MB (4297607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5986d16efdbfa2e9c259a221900e3bd9a54b436c8ba823b866e664d3804cfd9`  
		Last Modified: Tue, 01 Jul 2025 06:36:06 GMT  
		Size: 16.4 KB (16449 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f7affaf0ac0242e4e0ffb8648062aa4ca7bee1ab9a5bff6704fd58462430627d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230922995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33461445ad31e543d58c8250a5f0f20a94b95913015b5130bb66ed5bb70d83d2`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c3306e90503bf56d5d575fca0323e4953fc66cffec788094159d11570a81151f`  
		Last Modified: Tue, 10 Jun 2025 22:53:04 GMT  
		Size: 30.1 MB (30121041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2e53b293f1fdac6d661d1a380287310ad1f0a58ef8bf62fd8224dd5ab24535`  
		Last Modified: Sat, 14 Jun 2025 09:09:12 GMT  
		Size: 142.4 MB (142420681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d444a987569719c7ee55b89dea105106961714e48a2a8fc2428454e97b8e4b`  
		Last Modified: Wed, 11 Jun 2025 08:18:54 GMT  
		Size: 53.9 MB (53867098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1c1c3f27b135cdc48984b8762af13014dd28ff62778ddf718bd45866253edd`  
		Last Modified: Wed, 11 Jun 2025 08:18:49 GMT  
		Size: 4.5 MB (4514143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:96363cdb79a617cb2a2beab4d627f91e74957209c3f20c0865cf79950b1b68fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4320493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c83e7c59a67b59a2246a78fec88687bd3dd36f24fe49a10f434768ce17e5db`

```dockerfile
```

-	Layers:
	-	`sha256:d9a3704101180b52ee7b9f9d432005a4c5edce154d4b62629f33dcb97baf9c27`  
		Last Modified: Wed, 11 Jun 2025 09:36:22 GMT  
		Size: 4.3 MB (4303923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55243f47c1fd8d6288675fdada8b9016b812030403cf22eadab9dd5562582c15`  
		Last Modified: Wed, 11 Jun 2025 09:36:23 GMT  
		Size: 16.6 KB (16570 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:06e70dc869d8755a0b2e24b5d0ee565ce3bdad0ff267f7029b176df7d1201b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229793158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf407f0f1c677fa8d197dd8ec29d6a0e89e9ac0b81c29844c80de5f0b2c02f70`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:2adebcab7d76ecb14ead3f70af8ca34e5abca513c2fcbd9f40e3af1e18442ccc`  
		Last Modified: Tue, 01 Jul 2025 01:19:23 GMT  
		Size: 33.6 MB (33586035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed42b7a45be9a319908284c305fbff7f8a11100527571431a46ab61609503d1`  
		Last Modified: Tue, 01 Jul 2025 08:34:13 GMT  
		Size: 132.8 MB (132810556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bd5b8bb5cd3ff8c782ca00a815ea38bcd2efc4ec4af0e2e61c3fb0691651d6`  
		Last Modified: Tue, 01 Jul 2025 08:34:23 GMT  
		Size: 58.9 MB (58882393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e0d50575033eb60084cf445d62737dd47bdf407717da81c370faf15fbb8ca6`  
		Last Modified: Tue, 01 Jul 2025 08:34:20 GMT  
		Size: 4.5 MB (4514142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0dde700fd10bed497b620abee006c78206b3676981d9d96dd2e62d2af3a6909d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4317551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb214e7dd7e5414f3454997c47f4425d6fe0b7ebe2c414115995e98cb52042d5`

```dockerfile
```

-	Layers:
	-	`sha256:32741e53743fd5edd1c4f75b4bde363e9b13b65f2e7e4c59471a53296dcb6c51`  
		Last Modified: Tue, 01 Jul 2025 09:36:17 GMT  
		Size: 4.3 MB (4301058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68a2f24515694c32061e0b2d2823806ea802759245ca310d30df04ab93165267`  
		Last Modified: Tue, 01 Jul 2025 09:36:18 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4949d83cdb407f8ae3e2ba4605c28e6ff577ee02176c990bf3293d445d4d0d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214810784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee34436132a9d4c9f1cc6241f650422ffc0c9db2bf04b2fdb532272ca33cb41`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:728fbd29b8599bd56dcb8703b5c428523bcf0f3d48c5e95804f60267a128a3bc`  
		Last Modified: Tue, 01 Jul 2025 01:19:25 GMT  
		Size: 29.8 MB (29838345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb755fd3e834f02efea83622543254c015a4203f3a730f75a90cbca87af499d8`  
		Last Modified: Tue, 01 Jul 2025 08:06:09 GMT  
		Size: 125.6 MB (125585329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d0aa3338d5ce4aea7e22df164397d9da86c0a5c72df39b77d1134bd41bdf29`  
		Last Modified: Tue, 01 Jul 2025 08:06:00 GMT  
		Size: 54.9 MB (54872934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093bf25f3a591b07bd1283c59a4e1804673955eac0b268c63c44278d0576beba`  
		Last Modified: Tue, 01 Jul 2025 08:05:56 GMT  
		Size: 4.5 MB (4514144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2ed7d3731784c248d4bdda4f8e47610b41daab53b2fbd2a20c8eb426daa4c3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4310039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac799866187d35e9466e5356bc1b4c554a780fe51b6047089c1fad86059aeb83`

```dockerfile
```

-	Layers:
	-	`sha256:f0c48815a397c7031285db9844e270e22b4bd2cd9a1b09bfe29809fcba22dcfb`  
		Last Modified: Tue, 01 Jul 2025 09:36:22 GMT  
		Size: 4.3 MB (4293590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a54aeb5ed3b61e2d16f9853cafde9536d5d134430958f09d1923ee77ab33676`  
		Last Modified: Tue, 01 Jul 2025 09:36:23 GMT  
		Size: 16.4 KB (16449 bytes)  
		MIME: application/vnd.in-toto+json
