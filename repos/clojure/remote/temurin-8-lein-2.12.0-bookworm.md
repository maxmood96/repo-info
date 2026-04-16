## `clojure:temurin-8-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:cea56994465a0facf1a0b25ca27fac9d76b93bef700f57221b60aa25212ff710
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
$ docker pull clojure@sha256:2beaef6fba16ee6751d188b465ffc2c72277af7097b6b3b06e555492f04745bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127983206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace5cf33f10d2828fb97270c171999fbcfa0ca7b7e9ad8c8d33d5ff39f26b598`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:00:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:00:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:00:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:00:29 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:00:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:00:29 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:00:43 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:00:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:00:43 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:00:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:00:45 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f4ed036afffbee859ae4915feeef010e92bff8b7b13abb39ca803dfe51a8dc`  
		Last Modified: Wed, 15 Apr 2026 22:01:01 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5bdc28e0267a774b97b8b043a787ad9d1e9716115c9837bbe72bd97be304f6`  
		Last Modified: Wed, 15 Apr 2026 22:00:59 GMT  
		Size: 19.8 MB (19806544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744339988595b81dcb85eccc78e76ad4735b4047b17a68e9ceebc38f4a7b058d`  
		Last Modified: Wed, 15 Apr 2026 22:00:58 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:33c3576438b0e05b9b56fb62e6f8cf5fa303e9b25c94fea8308e9831b42dba89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e45cfdf134f0f42f5aea5dabd8b00333fbc0efb6f94ef4553636057697c3b9`

```dockerfile
```

-	Layers:
	-	`sha256:4fa9b682d1f3281267d87e6aa34de4d68ae5c28eee57382e5f85410b224e686e`  
		Last Modified: Wed, 15 Apr 2026 22:00:58 GMT  
		Size: 4.4 MB (4402720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aff82037faf449a272ab5a40d249db5ec075fd3361186a8e84ab121088457e0`  
		Last Modified: Wed, 15 Apr 2026 22:00:58 GMT  
		Size: 16.4 KB (16369 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fe0aecd8a81c10d39b50cb7eb990270533313e35a7d3cf2cb132d383d940f98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126779671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a45f0f5abf99fa3c72839f8a40d21548acf99b2f14e21e9b59facdb475545b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:12:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:12:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:12:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:12:05 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:12:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:12:05 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:12:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:12:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:12:18 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:12:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:12:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec106e7e12d89e8b261ac58611e219555f0fcc566bdf1d89a0cca283c07b59bc`  
		Last Modified: Wed, 15 Apr 2026 22:12:35 GMT  
		Size: 54.3 MB (54251615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5cb974acab42d94cd551f8024ab0324c566a345eba59737a302db1a0ab6009`  
		Last Modified: Wed, 15 Apr 2026 22:12:34 GMT  
		Size: 19.6 MB (19637044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0f44b544adc29c811f19bf7382ef854e807fbf2ab3ef219eb353c843072f80`  
		Last Modified: Wed, 15 Apr 2026 22:12:33 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3c44572db68b69a034f9653a35ab4113f0f7221e87aaf891e0fb599aab10794e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae97f011414181481f3b38619d43f1c5f98f4b3b5ef26afb34c91dfa83289a9a`

```dockerfile
```

-	Layers:
	-	`sha256:2d1291624ac6b024bb5998d9eb0aeefd8e3583171311f5cd2c51c53ede0cffe1`  
		Last Modified: Wed, 15 Apr 2026 22:12:33 GMT  
		Size: 4.4 MB (4403035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61e365406260f42678b3d19d741acee74c398aec68cd7ffc58644283a22fc27c`  
		Last Modified: Wed, 15 Apr 2026 22:12:33 GMT  
		Size: 16.5 KB (16491 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:b4058b0bcb78572bc837af36092605af69f572be0aaa3435bea42f7293a35290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129529035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8e35f129565c1c1662636908d26b93f47e66b6ce2637b062857509aca875f5`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 14:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:20:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:20:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:20:05 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:20:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:20:06 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:20:51 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:20:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:20:51 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:21:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:21:00 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198aa8af97ba5b55cc83e5b59bee258e24a99d12a6acfe2745f351375cceb0d5`  
		Last Modified: Tue, 07 Apr 2026 14:21:35 GMT  
		Size: 52.7 MB (52650379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb383308984a020a60db0d4162a081a34b3df4024506abee0b883e03f3d774b`  
		Last Modified: Tue, 07 Apr 2026 14:21:34 GMT  
		Size: 20.0 MB (20023892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42373a578b9b0dedc05a634bb74a23e25a792d7333467b0c060a3c4338c476a`  
		Last Modified: Tue, 07 Apr 2026 14:21:33 GMT  
		Size: 4.5 MB (4517794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:704dfd102684dcfb8d67440c7d1f83389c83a620ca8531288b6766e1faaad18d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4421590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c01f9d3a6ccc87f45f4e9ddd9b6b3f598511c122d01f0e19dd28ec248b6e9a3`

```dockerfile
```

-	Layers:
	-	`sha256:df4005b6b680808b50622c8477c5496fed493f55ce66b239744e79b6005e07cb`  
		Last Modified: Tue, 07 Apr 2026 14:21:33 GMT  
		Size: 4.4 MB (4405176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd0f7defcd411a231ecebc2da035179a50f1694318152a1cf1e953b0954a2911`  
		Last Modified: Tue, 07 Apr 2026 14:21:32 GMT  
		Size: 16.4 KB (16414 bytes)  
		MIME: application/vnd.in-toto+json
