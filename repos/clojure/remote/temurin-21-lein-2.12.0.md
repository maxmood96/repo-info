## `clojure:temurin-21-lein-2.12.0`

```console
$ docker pull clojure@sha256:f8c4c647b7802a1ed74687e6301fba7cdd4706796d2d915aa8899fa23ad4cdc4
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

### `clojure:temurin-21-lein-2.12.0` - linux; amd64

```console
$ docker pull clojure@sha256:431fa4e377f7d3905f5cece0ecac67fecc1d9f50d4770293881d64705250a437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230666852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c1679dbd5d2f449027bc9b30c8bf5d2835dca8099db74e795e15266b21d470`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:55:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:55:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:55:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:55:31 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:55:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:55:31 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:55:46 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:55:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:55:46 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:55:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:55:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:55:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:55:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc0e83d74fc0c7cc9cdf0e78de5af285f0fc089cee513dcb4b83c1c58024dab`  
		Last Modified: Tue, 24 Feb 2026 19:56:13 GMT  
		Size: 157.9 MB (157857067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dcb217d28f93e40b2b03dd7e841d536b1a2314069e23c10c3e65332adcc838`  
		Last Modified: Tue, 24 Feb 2026 19:56:10 GMT  
		Size: 19.8 MB (19802869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8a5b6070b7685b1e129fb570540e7475543a9df13cb1b8609f0b4b93bcc78a`  
		Last Modified: Tue, 24 Feb 2026 19:56:09 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4be17042e6096ac9392b9ca835a8e2582b2052c8df4f312a251ec731b50ddc0`  
		Last Modified: Tue, 24 Feb 2026 19:56:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:bccde9d6cbd423b91f4427139b179ad1355971c9f59625dcc6e298ed86611c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4efc355bae30e0c40d100a000431f408160d18338435bff1f6a2c862c2423b9`

```dockerfile
```

-	Layers:
	-	`sha256:eb0c2a9787a96d2575ccff6cd3c4fc3708fcd75321303225849db27ae3f6eaf4`  
		Last Modified: Tue, 24 Feb 2026 19:56:09 GMT  
		Size: 4.3 MB (4284233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:343eabcda76456609d14a412a0ca9668cf75461dd1aaec97b5570de6d9a608a8`  
		Last Modified: Tue, 24 Feb 2026 19:56:09 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0dfd5ed3b10420977dca769478423042c35b5ac7d5b09b7969fae45175610d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228657238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c3bc4551bf8791753d5f422fc817c4447e05362cd49e31cdf7edb583cb6280`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:06:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:06:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:06:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:06:09 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:06:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:06:09 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:06:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:06:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:06:24 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:06:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:06:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:06:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:06:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bdaefff09325a314dad0f08b79657c642629dba16328ab8d4ddff7d53b7b7d`  
		Last Modified: Tue, 24 Feb 2026 20:06:46 GMT  
		Size: 156.1 MB (156133092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f218710b53e5ae86ccc134f2191b5aa4287cfebd6e7fa97c3a6b2c6b93ba014`  
		Last Modified: Tue, 24 Feb 2026 20:06:44 GMT  
		Size: 19.6 MB (19632799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2a2c4945632026d2aa26160be85fb2c323e85bfdfd9979fc43bb4d967c4288`  
		Last Modified: Tue, 24 Feb 2026 20:06:43 GMT  
		Size: 4.5 MB (4517708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52371d88c6f56b8b925bcf357e61094fcee999197fbd9bd074947f0db3dd1d23`  
		Last Modified: Tue, 24 Feb 2026 20:06:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:6491a7639be2968482385a0753fc8838bbbc20b5018fc2fb48f54a7ebf0a994e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347834787954f879bc3b980ef05a9d14506f8975f8f595ed28f04bedcc08c765`

```dockerfile
```

-	Layers:
	-	`sha256:397dbdd7116c092cf994653c62b25d78c237611798562bd930824c8ec4f0b1d3`  
		Last Modified: Tue, 24 Feb 2026 20:06:43 GMT  
		Size: 4.3 MB (4283872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b53cfdccc717bb61c59902e55534c8c123615fcfb41364fdeed911389cabf61`  
		Last Modified: Tue, 24 Feb 2026 20:06:43 GMT  
		Size: 19.2 KB (19163 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0` - linux; ppc64le

```console
$ docker pull clojure@sha256:b292458accc75f9163d3a0a5e03b6fcc6b8899ac4a7acb254ae73bb2a64018b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234856318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cda18ac63cca2ecf2d2f57c8f18e3a9a0e8859b62894a7351b1144da6eeba5d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 02:05:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 02:05:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 02:05:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 02:05:49 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 02:05:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 02:05:50 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:06:38 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 02:06:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 02:06:38 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 02:06:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 02:06:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:06:43 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:06:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d3f5e74242b563425489fb40e572f07cd179ee7a7b86fa1a8e8f36a083f08c`  
		Last Modified: Wed, 25 Feb 2026 02:07:30 GMT  
		Size: 158.0 MB (157977502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50285f3786943d6a91a37e64d74f443446f42158e80a09b8b33cf6d04adf412`  
		Last Modified: Wed, 25 Feb 2026 02:07:26 GMT  
		Size: 20.0 MB (20023839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101c9fde50611b7b0e058750127f821b0236f9e4f460fa1e449f31951064828e`  
		Last Modified: Wed, 25 Feb 2026 02:07:26 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a61ab8c25662006212920c1d71bf1b69256c068040587a1befe2bc9d5ca580d`  
		Last Modified: Wed, 25 Feb 2026 02:07:25 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:1ae12122672c0c823ccb7de626ad799f412c66e340785dbbb3856a2248869a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d084fda3e220520283f9bb407548502dfbe78e7c0823e616c1f69a78d2c88c`

```dockerfile
```

-	Layers:
	-	`sha256:50219c6784559a6ee65115a400c2d19ec04a1aa047d5adaf18c4461476e0984b`  
		Last Modified: Wed, 25 Feb 2026 02:07:26 GMT  
		Size: 4.3 MB (4286106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7cfbd5c3f0bd02fc42afed72d5e230aa4f3425b6c6fd8ef33095ba2e9916be`  
		Last Modified: Wed, 25 Feb 2026 02:07:25 GMT  
		Size: 19.1 KB (19074 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0` - linux; s390x

```console
$ docker pull clojure@sha256:bc200876d84fb87e037a5b0e573bb059e8cb3916db85da4911930aab5ae2793d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218234965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b3e6d9dce3e08c0b36a110d3440fa14728228bf7bb880216664c993ae1c435`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:19:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:19:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:19:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:19:01 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:19:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:19:02 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:19:32 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:19:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:19:32 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:19:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:19:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:19:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:19:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49354e9f0679f3ff8b88e9d693551817e9930dd3f79f0b6470d4ff396a09d7f9`  
		Last Modified: Tue, 24 Feb 2026 23:20:16 GMT  
		Size: 147.1 MB (147105304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d029d48f8385a6e82d6d25771c55cb496ed9963da48ee1585e3bb41256565a7`  
		Last Modified: Tue, 24 Feb 2026 23:20:14 GMT  
		Size: 19.5 MB (19463372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1efe4f6cf3aa11e90816c6f6b7f95f4dad94b617ec5249dff28f5ad4777c623`  
		Last Modified: Tue, 24 Feb 2026 23:20:13 GMT  
		Size: 4.5 MB (4517771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05e262fe4905ca17d80c00f3761dbb2bec2fdfc0a8b43f330663e51260607d1`  
		Last Modified: Tue, 24 Feb 2026 23:20:13 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:7c0ba3e7838e22c42764d1a67a23005bb653af20c4904636eaa28945c17fa65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4295065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed092d5d7d75031b4f8dfa8c2e22a66a583c21c376b004a13b3f77d234a88cd4`

```dockerfile
```

-	Layers:
	-	`sha256:83f5870f7b5618b413600722db8acfd3be12c09b815a249d0daf734086d73819`  
		Last Modified: Tue, 24 Feb 2026 23:20:13 GMT  
		Size: 4.3 MB (4276047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b089e498d14298be826a99a22260dbfa4e9847ccce1f290801f9855fe005191`  
		Last Modified: Tue, 24 Feb 2026 23:20:13 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json
