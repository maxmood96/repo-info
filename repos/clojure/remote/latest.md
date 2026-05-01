## `clojure:latest`

```console
$ docker pull clojure@sha256:6d14d13edc934551a18bb18418a68026b50f0d1d9e7cdff73f370351866c08db
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
$ docker pull clojure@sha256:e489398718ee86d508ea6d9575f4dbcea73471615cfa0081fb384e6bf02ca4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 MB (239322443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c8faf631dd19295ce387c43d1548978a837ff542e907c318ae847761d94d44`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Thu, 30 Apr 2026 23:52:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:52:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:52:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:52:20 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:52:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:52:20 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:52:34 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:52:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:52:34 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:52:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 30 Apr 2026 23:52:36 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:52:36 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:52:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:52:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:52:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:52:49 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:52:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26db87fd7758bce1ad80c59bb46920600b4d6163b02acae6756d73c85ed127c6`  
		Last Modified: Thu, 30 Apr 2026 23:53:13 GMT  
		Size: 91.5 MB (91542288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10ff558c78748d143173c90b9d47f8a0eab377b35b34274001c69b5c0596637`  
		Last Modified: Thu, 30 Apr 2026 23:53:11 GMT  
		Size: 19.6 MB (19637027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a13cd3f8407a0cecad3ffc40ecd5b75aebd3d97a9065c4444d2c2d7ea405b6a`  
		Last Modified: Thu, 30 Apr 2026 23:53:10 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c7661cf08ad8585ff908a7f88d4c4a36135cc09f1f75b09f4b1aabd50942e2`  
		Last Modified: Thu, 30 Apr 2026 23:53:13 GMT  
		Size: 75.3 MB (75251243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9544175effa5c3e00ec59ccd7705782bc534068b59d258b4fca74ad981beed`  
		Last Modified: Thu, 30 Apr 2026 23:53:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b8445fa898998d2d9cbc8203bdedc507c4b13609562fed1e9c44c625244ba7`  
		Last Modified: Thu, 30 Apr 2026 23:53:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:a2bdf7f46535520e12ed5023716d093e6fbf3cfed843abcb6bc78dd165180a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7470963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd920b05091c7256e0fdc70a05075a4c6d97ff1025b571fc70657c47e6abb9b9`

```dockerfile
```

-	Layers:
	-	`sha256:cfe231e15f8088351dca9e5f5f3790c5a44302a3be1359c20fb9611c48f3a597`  
		Last Modified: Thu, 30 Apr 2026 23:53:10 GMT  
		Size: 7.4 MB (7445230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7811bc3f68436428225aa9db9cadaf62eecd3e7cf6b457eff495d58e2b83ad58`  
		Last Modified: Thu, 30 Apr 2026 23:53:09 GMT  
		Size: 25.7 KB (25733 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:ae536c5c110647ef8d6f935c38ca9bf1f71494e8d81cd17d2526e8e329154971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249493911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850c0a17381488f1b8a70f0e709042fcbb7cae26b2d12a3e160259826e36bffd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 01 May 2026 00:07:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 May 2026 00:07:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 01 May 2026 00:07:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:07:11 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 01 May 2026 00:07:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 01 May 2026 00:07:11 GMT
WORKDIR /tmp
# Fri, 01 May 2026 00:07:45 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 01 May 2026 00:07:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 01 May 2026 00:07:45 GMT
ENV LEIN_ROOT=1
# Fri, 01 May 2026 00:07:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 01 May 2026 00:07:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 01 May 2026 00:07:49 GMT
WORKDIR /tmp
# Fri, 01 May 2026 00:08:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 01 May 2026 00:08:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 01 May 2026 00:08:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 01 May 2026 00:08:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 01 May 2026 00:08:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01487bcba0d0c1649162f2116f011092d3effd12c3f381faa370fdd01952d8b6`  
		Last Modified: Fri, 01 May 2026 00:08:34 GMT  
		Size: 91.9 MB (91914030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5861fa1b14a7aebd53e77b55b7470ca4d71c7bc6806cd6a1f6b804c9bf9fb9`  
		Last Modified: Fri, 01 May 2026 00:08:32 GMT  
		Size: 20.0 MB (20030495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6131a869cce9f026526a23905f8b4d17749c6b20f162420b9f0904dcf4251db`  
		Last Modified: Fri, 01 May 2026 00:08:31 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59be60349e09d73f31b3ba4e7d4e5cc8e5b72e38cc78320417827e960701adfb`  
		Last Modified: Fri, 01 May 2026 00:09:18 GMT  
		Size: 80.7 MB (80693836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873a6c4f3d6400a31de3ba3b3c5e04e693691e508c5813da1b839e82a10f3400`  
		Last Modified: Fri, 01 May 2026 00:09:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e5207870876843ae9ee74c88cacc64def2a8c266df6cc07def79bef6878c75`  
		Last Modified: Fri, 01 May 2026 00:09:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:396d1bd41c5daec3d8f251cb8ef19ac5e25fa4915ec3141073e75a239c056bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7453659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68edd67971cb40e4976b9bbb81e4c166421c4d227e92037236838434bcf3ac81`

```dockerfile
```

-	Layers:
	-	`sha256:29675de34cc40617b541b23312078883695f07906f027eb55e68902d2b546953`  
		Last Modified: Fri, 01 May 2026 00:09:16 GMT  
		Size: 7.4 MB (7428010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa1c2fcbd797722e4cea541e07d2debd3899f6d09d977c1945f90b8b8872ff0a`  
		Last Modified: Fri, 01 May 2026 00:09:15 GMT  
		Size: 25.6 KB (25649 bytes)  
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
