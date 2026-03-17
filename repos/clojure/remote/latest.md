## `clojure:latest`

```console
$ docker pull clojure@sha256:db6f220d75a7b816a93d73d743fc1243d318596ba1f8e6f582ee8ecb0d6564fd
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
$ docker pull clojure@sha256:5be2766616bb9dc32f0c970b83a771eb91d6103824f8be835c13caa8c4f3d920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240158576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c005d5d83d309f6d328af3fae37ac9e88080d53c686d744c1f62f18799091c3b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:18 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 02:55:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 02:55:18 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:55:32 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 02:55:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 02:55:32 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 02:55:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 02:55:33 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:55:33 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:55:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:55:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:55:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:55:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:55:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc21d77b997e18aeecc3475421bc8a1eb6cea352b157313ec2aefe45e8757bac`  
		Last Modified: Tue, 17 Mar 2026 02:56:10 GMT  
		Size: 92.3 MB (92256299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b02fc45c9ec4888092de4d4e09f596a20b67300a897a335a51c93ec2b77ba5`  
		Last Modified: Tue, 17 Mar 2026 02:56:07 GMT  
		Size: 19.8 MB (19802836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781af1a0c2f70b2264de0b30ad65f5f028ef94e4c486a22a890c1ff2b0853b24`  
		Last Modified: Tue, 17 Mar 2026 02:56:06 GMT  
		Size: 4.5 MB (4517708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cd5db14024e1a2ad120c7775ea83d87b3c9754256b2cf4c99bfc874595bef5`  
		Last Modified: Tue, 17 Mar 2026 02:56:10 GMT  
		Size: 75.1 MB (75092078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1007398734ae645bef787bb90db2ae2eb65acba317580ccc6fe81c0abea01121`  
		Last Modified: Tue, 17 Mar 2026 02:56:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60fe885b6a4330364fb4f6f6334481d441a43625d92d39e3f271d9318a43450`  
		Last Modified: Tue, 17 Mar 2026 02:56:09 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:81e930a9608c8f3ff259597b3a0e0f91a499f7ab3e48c5dc80b93f07f77bde25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7464480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f123621a5ebc5128aff4c1ccb2007cb6feea237f1ad9a1048806009c616e119`

```dockerfile
```

-	Layers:
	-	`sha256:ad7bb9e326c780b99836abbbf10771ca2275e1a81fbf6d364ee083497ab83cb3`  
		Last Modified: Tue, 17 Mar 2026 02:56:07 GMT  
		Size: 7.4 MB (7438871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a07a62a2b994d2fd0988996261a545a8c291c6e1fe3f1ff9bbe3e5b61732e152`  
		Last Modified: Tue, 17 Mar 2026 02:56:06 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c73f1f3f7db6fd7495d8c6078947da796606acca22d99cac37bef80e9bcf89d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.1 MB (239064289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef86602d1f1449fbaacbfedecd5fbee2cf1ed82d50a3e571ccb3325349f647b8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:28 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 02:59:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 02:59:28 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:59:42 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 02:59:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 02:59:42 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 02:59:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 02:59:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:59:44 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:59:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:59:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:59:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:59:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:59:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cece5b6ef31d6e20939b80c25fefcac12a67ad13331af290ac6355366f11c6b7`  
		Last Modified: Tue, 17 Mar 2026 03:00:34 GMT  
		Size: 91.3 MB (91288265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b501d289d1d1d30a8e352b2ef0a484ed0beba9826e6435663b567bcea7e6a391`  
		Last Modified: Tue, 17 Mar 2026 03:00:32 GMT  
		Size: 19.6 MB (19632776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fb3316e3cedc8023538b8853dfc5b8a260ccfd3189de1e6fcf70133d4d225c`  
		Last Modified: Tue, 17 Mar 2026 03:00:31 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe8917a28f83a477e56233617bc1377944fe6a42fe0b2fe04a81bd3c00fc135`  
		Last Modified: Tue, 17 Mar 2026 03:00:34 GMT  
		Size: 75.3 MB (75251391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62ecad575bc4da45429ce93bd7e3efce0f0b8205fe88ce2262b51fc1b06d85f`  
		Last Modified: Tue, 17 Mar 2026 03:00:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937d0eb3c5879eafcf54e6ef723edea442bd6338af791c268733eb02727688a5`  
		Last Modified: Tue, 17 Mar 2026 03:00:33 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:d544a41335c5f9862139c6b9ea84f20b1ba848d97ac997ca5d2e992f9f97e024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7470340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e7a42dcefab29f29bb8b072b7af33432679269335e7530eca741cf1265e1b1`

```dockerfile
```

-	Layers:
	-	`sha256:1e655111d6956c911b620efc93531bdc6d163fb09c8758e3e74afcd860d404a2`  
		Last Modified: Tue, 17 Mar 2026 03:00:31 GMT  
		Size: 7.4 MB (7444607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0be00d24dd12e8ae09fac1c91c216533957aaa7bb38ceab2b3c11a7971aae9ad`  
		Last Modified: Tue, 17 Mar 2026 03:00:31 GMT  
		Size: 25.7 KB (25733 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:63af44601f5c369a85d2b8a4b9f8ca4a2ecda206b67bee0c3c18814571de301d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249205027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4475c2202971a4a66aea9dbbac3e150a857f2f7068a982bbfe0fc48c7b56014c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:39:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:39:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:39:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:39:48 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 09 Mar 2026 20:39:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 09 Mar 2026 20:39:48 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:40:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 09 Mar 2026 20:40:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 09 Mar 2026 20:40:31 GMT
ENV LEIN_ROOT=1
# Mon, 09 Mar 2026 20:40:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 09 Mar 2026 20:40:37 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:40:37 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:41:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:41:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:41:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:41:13 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:41:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375aa8eacf526a2bf938fbc2d4fee75e90900d45e6476502c1338fa7b89cf807`  
		Last Modified: Mon, 09 Mar 2026 20:41:55 GMT  
		Size: 91.6 MB (91632879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0214e9b7aa7a886adb2997268cac19dd878ec035b6634e54b5df1190190e61ef`  
		Last Modified: Mon, 09 Mar 2026 20:41:52 GMT  
		Size: 20.0 MB (20023934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a097b666606bd0a82642cbca80aafc0874dde1063f0bc56d74a7a88a3e851c5e`  
		Last Modified: Mon, 09 Mar 2026 20:41:51 GMT  
		Size: 4.5 MB (4517780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2fe8d0ad70108ba7b4fab895e854afa13a6f9a52038c0618512a73f2c5c129`  
		Last Modified: Mon, 09 Mar 2026 20:41:54 GMT  
		Size: 80.7 MB (80692563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb93a47726cbc05a7b9df8e54136d878d1cfed2a573ed14012fc1297b7f42c26`  
		Last Modified: Mon, 09 Mar 2026 20:41:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dca11fe8fb5446853b8f3975e99e5d63f513340bcf321228f0bfd7869fb0bb`  
		Last Modified: Mon, 09 Mar 2026 20:41:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:eda35d092b280af48e536e1598aec07f82eef55091b3685c1f8f05c1d79b5aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7453036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabd48ff0ce8a900024b66ba8fdef023e58e1cc60bdb7f2849ef8ae6a6211f04`

```dockerfile
```

-	Layers:
	-	`sha256:f37cf69ddfa1bc4c7a833c97f76cbdae676ac368a6ca71af90dd68282940c7e9`  
		Last Modified: Mon, 09 Mar 2026 20:41:51 GMT  
		Size: 7.4 MB (7427387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbddce8e45d56f2941445bbe808b011d52e5e4c82a60ee56c1a4b1f119cf730`  
		Last Modified: Mon, 09 Mar 2026 20:41:50 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:0bbcb655555a0baeb3254dd769eebca6ea18d7064428007c780999d2e669af4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233604210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf3d0145e1483967f401178d02504bd49a4af0e65570f63973663d794ea7a91`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:32:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:32:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:32:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:32:15 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 09 Mar 2026 20:32:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 09 Mar 2026 20:32:16 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:32:27 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 09 Mar 2026 20:32:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 09 Mar 2026 20:32:27 GMT
ENV LEIN_ROOT=1
# Mon, 09 Mar 2026 20:32:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 09 Mar 2026 20:32:29 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:32:29 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:32:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:32:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:32:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:32:42 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:32:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0090c1a93b6afd53923a7febafaf7e1aa30c3499c036618702ec7c47bcc97854`  
		Last Modified: Mon, 09 Mar 2026 20:33:13 GMT  
		Size: 88.2 MB (88233824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30eb361454b78cf8e6c287f764ee36eefba6bd09a02d0a7cad1d7ed505654271`  
		Last Modified: Mon, 09 Mar 2026 20:33:11 GMT  
		Size: 19.5 MB (19463247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5273da684b6b75d05aeb76ce0186b689900233fc29ea13ef070f4e684eae5c1`  
		Last Modified: Mon, 09 Mar 2026 20:33:11 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e67048d99ee8b5634a56f8564a0875d144e0465607a1cd49b5c00d08b02b1c6`  
		Last Modified: Mon, 09 Mar 2026 20:33:13 GMT  
		Size: 74.2 MB (74240230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c945060b8f85f9ea38074a2b846e69271d2e69b44ef14215e568afb0cee28b`  
		Last Modified: Mon, 09 Mar 2026 20:33:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b789ce1a7dc8e22ec5a33126340bb44fb148e7d0913f2e021a980fd43a908263`  
		Last Modified: Mon, 09 Mar 2026 20:33:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:7d7020bf1b8093d7ba0473e72448c9f874069876545cfd21409feedad9e5c5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca77c52f1a8033e38d87760ed09bc9c8fa02ae6f4e742b29c613daad4c31930`

```dockerfile
```

-	Layers:
	-	`sha256:7d7f151a7e3ed4457cb9bad63a0e110d5aaedfa3eac4e2c8f61c8ff77a335e5b`  
		Last Modified: Mon, 09 Mar 2026 20:33:11 GMT  
		Size: 7.4 MB (7414752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97adb8f30605f1b0fbe539e02bd5b06e4a5f4716e980d7fc4c2753d677eccfd2`  
		Last Modified: Mon, 09 Mar 2026 20:33:11 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json
