## `clojure:temurin-21-lein-bullseye`

```console
$ docker pull clojure@sha256:316535443dc117b80a501b7889c7409fed41dac93d6a457f623139c4fb44dfea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c10c807e287a5313ffd9bb9b857dcc13c41b9ce0bb45ef76a160f618534e2569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232767877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6363fb1f1beda0b5997141b55f3626d79398bb97c0f0e5e69fb5e9447ac278da`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:19:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:13 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:19:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:19:13 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:19:28 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:19:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:19:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:19:29 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:19:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafd308f62cf3dd75e9a399db7fa22aeb3a0c598a94eb2809da059e93c165d37`  
		Last Modified: Wed, 22 Apr 2026 02:19:51 GMT  
		Size: 157.9 MB (157857060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872144d9ef231db79e14c2ade09ebb28b5aa88dd750d0f52a1da302003e5993f`  
		Last Modified: Wed, 22 Apr 2026 02:19:47 GMT  
		Size: 16.6 MB (16629538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40de90656d3a0b3133ca7b82933e4e6cbe5a414ffd37ae08650664a627bcb7ad`  
		Last Modified: Wed, 22 Apr 2026 02:19:47 GMT  
		Size: 4.5 MB (4517700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc303eb781095ca050a140201d4c5681ddca6f74c59dcc3c45a5f80eacc39c2`  
		Last Modified: Wed, 22 Apr 2026 02:19:46 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d86ff6735b85c121f03dedb131856a59333779d273c86a0d256879e8b64df9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b1f83f8bd6c874c77c7b358604294eaa08e08039eb7f6dcb678ed42f2b4fee`

```dockerfile
```

-	Layers:
	-	`sha256:1dfcfb2f000a23f190f4271804878e039cef66d27f42ce00f88a05aa25e52744`  
		Last Modified: Wed, 22 Apr 2026 02:19:47 GMT  
		Size: 4.5 MB (4487714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08499f541718333bc85a450e53dd62cb8b3842ba4a24a401f64810b0dac3461e`  
		Last Modified: Wed, 22 Apr 2026 02:19:47 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3f237d6903738f30df27e7d8aa0a73713c9ad3d7e75e180deccc747feba7fba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229520722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59eb0aaff21bfa6d86c9fb106b634d3ccf682d0ebb286b2d50e7eba13b7bd1c6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:22:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:32 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:22:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:22:32 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:45 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:22:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:22:45 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:22:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:22:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3854926ffb4240d3079f2f4996089ddfbce787cb2cce59297bc05f8811172939`  
		Last Modified: Wed, 22 Apr 2026 02:23:11 GMT  
		Size: 156.1 MB (156133028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626b677d8b96d552ec975805cb5cb3d8b62f7c851ba6c01fd7c27d55897fb6e0`  
		Last Modified: Wed, 22 Apr 2026 02:23:08 GMT  
		Size: 16.6 MB (16616510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c05d043d84808690199ee55423ffcc0e7b125fc30ce3213d0d95b43cd677ee`  
		Last Modified: Wed, 22 Apr 2026 02:23:07 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6285fca4eee94b0761633d89a5ba6c6d126f996589cfa093cf85fdc9d0bcbb`  
		Last Modified: Wed, 22 Apr 2026 02:23:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1dc4eabc8542d45249131a3a593ab0e8ad8a0805bb3d37ceb3fbf2261c4a11b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4505177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c437fd291a0242120f219a6392d354550cfa7d352e45bd1932d5d45192fa83a5`

```dockerfile
```

-	Layers:
	-	`sha256:4c39fb53c0b30ea849aac645b9e9c033b7cec5c5da6009bb04a216776473b733`  
		Last Modified: Wed, 22 Apr 2026 02:23:07 GMT  
		Size: 4.5 MB (4486688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42345d9175cc4b5dea3f48a45903ae372ad8332124232b70ce8c6b89ae852896`  
		Last Modified: Wed, 22 Apr 2026 02:23:06 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json
