## `clojure:temurin-11-lein-bookworm`

```console
$ docker pull clojure@sha256:02a01b425944bf3ef99a792736d47ace714860d149b5d6c61bd06e384da2ab96
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

### `clojure:temurin-11-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:93e83b592d3b1f1dddc3410e7096cd1ae361f6f3a17e5e8b66723424530364bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218616359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66c76eb69b79130eb81e34aa8b2aa388024dd671c5f40de2980fe084f8df2f6`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:13:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:13:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:13:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:13:12 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:13:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:13:12 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:13:27 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:13:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:13:27 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:13:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:13:29 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5dbf0b1b820daacf5d001a649b8507b3fb315cbfe79f2796c3d4124bb1b9b9`  
		Last Modified: Tue, 07 Apr 2026 03:13:49 GMT  
		Size: 145.8 MB (145806872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060c51b7eaf8a254d3799d02844743e828e8308994f94a3289120a4f0a25fcd6`  
		Last Modified: Tue, 07 Apr 2026 03:13:46 GMT  
		Size: 19.8 MB (19802886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba46435bd68b810f011c5e99cd94791699098765f273d0bac37d871c90c0608`  
		Last Modified: Tue, 07 Apr 2026 03:13:46 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:69ba747fa997f49881f593fc4d6da1cd95b11166d2b93cedce53030c33ff1b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4318254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ecb4d0a619746016886d63a6323de523ef8785f702b1a49617488422544c41`

```dockerfile
```

-	Layers:
	-	`sha256:c823eb810d797ad649216b51e381c50a44114d024b2f3cc6e9edacb1c09e809e`  
		Last Modified: Tue, 07 Apr 2026 03:13:46 GMT  
		Size: 4.3 MB (4301872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b115399f6edfae6d915fb82fba8ae04175d6161b83ad061d27fb129f32c872`  
		Last Modified: Tue, 07 Apr 2026 03:13:45 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8d9ba8e44979195c8f94d450d00cfabc8ddfd25220ab8cfca7f911c81b5d866a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215023919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cecf38d5640458dfcd1b08ef68cc54dc2bfebae79b2cbca625fe1d01f7387fb`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:23:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:23:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:23:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:23:49 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:23:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:23:49 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:24:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:24:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:24:03 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:24:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:24:05 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015dec85e584445b377158665f9e919e7468a49591ab782e3ecbfe756ab745c5`  
		Last Modified: Tue, 07 Apr 2026 03:24:24 GMT  
		Size: 142.5 MB (142500071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480959d23f9583c2e15bc92b3aec20bc4bfdacca744853261d44fd0d3c5e1a3a`  
		Last Modified: Tue, 07 Apr 2026 03:24:22 GMT  
		Size: 19.6 MB (19632796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f9fe73df6fbb4a097eaba7bd6d477d754cc965049a33e40cb836bc43cb894f`  
		Last Modified: Tue, 07 Apr 2026 03:24:22 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4595b93be0c270bcfa388cf2bfea0a4000f258508a1146c739927318147f2db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4318607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d25c9e675bd6a064df2a3d79443833f7927202561928787064bb3cee36dc82`

```dockerfile
```

-	Layers:
	-	`sha256:d6ed0747dbd6abf6eea15c76aca608ed5be5b5b59ddf4425691a6d3af4081eae`  
		Last Modified: Tue, 07 Apr 2026 03:24:21 GMT  
		Size: 4.3 MB (4302105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab7b6e0193f4d399dfc599a657adebf1153317ec94f4ec3ab2c02e89f0ca03b`  
		Last Modified: Tue, 07 Apr 2026 03:24:21 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:3b4d2bdc8b53bd8c497a677278ec8b7b0349e4ee58b0473746b79a3e292c2779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209874995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e1822fc63b6a09fc434a5a55e76268569fca85f4968e517d3a2cb042b01ab07`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:15:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:15:41 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 18:15:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 18:15:42 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:16:25 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:16:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:16:25 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:16:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:16:29 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbecbf7ecf5689b9ec9a2fb7833196c9e479474539bbea61e477b10fa3c1a715`  
		Last Modified: Tue, 17 Mar 2026 18:17:05 GMT  
		Size: 133.0 MB (132996700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dd04e70559cb76df90a8ceb375263190a926a089c2f5ede46d08083ab2fa86`  
		Last Modified: Tue, 17 Mar 2026 18:17:03 GMT  
		Size: 20.0 MB (20023832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36993198c99b4c1f071dbb349fac0b3ceb0d6e3db94e38a81e1960ada1986556`  
		Last Modified: Tue, 17 Mar 2026 18:17:03 GMT  
		Size: 4.5 MB (4517733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5269bb450d36bd2da660e8590921cea13fb95c29523b3bbb3c5837eef534ac86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a0b5f47947aa7b4d923366ce9f547f15216c719e82d9fb7baa33799fe45536`

```dockerfile
```

-	Layers:
	-	`sha256:a725a4bcc398157e479ae9dca5bf1e366070ae31bda890cdcd82d4f32c4d88f0`  
		Last Modified: Tue, 17 Mar 2026 18:17:03 GMT  
		Size: 4.3 MB (4303118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a10c8a435f5856d5d410d24e515d071354b93ff852671cf1b4830159c53cd3`  
		Last Modified: Tue, 17 Mar 2026 18:17:02 GMT  
		Size: 16.4 KB (16425 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:c6158af6ac6547dd93d5eb535244ba5e4de5f41aa00cd575cbd60b67bc378772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.7 MB (197691304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57afbba2b7bb955c72c901def364072ed1bd03ce58fb721ace42f649fb0fda2d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:39:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:39:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:39:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:39:04 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:39:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:39:04 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:39:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:39:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:39:14 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:39:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:39:16 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb33c5f4283b505686015d05967affc51b9431339e1afe3ce037f4fbcceab57`  
		Last Modified: Tue, 07 Apr 2026 05:39:42 GMT  
		Size: 126.6 MB (126562240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b65faa3a29110d8e54422ab7bb2e749c86533a4668a663b8e7a148cbb07eaf`  
		Last Modified: Tue, 07 Apr 2026 05:39:40 GMT  
		Size: 19.5 MB (19463191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deff174a9a4306a8589e1a69029a6eef5fcacbd5dda00511521e92b7bddf1206`  
		Last Modified: Tue, 07 Apr 2026 05:39:40 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:966500346fcf08e7ed6161f50bc23788eba10e17437dab917f0c7f9933f3b0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4310072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cf601b96af8b866630d46a373d0469f136a7ce86bf1efc24211bee78586072`

```dockerfile
```

-	Layers:
	-	`sha256:9ca35cd6d215c1e213980193fe5a99d6d407c7696675bc13b8f714e0aae9ea71`  
		Last Modified: Tue, 07 Apr 2026 05:39:40 GMT  
		Size: 4.3 MB (4293690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcd7b02f4c721abf6de0f46dfe028c934a7966f6d061ec25e60b5fe26b8bafff`  
		Last Modified: Tue, 07 Apr 2026 05:39:40 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json
