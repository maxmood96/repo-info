## `clojure:latest`

```console
$ docker pull clojure@sha256:7389d41240324c7cc1269bb3c8cab60a506d1918e4f9dc01df9a316c688554a4
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
$ docker pull clojure@sha256:cf6214e05e810b28f8db89884a79291113ca3a0b0ad226f18aa20ceeb1e3a003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240164472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c77bbdb2ec7201db84510ad431801bd763b31f80e4cf836221905f14c0612c2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:00:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:00:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:00:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:00:23 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:00:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:00:23 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:00:39 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:00:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:00:39 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:00:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:00:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:00:40 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:00:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:00:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:00:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:00:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:00:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b3f010a47bfd06aa2f0c905b53d29f875a5ba739b4f17a48fd17f4e3728271`  
		Last Modified: Wed, 15 Apr 2026 22:01:15 GMT  
		Size: 92.3 MB (92256281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2c4aa23ace0150e7443c42fa143706360f662426a2e1b7f3419011d2ad12a2`  
		Last Modified: Wed, 15 Apr 2026 22:01:14 GMT  
		Size: 19.8 MB (19806574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97852d896b5e41beaf7d41647d5f57759ecde00c564097f40d267a175845ec09`  
		Last Modified: Wed, 15 Apr 2026 22:01:13 GMT  
		Size: 4.5 MB (4517692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e2579c5356521b354809fa60915a0785a75f3348fd882f1621418cb0455cbe`  
		Last Modified: Wed, 15 Apr 2026 22:01:23 GMT  
		Size: 75.1 MB (75094027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc67abb678ba55c519d095a779de2f423a375f1b7af1fd67b6b24deda9b1a5a`  
		Last Modified: Wed, 15 Apr 2026 22:01:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ef13a0b7e9417ab911ae90a276bb2d0dc6db93ba2e9ddd2a077f2d4d53604e`  
		Last Modified: Wed, 15 Apr 2026 22:01:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:a10c72abede1f8dbd26beb325554c03a906131630d0620c7593c836e2a549386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7464480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e28c846906241b6de672cfe0d2891a08cf5b069cabde21b4ff5aeb9fe3dbfa0`

```dockerfile
```

-	Layers:
	-	`sha256:b9507d209a95bbd3735cabf06510a06393f78964196327e46ad8da6bd3310f20`  
		Last Modified: Wed, 15 Apr 2026 22:01:13 GMT  
		Size: 7.4 MB (7438871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9bd4a622404ddfff74fb58c92f15e0bb23f0ba886449284a16a340d748295c1`  
		Last Modified: Wed, 15 Apr 2026 22:01:12 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c79675528f7842164280b1aa0c77aa0bbae5a864c2f1192fa7cc5b53dbad878e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.1 MB (239068170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64702c8c25868c8df437f90cbba7545bdc6b52cc12f352024d27e04c4c591df4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:18:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:18:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:18:31 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:18:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:18:31 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:18:45 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:18:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:18:45 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:18:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:18:47 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:18:47 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:19:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:19:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:19:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:19:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8add182d4e73f89ab43db28930e88b018b7e8debc2fd244436622dc010933c`  
		Last Modified: Wed, 22 Apr 2026 02:19:24 GMT  
		Size: 91.3 MB (91288305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4c4a3716b60762231841caa96d7ac8b5313b4f60c75444b1f4c1dd78f594c0`  
		Last Modified: Wed, 22 Apr 2026 02:19:22 GMT  
		Size: 19.6 MB (19637025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8189aeca669fadf5e2dded0205047c352c6a7205a409c395c5180188c09a737a`  
		Last Modified: Wed, 22 Apr 2026 02:19:20 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce72cbdae8014216df5822153d5673956ac25c02235f0be8dd84b62f7e7b342`  
		Last Modified: Wed, 22 Apr 2026 02:19:24 GMT  
		Size: 75.3 MB (75250950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750f5991216790005ec6eff15b9b142880d4748d3d7c004c05d0b4d82212d2db`  
		Last Modified: Wed, 22 Apr 2026 02:19:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b545186afe55914bf8e1860201fddd9981a30a37d83b44eb2a7ccce89a1c4905`  
		Last Modified: Wed, 22 Apr 2026 02:19:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:72b3429d2d46269501813b6e7a6b8080fb40c581bca0ae2bfcc95456e2d6c186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7470340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce31bfbbea09ba6f41d714f7ba44a5c996291c3a4f174b2035e677f02d4c735`

```dockerfile
```

-	Layers:
	-	`sha256:dc79ab13ddf7b21ecbff74865efb4e73d3d1d49cabc3c4843104e34e055851a4`  
		Last Modified: Wed, 22 Apr 2026 02:19:21 GMT  
		Size: 7.4 MB (7444607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0b0c359ac0d04e15495c9f200afa08be35c8c6abd9e7a2f2a997273c44e0db7`  
		Last Modified: Wed, 22 Apr 2026 02:19:20 GMT  
		Size: 25.7 KB (25733 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:0e2a3792de6906780c2391d1ed4c8f84c5bb3d304c3a3d60d0f26d45ab96888b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249212936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f8c14b06d4e4fda7b15ab6337eccc40877aaec10e1e659f6448baf5893f8327`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:29:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:29:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:29:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:29:27 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 02:29:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 02:29:27 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:29:58 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 02:29:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 02:29:58 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 02:30:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 02:30:01 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:30:02 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:30:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 02:30:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 02:30:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 02:30:40 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 02:30:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e921237880038077978485833f958f4cb6fe7cf35b55e5d3fcef9da28065c10`  
		Last Modified: Thu, 16 Apr 2026 02:31:28 GMT  
		Size: 91.6 MB (91632998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45cccf32f1e514d06337c765407fee36f0346212da4934180626a4d58c9e76e`  
		Last Modified: Thu, 16 Apr 2026 02:31:25 GMT  
		Size: 20.0 MB (20030552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c827a7ce8871e86eb0b97d7651119d8715a4774f01fe05aae7131d8d3e52e3`  
		Last Modified: Thu, 16 Apr 2026 02:31:24 GMT  
		Size: 4.5 MB (4517725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab37e67e76da1b5cfc8887cee39cc7def69ca86b48ae1b96dc1494f1ccf9ad5`  
		Last Modified: Thu, 16 Apr 2026 02:31:28 GMT  
		Size: 80.7 MB (80693648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934c95ed012c6fcfe7f411137eeb5154d0e14a2f6f31930cc063409ddbcc032a`  
		Last Modified: Thu, 16 Apr 2026 02:31:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f681a982441130245b58bd9fbf08a8e994ff398bd2f2126ace53ab0528266e86`  
		Last Modified: Thu, 16 Apr 2026 02:31:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:b007fa0f57546c6266fb4c48bf05d964ef3e2100d207751490151a04eda06d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7453036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a30744530d0453ea59a6612fca94437596d42fc6d139e1342312562b9911ed`

```dockerfile
```

-	Layers:
	-	`sha256:2533729059155840b101e2c19c784abbebb08431656d82df2dc73d15e9cb9ea9`  
		Last Modified: Thu, 16 Apr 2026 02:31:24 GMT  
		Size: 7.4 MB (7427387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bff3f3d87a8d4fbd87aa4146c72ea849fa6d4052ffa6df30187dc140fba18c3`  
		Last Modified: Thu, 16 Apr 2026 02:31:24 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:f820df9f1d33f0f902188fdf4c428b184dd82f1d04770d528d261e36489f5357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233607956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9517db6662ab840f43515c4b2cc19b9af410bd869354b2ec3a541c73730b243`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:34:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:34:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:34:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:34:42 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 00:34:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 00:34:42 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:34:54 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:34:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:34:54 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:34:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:34:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:34:56 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:35:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:35:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:35:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:35:11 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:35:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e6a078c5294ff2580dbfaefc5aef8edea3a70059ad98f2fa9ec22eb9d97069`  
		Last Modified: Thu, 16 Apr 2026 00:35:42 GMT  
		Size: 88.2 MB (88233835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c273abebe7c2309d222a4bcc9b4d5234a75a60da2412a71a5d4dbfcc1b8c9920`  
		Last Modified: Thu, 16 Apr 2026 00:35:41 GMT  
		Size: 19.5 MB (19466749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79f9a59840891b8a1b0ebc056e134b9f3be89feaf54135ec99f5cefe626251`  
		Last Modified: Thu, 16 Apr 2026 00:35:40 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26c9fc7223c076d81a1105c93fbf321d1999a223b8a0daf62b7b007a7aaf845`  
		Last Modified: Thu, 16 Apr 2026 00:35:42 GMT  
		Size: 74.2 MB (74240454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27249e6fe3804303b792a78611fc93a41ae9369dfd1c1f5519ccc2a1e257273`  
		Last Modified: Thu, 16 Apr 2026 00:35:41 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba23a7a5f87e5c15249e857d19582777651eb567ba585d1af212a06d0c8fee7`  
		Last Modified: Thu, 16 Apr 2026 00:35:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:30c874624edfe43a8abe7fbe2956893d339a99536bcc6d5fc6a6873d71a46b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13698bb8a2aae892fea9d7d4447714aa0edb6ecaf0f862c4156df53ece0d98cf`

```dockerfile
```

-	Layers:
	-	`sha256:419dc1a672c572a3d30dea6126ff1002e355b51ff5748554af94c3b1d4ff0547`  
		Last Modified: Thu, 16 Apr 2026 00:35:40 GMT  
		Size: 7.4 MB (7414752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80672191aa11d39766bd05f67feb97c4c5f16d61f5c34b617e4131d9a91c484a`  
		Last Modified: Thu, 16 Apr 2026 00:35:40 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json
