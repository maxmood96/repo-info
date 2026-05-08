## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:d8ec9ccb03a881b7132b75d5e231d1d3a774ef86b854db431928b4f98d36dbdf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f0d6dc402a362079ed9f0085af7c242ee2d3f91b310c322902782a28c44a3619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220796641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f03d3ef7a82b34386049b8bcc9fe0a0f05dab55e31f826d7412223aec68757`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:06:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:06:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:06:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:06:13 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:06:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:06:13 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:06:27 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:06:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:06:27 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:06:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:06:28 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926b73f3deaa412e41a5c599cc4a156e8178eb8f3b8b34559ee4e2b135ab7f51`  
		Last Modified: Fri, 08 May 2026 00:06:49 GMT  
		Size: 145.9 MB (145886206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243eb5606eeb0b1fc7247e5ddc90df1c3ac3e37b7f19c9caf729a21c057fe210`  
		Last Modified: Fri, 08 May 2026 00:06:45 GMT  
		Size: 16.6 MB (16629538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee17b04b3e34a830d593d08e987d291370eab5f357961310343ac5b34dd76582`  
		Last Modified: Fri, 08 May 2026 00:06:44 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8a0a4b733307530d49c0d8126e0b39ece97e1d62b364a4e2094a5aec0a0d59f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:853a4a225a915779b2d2c3e3cdf16d552ed48e5ef6c427c1cf71a4a8bea6dff7`

```dockerfile
```

-	Layers:
	-	`sha256:09c63ef2337b8971a3733d43d58dd13c604fbc47cb6cdc9af50778674741ffcf`  
		Last Modified: Fri, 08 May 2026 00:06:45 GMT  
		Size: 4.5 MB (4506005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:664c8e3282c6b9b114c1e840b273b783d21cfb6feb31e581d6f48d4bdd61ee92`  
		Last Modified: Fri, 08 May 2026 00:06:44 GMT  
		Size: 16.5 KB (16535 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:769fec2eb7e782d245c5c4d7bbbc8388ea860f44cd7ab8bf8419772ed0547fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.0 MB (215969451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7026d0c55a477d54ef3001e42cc69ba08999287591324758c09bceb258a77fa`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:07:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:07:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:07:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:07:45 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:07:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:07:45 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:07:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:07:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:07:59 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:08:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:08:01 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a2a4b94a11271473007f83172b4e762c98f385e20901aec6e0292cc59626bb`  
		Last Modified: Fri, 08 May 2026 00:08:21 GMT  
		Size: 142.6 MB (142582245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8530f9db220d1fd6969660b397ff43548e3447cb08c32e1676b4b6af26c21b48`  
		Last Modified: Fri, 08 May 2026 00:08:18 GMT  
		Size: 16.6 MB (16616430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff521a257a61153670affb9b9fbaca5ab835a7646bfd89061879a6e641846eac`  
		Last Modified: Fri, 08 May 2026 00:08:18 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:72f262cef54bfa3bbc576627272edd2d7f603ff4dddeca1ad96c14289a43576b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726580c3d5ae7f60c58e5386fe52c10f0bd7cbd59bd899a3c235765b635410b0`

```dockerfile
```

-	Layers:
	-	`sha256:b9dad1a7a1c5f1cd4beb96b8adfc51d5a27a090fad37a7bb71fd3385127ba001`  
		Last Modified: Fri, 08 May 2026 00:08:18 GMT  
		Size: 4.5 MB (4505597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:626d4a96c68f15983183dbd4f44933a6e62df8f365756e7692046464fedf2390`  
		Last Modified: Fri, 08 May 2026 00:08:17 GMT  
		Size: 16.7 KB (16657 bytes)  
		MIME: application/vnd.in-toto+json
