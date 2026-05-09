## `clojure:temurin-11-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:2482f07c526f2c4e190cbf1b7331098fef1234c81bd6b58a53ed4b394078b838
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
$ docker pull clojure@sha256:a6430671b9be4047e3ed6e3d2099c9fe377009aef1e68f40b0bf23db109da411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218291862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625c02e3448675815832ce7a51288442de9402fa12bed3ac9c8ba4543c4bb5a7`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:15:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:15:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:15:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:15:45 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:15:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:15:45 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:16:02 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:16:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:16:02 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:16:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:16:04 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68df4312c9f12c6bbfb1fb69a61d4048a1a82240966def62b29a2608720fb8ee`  
		Last Modified: Fri, 08 May 2026 20:16:25 GMT  
		Size: 145.9 MB (145886195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f1cb50d4bef0f7bee976db4fe5737217d808cd2d1d0219977ba04378c30a5a`  
		Last Modified: Fri, 08 May 2026 20:16:22 GMT  
		Size: 18.6 MB (18585591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7866c531db5a0bb92e37273b7bf023bf96ab9c46a9ff6920beb1d58ab18142`  
		Last Modified: Fri, 08 May 2026 20:16:21 GMT  
		Size: 4.5 MB (4517724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2ca08d8c23b6732e2fba7b0fe74177bd3c7db502672183d924ee08f200b667ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddcee15dce908f818f0c9f9f529f5a838ebc6948ffbd6b9b15538cdba7861d10`

```dockerfile
```

-	Layers:
	-	`sha256:f3f098727e7192b9339cd0e4a8749d2442e219364d5d4c0d4be42a633d5c23e0`  
		Last Modified: Fri, 08 May 2026 20:16:21 GMT  
		Size: 3.8 MB (3835670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dec0146c97e5d4b427d77ea50e81b3db39cb2e2bba8ef07a33bb659c3879a24`  
		Last Modified: Fri, 08 May 2026 20:16:20 GMT  
		Size: 16.5 KB (16518 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:772b89c5d32b37593bdf332d270b613061e946cded39826a5d5d16e0d19500ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215314830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6440ad3b2ced669ab0dc412c9caa3a95f03b2c1f034f2db0c841bbdc3bd6d0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:20:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:25 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:20:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:20:25 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:20:41 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:20:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:20:41 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:20:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:20:43 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8869a605edc468970ddeda3843e1c5a1b457f6e3633d0433d19902a1f2dcfc9`  
		Last Modified: Fri, 08 May 2026 20:21:01 GMT  
		Size: 142.6 MB (142582199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bda0545ba7f8ea69ff1b2dcff6ec61ece39a76548f085328a5c42a12826b9a`  
		Last Modified: Fri, 08 May 2026 20:21:01 GMT  
		Size: 18.5 MB (18545410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e35f193d5d02d4633e24d916bdff786da3a587d4d3ff9093a87dc5017137b1`  
		Last Modified: Fri, 08 May 2026 20:21:01 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:78e832b17bf64e85429cf3ffef9a1d2b07909893b17b43bd121ea620536bbfa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a78e9d6e7b5a8efc90ca8eafe9fafd98e8b80aa760781b44fde9df0215e3a14`

```dockerfile
```

-	Layers:
	-	`sha256:6de3be67177e949e9aa46051d54accdbd3753dba9428d26d60e1d9e789380171`  
		Last Modified: Fri, 08 May 2026 20:21:00 GMT  
		Size: 3.8 MB (3837165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e04d43311200ef8f563dafe83f1b51d819dcb1fe88f24e712df7155a901efd4`  
		Last Modified: Fri, 08 May 2026 20:21:00 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:528f4bd7979b0889754f95bde9b6904c33fe20e212f5a7107e1751be8b06c776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.4 MB (209392118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367a1ab62172ebf3b4ee71bdd0f8dfeed36a2718cf860cc46a748099d49b5d26`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:26:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:26:20 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 09 May 2026 02:26:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 09 May 2026 02:26:20 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:26:50 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 09 May 2026 02:26:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 May 2026 02:26:50 GMT
ENV LEIN_ROOT=1
# Sat, 09 May 2026 02:26:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 09 May 2026 02:26:53 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6819a6f95dd2e4192ab6b7dae90a40976321dcde2fda4665eb71bbac73d5122`  
		Last Modified: Sat, 09 May 2026 02:27:27 GMT  
		Size: 133.1 MB (133110167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f506d4c8c4f2046dc22e4a52e3389658ffe7dbe1cd5c02c370997da5803b15`  
		Last Modified: Sat, 09 May 2026 02:27:24 GMT  
		Size: 18.6 MB (18640994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7056bc111a59aa3385107d1b4adf98074024ec9a4428bad0be8fc32c2bf7d7bd`  
		Last Modified: Sat, 09 May 2026 02:27:23 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:af99f6b7613cced4cf2b826cc4e719eeb95b7defcc8f67ea01241c96c21f2707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19403bb8cad2bc2b7df00059e594ff58bf5c9f5dc7c5d9ece977eb667fdb8c2`

```dockerfile
```

-	Layers:
	-	`sha256:516fe59800c8eddb90514893f2f385fedda7368a861e46c3930c4672aa254167`  
		Last Modified: Sat, 09 May 2026 02:27:23 GMT  
		Size: 3.8 MB (3836055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e72b524fda22551526127d0f6495e2b3f6bd8d9190b72ff6ba0c28dff561e35f`  
		Last Modified: Sat, 09 May 2026 02:27:23 GMT  
		Size: 16.6 KB (16561 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:c00ccfce3e4aa4e23ffdde4d5f10550d52d720dc21ae756baaa8d8c5169e3b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199168560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0667dcc25d4836a00dc4cd23eeca971eeab6be573ee49a8a3c46634465b0e1d9`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:13:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:13:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:13:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:13:25 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:13:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:13:25 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:13:39 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:13:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:13:39 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:13:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:13:41 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3141bdc6a188297dcde1fc53d547484d702825156fc236e4ab9572430cd65294`  
		Last Modified: Fri, 08 May 2026 22:14:07 GMT  
		Size: 126.7 MB (126651743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03255a5036145bae3137f7d9bab831033f2a7a80a63098d3435892a62215bb40`  
		Last Modified: Fri, 08 May 2026 22:14:05 GMT  
		Size: 18.6 MB (18626723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6825f82e5c8d92d85b1d5d72b61c1df36ff73d701e6b176792849402cbebac89`  
		Last Modified: Fri, 08 May 2026 22:14:05 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9b40cafd5eeb45087977c309bd11c1d2268feeea8a62f74638ec1b7468469b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3848618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e9767f4db21e31c3d3496af082c80af4efe5f2d26763776fb77ae841a0c22a`

```dockerfile
```

-	Layers:
	-	`sha256:9a1febec2e6c606bbdeba0440fad561f4c8a29e7bb94b012a56b3097890dbd3f`  
		Last Modified: Fri, 08 May 2026 22:14:05 GMT  
		Size: 3.8 MB (3832101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c73121323635ed9105a16b9a69ed27bde70b20a33a2c8dd94703e3cdac9d55b`  
		Last Modified: Fri, 08 May 2026 22:14:05 GMT  
		Size: 16.5 KB (16517 bytes)  
		MIME: application/vnd.in-toto+json
