## `clojure:temurin-17-lein-bullseye`

```console
$ docker pull clojure@sha256:0b68c4cb74ffe0e018d73c977c0791c7a388cec90bd701285924b04bab02ccd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3b0c06f46ff1021addaf45ec2d6a1c5c30e600b1359f95c27e9065255fad5d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220538624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f89d67ee4f976378a333266dee691b97381d260c611687a8795126714fdb5a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 02:58:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:58:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:58:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:58:08 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 02:58:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 02:58:08 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:58:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 02:58:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 02:58:23 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 02:58:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 02:58:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:58:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:58:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e759575b5b0029fea51256b7ad3afa90c8ff1a6a9457787359c2b05b4a964edd`  
		Last Modified: Mon, 16 Mar 2026 21:52:53 GMT  
		Size: 53.8 MB (53762481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1d89e76e78c7cb051137c99ccc404ecffc4a405aa1a7ba74390397220da919`  
		Last Modified: Tue, 17 Mar 2026 02:58:45 GMT  
		Size: 145.6 MB (145628455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b986d6dfe617cf3be21f3daf53e3218e1cdab4347f18392e3c71c33a233d401`  
		Last Modified: Tue, 17 Mar 2026 02:58:42 GMT  
		Size: 16.6 MB (16629543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b3987fc0d43804525d87bc5519276c430b68f235212a9b166b3a4277258708`  
		Last Modified: Tue, 17 Mar 2026 02:58:42 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817ba554ba71cea113adb380e6dcf566c4662e19435a837a3522bf002631335f`  
		Last Modified: Tue, 17 Mar 2026 02:58:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0cf3a9ea84dc04c4f74f7bfea3f15461b541fe590745d9292091bcd3f3f2d288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4504228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c670f1c02e3ae50f3c22aa9ff25e687960b23a6782cfa05ee2d78bfa804d1107`

```dockerfile
```

-	Layers:
	-	`sha256:441cd324c77579a2cd3898bbcd243d9437dedee5eb855fe4ade9147db90aeaf7`  
		Last Modified: Tue, 17 Mar 2026 02:58:42 GMT  
		Size: 4.5 MB (4485862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:098f72f0ea2212b40d8781a14b3909aa30fdbc5581412ea041c09171cc49c582`  
		Last Modified: Tue, 17 Mar 2026 02:58:41 GMT  
		Size: 18.4 KB (18366 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5616e94ea406d97a9786fe5721df23e0d4afe02f26c381fc273d58b05048ef25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217818116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446a35250667466371e36f9c23e431c830430dc872ceb9634d38f2c5ac31788c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:02:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:02:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:02:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:02:30 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:02:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:02:30 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:02:46 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:02:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:02:46 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:02:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:02:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:02:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:02:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:da8e260297fdb91b3f012b26dd982feb43d0bf977ff8adeb7a850ef9c5829770`  
		Last Modified: Mon, 16 Mar 2026 21:52:51 GMT  
		Size: 52.2 MB (52247254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05c6ea7e869e2f290b3a380d217cce9bd766681b9eccfc7947f5d91a17c8c10`  
		Last Modified: Tue, 17 Mar 2026 03:03:10 GMT  
		Size: 144.4 MB (144436233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5d04f342b686bf059c046aec459a16923052017ca0482090e373e632d81d1d`  
		Last Modified: Tue, 17 Mar 2026 03:03:07 GMT  
		Size: 16.6 MB (16616491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6aa5ddb91b222c8fcbc17054dccd7b98cd384621a9c524dfb3718c69d8cdd3`  
		Last Modified: Tue, 17 Mar 2026 03:03:07 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9dd0c7459457a87cca17edbcf60280fe724ed0d6922deb7cf396136a540935`  
		Last Modified: Tue, 17 Mar 2026 03:03:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e3c6d34c1d1ec32401f60f21c65b536e0f35dfd6744fdd8b8b8212992cd7d49c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4503325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371237678b5d1f3bf3c9959d8f7dd364955950acb25b1683f69a688969e8fbad`

```dockerfile
```

-	Layers:
	-	`sha256:2b35622ac0a7b6df03c171e5b32193c8b730b795638d10db8b8704707034a015`  
		Last Modified: Tue, 17 Mar 2026 03:03:07 GMT  
		Size: 4.5 MB (4484836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5de1158ae12819ed605b233ccf4dc66ef0da64fd23feabdd1f38db1d125561b`  
		Last Modified: Tue, 17 Mar 2026 03:03:06 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json
