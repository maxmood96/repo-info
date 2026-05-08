## `clojure:lein-bullseye`

```console
$ docker pull clojure@sha256:5e0196c677c549335ee4b23151aa73a0ca426a6bc08244f7da76c4db81b6e91f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4d86a4c75527615eb38662eef4c6319ebbe4f72d7c5fc498f43937f48c1ef35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167485475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ec45f737440349f03320b85552127b5e5b8d1660caa85f5c4ff2e319c1d8c6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:27:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:27:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:27:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:27:56 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:27:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:27:56 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:28:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:28:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:28:11 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:28:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:28:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:28:13 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:28:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d029ad6c6da357c470842817e77d447806d56a4138acb37a58792f729eec8b`  
		Last Modified: Fri, 08 May 2026 00:28:39 GMT  
		Size: 92.6 MB (92574587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2eca6611eba049dd41b66af29dd0ec8548ba237cfeadf7e8287be3e9af5a0d`  
		Last Modified: Fri, 08 May 2026 00:28:32 GMT  
		Size: 16.6 MB (16629553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8619fa8afdb1d82f76cb406a2aad94f1c30dad16bbeedbc3b5bde6f91c462d9`  
		Last Modified: Fri, 08 May 2026 00:28:32 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef4400e3f814d57cdbb8a7ece59eee8784b7640c3a5890726644101d527eaf3`  
		Last Modified: Fri, 08 May 2026 00:28:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bba9cd14c1933b3b524b244dada57185924268e4d048398b0b3c24b1b43e95d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80411795603b66336b221db811d02da159a4e6ddfe0b16138fa103cbb6fc73b3`

```dockerfile
```

-	Layers:
	-	`sha256:709bed47904bd0ea85b1d176f99c383d7069cb704f1f0c16d75a22b1940c5c82`  
		Last Modified: Fri, 08 May 2026 00:28:32 GMT  
		Size: 4.5 MB (4454525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eedb4ca933b4b1837551d95efe1b1c38810f30a264da9b6e625727b136d60398`  
		Last Modified: Fri, 08 May 2026 00:28:32 GMT  
		Size: 19.2 KB (19157 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d55300324e43a9273f9dae47e3a25d1c08c0034f9f2beefccbc0596328af448c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.9 MB (164929907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf4dfae64b6d2c0af3f4711aee52cd3cf716b95cc7dce4f7c9558492bfd7e45`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:27:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:27:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:27:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:27:09 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:27:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:27:09 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:27:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:27:23 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:27:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:27:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2ba2d04412a926ea9f6ebac8d3d6d5738f9d008c45d94fd00311d3be4637e4`  
		Last Modified: Fri, 08 May 2026 00:27:44 GMT  
		Size: 91.5 MB (91542275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44074d7151de6fef0b171e25bca37e32ea9abbed5eccd2c5fb6d015789945e8b`  
		Last Modified: Fri, 08 May 2026 00:27:42 GMT  
		Size: 16.6 MB (16616499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffe9e29b4c44537b17b187bf18990e1e7c069e5891931d19c4005dcfb0386dd`  
		Last Modified: Fri, 08 May 2026 00:27:42 GMT  
		Size: 4.5 MB (4517703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9096672a7ae4df68de87be7c14747bed4b4f8954843f3cc513c1e5afedadb52b`  
		Last Modified: Fri, 08 May 2026 00:27:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b5b7c8c73c04ee2df09c60919d52643b3081e909ee06a1cc689ab0f857d73654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4472821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be6d02703e3311604df38b9274a90bb233dbc3f8ad446a96392e29942a4eb04`

```dockerfile
```

-	Layers:
	-	`sha256:2f78f46f7a2d98867d658d5cb19abe8fc10e5b03e34cdf8be9022d23e5fb1f8d`  
		Last Modified: Fri, 08 May 2026 00:27:42 GMT  
		Size: 4.5 MB (4453520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f29ba386ed26c5240710a63b3e455148afe119ae8356d8041115d765add0dc`  
		Last Modified: Fri, 08 May 2026 00:27:41 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json
