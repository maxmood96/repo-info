## `clojure:temurin-17-lein-bookworm`

```console
$ docker pull clojure@sha256:434cace0360367559ae4404127e268e4efe82134425f8f17e4d98303e6bafd18
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

### `clojure:temurin-17-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d1fdd55d90d214b511c152259efee2ffe2b0df9da00f0caf364c16483f1641ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217650120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43655e5accebd280a92a3acfb7168239e90caabe0dd845dc955bec7530b56204`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:42:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:42:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:42:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:42:22 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:42:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:42:22 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:42:36 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:42:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:42:36 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:42:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:42:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:42:37 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:42:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516d84ff9471a218e591b8e57000014c4e0f7f8cd13a62f151ae8d47123ed40d`  
		Last Modified: Sun, 09 Nov 2025 03:32:08 GMT  
		Size: 144.8 MB (144848032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db48cc9ca9fe0118a7a31e2d7f3fc4b36bfb891c81b30563dcdf647f08281e2e`  
		Last Modified: Sat, 08 Nov 2025 18:43:33 GMT  
		Size: 19.8 MB (19802897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e649242e26521251d3bb13250aca01d5c8ab4b5f8c770698533542e8d3e7e99f`  
		Last Modified: Sat, 08 Nov 2025 18:43:33 GMT  
		Size: 4.5 MB (4517706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89beb0c4982fd8faefd2251d4db4e5246fd5033740b0b134efe778c577644535`  
		Last Modified: Sat, 08 Nov 2025 18:43:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7799d30e30a8b6994a3ed9265d03aad7944ef7874938749a2144df3b16e3bfde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4298204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec3344bedf39b67362fc493e6d709d5df8460be4261a1a110591f4c39aef669`

```dockerfile
```

-	Layers:
	-	`sha256:13a889b6b713703b354c181c235cd4b38b47d3a850b3a03446c5e45154844be7`  
		Last Modified: Sat, 08 Nov 2025 22:42:23 GMT  
		Size: 4.3 MB (4279836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:421a02898a70e579965e290058f37b0bff29726e387dfd0753121438cb5f7eda`  
		Last Modified: Sat, 08 Nov 2025 22:42:24 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d0fac66bb17ceac617cff21b8b2b0dacb5232024a4d7a6077568e59c8f6225e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216189878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1098f1f4dc1ca23297ac204088a9533942b2f405ff2ecf4438a624ea93eb0800`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:41:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:41:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:41:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:41:54 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:41:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:41:54 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:42:08 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:42:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:42:08 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:42:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:42:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:42:09 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:42:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ba78719fec4fadfd02ef26219b7d588c5b60c3952530b4ba8b33e1f85e1faf`  
		Last Modified: Sat, 08 Nov 2025 18:42:31 GMT  
		Size: 143.7 MB (143680052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922c800b0b75bb2d4205d4abe6e750c659ef108331678363ab9c4deab69dda22`  
		Last Modified: Sat, 08 Nov 2025 18:42:43 GMT  
		Size: 19.6 MB (19632195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6443ebaf7814bb909c22ebe925165a974d8f143306cbcd53e4439ab6f925d7f9`  
		Last Modified: Sat, 08 Nov 2025 18:42:42 GMT  
		Size: 4.5 MB (4517724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38cbb40d4afd6373b815dda5fe598d6f031d47ea4714d264b6c681edb3798816`  
		Last Modified: Sat, 08 Nov 2025 18:42:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:53d64bad87b105c46b824a095921be751fcd1e1abdd6cb177c458db823bafcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4297940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d85a4fccae27587f7accbb19b6a7df86fd3d0285d0e4d6fad5db4c8e25ea96d`

```dockerfile
```

-	Layers:
	-	`sha256:4d32fc2d7f04684474a42d3447180d90a38df6f61b31fd9cde16fc5d70a622e2`  
		Last Modified: Sat, 08 Nov 2025 22:42:28 GMT  
		Size: 4.3 MB (4279451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30be2ee5e769fe2d0b699eb178f7bbea10c638cba2ea19d9be28de9ad0cebcd9`  
		Last Modified: Sat, 08 Nov 2025 22:42:29 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:8beb87b9f9794e7cd076134ce106d45cda8fd4d8dd8ac2ed413421ea78ed7051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221392226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753d06a4b70043d247b4ff077f9d2a42ea76f426933bbf649b2c30f4b4ca3fc9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 21:13:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:13:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:13:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:13:31 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 21:13:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 21:13:32 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:13:57 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 21:13:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 21:13:57 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 21:14:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 21:14:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:14:01 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:14:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b991744392cdb392b2eb2934ca9a948480035c261ce99f62fad6bd622bfcaaf0`  
		Last Modified: Sat, 08 Nov 2025 21:14:39 GMT  
		Size: 144.5 MB (144525137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e0261612cbbba28b9d1fca3656a9d14364c03222151fecc9a49606b6e2dfd8`  
		Last Modified: Sat, 08 Nov 2025 21:14:51 GMT  
		Size: 20.0 MB (20021634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53609cb508e9048466cb118fd4f28797a0bc17155bcfe22567d4129483c825ca`  
		Last Modified: Sat, 08 Nov 2025 21:14:47 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3087d601e6c9fb2d8da0e766423bb0b1784c525bb05e2dc5abd108d4f5ac37c6`  
		Last Modified: Sat, 08 Nov 2025 21:14:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dc1d4462be8dd991772ddbaf2fd12fe94f136bce89a0938c07c459643d0c311e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d292702d6c0e59bf7aa2e8e29b96edb563336103e043580158d927e673fbf08`

```dockerfile
```

-	Layers:
	-	`sha256:2516757a6075fa5d7e5321c30593b29d20cea3d0f4f892c04522fc97a00ef585`  
		Last Modified: Sat, 08 Nov 2025 22:42:33 GMT  
		Size: 4.3 MB (4281695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca79988b6587e87a16956ec765f17d9e1b60daacf376b3af75fcf76ed713a583`  
		Last Modified: Sat, 08 Nov 2025 22:42:34 GMT  
		Size: 18.4 KB (18412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:133be3188f76f78b638ca32555143f932781a1df7010c9918c7dabc632b71f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205976007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08201fc80f9d60855c2eb06ed61143b774fd3016b4970ccf55503e61bf27a70a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 19:35:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:35:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:35:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:35:45 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 19:35:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 19:35:46 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:35:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 19:35:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 19:35:56 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 19:35:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 19:35:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 19:35:58 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 19:35:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7c081acbe0e53579c655776769c55de0a79d0fdf1ffd7568881985607f4314`  
		Last Modified: Sat, 08 Nov 2025 19:36:30 GMT  
		Size: 134.9 MB (134858996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac6cef222064547a0dc390ed6d01ea563db2c6da2d16c6dde2a262a3367da17`  
		Last Modified: Sat, 08 Nov 2025 19:36:35 GMT  
		Size: 19.5 MB (19460775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a397a38a796ec41d8b1fa706f8c3f975fa953e8dfba96db86e0125d548a94a`  
		Last Modified: Sat, 08 Nov 2025 19:36:35 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7304e6a080e7faab2b9623aca4ed4faa7583d308ada26e8c1c94d31ec2f51f55`  
		Last Modified: Sat, 08 Nov 2025 19:36:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f850616253ad6ca9c1896f24e9c0b05adae637362f38150ef6adb17484ba2462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4290018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713f0cb0f460e60920ec131341d33188246aadc6a09d8886f9bdeb0c3158bc4b`

```dockerfile
```

-	Layers:
	-	`sha256:98ad805a541a66e3e407a0859bc4f07d482f8e831b1e59b810a49eeb637ec72e`  
		Last Modified: Sat, 08 Nov 2025 22:42:38 GMT  
		Size: 4.3 MB (4271650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70c472144e52b22bf225a66b9924ca1601a1389862e54506f979b040c80833f2`  
		Last Modified: Sat, 08 Nov 2025 22:42:39 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json
