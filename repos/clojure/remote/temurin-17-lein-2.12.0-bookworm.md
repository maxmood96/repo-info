## `clojure:temurin-17-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:deab3daa8ec22412719f6f855463909d62afb02fac6ce6217539cececb8914f8
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

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:54b19a9ad49977355caf39d99ec2326e8914689a9786d0025989e524b933763b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218438578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a3a538f4f0e5d940a33cb733695d8671ca221d8872654255dd41e45acf03c4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:14:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:14:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:14:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:14:13 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:14:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:14:13 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:14:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:14:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:14:28 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:14:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:14:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:14:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:14:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4b49c5eafc4a7b97e021e352567778f018ebe0e4a744f419c711fa431576d4`  
		Last Modified: Tue, 07 Apr 2026 03:14:53 GMT  
		Size: 145.6 MB (145628717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8b908f8de0a8bcadd46819a2c1f2ed47c64c27bf600e43012ad06791533655`  
		Last Modified: Tue, 07 Apr 2026 03:14:51 GMT  
		Size: 19.8 MB (19802850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b1568cf8aa17c02ff2f5babc8a819c617acb3370d5f75c374ea9322aeeb6e2`  
		Last Modified: Tue, 07 Apr 2026 03:14:50 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc065a2804d8df69ac8daa87d32556e87f341ab73e985d90543e87fe27dee3`  
		Last Modified: Tue, 07 Apr 2026 03:14:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fbe055f8f0ea0b113a978a1b3ad9f7d9507c5f6d5f342dcec49977ce0aa1989c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707cbba2a9ad653ab6a0150dcbaa5550cd3a6d152b8e63f59e6d02a678f82e91`

```dockerfile
```

-	Layers:
	-	`sha256:045f363085856ecee6252e27dca1c62b4bcdffdd51fe4fe0453b1f719de086c7`  
		Last Modified: Tue, 07 Apr 2026 03:14:50 GMT  
		Size: 4.3 MB (4281731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56dbb99cac7bbe0662f06152cc7bed95e879f2227ab952f338271cdcea9b7b1e`  
		Last Modified: Tue, 07 Apr 2026 03:14:49 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1aef423cbd973a351ba50a2d2b11905f78b33d72b6124035f8e8ba234a58ebe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.0 MB (216960471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10126aab6025debc4192a2c9e57ffe50f316d27338b0723eaa535a96319ce4cb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:25:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:25:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:25:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:25:05 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:25:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:25:05 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:25:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:25:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:25:18 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:25:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:25:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:25:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:25:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf427253fc8728be10ed43eedf6a0e82c152a8dafb35f202930abd3366b96b6`  
		Last Modified: Tue, 07 Apr 2026 03:25:44 GMT  
		Size: 144.4 MB (144436252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9758ebed5bb36bfd0f860a28ba909ff3e5c25fb229ed8d82ce88dc6982bc1ab1`  
		Last Modified: Tue, 07 Apr 2026 03:25:42 GMT  
		Size: 19.6 MB (19632773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfae1b7a471508c2463e5f1ca38debc9d7d3a6cc9115a885abb2b716fdb6ca0`  
		Last Modified: Tue, 07 Apr 2026 03:25:41 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971afb9165c35be15d504613bce02d0d4766ada8ef452755e8cb05cbcb033d8c`  
		Last Modified: Tue, 07 Apr 2026 03:25:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8bc61e2de46f60127693a66945dc61c4f5125bf9b44d07b5e048ab7d5a920810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4299835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9c934a8b360cc0f2e72b0ce8f05e42bc240c57fdf885892f4738f0d1646efc`

```dockerfile
```

-	Layers:
	-	`sha256:245ec7b25406be8a28be0b31f63a357c65240cd2b4dbafcfdee0b6defd30e523`  
		Last Modified: Tue, 07 Apr 2026 03:25:41 GMT  
		Size: 4.3 MB (4281346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26b63d67f5550c83ac645d2d270e1ca33d9e726e4599e7128221bc79cd0b8693`  
		Last Modified: Tue, 07 Apr 2026 03:25:41 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:6d0c746bfd2b5a65dbf0557e91f4f8e6e257d1f62216a886f39d6d85b7f28bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.3 MB (222316863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d9a65553ed7ca2abfd7dbf0528289065eabe64f88ac3b636e3dac6564d59ac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:24:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:24:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:24:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:24:37 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 18:24:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 18:24:37 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:25:08 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:25:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:25:08 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:25:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:25:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:25:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:25:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ee64ed0afeae873fd2f06096ddec7906316112c3693f7c534e02be26621b37`  
		Last Modified: Tue, 17 Mar 2026 18:25:57 GMT  
		Size: 145.4 MB (145438236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f3da28da228c484847ac03e7e497fbd147e1106eceb74d54eb4eda08d6c5e6`  
		Last Modified: Tue, 17 Mar 2026 18:25:54 GMT  
		Size: 20.0 MB (20023745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b9488a0403f4e4f33a46701d40df2112cf11b148852dab93b3f591efe624b3`  
		Last Modified: Tue, 17 Mar 2026 18:25:53 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca356e525aa4faa1d0db4ad7eb55fcccbddc06a5f7b08daf21e01517377ad0c6`  
		Last Modified: Tue, 17 Mar 2026 18:25:53 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:46a03a6efc0df3966aa3924b2a6ee98994b32f584e0d708408f5c2dad0c5f7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5561336930c342290e9b87e41db8b89e0f5d631f19bd2fecfecc18019c45394f`

```dockerfile
```

-	Layers:
	-	`sha256:03ed75bee1fa1f61f971c9873a191bba5584d076070136a6bea6570abd46447b`  
		Last Modified: Tue, 17 Mar 2026 18:25:53 GMT  
		Size: 4.3 MB (4283592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c61b6fef6a305a63698315528d0684c3d327bfd25b9883a053cf60f7f65498b5`  
		Last Modified: Tue, 17 Mar 2026 18:25:53 GMT  
		Size: 18.4 KB (18412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:d13f02b34e0f0a7978e08b87e35eb466df2544e9d22730eedd88941c0d7c2ffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206756335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f3799362e22aa2e1419d5d93accf1e5f68ccbd29bd1a562ce6e639b073d32a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:41:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:41:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:41:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:41:15 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:41:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:41:15 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:41:25 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:41:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:41:25 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:41:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:41:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:41:27 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:41:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4905caba1cd8b4783ed34ad9348e745f4d17dad9b73e5758f9e1b99a22ade98e`  
		Last Modified: Tue, 07 Apr 2026 05:41:55 GMT  
		Size: 135.6 MB (135626841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7088d58fbf4e4faa7c58fd24024e00e871a1f8724f4c46f2bd964a84533d24`  
		Last Modified: Tue, 07 Apr 2026 05:41:52 GMT  
		Size: 19.5 MB (19463225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071c3d00227bd662334eec2175e33b705d331bd84986044636c8e8e45d25dd74`  
		Last Modified: Tue, 07 Apr 2026 05:41:52 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb4dbc6b7b3e821359c597cede84c0ab6f3f75a029d34a5fba8549f31710d8d`  
		Last Modified: Tue, 07 Apr 2026 05:41:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5bd3479990ac981a7fb042520e773076ed34aaf700da2fb57eaa57bd48d9a72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4291913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41fefac8312e4f141d82b78d725c757eed813d6fb2e71c8d3ea01e1c63528c86`

```dockerfile
```

-	Layers:
	-	`sha256:9f9a8867d22464c061062d5e64a6e9f6a8557c5fc5779d8efb94b85108cef577`  
		Last Modified: Tue, 07 Apr 2026 05:41:52 GMT  
		Size: 4.3 MB (4273545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92722ce3fce7e7f11c6cb648926e39ae43af986c8d2a034958992350738f56cf`  
		Last Modified: Tue, 07 Apr 2026 05:41:52 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json
