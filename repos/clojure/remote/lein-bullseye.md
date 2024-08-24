## `clojure:lein-bullseye`

```console
$ docker pull clojure@sha256:6630bfba17f521c2ee5555cbf6fae1bd1226faf511145b86a80e83fda963f02f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5015acdfa8f610b2e14847e390c610f8fa9c068fe6490ea142eb3c38d4a34473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270709132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54404613e62fd54a29a7cd5b361eefdbc822a7d70564fcde5ee9020c3de6399a`
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
	-	`sha256:21559f04e772d0c40d2c39dae89a59df0421db9be2b62912a2fa34043dad7cd0`  
		Last Modified: Fri, 23 Aug 2024 20:04:27 GMT  
		Size: 158.6 MB (158579244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32900181e42bc4ca61d8d3b9ff6d65e6128b7790d04f9778519fbf2e3ed2fc95`  
		Last Modified: Fri, 23 Aug 2024 20:04:26 GMT  
		Size: 52.6 MB (52646698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86708150a3978958bf1e6f5547becb0fde7073a086693d71b4d050af0ff2d8da`  
		Last Modified: Fri, 23 Aug 2024 20:04:25 GMT  
		Size: 4.4 MB (4398086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd41e46bde7e28dd88640cf679ecb7154118c69cd39caba3ca081248d6b95db3`  
		Last Modified: Fri, 23 Aug 2024 20:04:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2cd457b3da6d7a2ff5a9327b79269031601708bb2cb6f3db9974247012f488c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6474825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40dc52793945821e7adf83887eccf2e59d35e5f7a1e65864991c01bda927ea6a`

```dockerfile
```

-	Layers:
	-	`sha256:460674b2131cd98a0a1bcd2c03d390597a528366615dee19c035f0da3f516007`  
		Last Modified: Fri, 23 Aug 2024 20:04:25 GMT  
		Size: 6.5 MB (6456141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d78e74eab5f71768069083fd9a0d129466edfada2094e87408a119cf465ce8d`  
		Last Modified: Fri, 23 Aug 2024 20:04:25 GMT  
		Size: 18.7 KB (18684 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f37fe1fed6eedc12a41fa4dfad680ee84964ddfdc5ec0c1a4ad1736b08b90cb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267535950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4351fdfed10dafc719d1d6ae708d3e83c4d37570b8540812d973e9e89eb8653`
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
	-	`sha256:7c6abbac4e39392b14f19d30958c95b49a4311cd8c0068291c0df9b77f1896d4`  
		Last Modified: Sat, 17 Aug 2024 06:23:00 GMT  
		Size: 156.7 MB (156746151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eee17bc08049fba9f2a9b1a410ac84c62ccabbf0c840cdae89eac98048f0faf`  
		Last Modified: Sat, 17 Aug 2024 06:22:58 GMT  
		Size: 52.7 MB (52661417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d394196b970bfdeeefc24f9783d69535775bb0b5113966c3c1f05dbd1ec069e`  
		Last Modified: Sat, 17 Aug 2024 06:22:57 GMT  
		Size: 4.4 MB (4398031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0206b0dec388c66ebe9841d62abd1f5600f881ceb9c5d58ea1b69298e33152`  
		Last Modified: Sat, 17 Aug 2024 06:22:57 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0c29bff94e951f998b07f6fedcfb6c229910592bf1e0907d9cb46d311a1dca36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b705596e6fb73177b124b9e3b1be06780964810ff57b52af558bc956fa488beb`

```dockerfile
```

-	Layers:
	-	`sha256:af7c6a247f75d9152eecc6fdbfdfa704d29fdd8e9987a9573d80ff82ac5b2ce5`  
		Last Modified: Sat, 17 Aug 2024 06:22:57 GMT  
		Size: 6.5 MB (6461819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf31868b3ddd1fb5e486692eca3bf6ec30a189cc2960e7e8ce949724f917cf41`  
		Last Modified: Sat, 17 Aug 2024 06:22:57 GMT  
		Size: 19.2 KB (19232 bytes)  
		MIME: application/vnd.in-toto+json
