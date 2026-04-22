## `clojure:temurin-11-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:d4b0725c3f162fd738eb0b62096243a158a0421255a56a1e80e2e021837e2282
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
$ docker pull clojure@sha256:e6cc51867c01730f2d4bdac8991a9cce779b741a7dc5825d33a9659c1edc5bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.2 MB (215233367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f848555b723f628465ebc5dd8d1cf8da52a927069c9ef0fbc43477d338482365`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:20:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:20:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:20:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:20:27 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:20:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:20:27 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:20:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:20:44 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:20:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:20:46 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2ac0a011ff98d6e10c248c6872e62b858b201f24d4b269a12f127c9cf2e82d`  
		Last Modified: Wed, 22 Apr 2026 02:21:06 GMT  
		Size: 142.5 MB (142500862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca19c4fcdf62c76e13356c8fa58b1f03987a0572c60afed9e4b08d6d85cec2e`  
		Last Modified: Wed, 22 Apr 2026 02:21:04 GMT  
		Size: 18.5 MB (18545469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1a0accc032dcd3efb9785bde2a9eec959fdafaceb504b907e1c044fc0b5203`  
		Last Modified: Wed, 22 Apr 2026 02:21:03 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:57d788536080874a537ce988ed566945f7391465f84cbc16d7f431f0496895b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb89a8f0abb7bd73fe875f7a88b6d13fc965ffc5911b1f8030bed49cade7711`

```dockerfile
```

-	Layers:
	-	`sha256:1bd106158f23baa0a7987ea0cfb42838ecffeabd0c1479ca9964a0a3fb639c93`  
		Last Modified: Wed, 22 Apr 2026 02:21:03 GMT  
		Size: 3.8 MB (3837163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18ae0ee9b8b1d2d959b3fc1b084b654eeaa1c198b66a6baab5a585e7a4656a9d`  
		Last Modified: Wed, 22 Apr 2026 02:21:03 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:c804a9ef25964f6424a2cbaf90894eed5f01a902c9a578a258d9f756b600fc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (213025607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8afe69c8e50f33456f58e528b7111b79c86f6f167946a193f0b99c42c8682b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 02:42:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:42:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:42:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:42:12 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 02:42:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 02:42:15 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:43:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 02:43:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 02:43:13 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 02:43:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 02:43:16 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76042bd72cd27c05c77d44bd98d120db7be804788d7f01116ecc64346fb992b6`  
		Last Modified: Thu, 16 Apr 2026 02:43:49 GMT  
		Size: 133.0 MB (132997414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5cfa2d033625a0dc5349375145e92f80e24398d79729f267989114dd0b3eba`  
		Last Modified: Thu, 16 Apr 2026 02:43:49 GMT  
		Size: 22.4 MB (22391736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895a87cc9973d1626c4e610018f3a8fc2632c27ac7f2acc2fa7edf8b5857ab51`  
		Last Modified: Thu, 16 Apr 2026 02:43:48 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bd34fa11d9cfe0078296236e6cecfdd9618382536790a815fab1ab8f9c6827c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15967c3b7ef2c3dcc1ae3bb4490daea2e76aea7f5d8e686fea78809b8318b63`

```dockerfile
```

-	Layers:
	-	`sha256:1a3dd7f6cdc6a5cfbde7c06307a1a8dfaf66eebacbe7e230598fde773e21e516`  
		Last Modified: Thu, 16 Apr 2026 02:43:48 GMT  
		Size: 3.8 MB (3836053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2b1cd402997250f96d35a46f584de266d4305c3b68d5e3a6c1333e669470af3`  
		Last Modified: Thu, 16 Apr 2026 02:43:48 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:3f93cb4748572483429bce7f2a9855f357ab5f0009322ee57e701141c5bf62b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202227267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e283bf6c8190df42a078902928afd27e89bb69dce322b68c3b7067f2499b6f2`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:35:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:35:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:35:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:35:54 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 00:35:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 00:35:54 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:36:12 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:36:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:36:12 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:36:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:36:14 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748b9567fa4d83a1f40eb87cf693e4c66a4a867a85d2af69dcbec8df6c50004e`  
		Last Modified: Thu, 16 Apr 2026 00:36:40 GMT  
		Size: 126.6 MB (126562154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f607d2fed6ad96fe019c5d8de53eb66f372fedc709334852e90b217d1da75e`  
		Last Modified: Thu, 16 Apr 2026 00:36:38 GMT  
		Size: 21.8 MB (21782226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5878da5040330d0e3486646be47d222e7aca68e8c196b71202114acf657103`  
		Last Modified: Thu, 16 Apr 2026 00:36:37 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:82cdeb3f5143c1e60cfa269424c2b153b6aea36cc00479e2f2a85efd917620ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3848463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8bf6b43d7cd0be49eae66395718d0490881952f4fa5462ff2f5bfdcabc172f7`

```dockerfile
```

-	Layers:
	-	`sha256:a246dbc56d68de9b195abbd9ab57b7eae5eca32ef943f813c18fd76c0392bc11`  
		Last Modified: Thu, 16 Apr 2026 00:36:37 GMT  
		Size: 3.8 MB (3832099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1caeba82af19f2bbaff9e54cef540807429ea86af99d41479cea3acab6535a54`  
		Last Modified: Thu, 16 Apr 2026 00:36:37 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json
