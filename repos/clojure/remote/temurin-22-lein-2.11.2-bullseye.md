## `clojure:temurin-22-lein-2.11.2-bullseye`

```console
$ docker pull clojure@sha256:e879ae6060c50a893a4c7c9dcd1761060f42ffefd62dcad34e2be4c59b7728da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-lein-2.11.2-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3908de7fce14036e701c16ce44f947f39e4d144a728033ea0cbf53d0a21559f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268611507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b72245d0b7d09f4e9c1f8620b7e649e617e7f6d138a6c5b06ffdad3b8ffbb9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
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
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6339fada5189840661cc1e39125cd2585288e4b90122ad94ed803eb26ce4072`  
		Last Modified: Fri, 23 Aug 2024 20:05:32 GMT  
		Size: 156.5 MB (156481609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3470c62ea32853a5da0e1340792cd2c57fbd7a613f644e6e0d11a4ae4b469da4`  
		Last Modified: Fri, 23 Aug 2024 20:05:33 GMT  
		Size: 52.6 MB (52646745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cd7eabe2f4b475f75dc4aec71b20e79425d4994a901095a9f71b357e6ba09c`  
		Last Modified: Fri, 23 Aug 2024 20:05:33 GMT  
		Size: 4.4 MB (4398049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80a5539c7ddaaef4be22b0dcaa8cde3adf829287d29ef5732c3bec8c8a0f81e`  
		Last Modified: Fri, 23 Aug 2024 20:05:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a237ccf24457fc0b3b23fc1176637d28133bff1b02f5a9c28f8789299dbbf61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6473525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7ebd210cee41fa262db07e3763e5c0df09e246b210ae052e6023b6c67157d9`

```dockerfile
```

-	Layers:
	-	`sha256:2302298912fe5d3ebdef600da5bafbf7b0779b1b607562eff0d9c5c6a35e5568`  
		Last Modified: Fri, 23 Aug 2024 20:05:33 GMT  
		Size: 6.5 MB (6455483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07ce0b6dc943dd29988148ab8501fba97007a04e1cb43d016f41f40d23af5ff5`  
		Last Modified: Fri, 23 Aug 2024 20:05:32 GMT  
		Size: 18.0 KB (18042 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-lein-2.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9b2b5bfd86096b4e6ff1d471f1cc03c8a0a685f83de51ab912c98c952d5cfbc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.3 MB (265293468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425aa9cddee814b4a10e6547b8797de99d67470339398b088152768a7ed10488`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
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
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458cd2a281eadaecc5ca931234450d99480ba147d820624e2c5f6ce0dfc7072c`  
		Last Modified: Sat, 17 Aug 2024 06:35:12 GMT  
		Size: 154.5 MB (154503707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d4c6664b68bf6506076184f43b618a5f0a24553d4d0930a183a55f15212d56`  
		Last Modified: Sat, 17 Aug 2024 06:35:10 GMT  
		Size: 52.7 MB (52661372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48efb407c0760744146e56aea53b0643bdbd7b8ecf75a058d9a33a1ab16edd`  
		Last Modified: Sat, 17 Aug 2024 06:35:09 GMT  
		Size: 4.4 MB (4398038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe77ab9e8c8ae8cd15d8e209ff2c540fe27227f403d15c3a99f134d62aaf909`  
		Last Modified: Sat, 17 Aug 2024 06:35:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d26f9647fff1bd4b9c1cceacec00f4869b1fa5db40120eeca017169725c7e90e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6479703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375c56a38794f289b7899d35cf3ee79a305cb399a94672c89acd05914861dff8`

```dockerfile
```

-	Layers:
	-	`sha256:8b5b32364a0979af59bbff4f7e9d2a0dbecdc0827528b294692fe951977ac5d2`  
		Last Modified: Sat, 17 Aug 2024 06:35:09 GMT  
		Size: 6.5 MB (6461137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0da3b9b1090845a1d394535f22d01c36b5c51d6cca245baf6e906ae16f61b8a7`  
		Last Modified: Sat, 17 Aug 2024 06:35:09 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json
