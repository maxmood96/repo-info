## `clojure:temurin-21-lein-2.13.0-trixie`

```console
$ docker pull clojure@sha256:ed82b96d85068b5474afff7df68e3505a3a731a7bbb5fead7bb722fb96349e2d
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

### `clojure:temurin-21-lein-2.13.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:18d33947f9f6a48ddbd2459a1cac1f4e4007a21fb04d86fc5e6c268b937cac4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230879633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820765e9782bd57f17b99b93a00dcac47186cb4ccdfdea1bd0fc073bf0e9e3a9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:19:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:19:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:19:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:19:23 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:19:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:19:23 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:20:34 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:20:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:20:34 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:20:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:20:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:20:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:20:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755602fbd69022b190d0e2cf641c314d21abe1ad06dadd5c49a8774030f3b1cf`  
		Last Modified: Wed, 24 Jun 2026 02:20:59 GMT  
		Size: 158.2 MB (158166915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd08af07ca1969bc3a39bc27f5abfa5f4936f405ed6705180fd6e80dde47e3a7`  
		Last Modified: Wed, 24 Jun 2026 02:20:54 GMT  
		Size: 18.9 MB (18879812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7abf8f8fdfa630acfccfea688e9e5ba4d2aa9a50ea5bb775fad6e65e93c0aff`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 4.5 MB (4515221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e618aadec40f8626dc9956e39243607b59d395c074e3c4730117340fa3c9c2b`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3bc95f190575bf4312fbc95edfd2ebd1c37204b673d67bcca0e8554c08d39bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3837390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a008ef3b916f3f236d22e84eb4e9e916621c020d6e56bd514332c6af2f07ba2`

```dockerfile
```

-	Layers:
	-	`sha256:3658ca0bfdaefe10a57589e2ae9b2cba3c72217fea4b0bbcfa5e7b9882791216`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 3.8 MB (3819672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ceee65d1861b58a3920f2ce18ff8511c1e238d1f0a459c28e6990bc5a7e1b31`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 17.7 KB (17718 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3e43489e0c6b3087818412cfe69ba5094ab4cee8e1f9c7f8c72cd951bb1eced4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229494881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3df8d79f045fabd8ecdf6f5a5a932726b946f6f91e60ff4c3a85711f7cc7c79`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:26:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:26:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:26:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:26:00 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:26:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:26:00 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:27:16 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:27:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:27:16 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:27:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:27:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:27:18 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:27:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2853fa5c58fd7137c6e377b68ff77f8b8653198204a7d2cb36ebd03aed101e`  
		Last Modified: Wed, 24 Jun 2026 02:27:40 GMT  
		Size: 156.5 MB (156461246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efdc618fb3586dd69dede9f869380a7d17746461acfbf6c0d9723715818d756`  
		Last Modified: Wed, 24 Jun 2026 02:27:37 GMT  
		Size: 18.8 MB (18839594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75db0e2b0ab6bd1f2de469a8ec1802c2d4e5d54e5fc2dcebe941f7fc89e59ad`  
		Last Modified: Wed, 24 Jun 2026 02:27:36 GMT  
		Size: 4.5 MB (4515217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6019bcca9bf043cf8a415d10f9481480ecb95a18a0d172410b2750b99bbde6`  
		Last Modified: Wed, 24 Jun 2026 02:27:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:507a91b3d54f4125e2518da49dc0efc7135301f0f5e12ce7ff8bf74c948e26f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3837751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca8dfd9d42ee4f8a0bbb31ee813d010eb803e0c2e26d5bc7681efa76c63fa57`

```dockerfile
```

-	Layers:
	-	`sha256:6dc60407baada80b5ef4e661d172d2c2a26c95a208509f5b5c254c4c18a8c6d2`  
		Last Modified: Wed, 24 Jun 2026 02:27:36 GMT  
		Size: 3.8 MB (3819912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88476c1a814babe0152bbe06ea1d9db1ac26de7badb74a5b1606c161bb846582`  
		Last Modified: Wed, 24 Jun 2026 02:27:36 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:ab14769b431f16a0a6ab95c589476021c80d4faac7f736afa5ce7adea03bfddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234933346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4e4786dc0651daedb080a89ce9a7ba162087af870616b772c44004ae17d31d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:58:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:58:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:58:45 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:58:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:58:45 GMT
WORKDIR /tmp
# Wed, 17 Jun 2026 00:01:51 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 17 Jun 2026 00:01:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jun 2026 00:01:51 GMT
ENV LEIN_ROOT=1
# Wed, 17 Jun 2026 00:01:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 17 Jun 2026 00:01:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:01:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:01:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb31c7f870ef8ec8aee6455f55c7a957b94017aabba051fbeec8aa80bef9255`  
		Last Modified: Wed, 17 Jun 2026 00:02:33 GMT  
		Size: 158.3 MB (158343224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7099720225c0913e06beb4b66d0993f2d24465d292ead3ccc21012c6ea6c60`  
		Last Modified: Wed, 17 Jun 2026 00:02:30 GMT  
		Size: 18.9 MB (18936575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572eb8e468a623338b828d27253938d7ebdcdafe0d2aa6fb9a99fb626d612a0e`  
		Last Modified: Wed, 17 Jun 2026 00:02:29 GMT  
		Size: 4.5 MB (4515178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6feada1fc189bbd5c1b77428e5da9f33471d76dde443943c45a2c74ca8af17d6`  
		Last Modified: Wed, 17 Jun 2026 00:02:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b593370ee92e6fe86a5c22afad7ae1274a04fe267489be3516d189ff163800fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5df3c4988872ad6ff719a593b52111e55a9a2f9ffa31b9787caa80dd33388ff`

```dockerfile
```

-	Layers:
	-	`sha256:19326b132076c95083fd5e71612040f62f8aaa1191fdee9bf1e8b43bc33f27ba`  
		Last Modified: Fri, 19 Jun 2026 02:49:51 GMT  
		Size: 3.8 MB (3820672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebd7c040213623a901057c08ae52d8ecf74bc60ed625ab0019d81d797c622efb`  
		Last Modified: Fri, 19 Jun 2026 02:49:51 GMT  
		Size: 17.8 KB (17762 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:e6b7a66657eea5881e8116c55eb2ae638eb3d93c6662b336a63fc26c15f101ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 MB (220212066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57560875545191631256b8d07931c4908c364bc0345a699b7f985cf890a1309`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:38:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:38:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:38:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:38:00 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:38:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:38:00 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:39:09 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:39:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:39:09 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:39:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:39:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:39:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:39:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c55ae26073105dbb12b878ce93ae33f8d0835ba25a28114c5d1f6b6e4fbfe51`  
		Last Modified: Tue, 16 Jun 2026 23:39:40 GMT  
		Size: 147.4 MB (147388349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ed8fffe07365062638d3780860c11f8ebedb06921526b4a116d98ac067672c`  
		Last Modified: Tue, 16 Jun 2026 23:39:38 GMT  
		Size: 18.9 MB (18922194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c44b7c05292bccf0719d305d7c8dae4e67c8b1c9b17020ee85eea9905c0b1c`  
		Last Modified: Tue, 16 Jun 2026 23:39:37 GMT  
		Size: 4.5 MB (4515197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77f648c5cda2aec12fce9071454320634ece56c82da8fbc8299f19a0178c704`  
		Last Modified: Tue, 16 Jun 2026 23:39:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6ca5b81a2e8cefb2a54d291a661174f0c2f48fa378c94a99109a652b4b83179f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c79ba919607906847ddf9ffb353028b4a9991d6a4740a447549fdaf63717081`

```dockerfile
```

-	Layers:
	-	`sha256:7da08f9f8c9d8c83c2e95d12a784ff563f810af428c56c704eabc4c1de1d54a1`  
		Last Modified: Fri, 19 Jun 2026 02:20:00 GMT  
		Size: 3.8 MB (3816099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e64c03082668cb74832df27a5678250a93334fd617e338854e6976a8dd074e4`  
		Last Modified: Fri, 19 Jun 2026 02:19:59 GMT  
		Size: 17.7 KB (17718 bytes)  
		MIME: application/vnd.in-toto+json
