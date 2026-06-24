## `clojure:lein-trixie`

```console
$ docker pull clojure@sha256:5e135aaa915fa23dbf26abb3af289a6c194ee1f4ff2b687f17a44252c26e28dd
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

### `clojure:lein-trixie` - linux; amd64

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

### `clojure:lein-trixie` - unknown; unknown

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

### `clojure:lein-trixie` - linux; arm64 variant v8

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

### `clojure:lein-trixie` - unknown; unknown

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

### `clojure:lein-trixie` - linux; ppc64le

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

### `clojure:lein-trixie` - unknown; unknown

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

### `clojure:lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:84cbc00654961e85a1cb27f47d15ed9eb601d3212764c0f2fd7536aadaac06ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161244442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ce2a30c79adc0bd5065f6f18e20ab1d60dbb86a9a609e9088291cdb93c5fc5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 04:17:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:17:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:17:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:17:37 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 04:17:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 04:17:37 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:18:43 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 04:18:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 04:18:43 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 04:18:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 04:18:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:18:45 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:18:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4acbf08d84aa74ba1f41a222ae6a061c228f6ba4fc5d1d428650c7427ca1fbd3`  
		Last Modified: Wed, 24 Jun 2026 00:28:42 GMT  
		Size: 49.4 MB (49386060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c5e6947f1b6426fde323acb1b84b8461079197a083c1fbd3d726da0e271aec`  
		Last Modified: Wed, 24 Jun 2026 04:19:11 GMT  
		Size: 88.4 MB (88420330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71273d117964d28a2a1283de756119092a010f72d12d2d5a565aa2268916dafe`  
		Last Modified: Wed, 24 Jun 2026 04:19:10 GMT  
		Size: 18.9 MB (18922419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203480495b34f37247e212241833a539a60b9db64d4affc85e63729717400a46`  
		Last Modified: Wed, 24 Jun 2026 04:19:09 GMT  
		Size: 4.5 MB (4515203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839cef9b95450efddf8f1062238bb98d9f9012b53826cd70c2b0d12bb696112`  
		Last Modified: Wed, 24 Jun 2026 04:19:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:332ef3a762e626a3c006702560ca946d2e3b8d962a98faa11c8b461c91d61e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587d32988919b02ce3c2f54c72b2f006abf8c6db00a2272f6c8df0abe7e50a73`

```dockerfile
```

-	Layers:
	-	`sha256:ec5d2a4f4dc86fde8b6fe2b430367e87c1bb49948b1a318b8a30c4c9177cd420`  
		Last Modified: Wed, 24 Jun 2026 04:19:09 GMT  
		Size: 3.8 MB (3766837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2632ad80acff7c1002d1338b44052b79e80c73a0c1dfcb6eea9abaced5bc9b90`  
		Last Modified: Wed, 24 Jun 2026 04:19:09 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json
