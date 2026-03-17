## `clojure:temurin-8-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:87d5b3b571b3a857d69193d388700bfd1e25f33451f1de5a8386bd85c66729b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0db2b6e250b6bb2f77d836e0709e46bbed72c658e71404a26f78719d9f4156fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105284482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd914409d01ab8254213b43f750c5178208489457af47ab849cc41d0ee51d26`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 02:55:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:34 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 02:55:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 02:55:34 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:55:48 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 02:55:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 02:55:48 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 02:55:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 02:55:50 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18274e6c2645fd55899846bb8b158083e568f972fabff2cd5754aaf923daddb7`  
		Last Modified: Tue, 17 Mar 2026 02:56:04 GMT  
		Size: 55.2 MB (55170146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315920bae76a38580fb0e3b23c51fbf36bb64534d6ea123300738a3a660fde7b`  
		Last Modified: Tue, 17 Mar 2026 02:56:02 GMT  
		Size: 15.3 MB (15338724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6221ae6547cd9d1986dee09bbf73f2903f0d7c4521a40b9165e898d57714b9a7`  
		Last Modified: Tue, 17 Mar 2026 02:56:02 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bacd476788589abc28bbb459f6f985e810167f5bee27b695c1002fb487dc1180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3164971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2834dd5bc43126c0ad23697dc4eae4b592b0fc8d5e27363acf5fe09cc3ec79f9`

```dockerfile
```

-	Layers:
	-	`sha256:648250de95405200e3d4417caf828f61e05018017d482b39be9babb2cf86e587`  
		Last Modified: Tue, 17 Mar 2026 02:56:02 GMT  
		Size: 3.1 MB (3148571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4ef70b25ff498aedd0cb6b44454b9f9a0212b4d71b2245c3f2605ca67fa329`  
		Last Modified: Tue, 17 Mar 2026 02:56:02 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3995c4fd22334f581cef50e2e6673b2158f5edaca83f843c9084cf9e583c68ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102841143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f72b7d33d22cc1c07b28e4d452811b3175e775fb780b112dcd8a02baa6396b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 02:59:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:48 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 02:59:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 02:59:48 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:00:02 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:00:02 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:00:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:00:03 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265a17e34f53e6cdf6859c95c4c7266c17eb62a024bf8304f2bfc68cb1a9b9f6`  
		Last Modified: Tue, 17 Mar 2026 03:00:51 GMT  
		Size: 54.3 MB (54251630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51924a289af08afc1dc637285ef6079c52ec6c65813740d262377b09ba0aebc`  
		Last Modified: Tue, 17 Mar 2026 03:00:41 GMT  
		Size: 15.3 MB (15327241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90e905f4aab24e65fc9d0c077f01718fbca5b503b6e57cb9b5790f54f1a6705`  
		Last Modified: Tue, 17 Mar 2026 03:00:49 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:356559a4297708fc9863f03bbac0ceaf1f82ecd8ecef0755a9615e13407201e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3165401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38e8e0528821c27b5574774020c180642ec29de4060431c050a034b8ab0eab4`

```dockerfile
```

-	Layers:
	-	`sha256:df117c032c1e5d52cb0c06de12964a15fc3f14368568c159c6650b7645e5c2b2`  
		Last Modified: Tue, 17 Mar 2026 03:00:39 GMT  
		Size: 3.1 MB (3148880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:171b24597656fce8a49fca3ee6145e24aef549669d78d9914ba779cd716ddcff`  
		Last Modified: Tue, 17 Mar 2026 03:00:43 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json
