## `clojure:temurin-11-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:60a963ad5e2e8c2883f901ed59a8305d40e496fd20ed14584f8cdd85de99f5bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8bae0733976357607745bfcfad216f4c1b55ad0fa6fdae000e39fe862f82fbf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195921382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf10c157093d8cb59c94c0f1d98fe10f04dfb810800579782926af69cf91275`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 02:56:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:56:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:56:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:56:54 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 02:56:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 02:56:54 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:57:09 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 02:57:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 02:57:09 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 02:57:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 02:57:10 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83ea031e9788cb4832e1a9eaaf4d5c2bfa117fb2d150f6d860bdc92233a20f6`  
		Last Modified: Tue, 17 Mar 2026 02:57:29 GMT  
		Size: 145.8 MB (145806965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc801f4676003e040ada38e120265c26c0b0caf6186f66811833bb3d115ac77`  
		Last Modified: Tue, 17 Mar 2026 02:57:27 GMT  
		Size: 15.3 MB (15338851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8930d38ab3b2ccc8617aed30f2f2d17bbafe81fbc2bf364dafd4d1ba0307f8e2`  
		Last Modified: Tue, 17 Mar 2026 02:57:27 GMT  
		Size: 4.5 MB (4517708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:efe234830d8dddda09b9286b980901af60c317101ea29eb0f2caeba2b7b58b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715d7b0dd2db8d722ac2e7257d1204c624c49b802b7750ceaf72a6e83aca724a`

```dockerfile
```

-	Layers:
	-	`sha256:4aff37bca210c0e97830d3a1d310035dc0ff2c107fe2035e7016a2034dbd6cee`  
		Last Modified: Tue, 17 Mar 2026 02:57:26 GMT  
		Size: 3.0 MB (3047723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71ef52170081c767a53f7313505dc3718c82d36abc77440bb7e92156697eab53`  
		Last Modified: Tue, 17 Mar 2026 02:57:26 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c2ecfe4a1d0122e682914bb5193f4bef495a9ca30f2679d69748b43e10e22fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191089503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db28b0300a2de77931d1ca0a89e65b9c11bb04769e2c8575281ff6bd7d75571`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:01:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:01:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:01:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:01:21 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:01:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:01:21 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:01:36 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:01:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:01:36 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:01:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:01:38 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2219d3c6ae11fe238893ef89c07f58953ee1c8d2579d7d4f7e3a4f38581fbc78`  
		Last Modified: Tue, 17 Mar 2026 03:02:00 GMT  
		Size: 142.5 MB (142500018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805ed432d7bd7830d4dee37af327cb3fa41eb917c23501f95a4e634dde7cde6a`  
		Last Modified: Tue, 17 Mar 2026 03:01:58 GMT  
		Size: 15.3 MB (15327170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d46b451217c93999f44fdd8e581ebe2fc6a8a3cfefda7cf898080906b8b98ed`  
		Last Modified: Tue, 17 Mar 2026 03:01:57 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9c38f63ceec342ac0a1a67433351c8901d10ed19d68957eb3528697af8f34fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b751584fb4b9ddfbeb8fc88de5716a8520286b67cc79d5fe2033ef38d74fb15`

```dockerfile
```

-	Layers:
	-	`sha256:6dc81cc04c4cc9d9a2929109009dc3e6377b9b789019fb5bc835372ec6e13247`  
		Last Modified: Tue, 17 Mar 2026 03:01:57 GMT  
		Size: 3.0 MB (3047950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa18c2a7ece1130f2824f291b669d14d8d6677bdfc442d247dd6bb07b91e1f45`  
		Last Modified: Tue, 17 Mar 2026 03:01:57 GMT  
		Size: 16.5 KB (16531 bytes)  
		MIME: application/vnd.in-toto+json
