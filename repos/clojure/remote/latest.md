## `clojure:latest`

```console
$ docker pull clojure@sha256:846413d573f9a1f50332e80cd821ad2553a85a8b2fda1a6fe6a2e99e38257109
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
$ docker pull clojure@sha256:1311410ceb15c9407909afbe3bdd2cea608dfa9ac75f15ffe8ff55d5ed0a2ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240138677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e054c5cc2bd66f9db32e905f81d41dd13e23e028cd289e930f9ea7e3e53b2ac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:51:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:51:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:51:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:30 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:51:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:51:30 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:51:45 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:51:45 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:51:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:51:46 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:51:46 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:51:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:51:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:51:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:51:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:51:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b243ccd64ab5ae9cf4ea98077e734ff90b8211d1b958d7a955641e74c1efaa`  
		Last Modified: Tue, 24 Feb 2026 19:52:22 GMT  
		Size: 92.3 MB (92256298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6e1b8714527447eb40cab774302b28007907a06911e8a979def0ca55e49e33`  
		Last Modified: Tue, 24 Feb 2026 19:52:20 GMT  
		Size: 19.8 MB (19802872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003d465b82b895ccbf8307e59563c6ba026f2db80017982334dffe0131239599`  
		Last Modified: Tue, 24 Feb 2026 19:52:19 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357ddd06b3b35433007ee0d028688cf62c469e49929de245348324cddb2b6646`  
		Last Modified: Tue, 24 Feb 2026 19:52:22 GMT  
		Size: 75.1 MB (75071939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83224d623b113bb792fb79e772efe1880e489bfea50ef765e6542553a0715a0f`  
		Last Modified: Tue, 24 Feb 2026 19:52:20 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02be34cba278f06e473ecfa9e63616332cc0a374544fd6cd8d24d89eeb1e9483`  
		Last Modified: Tue, 24 Feb 2026 19:52:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:28f0571e445d124a5f377f5dec81cedd9d68d3c86da536e87d939df682791b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7462967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a855fb8ea849531c6968460fee6496481fc6968e954fdb3acdd7dfbef3231f9`

```dockerfile
```

-	Layers:
	-	`sha256:60077cad45f9796a62f65bf0862448744ee0faf6c25c9be07de2aa87679ac04e`  
		Last Modified: Tue, 24 Feb 2026 19:52:19 GMT  
		Size: 7.4 MB (7437358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb2a3df4a7ccb86c3ab9eb2aee975a1d622a02d67020aeb2d092cf0a44dadeb6`  
		Last Modified: Tue, 24 Feb 2026 19:52:19 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:234bdb79e1aba1171599cf203b10c1f04d6d477852347652afad66e054a37c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (239044036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a161d62902f78ce77c8b52ab323a077f07fe503c1de220485b778a67110ff0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:02:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:24 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:02:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:02:24 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:02:37 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:02:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:02:37 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:02:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:02:39 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:02:39 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:02:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:02:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:02:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:02:53 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:02:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c81c80c7b69e4e786d3000ed02b7684f04659ca1951d1bf428f7793956815d`  
		Last Modified: Tue, 24 Feb 2026 20:03:20 GMT  
		Size: 91.3 MB (91288274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06027e063deddd360e2454899283d28172c5dc76947b9cbb5aa3f92e52f9eb4b`  
		Last Modified: Tue, 24 Feb 2026 20:03:13 GMT  
		Size: 19.6 MB (19632820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9740ac5ee9b58e9ca0a312faac69747852b41a606210764b888ad8486e64166`  
		Last Modified: Tue, 24 Feb 2026 20:03:12 GMT  
		Size: 4.5 MB (4517707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f484028b20dadd77d6fca4887a29c294539e6aaf5442d9ec547501bf8e5a6a6`  
		Last Modified: Tue, 24 Feb 2026 20:03:15 GMT  
		Size: 75.2 MB (75230956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b95c2fa36c514de3a0228d48bd41ce30aea5f1a4f266f1fea6a8e9f8ba98fd`  
		Last Modified: Tue, 24 Feb 2026 20:03:14 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401c5e4ae3b1b04596e1ac0e6f46a2f2fe75274af5a1f8f98b0ed796d87c7246`  
		Last Modified: Tue, 24 Feb 2026 20:03:15 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:0281c946880905c82e263bd2bd4e7f244aa3dbab80dd2257e2689d0145d576d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7468827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a585cacf33664ff94ed1e2bdb1abc16dff1453b7f644a78355f08747a827f7`

```dockerfile
```

-	Layers:
	-	`sha256:741ed8409ba1b1c1bcfa47a89268854d43f9ef8900bd7101d5f72bfab35d2577`  
		Last Modified: Tue, 24 Feb 2026 20:03:13 GMT  
		Size: 7.4 MB (7443094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc27ee149b8cfcb097f5f80812d2c213fb285cf0b3c0a6906a4d7dacfd92dccf`  
		Last Modified: Tue, 24 Feb 2026 20:03:12 GMT  
		Size: 25.7 KB (25733 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:98298c3387f883eaf2aa877e7b137eefaf3f56fda14fa4ee80d94d4220a7ff3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249186852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9cdf44324bfc5a977a41744655a4f6d65a74b6bda5d2f442a3fc0adef425d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 01:40:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:40:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:40:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:40:44 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 01:40:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 01:40:44 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:41:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 01:41:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 01:41:24 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 01:41:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 01:41:30 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 25 Feb 2026 01:41:30 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:42:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 25 Feb 2026 01:42:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 25 Feb 2026 01:42:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 01:42:14 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 01:42:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bab868bc9e6457cefbe0a5145acf421b2bdda0c0ceaa18c23cdb26dd06a94f2`  
		Last Modified: Wed, 25 Feb 2026 01:43:08 GMT  
		Size: 91.6 MB (91633010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2c130e1abc8f2d79fcc9209acb23596aaa4495d6ccc0b5a262c9f6bc0330ab`  
		Last Modified: Wed, 25 Feb 2026 01:43:05 GMT  
		Size: 20.0 MB (20023809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc95acb35de425f9b852c4f09629a64667b1c0300f5fe50f2f1f9be19798d51`  
		Last Modified: Wed, 25 Feb 2026 01:43:04 GMT  
		Size: 4.5 MB (4517785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9deb235185fa1a50a03f8cc58c1ccc01fbff79b54b5423ba39e9f3b0572aa558`  
		Last Modified: Wed, 25 Feb 2026 01:43:08 GMT  
		Size: 80.7 MB (80674375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395cd63f61633a5d36943016d15e4214b23d141907deef3338945ebe31e4d75a`  
		Last Modified: Wed, 25 Feb 2026 01:43:06 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7749783676ab28246db8513fba10ab87f406d380aeec85acef59c15ca96d359`  
		Last Modified: Wed, 25 Feb 2026 01:43:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:f9160092a4001e52306df3bbc049386246d3ac308d72e4f5c87cb17efd507579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7451522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c84ad0ce0c7737767426d2495125015828195be3152caecffb546d541135da`

```dockerfile
```

-	Layers:
	-	`sha256:e163903e9bd460a68e468f6f4c825ee4bade09033ae9b2fc0cc298b458ade273`  
		Last Modified: Wed, 25 Feb 2026 01:43:04 GMT  
		Size: 7.4 MB (7425874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667ceebd4aea53daff1fdde5d275f21b0344f172276cf5ca8b4c8313eb1b5279`  
		Last Modified: Wed, 25 Feb 2026 01:43:04 GMT  
		Size: 25.6 KB (25648 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:bd633d902f36699a40909056e04bec276e59cf8f5a2a9c0e97a1ff3dc966bb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233586396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c1c7ece5e0c00ead3988016a12fc6442e7a6450c9649bd0fd847dbf5663f56`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:10:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:10:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:10:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:10:52 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:10:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:10:53 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:11:25 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:11:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:11:25 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:11:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:11:28 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 23:11:28 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:12:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 23:12:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 23:12:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:12:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:12:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c28559b6f839a4c3bdfa9b4d00de6634a58ae89f9e73ea669e7ab540eb19fc`  
		Last Modified: Tue, 24 Feb 2026 23:12:46 GMT  
		Size: 88.2 MB (88233823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f91a8763e96bf88ea33864cf8a0c8ff7dc012566ae1dd9639ad237ca687e7f`  
		Last Modified: Tue, 24 Feb 2026 23:12:44 GMT  
		Size: 19.5 MB (19463239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd091f76797fb04b2f52970cce087c9306e8e5303e718d494bc9c350d7c3ae1d`  
		Last Modified: Tue, 24 Feb 2026 23:12:43 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bd240a5e19ad75c8a252242e750b6c34da169f1daaeaf0529e699db4c61ff9`  
		Last Modified: Tue, 24 Feb 2026 23:12:46 GMT  
		Size: 74.2 MB (74222418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0116fa80b008e1727d60c2e9a39b7d75c9a063461491d12ca22c1d8556bdc1`  
		Last Modified: Tue, 24 Feb 2026 23:12:45 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa8e96f7b7e71d749a6be361d89e4c19a8df95685a3d407d1c85eff02039e2`  
		Last Modified: Tue, 24 Feb 2026 23:12:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:c0fd673945ce71e89c92549be75a444143c5b1effc56d5076e8e4e0e4e449f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7438848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02d38d3d91c26445a9ddea6a47cae608357f321e2e32a3e12bfec77e7939804`

```dockerfile
```

-	Layers:
	-	`sha256:967a0b527be0276461265cd06c3a38188b3f66f404206d8c24fd2d3e030e6b71`  
		Last Modified: Tue, 24 Feb 2026 23:12:44 GMT  
		Size: 7.4 MB (7413239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41bf60816093f0ea8372f1372e82fd9a1814e12318b92bbd1d02c2bb3e7ba287`  
		Last Modified: Tue, 24 Feb 2026 23:12:43 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json
