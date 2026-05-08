## `clojure:latest`

```console
$ docker pull clojure@sha256:1c54c3f6e997042a402108f2a7162f354e26b9e9f3052a8116428f8234aeefa1
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
$ docker pull clojure@sha256:09df1d5a9d18b12e311da7fa44e28aaacba13fc366333a2f06956f259177d1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240482927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff9861444b5c6b20847ea25f3dda490b1aeb920c3eb500bd0aad42fdd5e6a4c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Thu, 30 Apr 2026 23:52:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:52:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:52:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:52:40 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:52:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:52:40 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:52:54 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:52:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:52:54 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:52:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 30 Apr 2026 23:52:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:52:56 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:53:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:53:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf3f87502125b653a96e884d0b344d68f6f75d2e9d71b47cc936b7741e6fcd3`  
		Last Modified: Thu, 30 Apr 2026 23:53:31 GMT  
		Size: 92.6 MB (92574598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08dc8fa885e76b1df3d0fe7c271929c2da597b0cca5d4b0dffff3b6e2d38e1af`  
		Last Modified: Thu, 30 Apr 2026 23:53:28 GMT  
		Size: 19.8 MB (19806560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ff320915231f7f405fb6245c87036dc08e222271e6af773e5ca2d4f5df43de`  
		Last Modified: Thu, 30 Apr 2026 23:53:28 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b38d2007f9ec4e449e8e9151fcb190b6277cd5b3ac9b2e26e0ef27e7ef6d5e2`  
		Last Modified: Thu, 30 Apr 2026 23:53:31 GMT  
		Size: 75.1 MB (75094325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d102d09996ba1c96c8044f45f12f8fffbacba000f42594ef3c342eda5bce74e6`  
		Last Modified: Thu, 30 Apr 2026 23:53:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a894ecfba3cf533a6b30069667589b2abdee6e3062d9b50f62f99cbcf955ba0d`  
		Last Modified: Thu, 30 Apr 2026 23:53:30 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:4ce2eb5f8dbea5530e86370c5114444e027bb2fc3e6a0bcbe88020fcc93a9d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7465103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa265b0d1c16ce65611897631f87f99bb47747b95da0e65f01d98597f70764a5`

```dockerfile
```

-	Layers:
	-	`sha256:e50546f547e091b0cd1ca0fcc02da35bd0ac2850d4e49356ba3eb96df42f9f0d`  
		Last Modified: Thu, 30 Apr 2026 23:53:28 GMT  
		Size: 7.4 MB (7439494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f54ecc79a19a9d5e4b4fd58d385e466df0c54407787b07f832011bc85dd5a6`  
		Last Modified: Thu, 30 Apr 2026 23:53:27 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9983503211c336e1b5a9b356c4da51ab1fd8fd73b6d9176f8ae83900c8a8b5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 MB (239322389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096675e645b3d9d4be9bd55f9a03653f67fbf8ccdb3167877a0977be3cc90ca9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:25:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:25:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:25:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:25:46 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:25:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:25:46 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:25:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:25:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:25:59 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:26:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:26:01 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:26:01 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:26:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:26:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:26:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:26:14 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:26:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7383eb1e477ed944e55ca0da53f88a603f4868b9aeff22a3cd48a492665496`  
		Last Modified: Fri, 08 May 2026 00:26:38 GMT  
		Size: 91.5 MB (91542278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47cb1eb2c1ed42a90cdd59a230ae48c07859bc60a5aef0200260b5eb2060521`  
		Last Modified: Fri, 08 May 2026 00:26:35 GMT  
		Size: 19.6 MB (19637002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b379099263805e13ab7d38c3bac8b56497b47127b90a0599e4ffc241f993c26`  
		Last Modified: Fri, 08 May 2026 00:26:34 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf7cffc50af18ce2b4c0ac2fc01ca2a3ab557cb0575a29c83a6b70dae220bf9`  
		Last Modified: Fri, 08 May 2026 00:26:37 GMT  
		Size: 75.3 MB (75251220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2a6741c25c61f6b05489d4865cd71537b1ef1a1d16d9d8582c7d33b5eda4d1`  
		Last Modified: Fri, 08 May 2026 00:26:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acaac0185c3e43d6e5837feeb5570f06c4282a0de99ba743c5ea77edab738f6`  
		Last Modified: Fri, 08 May 2026 00:26:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:b1b9e944bbdcea78cf6ee06608d528ea7046a6b725e9d14ad6895429989cc0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7471117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3212e8b35e20cfc63d08cdf65cf9a8c3a1475a656087082c998832a52487afd2`

```dockerfile
```

-	Layers:
	-	`sha256:83f42ef86b4f3a3c604a12f7b34986d0ceae1c47f6e82722c6b749e13a8bfca2`  
		Last Modified: Fri, 08 May 2026 00:26:34 GMT  
		Size: 7.4 MB (7445230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:923499612dd102438eadf0c7140de16b867533dc45b9fc2bebd1c51102d96980`  
		Last Modified: Fri, 08 May 2026 00:26:33 GMT  
		Size: 25.9 KB (25887 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:7b6bff3c872dc2a45032c27fba4efc9e1b860a2c4bced95c835bf8848371c9b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249493716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29460ac786994c22c5966422c01f1cc6e2808382e00768a10e35953f5ea34370`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
# Fri, 08 May 2026 01:35:17 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 01:35:18 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:35:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 01:35:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 01:35:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:35:47 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:35:47 GMT
CMD ["-M" "--repl"]
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
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8dc53f6c31945d16c100a7f9215bb213b62a3401c4b1d866f3effbbb1412e2`  
		Last Modified: Fri, 08 May 2026 01:36:27 GMT  
		Size: 80.7 MB (80693675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d007137eb6d7b79c5381e85e1825a23795216965459be3fd47eea44f73b33b1`  
		Last Modified: Fri, 08 May 2026 01:36:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018164cd70f109cb32c38bb9bb33f644e9fdff306e428f856ae29a28ca545dbb`  
		Last Modified: Fri, 08 May 2026 01:36:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:138fe7772739d35ef75676700a3c208421b4396b307cbe697a20fc039d1127c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7453813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2d850948d12fcff6a8a5cf4682bf48bc0598a6f768fa63c914c8cdcf370854`

```dockerfile
```

-	Layers:
	-	`sha256:74a498527a88d4698c6a9a5a346c711c19427a41fb2178c7d38457338fd5c964`  
		Last Modified: Fri, 08 May 2026 01:36:23 GMT  
		Size: 7.4 MB (7428010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e44339b9557881485a234717bf4ed407ece44da8cd6d8b59303bb031f02a7e15`  
		Last Modified: Fri, 08 May 2026 01:36:22 GMT  
		Size: 25.8 KB (25803 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:b4c0b2fa7bad0468cb26af3bf432c1a50e1b31c7c1778e8b1edb61f4bf7f413e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233794309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50bfbce7c757788cdd40b8187e453b029de575cd21891de18273475d30a2d04`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Thu, 30 Apr 2026 23:49:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:49:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:49:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:49:40 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:49:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:49:40 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:49:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:49:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:49:56 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:49:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 30 Apr 2026 23:49:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:49:58 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:50:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:50:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:50:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:50:17 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:50:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439ca7a271e362a7945b93efef6e6eb132b28afbec5dd9a21f35ce6c32acb6e9`  
		Last Modified: Thu, 30 Apr 2026 23:50:59 GMT  
		Size: 88.4 MB (88420341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f49fc5a549ed1553878c3915c3d1663ee51b316338bb43a8a9219a449809f2`  
		Last Modified: Thu, 30 Apr 2026 23:50:54 GMT  
		Size: 19.5 MB (19466655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf46a4b0ade1da07884078a69b4494442dd6325f8e102fd49e1138abb2fe0a8`  
		Last Modified: Thu, 30 Apr 2026 23:50:51 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50df84f4abdbb7153aa7e680e20e48e4668640e547b7c1cb47708be97befbee`  
		Last Modified: Thu, 30 Apr 2026 23:50:59 GMT  
		Size: 74.2 MB (74240517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c70da43cec59d53db14fbe8c48ed0860d870e899cf6206a40bcc388eeb2baf4`  
		Last Modified: Thu, 30 Apr 2026 23:50:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25792ca205c6200fb987f97f79ec8c2d9c59c9c4ccf896a2b5c8d730d881f562`  
		Last Modified: Thu, 30 Apr 2026 23:50:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:426a99d8d5ed1e7a9ef99601c4964fff84ec080918741cb66176a91b9b2e2d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befb45136e8a9725b8ba1c42116ff30d5501e75720f1586d5c1f2123fc523ee4`

```dockerfile
```

-	Layers:
	-	`sha256:c47781ce6e9c7f77050a144acbdf4210b8f8b899b88c220b0da3744f9d1a6e56`  
		Last Modified: Thu, 30 Apr 2026 23:50:51 GMT  
		Size: 7.4 MB (7415375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab9971738c5f6ffb013ea0e030fc51a11478253413af8a2703146f73d4c10ba`  
		Last Modified: Thu, 30 Apr 2026 23:50:47 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json
