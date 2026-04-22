## `clojure:temurin-8-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:1e81f7e702d1e769ecd79314bc672e6c4425632c3e0a05a35b54b95475bfaa94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:843ef48b181e9d04127190f5a995dd7262ecdb3ca9420c67f492ad4caf419ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127982990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1120be88e504818e8b3beef8865ab8ed28a908ca5ad0204ae2007c2316f76581`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:14:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:14:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:14:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:14:57 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:14:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:14:57 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:15:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:15:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:15:11 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:15:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:15:12 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d995cccfd481dc9559de151bb1f79bbc67d7843ef28036db69f60b1dfa9a4cb`  
		Last Modified: Wed, 22 Apr 2026 02:15:27 GMT  
		Size: 55.2 MB (55170085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5337efffa9542f5ebe8d854057660e4e5861b462070c07b6c4dad6d27a5f71fd`  
		Last Modified: Wed, 22 Apr 2026 02:15:26 GMT  
		Size: 19.8 MB (19806549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07189b703b81bac7e2fa5c114ca8ebc82afc61895640fd0d25ba7d9ed43aa065`  
		Last Modified: Wed, 22 Apr 2026 02:15:26 GMT  
		Size: 4.5 MB (4517696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0fa35255e1ec4a72873f5b3b8b334966711c5d5eda3ace16a7747cdb79695997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd428b967a67d0d86a0a0d0cbed52ce6ba302339957ee091fa42007d62d6dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:57afc89aaf3ebbe1ecd0472c9b8e3087bbf508c1ce5adcfe3dfd472f6517176c`  
		Last Modified: Wed, 22 Apr 2026 02:15:26 GMT  
		Size: 4.4 MB (4402720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e6c5043956e88702efc139f1d9a8ff78ba0ecf498446d05a6b9363dd7180c60`  
		Last Modified: Wed, 22 Apr 2026 02:15:25 GMT  
		Size: 16.4 KB (16368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d8c28dc5792339f3c79ff24653c07e16028f9bb5b4b258089760e15f33d9d9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126779487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59518934517acbace92868893954da3eddbde0a738d04a7ed892ed380158d85f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:18:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:18:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:18:23 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:18:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:18:23 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:18:37 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:18:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:18:37 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:18:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:18:39 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04227bc718d6a7834d7c476f5e87c0977933d6fefadf22006ac42c103c39f566`  
		Last Modified: Wed, 22 Apr 2026 02:18:54 GMT  
		Size: 54.3 MB (54251616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ddb9c012da22d82870813cbbd4b0c85a60e6b980b3a913f584b4e01dc271e2`  
		Last Modified: Wed, 22 Apr 2026 02:18:53 GMT  
		Size: 19.6 MB (19637027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654172a31313172ce1cbf72cc1ea61b60677effddf121420d620ba6576bd6ed9`  
		Last Modified: Wed, 22 Apr 2026 02:18:52 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b1dc17cf90ad79f268b29208ac33e55261a36caed9442f2cd101788ef7c05baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c31c955dcee260ae5f969ce41d1763c3ffc31fb5250eba87011357a36bde4dd`

```dockerfile
```

-	Layers:
	-	`sha256:30f04036cdd2ac035b3c84cfb265a26649125651fb21652dc7dbda5fa9a3f0c4`  
		Last Modified: Wed, 22 Apr 2026 02:18:52 GMT  
		Size: 4.4 MB (4403035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60e1a3b27144886e6800ada82cf4477d6c39c41d47385e3b864617690f7632d8`  
		Last Modified: Wed, 22 Apr 2026 02:18:52 GMT  
		Size: 16.5 KB (16491 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:41712afad55756ede5691480f0096e0db5affc14d2fac5e748b53f937aa8f8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129535605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af816680fc049e73dc5655f5ae09e767a17a575c9c8ca92c596593ef85f3c592`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:30:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:30:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:30:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:30:35 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 02:30:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 02:30:35 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:31:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 02:31:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 02:31:00 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 02:31:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 02:31:05 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f15e3be605c892a466173dd560f0c76f39571ad77e4b26767f367028c3c142`  
		Last Modified: Thu, 16 Apr 2026 02:31:34 GMT  
		Size: 52.7 MB (52650392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8347a7333900f52245bdebada5e7fd455d136d2668c7420b2662487686276df1`  
		Last Modified: Thu, 16 Apr 2026 02:31:33 GMT  
		Size: 20.0 MB (20030505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4f8381b4a8f1f6498d588c1ef4674b347a4b2bba73ea1d009aa291a574675d`  
		Last Modified: Thu, 16 Apr 2026 02:31:32 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d3dafcefa9268b66ed7a1db99c8c4e606e2467ace1fc3d16b40d4c8cf2f4e11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4421590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3df418f312266bed407558fec0e3d968720ba90f6b18faf4b1ca6ae1266cbe`

```dockerfile
```

-	Layers:
	-	`sha256:727f7cd26c09879f2cedec263ebaf3f0afa5045e7356a04e60471d91a0d85823`  
		Last Modified: Thu, 16 Apr 2026 02:31:32 GMT  
		Size: 4.4 MB (4405176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1590a909f747ed7a768e4c0fd97879b5b17949aee8eeba301d1f48f7d1259696`  
		Last Modified: Thu, 16 Apr 2026 02:31:32 GMT  
		Size: 16.4 KB (16414 bytes)  
		MIME: application/vnd.in-toto+json
