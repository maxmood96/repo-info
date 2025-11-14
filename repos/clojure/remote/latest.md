## `clojure:latest`

```console
$ docker pull clojure@sha256:a1449b4704bf342b69d0d6a0be1f682e9fb2031fd06c7554e1db1fd0425d6cb0
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
$ docker pull clojure@sha256:d43c8ea846f0986850391b7582c20ab9136af4ec06a979300a23bd624217275f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239920757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b92b30bf082f932019eea2a935d63f38073d16be1f9383ca4f3b8405c51e6f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:48:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:48:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:48:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:48:49 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:48:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:48:49 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:49:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:49:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:49:03 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:49:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:49:05 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:49:05 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:49:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:49:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:49:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:49:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:49:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6488beed083eb778acbc007024c46fe3c42a63868b4a71c096885c0de8360f1d`  
		Last Modified: Fri, 14 Nov 2025 00:49:54 GMT  
		Size: 92.0 MB (92045316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee800bcdd93685e37799c44f131fa824a3ed88b7d25ffe36f1092643fde9e5`  
		Last Modified: Fri, 14 Nov 2025 00:49:50 GMT  
		Size: 19.8 MB (19803016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bf7b6e2fbcb27051e8109502161a286503b39b684205b6bce8c9acfee25387`  
		Last Modified: Fri, 14 Nov 2025 00:49:48 GMT  
		Size: 4.5 MB (4517731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68d3b7e73d32f67a340352a7b488a3ff580f4443ff65442b35df07b04cc1288`  
		Last Modified: Fri, 14 Nov 2025 00:50:17 GMT  
		Size: 75.1 MB (75072560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd6427c47f54a925d2eca8e7979c9bae3680410966ba04360bcf54f8729ebab`  
		Last Modified: Fri, 14 Nov 2025 00:49:48 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea708928b230f69abbb21da3637cd6c28af2bc5bc332fcf61970fa0b5ff0381f`  
		Last Modified: Fri, 14 Nov 2025 00:49:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:dd89c72a64da08bde9ca4e1df513638e3ce1bbd2e9277c37d6b75f4f2ea24628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a3e81a6af010f62483ca127936e7a062a0798fef1c84e8737e26268c695ad0`

```dockerfile
```

-	Layers:
	-	`sha256:fc2300cf9bab44d87062cf5716aa4da46a5b540835c395b9877f75c20969b89f`  
		Last Modified: Fri, 14 Nov 2025 04:34:29 GMT  
		Size: 7.4 MB (7418725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8111adec4d213cae17ae63536eec99e6f9ca98f768f1d09e42f37342990397`  
		Last Modified: Fri, 14 Nov 2025 04:34:30 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:630b0de4856a1d40b9011924b44192b407785ecfb4db3d9b4c3c5d2b8eb10ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238688645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c3b053c75f93a200a933530add3c9b054cc36faddf07a4be6425d227f5636e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:50:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:50:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:50:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:50:31 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:50:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:50:31 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:50:45 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:50:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:50:45 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:50:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:50:47 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:50:47 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:51:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:51:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:51:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:51:00 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:51:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b832d4eba873c3cdb88b8f675998ea4a99675740d1053eabe6cd5779ff75ff85`  
		Last Modified: Fri, 14 Nov 2025 00:51:43 GMT  
		Size: 91.1 MB (91052531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fadc805dca28d6847fea2d5dcd631649a88b16243d52d6c87e19f8769ebe66b`  
		Last Modified: Fri, 14 Nov 2025 00:51:35 GMT  
		Size: 19.6 MB (19632239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc81d00504660c462146e28257e7541bfd276a935fb3ee98c541a751178cb43`  
		Last Modified: Fri, 14 Nov 2025 00:51:33 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8e88ffb93ac7d5cf5b62ab42e5ae174b2c82aec8fcf3e1c370ab9d8e8b55e7`  
		Last Modified: Fri, 14 Nov 2025 00:51:39 GMT  
		Size: 75.1 MB (75125577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c73dddd6fe29fc88d01e89e057b6ae66d08a43fc688e0c2bb8b1b3c9d0192f`  
		Last Modified: Fri, 14 Nov 2025 00:51:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae543c11896e8aa10d8e1a590c4d8be405d2683f7b5ce7a72d01877f7ffe688b`  
		Last Modified: Fri, 14 Nov 2025 00:51:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:047ee3c0442419dcfefdfe39144eae0b9dfde6a99e73806cc7b21aba2d6664aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7450194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197584fb2a36bd22e7129c517cfae3473812e4bfb2f31a97eb4d442f7e4fb183`

```dockerfile
```

-	Layers:
	-	`sha256:af599e1174a90a7c2e18f5512ed20500087f53ee768569fe30fb629895ba433c`  
		Last Modified: Fri, 14 Nov 2025 04:34:36 GMT  
		Size: 7.4 MB (7424461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cb4483047ebfe9cb79034a25fe3293000b4cbf570e1ff3d519e6aee232b85a7`  
		Last Modified: Fri, 14 Nov 2025 04:34:37 GMT  
		Size: 25.7 KB (25733 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:2238438ac6effe47f84a479baa05c2d39e715a6f1b3c6aeb0f5fda17ff70692b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249153861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2415addab03c14a12c60a5cd4dd701da78f1dc76cb0c58bae06ac7dd0c7dff7e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 06:21:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 06:21:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 06:21:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 06:21:26 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 06:21:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 06:21:26 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 06:21:50 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 06:21:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 06:21:50 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 06:21:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 06:21:55 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 06:21:55 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 06:22:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 06:22:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 06:22:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 06:22:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 06:22:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b82b3e70d58ebb4cb7d9c4cd081419d84bca24a84c5775b7d96f1c00b8d2786`  
		Last Modified: Fri, 14 Nov 2025 06:23:31 GMT  
		Size: 91.6 MB (91610755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45e5a2b942e3451e07921dd20937eaf5215e9085d38b1786938333d5dbecd0`  
		Last Modified: Fri, 14 Nov 2025 06:23:24 GMT  
		Size: 20.0 MB (20021751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2370059ad317e23d03895665cc5590d048346b24489188d84fc0c1d4b48472`  
		Last Modified: Fri, 14 Nov 2025 06:23:22 GMT  
		Size: 4.5 MB (4517765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da72bc78cd688af1210529e0214f723d0925fb5253988d16e84437b3c110c006`  
		Last Modified: Fri, 14 Nov 2025 06:23:28 GMT  
		Size: 80.7 MB (80675234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9025d86a8c0d1fb6ad4f065a9fdcc8119ae41cc37dabe48b435cfacd1cf19f7`  
		Last Modified: Fri, 14 Nov 2025 06:23:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a404ed41d4f504fb6ae2a1aa7f6301437ce25e35c124bf75e9dfa6febabeb49`  
		Last Modified: Fri, 14 Nov 2025 06:23:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:e49aec1f756e4df0de88a01b8fd9de1492f147cd152ee5e5778d52889c8437fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7450874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b29f5a335e4e31e72c436d50e69f9c1cc54086605411c006146a193c3bef38`

```dockerfile
```

-	Layers:
	-	`sha256:7201a65f57e8b1e9e03433e7a825037ec2c49d104e55d0a7b6e1fd24744012bd`  
		Last Modified: Fri, 14 Nov 2025 07:34:38 GMT  
		Size: 7.4 MB (7425225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcea9a069907e51dd05370f00b8a9c7f616a012e077c32e516f46d561fc79531`  
		Last Modified: Fri, 14 Nov 2025 07:34:38 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:755b3ace72897fe0ce47ec2dc9c451115106d25b7353521afc59b88bcc7e2e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233550635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053b29eeeb50f2baf45735dad3d37cc99e590ccdcb44812a6ad6b455c90e2e29`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:50:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:50:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:50:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:50:44 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:50:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:50:44 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:50:58 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:50:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:50:58 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:51:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:51:01 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:51:01 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:51:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:51:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:51:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:51:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:51:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ef362c972377511f4db0a194b82aa6385c02a2dad43ae7599f19d9205a09ba`  
		Last Modified: Fri, 14 Nov 2025 00:52:04 GMT  
		Size: 88.2 MB (88210700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07751f439dd96701c71eddb47a82e1bda8e7d0ccbaef651ab3e775724b7ebb1`  
		Last Modified: Fri, 14 Nov 2025 00:51:55 GMT  
		Size: 19.5 MB (19460721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcbb5c9e42855973c5112f1e98737135205ccd6d8b2d1c89249cec53c351adb`  
		Last Modified: Fri, 14 Nov 2025 00:51:53 GMT  
		Size: 4.5 MB (4517763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605141f28a017a06386c1b949a5ad74b11f5700b196ff601eea97587941f1d1b`  
		Last Modified: Fri, 14 Nov 2025 00:52:01 GMT  
		Size: 74.2 MB (74222281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdd5285c5200e6ddf21f8a7afdc678ebf9a3ae08903da0c260b4f8f1ace3b44`  
		Last Modified: Fri, 14 Nov 2025 00:51:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846d84a71d58ef966155be9a7b83288fce9a0ad81e14939e5bd85c90d48342e7`  
		Last Modified: Fri, 14 Nov 2025 00:51:54 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:2e1a1bcda95a78ddb2db591195f8aa3c3c3cb6a0f17ed855b1c06e95eeb7510c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7438201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1524bc15364c885c7446d1106f1b0bef9f52927d208e27b62dae6f5c7fc6c64e`

```dockerfile
```

-	Layers:
	-	`sha256:8d7a89373c143750ff84e499590725cd1f057297d1ac698b18d9b7748a415d69`  
		Last Modified: Fri, 14 Nov 2025 01:34:52 GMT  
		Size: 7.4 MB (7412592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:960b78355691550675b3843605dad8bccc163c2a0c92b67ae378c75dd7664cdc`  
		Last Modified: Fri, 14 Nov 2025 01:34:53 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json
