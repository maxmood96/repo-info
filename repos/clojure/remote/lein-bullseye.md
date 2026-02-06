## `clojure:lein-bullseye`

```console
$ docker pull clojure@sha256:32c66bba8ef78b684efa51eeffb9d8f77b989e1d1a7674eb42d4d897f6d7221a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d0041441c54e6d79bcef326c82422339f4faed8af08f12303029d06c8283652b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167138270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5293da9242603fad16660c8ac3bffabd5821ccd42144b19ba2cb6ec0bcda73e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:06:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:06:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:06:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:06:50 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:06:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:06:50 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:07:06 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:07:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:07:06 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:07:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:07:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:07:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:07:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c91194f72f6299c26d32d455c49f08d876c5945338b58a2601adc977d8fdb9b`  
		Last Modified: Thu, 05 Feb 2026 23:07:27 GMT  
		Size: 92.3 MB (92256227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c33f2a57023b3e5f403e06d84bdb6bf90d5660db808d78cc4579693e85cb8a`  
		Last Modified: Thu, 05 Feb 2026 23:07:26 GMT  
		Size: 16.6 MB (16607623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fe9ca60d2743dbfe3935e3532467601d036f1b824f252e82ca73abe8896dfa`  
		Last Modified: Thu, 05 Feb 2026 23:07:25 GMT  
		Size: 4.5 MB (4517732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa7fca9403afb8837c76632b43bd2343b70b627d441a44de3db2bbe98559772`  
		Last Modified: Thu, 05 Feb 2026 23:07:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e836567db477ae3157423ca9458651a7870b945850941306d8fbffa5f08cc976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4464485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15947822b477729caca8718b34ca5a050809f4dd2afade6152373ca07b6057fe`

```dockerfile
```

-	Layers:
	-	`sha256:20d7a9c90b8fbf06b8f83504c0202ba4e30f6724fdcb75c3bb6ed72586768cf3`  
		Last Modified: Thu, 05 Feb 2026 23:07:25 GMT  
		Size: 4.4 MB (4445482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d53c2aa27fe6b72c5763505801b47f91ac53f28310debbd107450c54ba59fc6`  
		Last Modified: Thu, 05 Feb 2026 23:07:25 GMT  
		Size: 19.0 KB (19003 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:edef41d7bcebb4774cc8c9376fd0a75e007630a44a29a710b524df8e80d267d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164659766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982f4f50a3bf48c919e0bab259fc27e9806e9f058057945a088071f9c8f52f15`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:08:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:08:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:08:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:08:06 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:08:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:08:06 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:08:21 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:08:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:08:21 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:08:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:08:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:08:23 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:08:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8f3e7508d6f1d4bd3071199e5a8ff8d72ca80532103a996622841fb6ce83e1`  
		Last Modified: Thu, 05 Feb 2026 23:08:44 GMT  
		Size: 91.3 MB (91288271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488b9e0e74c7b407e78ee9cb69697f36b0ef10226fd85162b679d15f0ddc3429`  
		Last Modified: Thu, 05 Feb 2026 23:08:42 GMT  
		Size: 16.6 MB (16595007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872fe920226f9065f78a803a015ead89d29d7e69cb25edc1129af8e4731eba9`  
		Last Modified: Thu, 05 Feb 2026 23:08:41 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a3d32d07e820497f12248b98054646bbdbd717f8140973dcef766e388e7ce9`  
		Last Modified: Thu, 05 Feb 2026 23:08:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2f96676168948515d2119f49655fd2f161b70278aeb9941ccc6da6f74e312fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4463624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c686465781d56ea7fc45ff0a696378ef27bf39a585feaf3289fd1b72218ef629`

```dockerfile
```

-	Layers:
	-	`sha256:1474fe0eb611f3c1df712d21c6ec81a30db6a6203311a929dc3178649d5983c2`  
		Last Modified: Thu, 05 Feb 2026 23:08:41 GMT  
		Size: 4.4 MB (4444477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:007a0a74516ea594452c177ea77cfad2019cb217cda3ae03a8d43f5d67bbb76c`  
		Last Modified: Thu, 05 Feb 2026 23:08:41 GMT  
		Size: 19.1 KB (19147 bytes)  
		MIME: application/vnd.in-toto+json
