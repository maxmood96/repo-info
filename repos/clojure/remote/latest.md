## `clojure:latest`

```console
$ docker pull clojure@sha256:c9ae723edea62f565752375a028608216d90043915d6da2b4f93aee624458fa8
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
$ docker pull clojure@sha256:1f8e59304c0b4165508a605da959ba4a6e5bdeaec0540c629f1a612c317ff04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240536681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f219dac2217c6d272dbe9dc6b219863b4470ce87dc3aba7b1415d06650726d3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:55:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:55:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:55:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:55:17 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:55:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:55:17 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:55:30 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 19 May 2026 23:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 May 2026 23:55:30 GMT
ENV LEIN_ROOT=1
# Tue, 19 May 2026 23:55:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 19 May 2026 23:55:32 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:55:32 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:55:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:55:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:55:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 19 May 2026 23:55:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 May 2026 23:55:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a55d8770144302e730b0cc0a85264395edb8c9c0f5c5277a2230b4a299914d`  
		Last Modified: Tue, 19 May 2026 23:56:07 GMT  
		Size: 92.6 MB (92574564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f2eb5faf9e4a4d2839534f0c6c64b08c55c838def1fe5fe8b7a2879c180519`  
		Last Modified: Tue, 19 May 2026 23:56:05 GMT  
		Size: 19.8 MB (19811712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e0450060e317c2effbafb71361b805b3990ad126f9cde982def0f5e47c9ff5`  
		Last Modified: Tue, 19 May 2026 23:56:03 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e116cc48f0315772dfbcb1ac561ed5a6ab8230a8c85c1f89c1e6f7e1335ecdf`  
		Last Modified: Tue, 19 May 2026 23:56:06 GMT  
		Size: 75.1 MB (75136156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1fb6de800bea71989c393b0c9c7e195ed30fe9dbc729dd9cec38976741a9a3`  
		Last Modified: Tue, 19 May 2026 23:56:05 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb214ef81ecbf029451146d6a8fa9181d7a29e9f291962507edbc2b780c5b71`  
		Last Modified: Tue, 19 May 2026 23:56:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:b811d67e44775e4b534113592e1b5e06845373a8f407b51acca5bea92d906558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7465277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1737d46e792d70d91863dae477d4da8c11b6c1c59b55454b2b771f5a82cb6b`

```dockerfile
```

-	Layers:
	-	`sha256:b9198e56b4d673cb6caf181ac791c8a06f2839cb4c0e7d75e8ea74de636eedbc`  
		Last Modified: Tue, 19 May 2026 23:56:04 GMT  
		Size: 7.4 MB (7439514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f67215fbababeff4779c7831f8263542f12c4d0b039527771ea7c596983ed908`  
		Last Modified: Tue, 19 May 2026 23:56:03 GMT  
		Size: 25.8 KB (25763 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:863560b1f8c9b9eb57736ef10cc5104b70975681f798db55983453ed6164536c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239368016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1014959de97fbbf314bcf356ae2e1dd8d612818d73eef608c539de9dfbdef1b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:02:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:02:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:02:29 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:02:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:02:29 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:02:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:02:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:02:44 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:02:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:02:46 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:02:46 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:03:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:03:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:03:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:03:01 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:03:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f9db9d75dc6e3cdce36746f39afac30f286f8c87846cd54d4cb620cec9b91`  
		Last Modified: Wed, 20 May 2026 00:03:27 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66be0c9b2dca80a16a9cec8f10893d433d8fbd3556762524619705c0ea9ac183`  
		Last Modified: Wed, 20 May 2026 00:03:24 GMT  
		Size: 19.6 MB (19641763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58d63302592bb18ee060d998fbeb77daceebd01bbccda2986414b17c610b573`  
		Last Modified: Wed, 20 May 2026 00:03:23 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49582da3c99c0bd7ec6bae9aebd0cad73398bc84aa6a6eea32a363ccd07a2049`  
		Last Modified: Wed, 20 May 2026 00:03:27 GMT  
		Size: 75.3 MB (75285740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bdc1775c00635ba32a28cf7d08b6fdc11a839f87006a7b84142d9fd6e4bc3ad`  
		Last Modified: Wed, 20 May 2026 00:03:25 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1406ffda1a4328e8b4683128f5c5d31a09fe12ad2116ca48f2582a19576fac`  
		Last Modified: Wed, 20 May 2026 00:03:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:71ff54cd736a6f392f3b46145d347c514e71ff4e414b018fcfefc1ef37d65d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7471136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ce14b198ca21d2a214930e35f721adcbd07b58b69640a45e0ffe1ac0995b84`

```dockerfile
```

-	Layers:
	-	`sha256:9470a3219f1a7c355e5a23b2c2c5cfd532b228cdf7a18e3c447ba43584b9cec0`  
		Last Modified: Wed, 20 May 2026 00:03:23 GMT  
		Size: 7.4 MB (7445250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:841a7f290dae3a5f3bc95105f537dbd3a04b4351d3eb07f865b398dff167c778`  
		Last Modified: Wed, 20 May 2026 00:03:23 GMT  
		Size: 25.9 KB (25886 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:f7fc172d25253a64fe934de8db36be55c0d65ed724970ace8b8cc78febdee124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249530188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eddef8fe6c2c9141b1e194dc73a20287222ec509890240aac702a55fce41b9e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 05:41:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:41:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:41:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:41:51 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 05:41:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 05:41:51 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:42:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 05:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 05:42:24 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 05:42:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 05:42:29 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 05:42:29 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:43:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 05:43:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 05:43:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 05:43:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 05:43:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9d252f0e38d109f9943592c87001ada39f271784191f398d66e991f1eda37`  
		Last Modified: Wed, 20 May 2026 05:43:46 GMT  
		Size: 91.9 MB (91914038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35d3313261f425bb57fe0ec2df94d71655d5cab502cf29befe49b7076ac4b95`  
		Last Modified: Wed, 20 May 2026 05:43:42 GMT  
		Size: 20.0 MB (20033270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583ae030626da8366bd7fd80799babfa8092b34004fc94d6d0e6d56dfb0b43b9`  
		Last Modified: Wed, 20 May 2026 05:43:42 GMT  
		Size: 4.5 MB (4517774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd78aec47a5a32410e4e021a73991ee0daac18b67aa3f45ec04ebcc0cf6aca4`  
		Last Modified: Wed, 20 May 2026 05:43:45 GMT  
		Size: 80.7 MB (80723832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263aeb416fe6911401950e539beb9f79a4494cceb66a44238a32aed60fe0a0c7`  
		Last Modified: Wed, 20 May 2026 05:43:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e182469677e245819cd2ebe567510e0e4ebecc73899e8aa50fac0f0cd01c6ef5`  
		Last Modified: Wed, 20 May 2026 05:43:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:088500a65ac7714226caf5065d5bf6717e9979ef3052b562ead191cec4edddef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7453832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458dd84987dc119a14d830bcec28478c16da16234d45edfb22a23897c8e19810`

```dockerfile
```

-	Layers:
	-	`sha256:efa91c53dfb6a49e3ed0d0379d91c34682d22bdffc6082b21e80c4969404aa83`  
		Last Modified: Wed, 20 May 2026 05:43:42 GMT  
		Size: 7.4 MB (7428030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbf074388ae2c323070249c56a2cdbd6c02354719c4d48f442e62dac1ad56236`  
		Last Modified: Wed, 20 May 2026 05:43:41 GMT  
		Size: 25.8 KB (25802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:70e059c7a66d264586e33061a6554cf58d4868286fe8aa6b5afe8c08cb9288d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233829344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db3208c91287033640767e4def5d2e6f7466ce26840642948dd1b77e06e7e43`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:40:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:40:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:40:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:40:39 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 01:40:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 01:40:39 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:40:55 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 01:40:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 01:40:55 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 01:40:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 01:40:57 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 01:40:57 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:41:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 01:41:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 01:41:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:41:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:41:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a934554ab57d2fd5986adad7cd7478af54f0d87c944e186bd166c53ad21467`  
		Last Modified: Wed, 20 May 2026 01:41:43 GMT  
		Size: 88.4 MB (88420319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdd88ea48242c31c3879754e78c6bf8e58100cb6a81ed18f4b20caeee46d46c`  
		Last Modified: Wed, 20 May 2026 01:41:41 GMT  
		Size: 19.5 MB (19473757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9ae8639f45bbe737a5ad3c701692aedd0f3a28c0cd34dfead8ea724c82fee6`  
		Last Modified: Wed, 20 May 2026 01:41:41 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126ce5e3f3b3d2e4fcdbde8b09da654146d5ade06e0326ed5adc36394d8b18e7`  
		Last Modified: Wed, 20 May 2026 01:41:43 GMT  
		Size: 74.3 MB (74260858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af12eae1f21e4904011687ff0c3e2a2af82cd2e2fde0c16c44ba58c14c8ade84`  
		Last Modified: Wed, 20 May 2026 01:41:42 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac89fbf29335c7f1857a720f4d014532203c800eced02995e4119feee80eb157`  
		Last Modified: Wed, 20 May 2026 01:41:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:f0ed77be2d7a04d3e1fe73870f88e06077b2553e0047b4030fc2d0d484dcd220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b235e4f44ed65736ad45d2246205756a049f6d56239c664f35b1fb188ca0d749`

```dockerfile
```

-	Layers:
	-	`sha256:a5d949900970f4c81e6eb22185e2858d328d960006f019f8b84fa83ecc728a08`  
		Last Modified: Wed, 20 May 2026 01:41:41 GMT  
		Size: 7.4 MB (7415395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49087f23f9613a68c9f0d0dea762b162659721b1c8f834e5e1d712451b19fd5a`  
		Last Modified: Wed, 20 May 2026 01:41:41 GMT  
		Size: 25.8 KB (25763 bytes)  
		MIME: application/vnd.in-toto+json
