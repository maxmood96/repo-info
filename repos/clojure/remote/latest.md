## `clojure:latest`

```console
$ docker pull clojure@sha256:0af30a4292ee89de3166551c298c0bf8daa4a5c2368d105dc748cd4f3ea0c461
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
$ docker pull clojure@sha256:9e66a680b7dbeab490a2c8503f96c91fdcbbd055aa82bd8ce267cb39a358f9b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237443814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd59e86cbb99c7a835106b5ac72aac5a150f1bb55ccb87634cc07293b8a5ca80`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:40:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:40:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:40:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:40:10 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 04 Jun 2026 17:40:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 04 Jun 2026 17:40:10 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:40:26 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 04 Jun 2026 17:40:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 04 Jun 2026 17:40:26 GMT
ENV LEIN_ROOT=1
# Thu, 04 Jun 2026 17:40:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 04 Jun 2026 17:40:28 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:40:28 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:40:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:40:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:40:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:40:43 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:40:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1822e6fd6c4ec6fe4656df66e41d36b4c1bd3537c94de68ad84e75793f5098`  
		Last Modified: Thu, 04 Jun 2026 17:41:07 GMT  
		Size: 92.6 MB (92574588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfae3a82caa8acf96c54c85768353c92fd84f295fed09ec01879c6b4b009b4a5`  
		Last Modified: Thu, 04 Jun 2026 17:41:04 GMT  
		Size: 19.8 MB (19811759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7574cfb39ce567198d8e3b6ccf4697e9042db16410e5ae55abcaaa4e72913a62`  
		Last Modified: Thu, 04 Jun 2026 17:41:03 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a72dbbee5b6e79a8a0285ffae2abf2629d6010af4356f99315fab635a7363b5`  
		Last Modified: Thu, 04 Jun 2026 17:41:07 GMT  
		Size: 72.0 MB (72043211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bd7113461c1d93612bb27872f122f6a389224f570340267a6cefd0eea7ff5d`  
		Last Modified: Thu, 04 Jun 2026 17:41:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d6e872a26750fede0c7da98dc0d26c525d3945306030856ec9bb8a4f9161f1`  
		Last Modified: Thu, 04 Jun 2026 17:41:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:5c0afb8c47c917f75955d5483a09527c51410f7d96b42cd83dd13b2832f6c904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7461884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1572395544e859e2f3bb64be9a399d6fdcc3047538af1cc6f57dc3e6fa4e27e8`

```dockerfile
```

-	Layers:
	-	`sha256:3ccc990f71fc71c05476343aa11d04baff51efdfa0461adb611cca4e8c7f0a51`  
		Last Modified: Thu, 04 Jun 2026 17:41:03 GMT  
		Size: 7.4 MB (7436121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd388534d44db2d099bfe57180fa4aa8c72d8e57d0f4f84f943efa33747600d0`  
		Last Modified: Thu, 04 Jun 2026 17:41:03 GMT  
		Size: 25.8 KB (25763 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:41a8fa3089197213526b96a6bb3bfe958148f3ea8a761ba88b77a63364f74bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236280422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2a4bae6e8af6dd71859387c88c0e1d09c40aeb51bbbe3230c4412f07961444`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:39:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:39:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:39:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:39:35 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 04 Jun 2026 17:39:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 04 Jun 2026 17:39:35 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:39:49 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 04 Jun 2026 17:39:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 04 Jun 2026 17:39:49 GMT
ENV LEIN_ROOT=1
# Thu, 04 Jun 2026 17:39:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 04 Jun 2026 17:39:50 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:39:50 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:40:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:40:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:40:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:40:03 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:40:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0abdea9e676a846e8fb0789d3b41c9789f2eb42b1dc72c1cf09f19869723475`  
		Last Modified: Thu, 04 Jun 2026 17:40:26 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723e40d610b5f339ef18b5879a61d07ace9399e4b77fb4e57b09549b079a9167`  
		Last Modified: Thu, 04 Jun 2026 17:40:24 GMT  
		Size: 19.6 MB (19641905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd98b9e2df60543a856461d0fcf1d3920d646f5cf5fcc62145012e8f7773155`  
		Last Modified: Thu, 04 Jun 2026 17:40:23 GMT  
		Size: 4.5 MB (4517709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d58bbd91952ab04d80160e87b18e85bb0aa0533ece7ebff500ba75066a7b6fe`  
		Last Modified: Thu, 04 Jun 2026 17:40:26 GMT  
		Size: 72.2 MB (72198049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4d794799ca77c83702e6c81bec90fcdb5c9800c4a82cff727305d088e9428d`  
		Last Modified: Thu, 04 Jun 2026 17:40:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7474b0f52e37935423df48a951992cc1446fb3b6e4d84d044be16970eaa063`  
		Last Modified: Thu, 04 Jun 2026 17:40:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:75de91bda425672c1c74ae7d41d578d9a35f7b64d0bde47b1ecc422b34ceb6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7467744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23a520c25696181a974523c694ede0794b07af46557ec42fb2466937b08cc69`

```dockerfile
```

-	Layers:
	-	`sha256:c13f4701db75413e20fadacbf3be51fae797e9ad5587d23b078dbe8121f97d7d`  
		Last Modified: Thu, 04 Jun 2026 17:40:23 GMT  
		Size: 7.4 MB (7441857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a9d0f58768a41fca66c126b3a417a8ba47ddc3b8da738139c6915c347749ca1`  
		Last Modified: Thu, 04 Jun 2026 17:40:22 GMT  
		Size: 25.9 KB (25887 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:36bdf29bf63b2e29881143158cb363799e00a4211d7abfeb621c16ad8b2a2469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246438281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b99a76623dc33a6f05143ad8fee36f7b7479e01f512a943110143f5ed647ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:40:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:40:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:40:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:40:22 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 04 Jun 2026 17:40:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 04 Jun 2026 17:40:22 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:40:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 04 Jun 2026 17:40:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 04 Jun 2026 17:40:59 GMT
ENV LEIN_ROOT=1
# Thu, 04 Jun 2026 17:41:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 04 Jun 2026 17:41:05 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:41:05 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:41:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:41:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:41:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:41:44 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:41:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765ad15186d8d84e420a575b6c5b5cc83f858814242800a49d0e2c53649e1ea9`  
		Last Modified: Thu, 04 Jun 2026 17:42:36 GMT  
		Size: 91.9 MB (91914009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21ebf98c2ba711c27f5d745a1b3fde21ceed991f50d35170b70b562d32e0e8d`  
		Last Modified: Thu, 04 Jun 2026 17:42:33 GMT  
		Size: 20.0 MB (20033244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc7da96e1e2f20a8d848a19deb828f6c4bbecbe56d03356aa2a17a7bae8e1c3`  
		Last Modified: Thu, 04 Jun 2026 17:42:32 GMT  
		Size: 4.5 MB (4517794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b59f5a8d7dd9ae80ccaddb30732be20871c98fa2b87630cb48c6a0f2862f0ce`  
		Last Modified: Thu, 04 Jun 2026 17:42:36 GMT  
		Size: 77.6 MB (77631962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c78137d95ec7ce6ece538afa155b8635b45d1682abc89c5164f77870351127d`  
		Last Modified: Thu, 04 Jun 2026 17:42:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bdba9dd382a09c0873d84f0843473a1d4cd4eaec46cfd20e1f242c7342f98a`  
		Last Modified: Thu, 04 Jun 2026 17:42:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:9095af26a824cbbffd6fec5f94a502082c1c04d1644149ae338edd3b57b590eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7450440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a1a7c6ee446f2ab1b88873596c52b01eeaa2daafb9583eb0dad0a54d8880d4d`

```dockerfile
```

-	Layers:
	-	`sha256:61362994a03893af9f5f270c53a0af094c519baa2e4f1b50e8a00b894ffc47c2`  
		Last Modified: Thu, 04 Jun 2026 17:42:32 GMT  
		Size: 7.4 MB (7424637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:957f4f7dcc8ffb82e03f079aa922b68fceef6a1bae697d371ef10b5187c489b3`  
		Last Modified: Thu, 04 Jun 2026 17:42:31 GMT  
		Size: 25.8 KB (25803 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:166fb84177e3cf5f7765df5ed3bb766f8f74b93a84dbba892cff4ce3b7633f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230735816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2313221ba51c834e4c7844db265b4233177fe3ef896a69234bad694c6e524c6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:40:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:40:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:40:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:40:07 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 04 Jun 2026 17:40:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 04 Jun 2026 17:40:07 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:40:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 04 Jun 2026 17:40:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 04 Jun 2026 17:40:20 GMT
ENV LEIN_ROOT=1
# Thu, 04 Jun 2026 17:40:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 04 Jun 2026 17:40:22 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:40:22 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:40:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:40:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:40:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:40:36 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:40:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e796c4b6ad9611e7823f643a0d59c67532ff002815e1c2d0d1aaef4b08db356c`  
		Last Modified: Thu, 04 Jun 2026 17:41:08 GMT  
		Size: 88.4 MB (88420336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9861681d8d029bab4ef384bd751941f74217920082a4a3fe3d859195bd71405`  
		Last Modified: Thu, 04 Jun 2026 17:41:06 GMT  
		Size: 19.5 MB (19473871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527b0b358c8ea701b485df00367ca3927d788c3bc7f94e0cd240d00fda637b5a`  
		Last Modified: Thu, 04 Jun 2026 17:41:05 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95268e07498a705b61bf240798259b5494dd1b7bb3a0a9472f1f43da56e2146b`  
		Last Modified: Thu, 04 Jun 2026 17:41:08 GMT  
		Size: 71.2 MB (71167199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c7a48289d488d06d2c300377cf91ea163332802f0cbc2f10a648643559538a`  
		Last Modified: Thu, 04 Jun 2026 17:41:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e6495b6f3aca6bad8caed95188ea95a6c5326ce6d762f6b68a414beb086e3d`  
		Last Modified: Thu, 04 Jun 2026 17:41:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:032f1f4bf53e54c73ea1eed8eff5127e815417e277065167238869d78064e6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7437765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746bea2779e76e6eaaa92d09bb49848e3f32481a29c05b07633540e765f6893d`

```dockerfile
```

-	Layers:
	-	`sha256:f5ca8cfc27645f9c907146ff7ce8d21bbc4331fc141ae97a5008f6672f908288`  
		Last Modified: Thu, 04 Jun 2026 17:41:05 GMT  
		Size: 7.4 MB (7412002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff4157c407c58b2cb119477f61acf8827fe07191272ca8f0381df86a622cf538`  
		Last Modified: Thu, 04 Jun 2026 17:41:05 GMT  
		Size: 25.8 KB (25763 bytes)  
		MIME: application/vnd.in-toto+json
