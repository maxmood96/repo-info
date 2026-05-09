## `clojure:temurin-25-lein`

```console
$ docker pull clojure@sha256:b2860fa66c5919d1ebc891b3887b6f89774b9d01d5d3a05fb36a057f21d2be5d
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

### `clojure:temurin-25-lein` - linux; amd64

```console
$ docker pull clojure@sha256:7cda1947aab6dbf79c518699bf230d72b5ef5938a7a89549b8ff541351adcde1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165387910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09a65a93015cc1aa89476582c401957d1743b2336f2b85b4fb4991605b2d0df`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:18:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:18:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:18:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:18:46 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:18:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:18:46 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:18:58 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:18:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:18:58 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:18:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:18:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:18:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:18:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe85d4fad53dad338d296b4edd0775f5033dde513c18d43b5f7a31a2a0bb1c7`  
		Last Modified: Fri, 08 May 2026 20:19:17 GMT  
		Size: 92.6 MB (92574587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072a5409bb6dc17e3ebec44b0c2ae94ffc5cce54306bcf22cd8f8477edd9bfb3`  
		Last Modified: Fri, 08 May 2026 20:19:16 GMT  
		Size: 19.8 MB (19806514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d452af9140c0356d06a316826d7cd20bf8a069775e79c816e96c090751a261`  
		Last Modified: Fri, 08 May 2026 20:19:15 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b1d04398982f65a1ab4456d176172abecf60a1b6f4a1fb53c1376d0f4c943e`  
		Last Modified: Fri, 08 May 2026 20:19:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:b8369c7263204d465180bf3a678e8fe0722cc9e43ea58d7bb4aa9e095a96a798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29af8d564f743498a3dcf0dcf077b5f9048350cc6a73eaf20d94a9bf203a770`

```dockerfile
```

-	Layers:
	-	`sha256:7bc9015b9f14fa0c28c8e9baaf4ab1f4b78638e5ccdff09f8e1900a0ee7fb6ae`  
		Last Modified: Fri, 08 May 2026 20:19:15 GMT  
		Size: 4.3 MB (4251650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98cdf3214b0f4e31eb67a24a1ca9f7766722061a95c4396319efebe621c47d78`  
		Last Modified: Fri, 08 May 2026 20:19:14 GMT  
		Size: 20.4 KB (20413 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6f395e532d1ab7741832b8497d826f58fa8370452235313956eaad9a72264658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164070513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef55c07409f592c60780beac29deb1adf504dd01a5ae18223fc5ad23f94c00c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:23:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:23:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:23:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:23:05 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:23:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:23:05 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:23:19 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:23:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:23:19 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:23:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:23:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:23:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:23:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8fb3145a758021bc23a059f8bb43ba02eb3a4ee2f74ca3fb3808594693354e`  
		Last Modified: Fri, 08 May 2026 20:23:41 GMT  
		Size: 91.5 MB (91542268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df132b23e085aa4b900b26387c404d30104e156d609b0aca47e79008b69b08da`  
		Last Modified: Fri, 08 May 2026 20:23:38 GMT  
		Size: 19.6 MB (19636964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9d076e49e63fee86fe57a3822fee53cf067f2dd7d04e049e736d059e9655d2`  
		Last Modified: Fri, 08 May 2026 20:23:38 GMT  
		Size: 4.5 MB (4517703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddfeebbbf6c9d3236de3393a85acef1de10f3a0974f7b51918764489d79c34a`  
		Last Modified: Fri, 08 May 2026 20:23:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:42ecb4d05ad073ff080670fa2e7de76459b116589c8f3e531383d7287c0d0835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3aceb968b53ea264aa5b752b8f7725bc5951ef7afed78f94634d50f05b266f`

```dockerfile
```

-	Layers:
	-	`sha256:262adecf1e1172138385c5385bf602659c8771588139e3b716bd0f7b9c819477`  
		Last Modified: Fri, 08 May 2026 20:23:38 GMT  
		Size: 4.3 MB (4251334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b862ad6824a0fda93f31aa9a98e7257f66cf59ece14e8a0d2793b12d8538d85`  
		Last Modified: Fri, 08 May 2026 20:23:37 GMT  
		Size: 20.6 KB (20606 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein` - linux; ppc64le

```console
$ docker pull clojure@sha256:403dcebf1a2adcd22672cbd1f7d14e79be47fb68cc907f3568f2b51ac3eaa49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168799393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6232452c87c38f9d1afb28a1d7180b39bc2b6605d217a8a5e920ef7db9682832`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 01:34:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:34:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:34:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:34:38 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 01:34:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 01:34:38 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:35:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 01:35:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 01:35:14 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 01:35:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 01:43:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:43:29 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:43:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d733e476aa8595c677a7a8e78f0fbc11c82e45660c7657482695df3b0260f12`  
		Last Modified: Fri, 08 May 2026 01:36:27 GMT  
		Size: 91.9 MB (91913990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd71281f76e595b73d8d0c8f07fa830b4a334af9eec5d0149a1efb2e6e272542`  
		Last Modified: Fri, 08 May 2026 01:36:24 GMT  
		Size: 20.0 MB (20030493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed03b88e86956a26e7e85d64d8501f485f4609b55f6d6b475eaa3fc1c096d88`  
		Last Modified: Fri, 08 May 2026 01:36:23 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafaaecadf554c123e98402fc8e61b12c12c1a5e1b3738989f8a0f101c20471c`  
		Last Modified: Fri, 08 May 2026 01:43:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:856cb3e08037617b36d2dc401e7e5a3d1dc015d849bd775331686cfa8ba1aac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4257351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4cfb02d123e710d4810c1493b6a07c43cc982933000b84b685e389ee74ea36b`

```dockerfile
```

-	Layers:
	-	`sha256:5d5f376d8c9793e9c18778b07fe171e509032aa312c3464bb3fc9cda2e1af383`  
		Last Modified: Fri, 08 May 2026 01:43:44 GMT  
		Size: 4.2 MB (4236859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92968f68ba1192f40bbbbad78738cd8e9f9348bb17f899245e3a771b256dd115`  
		Last Modified: Fri, 08 May 2026 01:43:44 GMT  
		Size: 20.5 KB (20492 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein` - linux; s390x

```console
$ docker pull clojure@sha256:17f3b729cd256b160d297db03d072b9d28ad16f6b8988217e7083aa6f999cd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159553284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c9654f59e9f1d5da57b789e9c8996d34a4cf61a917976e8cc991eb9e72f3b9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:12:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:12:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:12:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:12:41 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:12:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:12:41 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:12:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:12:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:12:52 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:12:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:18:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:18:53 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:18:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a188a913daf22f341771db62166f6bc3f7d8f891104f744dec07784a901e7ce`  
		Last Modified: Fri, 08 May 2026 22:13:43 GMT  
		Size: 88.4 MB (88420321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c733194e0e799c2d764ce0d3324ff52913e41da44cadaa52465ce4b5e3a48d07`  
		Last Modified: Fri, 08 May 2026 22:13:41 GMT  
		Size: 19.5 MB (19466774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b715cf92e86d57654fdb72c5429f6d5c3378402893f9eca8a1f6b31bfe815fb`  
		Last Modified: Fri, 08 May 2026 22:13:41 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79b23612d27882b1ee7c5f4072c8b2b36cd72306c080519c0135a995b3b0c12`  
		Last Modified: Fri, 08 May 2026 22:19:06 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:d86713b038e85558362a274fe9ef2a5742915c2915db051b2d43d4d8abae0e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70be9489f7a3a876739847c7d43cdb49bbf44bfb9370919b98f50dd8826933ec`

```dockerfile
```

-	Layers:
	-	`sha256:fb82a1f272573a733a31824be1d62b4692141469ccf82728e363eaf2c633a8bb`  
		Last Modified: Fri, 08 May 2026 22:19:06 GMT  
		Size: 4.2 MB (4228026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51b8c5c320d931770964114f203f621780db507a1953410e9272eb8eff10e971`  
		Last Modified: Fri, 08 May 2026 22:19:06 GMT  
		Size: 19.5 KB (19460 bytes)  
		MIME: application/vnd.in-toto+json
