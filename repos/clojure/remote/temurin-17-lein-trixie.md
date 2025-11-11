## `clojure:temurin-17-lein-trixie`

```console
$ docker pull clojure@sha256:7af1a335cf9efae8373fb9ee36f233de7aa199c513b4b7675a37e4003cdd3364
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:e393daf59fa058df9e4353e1fdd17542c487cb8a5c66ac4fb5637846ae4db7be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217231078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415c7d071617e933d74dcb5c79ab13ed1c3797a8426e93c0e6b4a1a66a99ddf3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:42:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:42:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:42:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:42:39 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:42:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:42:39 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:42:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:42:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:42:56 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:42:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:42:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:42:58 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:42:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e93141487cd04dee4d42a4de0a6f0a609cd66ceba5375394bf873be93206fda`  
		Last Modified: Sun, 09 Nov 2025 03:45:25 GMT  
		Size: 144.8 MB (144848032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17983ce473d4320b99bbc2bcf8ca98b0d326be898cb138f14b4632f201c9023`  
		Last Modified: Sat, 08 Nov 2025 18:43:57 GMT  
		Size: 18.6 MB (18579274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76d91f984be38ca7a2df316a7afdf46f3b4120b440c33455b1113c50f8d471b`  
		Last Modified: Sat, 08 Nov 2025 18:43:52 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f2504c799feed2059f2930802eac5cb1a0b204edc1cc5c708d1c53100ecb27`  
		Last Modified: Sat, 08 Nov 2025 18:43:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:18f95c7d42a65d3f738004a6257d3825f12d6781895b241eb016d750c7b807f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60090ac919012fa1ec6bf1b7972cd2254bf80beee27316724b787d6783c5b016`

```dockerfile
```

-	Layers:
	-	`sha256:ba5386ac0d97c416c8329d4cf0c921f2166cb0f22262cc517036aaa1e4147a47`  
		Last Modified: Sat, 08 Nov 2025 22:43:26 GMT  
		Size: 3.8 MB (3813386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7efe1129f8f76415342cfaa0c217be148b5a2c62a10d024e1c99ef3da43db696`  
		Last Modified: Sat, 08 Nov 2025 22:43:26 GMT  
		Size: 18.4 KB (18351 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5b2372aac6f99a1c264c4c62dc4c227daf8bb4497ca961dda7ad158dd5f40835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216388492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10076d89e8b0a0658e75cb874b145477de374e0154fd29f6c8ee014e3002d51a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:42:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:42:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:42:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:42:11 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:42:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:42:11 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:42:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:42:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:42:28 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:42:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:42:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:42:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:42:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30497946a7e5378465079cac7e7920a5f022451d6124a4d18c846dd355848fa`  
		Last Modified: Mon, 10 Nov 2025 05:26:53 GMT  
		Size: 143.7 MB (143679948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23989533dfb6a0d04fb8c536581594aedd6e91c422c721dcd4118d9e60293a3`  
		Last Modified: Sat, 08 Nov 2025 18:43:18 GMT  
		Size: 18.5 MB (18539964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccadc1eeac4cbdb3263bbb7e1603a67636ed39e68825e21eff821eb77486c3b`  
		Last Modified: Sat, 08 Nov 2025 18:43:18 GMT  
		Size: 4.5 MB (4517721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817e628e1a06563457a21db0c7f887de7cc39351d26b6f570d3d52c604b3fc73`  
		Last Modified: Sat, 08 Nov 2025 18:43:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8f533d0ec2d47b06c8dd41362fbe6d0276e25d2851c58b2e1965272254087aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86efddfa18165f2a3c816963b371d115cdb2c3151e75547dba08ff151e46f38`

```dockerfile
```

-	Layers:
	-	`sha256:3a2645c3ebf96988e8e203d5e4ff04cbcfda8bc3a2f559fd37c810a77b1f6337`  
		Last Modified: Sat, 08 Nov 2025 22:43:31 GMT  
		Size: 3.8 MB (3814263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c09988cd73183c17c23d194fb0368f7e495642bf5ad6b5296d60ffc614cbb5`  
		Last Modified: Sat, 08 Nov 2025 22:43:32 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:1e3ce19166686d6a2021543770334ae38b12db75c9d31301f1429baf09384797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220790072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455c59626ec6dc7c030dd1a6df41f2c0cc47ffd737016ac650b2123d1aad7834`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 21:18:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:18:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:18:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:18:18 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 21:18:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 21:18:18 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:18:51 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 21:18:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 21:18:51 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 21:18:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 21:18:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:18:54 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:18:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e8782314f27b926983211cc829d4001e3f86049dca101a7fc7515489a4bfe7`  
		Last Modified: Sat, 08 Nov 2025 21:19:39 GMT  
		Size: 144.5 MB (144525137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113371895fde9a914f4bf726d49e56d0154e7a134840b32b04d2658367bd3bbf`  
		Last Modified: Sat, 08 Nov 2025 21:19:48 GMT  
		Size: 18.6 MB (18636618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffaa53acd9fa099096d4bcb83e5cbf9283044ddc3d0207ac2bd5e6cd61be599`  
		Last Modified: Sat, 08 Nov 2025 21:19:46 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af49d4f33473a416de1b69037a1425dbcd2d6f4f86e82db68b7b5b67b641170b`  
		Last Modified: Sat, 08 Nov 2025 21:19:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c89bbd5b4382e0e7b7a270de8ca2ca9d17b231d5fa27f1c803da5eebba23e57a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6f16be379c240f603a25b9aec80cac5b30b70dc6fa31830769ef7d506880ab`

```dockerfile
```

-	Layers:
	-	`sha256:c4ebd3f0e0b9998a82f6e971bb47e6c690556a413d5d96325a9068d83af30618`  
		Last Modified: Sat, 08 Nov 2025 22:43:36 GMT  
		Size: 3.8 MB (3814384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf38ee5853aa7235634a8b4bdb3f23486e25d8f595e6f55899eda95acabc146`  
		Last Modified: Sat, 08 Nov 2025 22:43:37 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:45358eb74983b43b6ec47803ef42e7ffe45be4cd64cbb0f44458af3bd2205e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 MB (212709807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2590818b301a8cac28375e53a9cfedfdafb27dfcf6c1c4218e22119d5dc416b7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Mon, 10 Nov 2025 03:15:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 03:15:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 10 Nov 2025 03:15:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 03:15:22 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 10 Nov 2025 03:15:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 10 Nov 2025 03:15:22 GMT
WORKDIR /tmp
# Mon, 10 Nov 2025 03:16:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 10 Nov 2025 03:16:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 10 Nov 2025 03:16:52 GMT
ENV LEIN_ROOT=1
# Mon, 10 Nov 2025 03:17:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 10 Nov 2025 03:17:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 10 Nov 2025 03:17:08 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 10 Nov 2025 03:17:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ab2569f219df552fc00a9a5e017ffe204ab8c96ed1cf8ccebefe31e0bca0b8`  
		Last Modified: Mon, 10 Nov 2025 23:10:58 GMT  
		Size: 141.9 MB (141889570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9f5b4b719960c735bd611902dd28e690775d08dd452ace841868ade48fdccf`  
		Last Modified: Mon, 10 Nov 2025 03:21:20 GMT  
		Size: 18.5 MB (18531091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1049155260a1819437ebe1c40b0c9ca45c198b378034f289833ffad27ccd3540`  
		Last Modified: Mon, 10 Nov 2025 03:21:20 GMT  
		Size: 4.5 MB (4517791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da7f33639b97267004aec922c1f9922f03f460286ea7246810e4d7763643b63`  
		Last Modified: Mon, 10 Nov 2025 03:21:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e0a4d14e2070de537091d0980bbe9e4683121c73ccffd44134fd18874e20cb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3820337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2eba8b54ad1dccbabe0c8724ec9d03b8abe4af85dabbedcd146e9bc5249f47`

```dockerfile
```

-	Layers:
	-	`sha256:03c2db77dbb7093af7d05617b5ce3020a9d120f6a4f7900d9f7adcf38ae31de7`  
		Last Modified: Mon, 10 Nov 2025 04:35:26 GMT  
		Size: 3.8 MB (3801942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f87cdc7d8e734ee8c70448b2dc8751d996ba886d67680c3d73d2d1b13e86478b`  
		Last Modified: Mon, 10 Nov 2025 04:35:27 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:4bcf377243f0183cd9ee667293bf8c9070dab6b54bcdc188e1429380b509cc26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.3 MB (207349771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62024d72113320fd55dfd8d3d8d2803189bba7b86efdb6cf1a0759ae6829ca3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 19:39:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:39:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:39:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:39:26 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 19:39:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 19:39:26 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:39:38 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 19:39:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 19:39:38 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 19:39:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 19:39:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 19:39:40 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 19:39:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fb01b7f7bdd48ce68cf5bc1fa2e5f51b291cd23fe79f128847de11af6c4ff9`  
		Last Modified: Sat, 08 Nov 2025 19:40:07 GMT  
		Size: 134.9 MB (134859055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b189bf299990a6b1dad86bf486129eed7ee583fe1409c7b91026cf77330f7184`  
		Last Modified: Sat, 08 Nov 2025 19:40:13 GMT  
		Size: 18.6 MB (18620276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d594477dba9008d694b003f268faff2267e72cc9d7a434b02d268460fc3529b0`  
		Last Modified: Sat, 08 Nov 2025 19:40:13 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853a3f70b190745c4995a4e2617328372f73e8d45300166ae8f151c5bc5d6131`  
		Last Modified: Sat, 08 Nov 2025 19:40:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:daeebd64aded704403c5b1a7e1e8b80b2b76a15f8fbf45afc2a0b720a53d0b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3828165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df92fcc2697bbde414f8488f97148ee8a7447c3138f82e75b7d443030e525af6`

```dockerfile
```

-	Layers:
	-	`sha256:61d0ff3260d5ae8639a577750bbcd65f4cbd791170da4454ce806a77d95ae798`  
		Last Modified: Sat, 08 Nov 2025 22:43:44 GMT  
		Size: 3.8 MB (3809813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0e558aabd6bd6704a29accd1d1cf88d3e3aee5726d4c29b768912af26ea7dda`  
		Last Modified: Sat, 08 Nov 2025 22:43:45 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
