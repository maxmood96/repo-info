## `clojure:temurin-25-lein-trixie`

```console
$ docker pull clojure@sha256:20ebb4326fd57712e056ad1e0379b4bcdac57b8067dea761d853b47b4caeecc4
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

### `clojure:temurin-25-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:efb6e1da75a4dc54b50b2881d6bffa5c1513162e262f7d04e07b8839c9f95573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165287561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03fb2079fe491455c516c83f6cfb4f55571d1d87f562c1e25333cb7fd811203f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:20:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:54 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:20:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:20:54 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:22:02 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:22:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:22:02 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:22:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:22:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:22:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:22:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedc20d5f9433e7aec9e8125310bc7411b41244e055e0e6a6476a78a6c2c894b`  
		Last Modified: Wed, 24 Jun 2026 02:22:25 GMT  
		Size: 92.6 MB (92574611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867cd534d8e8b2ceef80f2450afdfa8ef091a4f73e6cd8bc0de958711f1a07dc`  
		Last Modified: Wed, 24 Jun 2026 02:22:22 GMT  
		Size: 18.9 MB (18880059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967239ac8aebad0517adbdee7f06a61e9a48b77d08a592567a78676541c7d721`  
		Last Modified: Wed, 24 Jun 2026 02:22:21 GMT  
		Size: 4.5 MB (4515207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01294682be0bfd96870951102ec519f75a2d780d5fe6832f7b4bd2f574218ce1`  
		Last Modified: Wed, 24 Jun 2026 02:22:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:40a614da9d8c7245cc6f06b01293548c6c698690fe0fa60d4f65780486faee8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3804193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e850ff7b0b20f185f2ba91ec75b9f5f50834052eb23b771362cb71309e4be54e`

```dockerfile
```

-	Layers:
	-	`sha256:867e548722d2de2f9e0158ed3ce0ab0f89fd941144e31c5e6f993fe8551037f0`  
		Last Modified: Wed, 24 Jun 2026 02:22:21 GMT  
		Size: 3.8 MB (3785848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53fa442aa6ac3eac2b3a1a247c929a36446b5019b5694d77d9d12b7d8326b27f`  
		Last Modified: Wed, 24 Jun 2026 02:22:21 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8b5be8c39cb189750be6f2ce6a04fcbe9488d3c5ac0d95ea121d6bc235263506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164575859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ebd545576e176aa2e3dfc9a592776819baf2c26695ff2b1a10164c8bcebfa38`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:27:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:27:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:27:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:27:38 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:27:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:27:38 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:28:57 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:28:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:28:57 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:28:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:28:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:28:58 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:28:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7cecd7735e174cb3a21caa3c827943dcb0eeea054af82bf5e9f8924c804d91`  
		Last Modified: Wed, 24 Jun 2026 02:29:18 GMT  
		Size: 91.5 MB (91542270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e667be9d1194fd9e3d0b31736416345799c85c928731731229d5e12ecb9a624`  
		Last Modified: Wed, 24 Jun 2026 02:29:16 GMT  
		Size: 18.8 MB (18839595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73e4705a18911a49f7f914706cba47110d7357091a9c727be8b1572638401da`  
		Last Modified: Wed, 24 Jun 2026 02:29:16 GMT  
		Size: 4.5 MB (4515170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d34d60bb694645cf8998c69b5e4dec43c86f496277acce571dc6eab55d877e1`  
		Last Modified: Wed, 24 Jun 2026 02:29:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d9d70df84c1037b7dbea86968e5abd722cf2808c6185ea97e8c8a50e867e9307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3804599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03aefbe224f964f20d89cb13ac6b262b0fcb00c6ab209f9dd1aa0ea0395987ce`

```dockerfile
```

-	Layers:
	-	`sha256:4229c3aeb1efe1b9323effc004b56387df76edb77f39aaa4dec29a7629178cc2`  
		Last Modified: Wed, 24 Jun 2026 02:29:16 GMT  
		Size: 3.8 MB (3786109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab96e26cd8178f4d46537693894e2505ca5e7667be0f33d3203d2ae9865cd33c`  
		Last Modified: Wed, 24 Jun 2026 02:29:15 GMT  
		Size: 18.5 KB (18490 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:4981c8e6c5275a05f69d3da84fdbc0a73e7136160c7838d4d97bd8b32bcc66fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168504056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc7af32c2b409e0c04012fcac01cd73d7684dd9608423c672b5d84e756015a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 00:11:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:11:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:11:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:11:00 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 17 Jun 2026 00:11:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 17 Jun 2026 00:11:00 GMT
WORKDIR /tmp
# Wed, 17 Jun 2026 00:13:43 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 17 Jun 2026 00:13:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jun 2026 00:13:43 GMT
ENV LEIN_ROOT=1
# Wed, 17 Jun 2026 00:13:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 17 Jun 2026 00:13:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:13:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:13:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc6e91230e9fcb06c48eef2eae63696efc222edfdf9387e828c0e8a79c0a8c9`  
		Last Modified: Wed, 17 Jun 2026 00:14:23 GMT  
		Size: 91.9 MB (91914030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545271dc17cd609e72c45c99cc2b4c230217501733bc396ea85bb6cff9be56e8`  
		Last Modified: Wed, 17 Jun 2026 00:14:21 GMT  
		Size: 18.9 MB (18936466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c816ddc4d5518aa88e3295640163da90bcf82a13d4b932d4a76c10753cb825`  
		Last Modified: Wed, 17 Jun 2026 00:14:20 GMT  
		Size: 4.5 MB (4515191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70de2f92949336d91b0ec75fa618b27498fcb6a8e3610fabf898d448df7b34d2`  
		Last Modified: Wed, 17 Jun 2026 00:14:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1d2f6b9359c27ca137462b3b4b2208b3d4a5606201e3af3b09f261fa0b3c4629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3788573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959de4091a6cd882da19bef09042035a175aec6475b471725ee9c7349e51aeaa`

```dockerfile
```

-	Layers:
	-	`sha256:b29526bec01305e8fbf25ffc9ec7b76d215f3c56384f7fed330cb99fdc8ec023`  
		Last Modified: Fri, 19 Jun 2026 02:54:49 GMT  
		Size: 3.8 MB (3770172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d9e689dcfed501c47c21abe3dac107a5e9c1a58103e81f53b88de49963bd70`  
		Last Modified: Fri, 19 Jun 2026 02:54:48 GMT  
		Size: 18.4 KB (18401 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:8d43703a222e075f821e7152e64d96a884d99a0c5531667aa3d8d6ce2e995c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161244298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1818ce55cbe9f34b4010ac65785166e6a6747d2219c27a5512a7dad8a36403ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:21:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:14 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:21:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:21:14 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:20 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:22:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:22:20 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:22:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:22:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:22 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61adec2576be28516842462114579539904738dc16abf2591b21445e78b04e67`  
		Last Modified: Fri, 19 Jun 2026 02:22:47 GMT  
		Size: 88.4 MB (88420353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9873fa465d3bec1aa8b3d55c02291bbfb10221cbe07b981c9af8ca839115a3`  
		Last Modified: Fri, 19 Jun 2026 02:22:45 GMT  
		Size: 18.9 MB (18922406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e440901d2089b07683b29baecc9902bc52c5f9df173bf32e7aad54e18440dc`  
		Last Modified: Fri, 19 Jun 2026 02:22:45 GMT  
		Size: 4.5 MB (4515211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ad4ce9151d8942e20063529fe7a312e7d514686da05d72d567b14a80e251f9`  
		Last Modified: Fri, 19 Jun 2026 02:22:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:40541c44f656bb03ca44b9dd0b152a55f46d9b8e0e0c3a4b50d313cf4bb51ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3929695e1020b4b52b312873badfd9f6a66807549391c2b6e9e2902b37d00e`

```dockerfile
```

-	Layers:
	-	`sha256:8b33bf85b203a59e6f4cf3dbcd7abadda372ef84b39851f34fa8bd528deba340`  
		Last Modified: Fri, 19 Jun 2026 02:22:45 GMT  
		Size: 3.8 MB (3766837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c94a231ec87af8b55771a69878f7e2b218b5aeb4f44f3df35118ad9ca4adf735`  
		Last Modified: Fri, 19 Jun 2026 02:22:45 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json
