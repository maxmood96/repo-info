## `clojure:temurin-23-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:bfbeb78f0c245e3001905f132bb1c31fed6f3845c2f5da4a6ff95cc42ebdd389
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b2e831dbe5c4eb23d7c6e1196730cff1e781f22605f6efff4afc1b694f4e640a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243157548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7c669f97fc0739c332483a5b8a20a4788df66484619dc03c6c53ef41d9dd75`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_ROOT=1
# Wed, 29 Jan 2025 19:11:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2806fada5bbd726211d6a40cdf832269f7e95cc54ce25b42cce88358a98ffc32`  
		Last Modified: Fri, 31 Jan 2025 02:18:34 GMT  
		Size: 165.3 MB (165316197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13dae2844334798276b9ebaf03f666507749576c4309e068e7319b1c7a1a418`  
		Last Modified: Fri, 31 Jan 2025 02:18:33 GMT  
		Size: 43.1 MB (43074079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd65e8ba85015434d679713e77c284aa8fd7d75bcaca1557a1819cdb8dc938b`  
		Last Modified: Fri, 31 Jan 2025 02:18:32 GMT  
		Size: 4.5 MB (4514179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2428a30700eb32ee22f01c9ed71af3e68b27a0f4c5001841cd166ba50352c688`  
		Last Modified: Fri, 31 Jan 2025 02:18:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:db0b394c0ea54df9ae9332e5a25841296ff526143e600612fa4c95a07d0294da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4fa29d5e870231ce4611a435ceb02aaa021533c647fde4ad8faa4a060cf9ba5`

```dockerfile
```

-	Layers:
	-	`sha256:8378db47f9b70bf0ebdcc094ee6e7cb5f6df980983764d2115f4892b793c1c50`  
		Last Modified: Fri, 31 Jan 2025 02:18:32 GMT  
		Size: 4.6 MB (4573174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b168b9f45b1ac0a2ab581a1c0c2992c1da4088838a63f517e6eb0aa6688ff68`  
		Last Modified: Fri, 31 Jan 2025 02:18:31 GMT  
		Size: 18.5 KB (18456 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:08db19699730832902dabd84e56b94dbc83e9adc7c9d16aece9fcb01faf3050c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239711885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d94859731a878d83a0f809ec5a49d202a566a0eba1fbcc7730abbfba8899ad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_ROOT=1
# Wed, 29 Jan 2025 19:11:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb526c5d9257b008ce9e6f38b15ff60d85e230a9348d9b3dfd8794b4a0feb10`  
		Last Modified: Fri, 31 Jan 2025 05:31:53 GMT  
		Size: 163.3 MB (163341446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09f99f7285debc7b115475e588654aa576a8c68b25c94d7cfdc9372e1946037`  
		Last Modified: Fri, 31 Jan 2025 05:31:51 GMT  
		Size: 43.1 MB (43110900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0438fd7a2e6d06127639c6fa31c91df18b695463e4e78331609371adece78444`  
		Last Modified: Fri, 31 Jan 2025 05:31:50 GMT  
		Size: 4.5 MB (4514198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed91e8a26c16b266c8d059224fc05c6ad501c8cd20075d5e145eb26b6a473605`  
		Last Modified: Fri, 31 Jan 2025 05:31:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3325b0d89895fd9c2bca5601777e4335ca75ec120a1db34e50568bef91d2b153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4596794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac909bb4a41aed62248368dd1a9f1d12ba7c781e136f3806a012991a9ea4e840`

```dockerfile
```

-	Layers:
	-	`sha256:683a8ae6620f4808f7879bacffcd84c0fbd0846ddfea1e2a459dc933ee90c8b9`  
		Last Modified: Fri, 31 Jan 2025 05:31:49 GMT  
		Size: 4.6 MB (4578217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d89f6161f0906ca2d363718287c273296992ddc7db3ac26ec10438cd00f08eed`  
		Last Modified: Fri, 31 Jan 2025 05:31:49 GMT  
		Size: 18.6 KB (18577 bytes)  
		MIME: application/vnd.in-toto+json
