## `clojure:latest`

```console
$ docker pull clojure@sha256:208fba4f0d3c0c76b6567c82eb82fb52eef314647e35431981b97029ff1aa5a1
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

### `clojure:latest` - linux; amd64

```console
$ docker pull clojure@sha256:d7da101aa452f3ffd3319d928b5da6cad4422a8b7613cdcec300d11c17a63c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240153820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071d2498a2fbfcf1eb5c272d4ba544dd5bc3095e509daa3e479f665ea0b785b0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:44:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:44:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:44:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:44:56 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 02 Mar 2026 19:44:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 02 Mar 2026 19:44:56 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 02 Mar 2026 19:45:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 02 Mar 2026 19:45:11 GMT
ENV LEIN_ROOT=1
# Mon, 02 Mar 2026 19:45:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 02 Mar 2026 19:45:12 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:12 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:45:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:45:25 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:45:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76b699a67cd85fc2cd6339f3f0a11962950094f89b72fbc304b1cf5fcd2ade1`  
		Last Modified: Mon, 02 Mar 2026 19:45:46 GMT  
		Size: 92.3 MB (92256297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b7ca960a4e40dadfd0dd5639e95dfdef066986c93b05c93280d73b1e865f86`  
		Last Modified: Mon, 02 Mar 2026 19:45:44 GMT  
		Size: 19.8 MB (19802889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1925f255ae459c38f166797cc6caecb6e24f00548f8d2e33a322d65b79ffcaa`  
		Last Modified: Mon, 02 Mar 2026 19:45:43 GMT  
		Size: 4.5 MB (4517699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d363569178bc0fad27dc5159f9dec091aac5a463104cb44352d4878f298aa31b`  
		Last Modified: Mon, 02 Mar 2026 19:45:46 GMT  
		Size: 75.1 MB (75087080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e1688530163683d848a7e2f9ebe744d1fc9bda5e466ffd6dcee4217f78d538`  
		Last Modified: Mon, 02 Mar 2026 19:45:45 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ccde7ec02ba041e17030136dce257087f974861d31618d3c833d3f8ccdb46d`  
		Last Modified: Mon, 02 Mar 2026 19:45:45 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:559911fda81b315cef7fe450dd83d096c2c9a44f70f22e51baa9c816df73156c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7464479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8805315253b48d8f6309cdadb1571ec517bd108a994d426c2c351cb91bd915a`

```dockerfile
```

-	Layers:
	-	`sha256:30bc74f5a030b37a984d8cbb8a65460fbe5ab411050556292a6d2a15f728dc1e`  
		Last Modified: Mon, 02 Mar 2026 19:45:43 GMT  
		Size: 7.4 MB (7438871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f64733f0912d1992550576c4a47fd843fa41fd43f3cc72abef7b80b176e34756`  
		Last Modified: Mon, 02 Mar 2026 19:45:43 GMT  
		Size: 25.6 KB (25608 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a0fe63dedd894061959cd10a27581d8f1be3a348ddd3a8494e9386f84c93cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.1 MB (239059948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b7d779f6025265d3739e96606b4cedce8491517567984f7e6e0fc06c4f59ac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:44:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:44:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:44:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:44:41 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 02 Mar 2026 19:44:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 02 Mar 2026 19:44:41 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:44:57 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 02 Mar 2026 19:44:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 02 Mar 2026 19:44:57 GMT
ENV LEIN_ROOT=1
# Mon, 02 Mar 2026 19:44:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 02 Mar 2026 19:44:59 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:44:59 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:45:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:45:12 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:45:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9c01e8c62b6a4ee3dcef0a1f04240589e4f30f06ddf16fb3bea6c0ff38a9a0`  
		Last Modified: Mon, 02 Mar 2026 19:45:35 GMT  
		Size: 91.3 MB (91288275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df77e85c1e83cd6744472db17dde0c4d678780c23032f72e9700539d81371a3`  
		Last Modified: Mon, 02 Mar 2026 19:45:33 GMT  
		Size: 19.6 MB (19632836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a50bfafbf5b5dbb4562103b8349c64c067aa68bd9feba04f7c3deaa8e31d43d`  
		Last Modified: Mon, 02 Mar 2026 19:45:32 GMT  
		Size: 4.5 MB (4517720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80dfceee0aeb881c970cbb1379b1ec87a0faf79b0725f2a86c078f7d0fb6377`  
		Last Modified: Mon, 02 Mar 2026 19:45:35 GMT  
		Size: 75.2 MB (75246830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e1d70574adcc83828b57040d9157df7e8ea419bfb886ed889df4f4ebf813c7`  
		Last Modified: Mon, 02 Mar 2026 19:45:33 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b3025e59096b5942625b4042973e1876666aa4184c397269001f3d7e60160c`  
		Last Modified: Mon, 02 Mar 2026 19:45:34 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:abb933d1de178d2be51eaea3b5728202ef317a8e1fc37efe72efd8c3147b7643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7470340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb574877a11cc4239d375f2ed59bf723b45119626aadf7e28e74f30ca6d1362a`

```dockerfile
```

-	Layers:
	-	`sha256:ae0126efef229559a8539b6bdad788b8df03f721828a7e42de689734bd13e2da`  
		Last Modified: Mon, 02 Mar 2026 19:45:32 GMT  
		Size: 7.4 MB (7444607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5640c50e4aa276620e8a62a7fe0136820f1ece3f18b9581ea1a88e350204d6e2`  
		Last Modified: Mon, 02 Mar 2026 19:45:32 GMT  
		Size: 25.7 KB (25733 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:3ac3a5c7d3a97ea1255f9442ef24134667935fbb7f9db066b42b9d21caecfda9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249201665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b311ef5a82b097c6d263cfbd379aa335b2f995d7caf2654d561e848fc8fa39c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:43:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:43:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:43:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:43:33 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 02 Mar 2026 19:43:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 02 Mar 2026 19:43:34 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:44:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 02 Mar 2026 19:44:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 02 Mar 2026 19:44:28 GMT
ENV LEIN_ROOT=1
# Mon, 02 Mar 2026 19:44:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 02 Mar 2026 19:44:33 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:44:33 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144f17a3e7d82510fe9dc0d0bcec634fee1e230b910b421966d0efc2cada5dc0`  
		Last Modified: Mon, 02 Mar 2026 19:46:31 GMT  
		Size: 91.6 MB (91632868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3fcea0e2fc1ecd70c7be43c8017e7f6b1813426265e20284695f2d82d45049`  
		Last Modified: Mon, 02 Mar 2026 19:46:28 GMT  
		Size: 20.0 MB (20023867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79f8d01d22e13490980f7b437988323003ff24cf034e0a86bb0e2bb286dae5d`  
		Last Modified: Mon, 02 Mar 2026 19:46:27 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5166d303bbe0285d25a7133a0aadc04743aa6fc9223da28e06758c984b8f3266`  
		Last Modified: Mon, 02 Mar 2026 19:46:30 GMT  
		Size: 80.7 MB (80689295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb1b4b8d4f213eae94f73fa68ad8bcf6587c3c42864b47292c3b710926fd0d1`  
		Last Modified: Mon, 02 Mar 2026 19:46:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd53d6755fa70c2b3fea5e3c5ceba933623feb7bb0cdf9565693a4e066a9fc3`  
		Last Modified: Mon, 02 Mar 2026 19:46:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:2daa35b7f4f6236e007a1c944a359f34b02e80e2dae80b8dde3a549488406e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7453035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8adffd8354121a5b0d927c075322bf2d66d4f2985e8c70590dbb25c4006ca3`

```dockerfile
```

-	Layers:
	-	`sha256:b52cff5dfb16db76890c48686e28eafa42733dc2239b8d7bfc3268b27ffd599d`  
		Last Modified: Mon, 02 Mar 2026 19:46:27 GMT  
		Size: 7.4 MB (7427387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaef37d583952cea86632be682a2b46a0704390731ff4f8a513723bdbe4ac5fb`  
		Last Modified: Mon, 02 Mar 2026 19:46:26 GMT  
		Size: 25.6 KB (25648 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:a615507f4c35297696ba99a4aecd6afab8a08e5b0e61f181596e6101e4bc2d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233599976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0b87ff53befcb10549cd8383b5470b8292f47d1c4a640df95b63fdb2ced016`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:43:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:43:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:43:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:43:48 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 02 Mar 2026 19:43:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 02 Mar 2026 19:43:48 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:44:01 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 02 Mar 2026 19:44:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 02 Mar 2026 19:44:01 GMT
ENV LEIN_ROOT=1
# Mon, 02 Mar 2026 19:44:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 02 Mar 2026 19:44:03 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:44:03 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:44:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:44:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:44:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:44:18 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:44:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8781f03b454859a22c4fa25519a34b79cfb12298079f54ca3a9dbeeaca5b04ac`  
		Last Modified: Mon, 02 Mar 2026 19:44:50 GMT  
		Size: 88.2 MB (88233869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e175fdfbe41a68cebbd3f5cfeac063714aba6f2e1d46b915512490c74a9b6a`  
		Last Modified: Mon, 02 Mar 2026 19:44:48 GMT  
		Size: 19.5 MB (19463167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27491a6351f684f328980b88d72f9a646c15345e9e362c9ff6b5ab2e35026351`  
		Last Modified: Mon, 02 Mar 2026 19:44:47 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d33422f9ecadf4be68ab071446e74424a9e8ab2d3940b174900eccadde0fff`  
		Last Modified: Mon, 02 Mar 2026 19:44:50 GMT  
		Size: 74.2 MB (74236026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a515fe4de937795a187ed08ae562eb8e6a746bcc616cfd36a623ca759eaf93`  
		Last Modified: Mon, 02 Mar 2026 19:44:49 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f8f19422f5351dfbbfb0ca6ccb8eaa26debfde0118e7639fbabf0085f77733`  
		Last Modified: Mon, 02 Mar 2026 19:44:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:09f5f999d420a24e9e62e7879f400c0d57cb8c298299a990791d189e9fd8a5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14e91c6767791efa58216e5eac9c460af61f662701cf24e5b14cdf86d059df2`

```dockerfile
```

-	Layers:
	-	`sha256:c528aad99970499fa86723ce41a080286d9fdc30e6e1d927b62f2fba4aef732f`  
		Last Modified: Mon, 02 Mar 2026 19:44:48 GMT  
		Size: 7.4 MB (7414752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba70b57108ba7656f4d9879b1613f363873e9566aff7ac7b3e0e97ff04cc3349`  
		Last Modified: Mon, 02 Mar 2026 19:44:47 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json
