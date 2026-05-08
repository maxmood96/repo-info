## `clojure:temurin-21-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:563a2ef1115a87afda8c347c6632d08c322a1010fabf108cc4faa8278af8507e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c10c807e287a5313ffd9bb9b857dcc13c41b9ce0bb45ef76a160f618534e2569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232767877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6363fb1f1beda0b5997141b55f3626d79398bb97c0f0e5e69fb5e9447ac278da`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:19:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:13 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:19:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:19:13 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:19:28 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:19:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:19:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:19:29 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:19:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafd308f62cf3dd75e9a399db7fa22aeb3a0c598a94eb2809da059e93c165d37`  
		Last Modified: Wed, 22 Apr 2026 02:19:51 GMT  
		Size: 157.9 MB (157857060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872144d9ef231db79e14c2ade09ebb28b5aa88dd750d0f52a1da302003e5993f`  
		Last Modified: Wed, 22 Apr 2026 02:19:47 GMT  
		Size: 16.6 MB (16629538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40de90656d3a0b3133ca7b82933e4e6cbe5a414ffd37ae08650664a627bcb7ad`  
		Last Modified: Wed, 22 Apr 2026 02:19:47 GMT  
		Size: 4.5 MB (4517700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc303eb781095ca050a140201d4c5681ddca6f74c59dcc3c45a5f80eacc39c2`  
		Last Modified: Wed, 22 Apr 2026 02:19:46 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d86ff6735b85c121f03dedb131856a59333779d273c86a0d256879e8b64df9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b1f83f8bd6c874c77c7b358604294eaa08e08039eb7f6dcb678ed42f2b4fee`

```dockerfile
```

-	Layers:
	-	`sha256:1dfcfb2f000a23f190f4271804878e039cef66d27f42ce00f88a05aa25e52744`  
		Last Modified: Wed, 22 Apr 2026 02:19:47 GMT  
		Size: 4.5 MB (4487714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08499f541718333bc85a450e53dd62cb8b3842ba4a24a401f64810b0dac3461e`  
		Last Modified: Wed, 22 Apr 2026 02:19:47 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c84f278559cd186c2fdc2abcaccc7170d2dd3546b6b7ce13ff8ba48db3a3a3fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229848883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef08dc3d96c3bbc328d57c04056dd821be811e936209e5ecdda5f321ec078b3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:25:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:25:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:25:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:25:50 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:25:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:25:50 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:26:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:26:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:26:03 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:26:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:26:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:26:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:26:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ed538be3440bd13866dfa4333600e40b79f026113b288e7e2ee989ae31389`  
		Last Modified: Fri, 08 May 2026 00:26:28 GMT  
		Size: 156.5 MB (156461247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca93bf331061d77c9d5d9c69117d4135ce6db4404aea3264fffc0e78af3f733d`  
		Last Modified: Fri, 08 May 2026 00:26:23 GMT  
		Size: 16.6 MB (16616478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8340bee5404d5c0f1c8c5bd3de8c746b86615ef5dcb610d54e2fc8be90db0e`  
		Last Modified: Fri, 08 May 2026 00:26:23 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea526f9537e3a0f3ca7f6abdd6c932f242fe143fc8504ae86b9ace99bd131c9a`  
		Last Modified: Fri, 08 May 2026 00:26:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2c88054a5ebfe6f0bfa0628c1ee370154ccf0ea5ffbabb5c301945d8252b1fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4505958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c49a03e8eb7b480b678a0f4ecf3aeb5fe1bf574147f2d6c23549010e5e287a9`

```dockerfile
```

-	Layers:
	-	`sha256:93657b8bc7a50f07cf4a2d8ded7635ccbdabdb5e16fce7744ffc6d63b2003d15`  
		Last Modified: Fri, 08 May 2026 00:26:23 GMT  
		Size: 4.5 MB (4487315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162e9e299910bb17e6d1b2c2ecefafb95785531cd4dbb37d3e5c2d78743f0c77`  
		Last Modified: Fri, 08 May 2026 00:26:23 GMT  
		Size: 18.6 KB (18643 bytes)  
		MIME: application/vnd.in-toto+json
