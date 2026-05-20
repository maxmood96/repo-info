## `clojure:temurin-25-lein-bullseye`

```console
$ docker pull clojure@sha256:b9b89a25d646fe1314406b6f81286f75f2a599962d566a7642b43f22b9d3c209
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f92714708e8375c6ece22136f51c1051105522fc129cf7e61bf378f010482be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167491158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e959daf25fca440a28624e0eb436c8b6d16f1970d6e4d78bc7a4fbf426a3fe8a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:01:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:01:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:01:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:01:06 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:01:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:01:06 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:01:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:01:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:01:20 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:01:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:01:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:01:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:01:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14149234164fb1b093f9d80c325d5e6115405ab7e7c512f266b3104394d0a182`  
		Last Modified: Wed, 20 May 2026 00:01:59 GMT  
		Size: 92.6 MB (92574586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fd2015b887cb45ae9f6046c4a7a78d2a77076f771644cea43bd94460d594ae`  
		Last Modified: Wed, 20 May 2026 00:01:57 GMT  
		Size: 16.6 MB (16629536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2fadd00b85a6c9ddb7ef35e8af94871b9ff3ad69978f6ae2817cb56710b664`  
		Last Modified: Wed, 20 May 2026 00:01:57 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a036e2083dff81600c54f6546f23bf47a9ede404b8eb3607c23550667cd499`  
		Last Modified: Wed, 20 May 2026 00:01:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c1c4d9f1138ca1920729536aea1b5e4e882de565fd501d7a1fddc7c5aea14c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d3045429c7bf28bce6782becb994f54aeb3e275a74b855241c9bdfd4844e3b`

```dockerfile
```

-	Layers:
	-	`sha256:8c006c27106189bc6d97c9be0497dec4b584298ea99e3994db801a1d9f0e6dc3`  
		Last Modified: Wed, 20 May 2026 00:01:56 GMT  
		Size: 4.5 MB (4454525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b9dde8f61855acb3b330f8c9e7385746c8be2a4d2938aa50f1d27163764dac`  
		Last Modified: Wed, 20 May 2026 00:01:56 GMT  
		Size: 19.2 KB (19157 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a10284ababfab86a98dd51b29ae15876e12ff4a68e09dada46b770bd6d07e1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.9 MB (164933525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e11346a01d08ac5477248fc8d566374525cbb0c7e82bc7a438411f418379614`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:07:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:07:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:07:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:07:31 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:07:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:07:31 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:07:45 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:07:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:07:45 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:07:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:07:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904692883b379033b5240eaabaaffde22cc721743335fd6bd53a5598330986bc`  
		Last Modified: Wed, 20 May 2026 00:08:07 GMT  
		Size: 91.5 MB (91542253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d82fcb222a169139b6c4ea8f81e895eca2ae90018be78d5b8ed1a21110ddbd`  
		Last Modified: Wed, 20 May 2026 00:08:05 GMT  
		Size: 16.6 MB (16616562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b189c0629739784bbc08a243aef62332a781952af641b5e6b94b23d62112e2`  
		Last Modified: Wed, 20 May 2026 00:08:04 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829c7da9d593c4cda7cdba8221c0049719fe460cfd52d5ee67127ce699072bdc`  
		Last Modified: Wed, 20 May 2026 00:08:04 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6fd5fbcdd80cd8076dd0e6d0a10f1c42844c539915c51f1229df0f029382f9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4472821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11f02c484c6ca26011dc7f7462da438383f4b9bae3392ec58853dbf2c4d02a4`

```dockerfile
```

-	Layers:
	-	`sha256:514f35f583fe632fe086b259e28cc5a7a48c877fa71811007456cd2dddec7b08`  
		Last Modified: Wed, 20 May 2026 00:08:04 GMT  
		Size: 4.5 MB (4453520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6b657d8f67ce3228a2f67d01ca7a312dbb704d2eba0349b83878ac0052a045b`  
		Last Modified: Wed, 20 May 2026 00:08:03 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json
