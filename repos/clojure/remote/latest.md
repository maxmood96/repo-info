## `clojure:latest`

```console
$ docker pull clojure@sha256:dbb0cb42e5d673bde85fc235a189cdd1dee5ee518a62486a9af38c11998d706b
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
$ docker pull clojure@sha256:b9dbc99ac4d36b8905c45bca5a7fd03fe91e0ea6b4c1a4b38681624d2cb117bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239911333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e125758412d4ca938fd5709f74ff66718d71888004ff89adc3451b707673c670`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:52:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:52:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:52:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:52:17 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:52:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:52:17 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:52:32 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:52:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:52:32 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:52:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:52:34 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:52:34 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:52:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:52:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:52:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:52:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:52:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b863b5ad647b112568d84df0559c2a1576ca14c43992df62a761840e70cacd13`  
		Last Modified: Tue, 04 Nov 2025 00:53:29 GMT  
		Size: 92.0 MB (92036011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de78d2a0ad76b04eac5187267c0d5be05f847e5631a16d8db3751f7a22b8ddf`  
		Last Modified: Tue, 04 Nov 2025 00:53:17 GMT  
		Size: 19.8 MB (19802935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfddcfaf7c9a31802c7acaff24edbdfb4d18f3f4cd26109b4bda89f8d4f526df`  
		Last Modified: Tue, 04 Nov 2025 00:53:15 GMT  
		Size: 4.5 MB (4517733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c195b40a43459b05e978ccf224d58bd36a5240ab2c104d151e3825c66f4712ff`  
		Last Modified: Tue, 04 Nov 2025 00:53:19 GMT  
		Size: 75.1 MB (75072524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7814557113cd87abb6fbb36fc9638de8dca2548c33aebc6503d8a07ad0ac32`  
		Last Modified: Tue, 04 Nov 2025 00:53:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67435b1d6ed26350c9aee2007411b36e5d655a3d41e54ed6b3dede80b3ac6754`  
		Last Modified: Tue, 04 Nov 2025 00:53:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:aa7fc97e4850807b8dee0a93b06fc218f49ee4b51cb4c34807ff1496cad24ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3847b3417314e3aa129b28d22d4ebe844b1bd5f7fcb2a58c535f43b3dab558d7`

```dockerfile
```

-	Layers:
	-	`sha256:14ef267f0c975dbcf4f2be117dca772c98b9950af6482ea3e52910c4846020b7`  
		Last Modified: Tue, 04 Nov 2025 10:34:30 GMT  
		Size: 7.4 MB (7418711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aefeced6d583bda6a3d6e89b765a53701df1a563265e1a688c84b6404fc7082`  
		Last Modified: Tue, 04 Nov 2025 10:34:30 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a9929b5dbbbf99fb597d33f0fc36ffea629d718e56e32612a7cf2dca1bd9abe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238681216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f949ce4d5c4120fe2fe01bf6b0f16f053516e6edf432bb5dddd312b5ccdfd1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:53:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:53:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:53:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:53:06 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:53:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:53:06 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:53:19 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:53:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:53:19 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:53:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:53:21 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:53:21 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:53:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:53:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:53:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:53:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:53:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f2b8b05f62addd665bcc947b91ff66f7b2ca9dacae57543ea548d284c1c11f`  
		Last Modified: Tue, 04 Nov 2025 00:54:13 GMT  
		Size: 91.0 MB (91045237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cb68816570efa15b42a65ad7a553c08935af4ef8e92b73d978992b74cc585e`  
		Last Modified: Tue, 04 Nov 2025 00:54:06 GMT  
		Size: 19.6 MB (19632171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9f8c995f38a0b647e17c288607300bda4376d8c5dbfe5b804eb1d316bc3179`  
		Last Modified: Tue, 04 Nov 2025 00:54:05 GMT  
		Size: 4.5 MB (4517727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3566591520d78d58c54dda5c4d6aa201cd77b209cb670bf47608801bbaae3b7`  
		Last Modified: Tue, 04 Nov 2025 00:54:12 GMT  
		Size: 75.1 MB (75125529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228aa9732656ca6cc2e03f1042d8ec150bb50931c9bd3ba8fc3bb1f678603052`  
		Last Modified: Tue, 04 Nov 2025 00:54:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d6ffa7a1b794ba12f5b4e1ca536a2d07fad3d24721ad57ea348665cbafadda`  
		Last Modified: Tue, 04 Nov 2025 00:54:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:eb49ff631e322267b607f67bd3316717a763181222c3113555461b3a7c3cf0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7450180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5565d8066954f56063755e4c27cd88f03b6b0b8e5d31ce7cdbebb77f11c331`

```dockerfile
```

-	Layers:
	-	`sha256:79ccd647c5c940b49cab0603a75e79ae9ffb760ab1d25d537937ba887c3a6227`  
		Last Modified: Tue, 04 Nov 2025 10:34:37 GMT  
		Size: 7.4 MB (7424447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acda216c132b5e50c9bc27c62859ec4c3bdb3c55873c3cb008494ec879762586`  
		Last Modified: Tue, 04 Nov 2025 10:34:38 GMT  
		Size: 25.7 KB (25733 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:c3178f74d61946498da10845e5f400455e68ba34c70d931d21cb7384a95a400e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249144553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f10cea7e8d0e7e9e4e0085a00fba558da6e81d21bc7fcbc4eff2ef019ec54a9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:57:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:57:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:57:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:57:05 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:57:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:57:06 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:57:38 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:57:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:57:38 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:57:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:57:41 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 01:03:09 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 01:03:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 01:03:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 01:03:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 01:03:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 01:03:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697fd59e7c3bbc197eda379a24912ae560eb9e07af558ef7f46c037d6dbf5da3`  
		Last Modified: Tue, 04 Nov 2025 00:58:43 GMT  
		Size: 91.6 MB (91601697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb44fbb0a692ca1c605ebf796a038a602f14dc4157e7bfce32f74812b4b98e90`  
		Last Modified: Tue, 04 Nov 2025 00:58:35 GMT  
		Size: 20.0 MB (20021708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48373f5d15d57d462c1a3df1d72fef37b255e79a80e3bcf4ee0328ff5b62f5cd`  
		Last Modified: Tue, 04 Nov 2025 00:58:33 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc5662eaa42e5da835a9bdf2c07850952ddd95a2903a6eb2e4027253c9ef601`  
		Last Modified: Tue, 04 Nov 2025 01:04:56 GMT  
		Size: 80.7 MB (80675088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d35eb76a0c3b2259e44f66ae18d15e551fad2f95bedc00e1a6a60093d149cd`  
		Last Modified: Tue, 04 Nov 2025 01:04:40 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50521674cae32d17e89117521e2b647fdbbf8c1150d9ec61b30fd00efadf7037`  
		Last Modified: Tue, 04 Nov 2025 01:04:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:ec94d0f0d808efe4c68fc860825afe2db15df68edda540e270328545114952af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7450061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8ff8bd3ccff68ce9e18e1ace6692a76dbe22213220cc8374c2027972c143be`

```dockerfile
```

-	Layers:
	-	`sha256:af41a377bca326021bac648ab8825e960ea42f2d60c6e26799cbc75c49e621c9`  
		Last Modified: Tue, 04 Nov 2025 10:34:44 GMT  
		Size: 7.4 MB (7425211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9990475e68bdd2fe927d1ab802542c894380534dd4a463d59c0532c7885fc1`  
		Last Modified: Tue, 04 Nov 2025 10:34:44 GMT  
		Size: 24.9 KB (24850 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:989aa7a81ba2ed9dafabc9a9e05b6121b5c3f7549faa3c3460819e7b210ffb9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233546149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac25be05e376fc42eea14a6b491dd718ccfb0d77ddc312d1d8fa9a6ae0d7c6cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 06:16:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 06:16:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 06:16:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 06:16:46 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 06:16:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 06:16:46 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 06:16:58 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 06:16:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 06:16:58 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 06:17:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 06:17:01 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 06:17:01 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 06:17:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 06:17:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 06:17:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 06:17:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 06:17:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44c022f304dd76bdc7608befad5bc0f9a88754ecb1970943a535e7f9c6a8b41`  
		Last Modified: Tue, 04 Nov 2025 06:18:05 GMT  
		Size: 88.2 MB (88206432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4797b699d0becca5ee1201eb2c1a06b6472748208b2348a5cc34af731bf2ae5`  
		Last Modified: Tue, 04 Nov 2025 06:17:59 GMT  
		Size: 19.5 MB (19460647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b04185c3db4a984d05b99a92d23a73c5e1e780e57aaacebc16c52fdc474f41`  
		Last Modified: Tue, 04 Nov 2025 06:17:58 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a304f6a0a0ca4b7e4732ea21a973f8bc4238abcc01598be68d94af5bf074ca`  
		Last Modified: Tue, 04 Nov 2025 06:18:04 GMT  
		Size: 74.2 MB (74222149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e3763fd19e0509a2473bc0262cfb7faf75b2de00b7f8b8de78aa65e59f734d`  
		Last Modified: Tue, 04 Nov 2025 06:17:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad53c8b14a49f3daaeba26fea4c16f63b696d505afbdfb32fd2de5c904991ba`  
		Last Modified: Tue, 04 Nov 2025 06:17:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:917401ab80c63b23788e80919c3938402c517d9a72488311d2b626ca933f310e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7438187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9160c781e2aa8b429a0ee0f7323f0690318bd5aa71830b0b1134f6138373f4`

```dockerfile
```

-	Layers:
	-	`sha256:d048f251b1910458d425ef2bcfcb410cb4ba28a64e59a416ac1cd2ba59e0162b`  
		Last Modified: Tue, 04 Nov 2025 10:34:51 GMT  
		Size: 7.4 MB (7412578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec28f1a8aae85fd70fcb1fdd90bf198e84ec7549936007506be2ce735f157c95`  
		Last Modified: Tue, 04 Nov 2025 10:34:52 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json
