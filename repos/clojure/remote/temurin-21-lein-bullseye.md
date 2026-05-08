## `clojure:temurin-21-lein-bullseye`

```console
$ docker pull clojure@sha256:3050bb8c0bf4b576d4b28af17bf7d4c832b1052f5e05f35c63488c18077b0607
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4b939d8bdbd05e97ae9fa87c653f07ae11e3d49bd9549315fe193d87aca43c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233077751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4733c0337516c1c1a332aaf358275f82fdd811eaa91bcfeb27d8e38bce3a2d17`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:26:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:26:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:26:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:26:26 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:26:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:26:26 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:26:38 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:26:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:26:38 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:26:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:26:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:26:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:26:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2f11661ff1e0429f0c7434e465d66c42d45cc84dca5317d1b833dc543c78dd`  
		Last Modified: Fri, 08 May 2026 00:27:00 GMT  
		Size: 158.2 MB (158166935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51cc83e16cdc2bcb10d2370d926e60086ce2a13d7eae0e809aa4258b3075336`  
		Last Modified: Fri, 08 May 2026 00:26:56 GMT  
		Size: 16.6 MB (16629509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46387d7b51a19166ec55a53500729be1b1fd1b96576a34a77c721724f1b0f886`  
		Last Modified: Fri, 08 May 2026 00:26:55 GMT  
		Size: 4.5 MB (4517727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402b94437dee365bc79f49599727dbaf321c5db2e5d070bae5aa960a21cdcf35`  
		Last Modified: Fri, 08 May 2026 00:26:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a78da41e89883123e186f64f162a656ad68ce4ef083ec7b136ef8df553e0a23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0b987957af145b2b25c919be5d23352d52b0f19562931464b0859bf5dee92a`

```dockerfile
```

-	Layers:
	-	`sha256:b27185601576bcb627b8a657d20bac6585266e6bf4b8fd59c27fd4733ab00977`  
		Last Modified: Fri, 08 May 2026 00:26:55 GMT  
		Size: 4.5 MB (4488341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0117f2e348674acd27bf83cdebba2d8ef96086f230f7f3a5a2092e040ad79820`  
		Last Modified: Fri, 08 May 2026 00:26:56 GMT  
		Size: 18.5 KB (18522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye` - linux; arm64 variant v8

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

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

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
