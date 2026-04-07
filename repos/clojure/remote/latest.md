## `clojure:latest`

```console
$ docker pull clojure@sha256:a490f349853c4c8b063d9a1579cefebece7deac91e2a93e4d7c860f0df3e4b44
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
$ docker pull clojure@sha256:1b5cb32c44300fae18ce70f5edb9be95e6c5be74927b7eb3e7e7110254313271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240159234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a298f228576ddd8a3ba770ab3e59a0c01bc278cba27a0e9a7f4b41f786de5f7a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:12:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:12:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:12:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:12:10 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:12:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:12:10 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:12:25 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:12:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:12:25 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:12:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:12:27 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:12:27 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:12:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:12:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:12:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:12:41 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:12:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed0682163f50fda46ced4c550083e8c672962d36fb5f162439299fb2f898bf2`  
		Last Modified: Tue, 07 Apr 2026 03:13:05 GMT  
		Size: 92.3 MB (92256290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19176d15ba61db59b20073d16f1899d147bededff84effe4536f6910f7597ed1`  
		Last Modified: Tue, 07 Apr 2026 03:13:03 GMT  
		Size: 19.8 MB (19802873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b369d54afb21a23f7bd1d26f0835588ece786317db1413f77a19dc67c17a13f`  
		Last Modified: Tue, 07 Apr 2026 03:13:02 GMT  
		Size: 4.5 MB (4517726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983955cd285b7b990089eafdddb34ab2a78f1564af081cde4522e9d8749668dd`  
		Last Modified: Tue, 07 Apr 2026 03:13:05 GMT  
		Size: 75.1 MB (75092452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17808a4931b499a90fa22b3ad6a4b0e2bb80c31d738c9cbc6cef6d9044142fae`  
		Last Modified: Tue, 07 Apr 2026 03:13:03 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ca3b88a7a7c45cf6da4377d73fec97634c4a5555874f27a2aa8891eb3df62e`  
		Last Modified: Tue, 07 Apr 2026 03:13:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:9b056e22848249ccd8a755a95755729d87ac455ef4fbacdb75df51793ed7f911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7464480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2821821fb9bda579ad9920a184461f0ec7c6a776b7b2cfe93b6170145f1f5f49`

```dockerfile
```

-	Layers:
	-	`sha256:6b8d9dfbc1c55ea1ca05c55f8d473c49462801ed3322b5485e362daab60f1365`  
		Last Modified: Tue, 07 Apr 2026 03:13:02 GMT  
		Size: 7.4 MB (7438871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6cc9a623731a069e8ccd14986ddb9024fb2af76bcfb5559d8f40364d1301c55`  
		Last Modified: Tue, 07 Apr 2026 03:13:01 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:988d1d081aa2142e9fe38414149d40e81c799c0d5cf5f9e59780ca3ff6c35b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.1 MB (239064336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0226664d9719a05e7fda4c10076375a808f02d1e363b9a339a3a59cb370d19`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:22:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:22:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:22:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:22:37 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:22:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:22:37 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:22:51 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:22:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:22:51 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:22:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:22:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:22:53 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:23:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:23:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:23:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:23:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:23:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3140cdfa9f00aacb0f104b2f538157e423b5d9e1a2f3f14a8b7cd112846fc619`  
		Last Modified: Tue, 07 Apr 2026 03:23:30 GMT  
		Size: 91.3 MB (91288284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58e46510bd2190b4805ea90d0b1fec7a68e51b5e34abc2414c368f6c7ad2fab`  
		Last Modified: Tue, 07 Apr 2026 03:23:27 GMT  
		Size: 19.6 MB (19632815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8f1a6f02991741551033ad1372cd2cd8f1ed6523a2b834b0d4a8e267196178`  
		Last Modified: Tue, 07 Apr 2026 03:23:26 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e98efa929ff69272b4e41aed54d8cc99c7df74f0549977b29410d48f994653`  
		Last Modified: Tue, 07 Apr 2026 03:23:29 GMT  
		Size: 75.3 MB (75251159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd4040acab0e98ccc287a8a2cd0604e43e4463424690f9394e37fbdb92aeb1c`  
		Last Modified: Tue, 07 Apr 2026 03:23:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d4ac38bd87a8c5a50f376e9757e92227d627fc70b6397309776c88c0438604`  
		Last Modified: Tue, 07 Apr 2026 03:23:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:7f38d822680c6d533dd88445a77eeaeaed304a1420c5651046d6e978d7892ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7470340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60ee11a97a6a4d0b18000feaf95373bf87170e2ccaa825a9a8f654aaf3eecf1`

```dockerfile
```

-	Layers:
	-	`sha256:bb3415d20506d097a2d34823fd5b5051f1a6e9f7791741a8562deb27113fbe70`  
		Last Modified: Tue, 07 Apr 2026 03:23:26 GMT  
		Size: 7.4 MB (7444607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56d904716515b46c21ce37d7751099a9edbd3b3d37c7fe2fb3542c2b77f7be06`  
		Last Modified: Tue, 07 Apr 2026 03:23:26 GMT  
		Size: 25.7 KB (25733 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:3dc1149cd531bcee140e0481dc84981337c1e067790bc717b116bf27b2fa45b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249204542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4dd1b7fe616a63c2804832cbaa7efbad6d89d815f81bd7fb1cb9a175ac86b5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:03:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:03:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:03:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:03:56 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 18:03:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 18:03:56 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:04:37 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:04:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:04:37 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:04:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:04:42 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:04:43 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:05:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:05:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:05:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:05:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:05:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81438db6b066b5319caf43fdad1d2cd4324d06132f04193db065dad00c8bc101`  
		Last Modified: Tue, 17 Mar 2026 18:06:02 GMT  
		Size: 91.6 MB (91632940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbb7e0a4408fd05d90beb04f1c7387137fa2b4b6a0805400ed94ee63a9d2443`  
		Last Modified: Tue, 17 Mar 2026 18:05:59 GMT  
		Size: 20.0 MB (20023636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b66ec7b7df251db8f61f857203f7844ef8845574dabd5a355949632b6471a1e`  
		Last Modified: Tue, 17 Mar 2026 18:05:59 GMT  
		Size: 4.5 MB (4517770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82560bcc901bde788c59d0f7eeacfe913341fbaa9728407ba72e324423d89e21`  
		Last Modified: Tue, 17 Mar 2026 18:06:02 GMT  
		Size: 80.7 MB (80692425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6f5619d5361a5bcdcb6e04019fe6055b1ee7fba326558da335e41665c33e0b`  
		Last Modified: Tue, 17 Mar 2026 18:06:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423db4ea0e47c103137b8270f07abb64be86a3aec23c4aaa073022e882f01dc6`  
		Last Modified: Tue, 17 Mar 2026 18:06:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:95384fb966e2d178d9c3e81d2a89056ef18517ef3d79301d415a77085e809819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7453036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7730563cc2db0d699d9db51294410fcbc40b175c9707aff507a76a3dbb76e999`

```dockerfile
```

-	Layers:
	-	`sha256:56a6039eb1bee5fedef0e9d17f7b53d44ff6018c85918704636020e4daf7dd92`  
		Last Modified: Tue, 17 Mar 2026 18:05:59 GMT  
		Size: 7.4 MB (7427387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79baab9554108b25f01bcce1eeb6717b9e04fe6d29d15e59540d8cc2d132a72b`  
		Last Modified: Tue, 17 Mar 2026 18:05:58 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:4dccc51c20ee4aa398f3d7d9fc3ed0eb3e64e0be725e241bf53b7a4f01ce4c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233604112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd3e19a010e3c24c52c1d0ea9efec77d01d796cb3f08518daff77d81486024f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:38:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:38:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:38:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:38:40 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:38:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:38:40 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:38:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:38:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:38:53 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:38:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:38:55 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:38:55 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:39:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:39:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:39:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:39:10 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:39:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6336049cfea2fb1bf6fe937dfa06a3231de1bcd109cc0d07cc3ba41fd378402`  
		Last Modified: Tue, 07 Apr 2026 05:39:45 GMT  
		Size: 88.2 MB (88233804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94d5138627d9e4edb404122d05597758714dcab9e5b88c41aa2fe814dd04b85`  
		Last Modified: Tue, 07 Apr 2026 05:39:43 GMT  
		Size: 19.5 MB (19463188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c53efa365a3be02bd634a88ae7bd02b5fa2c28b559bb0375684b4319d37eee`  
		Last Modified: Tue, 07 Apr 2026 05:39:42 GMT  
		Size: 4.5 MB (4517767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c456d4ed2ec54f96c3d0cd237ea0b80ed506473ab401ceac52df17b6f0f0ddf`  
		Last Modified: Tue, 07 Apr 2026 05:39:44 GMT  
		Size: 74.2 MB (74240196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c1e5f3316ea9115c2044c158f2b54dfd8f28a64ef67f31a126fcfbdd8c7e17`  
		Last Modified: Tue, 07 Apr 2026 05:39:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a10e0b45d2481e664842c884b5d201b92c872ea558129e2d51cf46455a5440`  
		Last Modified: Tue, 07 Apr 2026 05:39:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:c2656a443c368f25f8521972d912a5042d213d106c7ce205062e6746a1aead7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fc130df90d32e738677d27b890ec146393fc86d11bed88fec065e74b955d7f`

```dockerfile
```

-	Layers:
	-	`sha256:6a1b7d8302c161ff6fa9d30c6822d7205c0cdf8f61b2b1c2eea5805f495409e6`  
		Last Modified: Tue, 07 Apr 2026 05:39:43 GMT  
		Size: 7.4 MB (7414752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e49ef8a17ad5ae1a9372dc248726feaf775b5584aaf2c6c373d3e6918091051`  
		Last Modified: Tue, 07 Apr 2026 05:39:42 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json
