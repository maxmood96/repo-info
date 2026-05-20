## `clojure:latest`

```console
$ docker pull clojure@sha256:51fdcb58ffecfeb370aa2a365ce27f7c4cd0f8f50e632a166dd1014e5d5a6239
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
$ docker pull clojure@sha256:55a240316a9d920b8c143c79aff1408ee1ad873dcfe5d0ae91513b6513c039d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249523361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcc406576ae5b8966cc33a22962825202de5c20036bfe9eb491676f2801497f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:18:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:18:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:18:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:18:51 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 09 May 2026 02:18:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 09 May 2026 02:18:51 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:19:17 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 09 May 2026 02:19:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 May 2026 02:19:17 GMT
ENV LEIN_ROOT=1
# Sat, 09 May 2026 02:19:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 09 May 2026 02:19:21 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:19:22 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:12:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:12:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:12:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:12:28 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:12:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5de956b7a11284f1a158aa4d174299365ba072baa5eadc5c41d537c7ba7509c`  
		Last Modified: Sat, 09 May 2026 02:20:31 GMT  
		Size: 91.9 MB (91914029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7c27935ce89344c9f2063adaf35463730e2c3db3cda2b4435240ccf8a48f5f`  
		Last Modified: Sat, 09 May 2026 02:20:28 GMT  
		Size: 20.0 MB (20030513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8435cb421dfc3e57ae86315bbfd20609e9a621d5a198bd965880b6dcdf4018b5`  
		Last Modified: Sat, 09 May 2026 02:20:27 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3480ccbbc6ca8bf80dc87ce587b39b4507c07b2aa5473a93c91d33d7a03e4e7e`  
		Last Modified: Fri, 15 May 2026 20:13:24 GMT  
		Size: 80.7 MB (80723211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccef7e77db703a0184bff31647a6cd0f4e14f89be88d913d0d638eeae7d45c9`  
		Last Modified: Fri, 15 May 2026 20:13:21 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a02d671699b84d0d277341c964795f1b0962eb9c424d321fd0c4d02e5fa08`  
		Last Modified: Fri, 15 May 2026 20:13:21 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:cdb241f98659688e7695c26df10cba176631eba0c909268d5fae0803cf5c5210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7452857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6562b6cc3eecb9798b8d8baed4d6ac432f3a06fac42a50a9afba2a6010464309`

```dockerfile
```

-	Layers:
	-	`sha256:91b161329b75c3fcf02284e734135e0e321ed41332ed724fb26e0fce17892050`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 7.4 MB (7428008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d160b5023e98a93cd0ae79dca4af677d4c80b54f96f7bc2b23abda4328be5fad`  
		Last Modified: Fri, 15 May 2026 20:13:21 GMT  
		Size: 24.8 KB (24849 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:02e673048812166aa47f446c40047909db422f3505a300578737ce8409cb7520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233825195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec886ca843cca4d17b3cc9a509ed20ab2adcc4d81715edfa9395e0ec0ea21414`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:32:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:32:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:32:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:32:13 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 14 May 2026 23:32:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 14 May 2026 23:32:13 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:32:26 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 14 May 2026 23:32:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 14 May 2026 23:32:26 GMT
ENV LEIN_ROOT=1
# Thu, 14 May 2026 23:32:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 14 May 2026 23:32:31 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Thu, 14 May 2026 23:32:31 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:13:25 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:13:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b6df7c9202b34e5001f1810110d9cec30a4c24152183a755a378cbd2825b9a`  
		Last Modified: Thu, 14 May 2026 23:33:14 GMT  
		Size: 88.4 MB (88420318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea434e4bdaff060dd5d86848dd71f8fef7178355b899145cf2fcc6ca8551dbdb`  
		Last Modified: Thu, 14 May 2026 23:33:13 GMT  
		Size: 19.5 MB (19466847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302e9e28690038c8afdfe1a08c88ca42f5db41d05a25ae8720270cd48ac7cbc4`  
		Last Modified: Thu, 14 May 2026 23:33:12 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3174af8f703173f423fe49f9bacac707ca1b5536d1508ecdd417a30ab549b4`  
		Last Modified: Fri, 15 May 2026 20:14:05 GMT  
		Size: 74.3 MB (74271184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e144ea544e7de2fdff53881c159143b14b53986f086805c52d82dcc165a9edb`  
		Last Modified: Fri, 15 May 2026 20:14:02 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb92a787871937c5810b85fb16bc5a5f87a120ebba52a30f72d58f13f73ec14`  
		Last Modified: Fri, 15 May 2026 20:14:02 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:1a7f9e96fb9dc039a9e2614483238b1abe737a794f2b20da01ed6335cf785f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29169c8a5279befdc4b56dd2dc04922dbb7ff335dba90908034b314a0c7e77d2`

```dockerfile
```

-	Layers:
	-	`sha256:55ab25741b1cbfb5010d4a0300532fcfa650b1c32356965fc6bb6f449794f6f2`  
		Last Modified: Fri, 15 May 2026 20:14:03 GMT  
		Size: 7.4 MB (7415373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4352184a9c11d76df233e0fcee3639ca5169c536600f2b8e352e0919511db21`  
		Last Modified: Fri, 15 May 2026 20:14:02 GMT  
		Size: 24.8 KB (24810 bytes)  
		MIME: application/vnd.in-toto+json
