## `clojure:lein-trixie-slim`

```console
$ docker pull clojure@sha256:0dab63bd90226e42f8442615da0ed844d7dc57555f0a86465b34746d7407590a
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

### `clojure:lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2f265bc90ee4b0b4f18a2e5dd52eda4593fe7df2734291126758364073252d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143000277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06ccee5104b380c17d7aaea7a6c298aaad3e4cdbee7060b6ef9b8e82d491ee9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:57:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:57:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:57:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:57:12 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:57:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:57:12 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:57:28 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:57:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:57:28 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:57:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:57:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:57:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:57:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edc6fc8698289953a24180c95b172dc14969bcd79196a912bf1616786e1bc19`  
		Last Modified: Tue, 24 Feb 2026 19:57:49 GMT  
		Size: 92.3 MB (92256301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bd90d1b96bf67b7f3ce6259b8e8978241b2cefc3c3e2efd63f18f623fa126d`  
		Last Modified: Tue, 24 Feb 2026 19:57:47 GMT  
		Size: 16.4 MB (16447161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f51b23c47f40d45b9aa3a953ea80960d3cd9dad0e369509a23d0e4b899d288`  
		Last Modified: Tue, 24 Feb 2026 19:57:46 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf239b13d995163c49e71c4b47014f639eb2ee88f20f5e30937888dc78842b8`  
		Last Modified: Tue, 24 Feb 2026 19:57:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a58ffc86be5c450db79bc891e724be385ff07abec0ca86023967919c75abef29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2351837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f86f9b129f8b8b426bc5e7229e7a48e7211f80b0eece809290fa31960b27429`

```dockerfile
```

-	Layers:
	-	`sha256:29c8db4221b65daf0b5dff93034d5d46c60cef8812cb4fdd20d54962407f300d`  
		Last Modified: Tue, 24 Feb 2026 19:57:46 GMT  
		Size: 2.3 MB (2332804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ab7019c8bf23b1b42b64e0d1a0ced366f1c0814fdeed2b9fdc6b25f93ca7a62`  
		Last Modified: Tue, 24 Feb 2026 19:57:46 GMT  
		Size: 19.0 KB (19033 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:15f368fe03991cd49e9804e2f9906820b711ae1a577697266813598061dc8d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142360183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6614d0f5873704280b2ba63ea61dda43623e0edafc6cfb716e17a8756b822c11`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:07:46 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:07:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:07:46 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:08:02 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:08:02 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:08:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:08:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:08:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:08:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c702bb5e8410fb710a9fd14be7daa96fab4bb75e1c89df2b9d216243bea9559e`  
		Last Modified: Tue, 24 Feb 2026 20:08:21 GMT  
		Size: 91.3 MB (91288274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9346b9100ac8e8a686b1a552f3639de0ceac8c4b280fcfcd2c9ff0dc41dcd93`  
		Last Modified: Tue, 24 Feb 2026 20:08:20 GMT  
		Size: 16.4 MB (16413645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094ba1c63f35b1d0fae3e3cf9053313cdb6ef096fbce5179d6041dad15180ff5`  
		Last Modified: Tue, 24 Feb 2026 20:08:19 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4842d766e975202f0a207e7e66e540a1530315ba816f63b3bf68f7d177c0c6f4`  
		Last Modified: Tue, 24 Feb 2026 20:08:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:15f9344ea62c06d81d7b712bcdca962c135c1288633473751a3cd4769265bd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2351622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf54756359bcc4dfc3f67fbcd678e36defde724d84927b6ee84f7b8b99a43682`

```dockerfile
```

-	Layers:
	-	`sha256:1ba3c17796d3f0b55c3e9f3a34ff2abe88c86cb8978ad0bb9eefe58b15c52ba1`  
		Last Modified: Tue, 24 Feb 2026 20:08:19 GMT  
		Size: 2.3 MB (2332443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eec383262f0929cc4719fc76fc04c81d499a33c632dc920bec0dca768b64454`  
		Last Modified: Tue, 24 Feb 2026 20:08:19 GMT  
		Size: 19.2 KB (19179 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:9b71de11cd9be47983ec38470ea7518be686e995e00fc7eabfba2646498ea25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146236216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109f678caa38eb7c2902649a4d374eb284e0c0b87a2358e591eff324a4f187a4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 02:16:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 02:16:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 02:16:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 02:16:00 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 02:16:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 02:16:00 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:16:49 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 02:16:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 02:16:49 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 02:16:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 02:16:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:16:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:16:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298dcaf9753f81c5e53558fa373fd37f301367b171dcf2c711fb1baa27c30921`  
		Last Modified: Wed, 25 Feb 2026 02:17:31 GMT  
		Size: 91.6 MB (91633002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ee467a8c8658854414e315888052b42adad22f630403a1092286b7db3bf83e`  
		Last Modified: Wed, 25 Feb 2026 02:17:29 GMT  
		Size: 16.5 MB (16484814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4f4a35c3040464a83501b6de5920e54fe6fab26a4f9d60d076141d1d8d171c`  
		Last Modified: Wed, 25 Feb 2026 02:17:28 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ea4d482f3f8e8331160c503f471909a3e4016dd7d451203cdf23da92ef482`  
		Last Modified: Wed, 25 Feb 2026 02:17:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b090d08a26b90da3cfa2956eb66ee3932324810098c99d3cdc1fb4cce825881d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e508411775e8339a55418259bc7018eee96d81401184d77ec18e70f544103af8`

```dockerfile
```

-	Layers:
	-	`sha256:c9306a67c05b2eb35fa3790c3ccdf2d7a67538bb3540e2d9a712937d1e7dfacd`  
		Last Modified: Wed, 25 Feb 2026 02:17:28 GMT  
		Size: 2.3 MB (2317108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:296b4bc42fb56d8771e370c762e703ee2f32255611502ac4794a196e00838c23`  
		Last Modified: Wed, 25 Feb 2026 02:17:28 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:390d5be9fdaaaba4d00f27e665d083364a3050dc360944f1d3f6d88e609d2ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139965978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed3ab0ce166dde1c5e2e98ebf53f9b21714be277eb95345817ff91577136cbc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Wed, 18 Feb 2026 11:37:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 11:37:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 18 Feb 2026 11:37:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 11:37:05 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 18 Feb 2026 11:37:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 18 Feb 2026 11:37:05 GMT
WORKDIR /tmp
# Wed, 18 Feb 2026 11:38:38 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 18 Feb 2026 11:38:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 18 Feb 2026 11:38:38 GMT
ENV LEIN_ROOT=1
# Wed, 18 Feb 2026 11:38:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 18 Feb 2026 11:38:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 18 Feb 2026 11:38:54 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 18 Feb 2026 11:38:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a69466dfc7b8b2fe8edf62758177fe993cfe6f66d072d0ca0803ea54b9a979e`  
		Last Modified: Wed, 18 Feb 2026 11:42:30 GMT  
		Size: 90.8 MB (90773436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713bade42f344ec05f37954820e5d2cf60b13085aea7505efc44160c9cd5eb41`  
		Last Modified: Wed, 18 Feb 2026 11:42:18 GMT  
		Size: 16.4 MB (16397939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8ab99896a59b52a1b5a0017ba63c0426f57e05a6821e522cdf39e291445456`  
		Last Modified: Wed, 18 Feb 2026 11:42:15 GMT  
		Size: 4.5 MB (4517784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea6825ef778a00b3304e1a0e4526b8bf42b7b7a0f4bb3d4a364a7e22d6887cf`  
		Last Modified: Wed, 18 Feb 2026 11:42:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:33092078cb90908817e78e32735e1f80528166c6efd4741f7b26bf9668791b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2325965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3648d92b0521d715c53c224ffacdc7dcd245f44f6ff96a0f3317d565d5b0ee54`

```dockerfile
```

-	Layers:
	-	`sha256:42f788254f3d00a3e316ad624b38fc8a8a0ce752076bd14516ad72dcd5797832`  
		Last Modified: Wed, 18 Feb 2026 11:42:14 GMT  
		Size: 2.3 MB (2306875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81c8aca4c544a69629aae30aedc018c8f711cc729958a53b4e64ee1810f90635`  
		Last Modified: Wed, 18 Feb 2026 11:42:13 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a0b69bf98ed07a6255d9b5e23549bc2496f1b6f72676270a48d6837d73a2fe31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139073673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fda94ec68cf73d26d37e23532df5935da51ffbd8e15f40132b63827a7af35a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:24:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:24:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:24:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:24:44 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:24:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:24:45 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:25:10 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:25:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:25:10 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:25:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:25:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:25:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:25:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17752fdef1f284b40fe320bd54d7f9eefb1972a0ccd86993bc2287b508f560f7`  
		Last Modified: Tue, 24 Feb 2026 23:25:51 GMT  
		Size: 88.2 MB (88233869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b41e8e43554d43ec225c75dc12640848157147ee64db34b7ef25a170730a3a`  
		Last Modified: Tue, 24 Feb 2026 23:25:50 GMT  
		Size: 16.5 MB (16483462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ee72e81a01f02c2558987b390da7e1994b9caabe487ca714a4cb5bde9b304e`  
		Last Modified: Tue, 24 Feb 2026 23:25:50 GMT  
		Size: 4.5 MB (4517733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2cba248795a969c7453b463e4e734f5577cb0dfb3934c1b73a2d571680970a2`  
		Last Modified: Tue, 24 Feb 2026 23:25:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:64c9ec5fe8076ecf7f0172f2b8699f1e4815639e2a142dc0df1bd5968e800884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2332827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4b4cc4583e9d8f0d14f250ea23a3bdfc3ce81001210c57397ad6e99fe3bc7a`

```dockerfile
```

-	Layers:
	-	`sha256:9521f83aa93cb8a50c687486a4e81b83ae5e38dd6d84b527c67afc68917a7d1a`  
		Last Modified: Tue, 24 Feb 2026 23:25:50 GMT  
		Size: 2.3 MB (2313793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ebb0edc6007021dfd4560b729971f6bb1f77d927441a0e2975751e9f6cdee95`  
		Last Modified: Tue, 24 Feb 2026 23:25:49 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json
