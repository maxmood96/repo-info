## `clojure:temurin-11-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:ea525f6669eb4f4f5b65b9f770dc72d9e6e0dc1bc4caacf2cac41f0799f73465
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

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:acfcd220b44fca1ec9f858bcea7ce706fa495ea6740abd75579f58b518cc2573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221711550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28980b9d5b88ac83794428bdd63e084ed775796ff3efd1cd0f24643cb14e41d8`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:02:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:02:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:02:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:02:32 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:02:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:02:32 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:02:50 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:02:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:02:50 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:02:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:02:51 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc7a73373a5f4a873ddffdb5097ee7197bee9840aca3f38f38fea575c0999ee`  
		Last Modified: Wed, 15 Apr 2026 22:03:13 GMT  
		Size: 145.8 MB (145806793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689c04710851b2bd8eae956dfdd297768375feb9e31949891cfc3c194cba6dc4`  
		Last Modified: Wed, 15 Apr 2026 22:03:10 GMT  
		Size: 22.1 MB (22089180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58cd54bcc1b14e96c8e8de2e252b24e0a775a123ac42fc6ea9dd2246f461e9a`  
		Last Modified: Wed, 15 Apr 2026 22:03:09 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ae2b060ccc9553aa3d97226241e6d472b66b2b6f6995c1c019a59fc63637fa75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb97907d72e47ef0e97041d9dbdb4d843414fd30f8ef0d21ed47d0fb89f403be`

```dockerfile
```

-	Layers:
	-	`sha256:0217e8bc1f3c1846f7f3615c173b0a763b44741232e8ad6893065fe1c40c7a9f`  
		Last Modified: Wed, 15 Apr 2026 22:03:09 GMT  
		Size: 3.8 MB (3835668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa35738d4d502d250bb7d1af14f3f44ad60e2b69eec9d3360103e776fe161106`  
		Last Modified: Wed, 15 Apr 2026 22:03:09 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8f01fd3bd7cb1efa79cefb6a77b24d7f4e7e407b12562e8a712ef40819b8984a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.1 MB (219108139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b72dcc0eaf9743c7e6f484d5b804040717c303d5947e5284fe5dec434975593`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:13:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:13:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:13:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:13:51 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:13:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:13:51 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:14:09 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:14:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:14:09 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:14:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:14:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e06c67851d2efe4d528413942eeb5edde1e1482aa3ef8d75d1175e75e625e2b`  
		Last Modified: Wed, 15 Apr 2026 22:14:33 GMT  
		Size: 142.5 MB (142500803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b73111cfea5d0e6974230772a81d534b5dc6c7bea608fdb231cc9b73091b872`  
		Last Modified: Wed, 15 Apr 2026 22:14:30 GMT  
		Size: 22.4 MB (22424325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1dbead921db3d284fcd1ed947a98cda2b3da27456370050268b9c90b48490d`  
		Last Modified: Wed, 15 Apr 2026 22:14:30 GMT  
		Size: 4.5 MB (4517723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:57266fda63f70126f225e8e1c4e208c03de17efeab56cfc38a1c5de690fd128a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac354e775fa7a8bd69ef6d0d15001a5b84b42fc23254c35682c42dfa5fc7281`

```dockerfile
```

-	Layers:
	-	`sha256:b16dd5e7777b0af9fea41ea0a9648890a93d92fae01e3e99f190eee5f66c3230`  
		Last Modified: Wed, 15 Apr 2026 22:14:30 GMT  
		Size: 3.8 MB (3837163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f09ede90f7ef42756ec095f178fe260472f235764a17e8644f5cb7cb6643fa36`  
		Last Modified: Wed, 15 Apr 2026 22:14:29 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:c51ca16048f792286fd6667347bd97f1f48d45a6c19e27b40a43765e866e28cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.3 MB (209274952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5d4ae1cfa8c3ebd8452d9e22616a62213b447a4ec2ed813e0fe703714626e9`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:31:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:31:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:31:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:31:24 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:31:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:31:25 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:31:58 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:31:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:31:58 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:32:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:32:01 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e47589c6fe4c4dc982ab170f9b8ead6b8f83c6423e7987728feb0248d380cd`  
		Last Modified: Tue, 07 Apr 2026 14:32:43 GMT  
		Size: 133.0 MB (132997689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb86ce699d487a7da2ab09374c68289fd81ef2f9c9fbe1f42f8ebbf71d278eb`  
		Last Modified: Tue, 07 Apr 2026 14:32:39 GMT  
		Size: 18.6 MB (18640804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73709d88bf18bf1f0b82842cb606809237adc1331b3b7d3b3b02f7adfc59209b`  
		Last Modified: Tue, 07 Apr 2026 14:32:38 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2cf74708967b3e8f11529fd218b10fc4cbf58c5d59ec24f62913f5387623e9f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b36425b8a2d2a7d79a4f496b8a166ca5ea09216e162c154822f51f3abbecd3`

```dockerfile
```

-	Layers:
	-	`sha256:bba5b32f21c359025db00ffdffe2f8d48fe07105ef3618508f5eee0ca7044a59`  
		Last Modified: Tue, 07 Apr 2026 14:32:38 GMT  
		Size: 3.8 MB (3836053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80ff40483df3ddfeeba95842d4fc8d095520fe8d34a31b0002e172e4323c9815`  
		Last Modified: Tue, 07 Apr 2026 14:32:38 GMT  
		Size: 16.4 KB (16407 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:2bf79a6426fb8a48368001be4c2975c62c71d432eb22396c9b188a7e54ff2f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199071386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1e1c7ea4a1bd9ceea47e27f33e186a26d49276bb9d89572623a6f9be48a699`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:39:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:39:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:39:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:39:58 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:39:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:39:58 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:40:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:40:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:40:14 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:40:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:40:15 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a0f6af54b41978b4b00c1cf75bd9972713058d469f37803b6fe31ba2949998`  
		Last Modified: Tue, 07 Apr 2026 05:40:42 GMT  
		Size: 126.6 MB (126562219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966b00b54f541f2b1cebc9021034d726555986d98deed7f7aaf9917bcd009da8`  
		Last Modified: Tue, 07 Apr 2026 05:40:40 GMT  
		Size: 18.6 MB (18626311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af2cd9c475236055f22fe658eabf0062b5932c10f93fdad2951640b0afd38e`  
		Last Modified: Tue, 07 Apr 2026 05:40:40 GMT  
		Size: 4.5 MB (4517720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:268d7bff08303b8124b1fa9f7834c5fcd9848d5e3f505852e9e9edcd11984e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3848463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fa2513d59243be2746dc2e7a351cabdf326975a997ecd630314452df8c25a3`

```dockerfile
```

-	Layers:
	-	`sha256:7c4b0935d9d5d9528f5c0e8d10588c7763c5b2173e44ac6f0372d9c1aebf0767`  
		Last Modified: Tue, 07 Apr 2026 05:40:40 GMT  
		Size: 3.8 MB (3832099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0ea262f96640e7345cd327979e8fb14e86ea40ac6594e5a6cac7c5cfecec9f0`  
		Last Modified: Tue, 07 Apr 2026 05:40:39 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json
