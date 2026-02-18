## `clojure:temurin-11-lein-bookworm`

```console
$ docker pull clojure@sha256:6a3ef2b6c1eb41bc2797e9af3074952a592ee5b02590243cc797f64cd65146b5
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

### `clojure:temurin-11-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4ac0bf126dc88b21c39f8a212484bd097dfa6362e00aa0a2d344f78c1006d486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218608806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b12dc917d5f4e9ac5d159eb3b41d4a2a9d4488ef837a624ee2d67e66e06140`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:41:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:41:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:41:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:41:20 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:41:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:41:20 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:41:34 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:41:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:41:34 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:41:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:41:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e3675be505d129deb95f2aa54dbb8b2c95185c50bf30e63a394422afb47db2`  
		Last Modified: Tue, 17 Feb 2026 21:41:55 GMT  
		Size: 145.8 MB (145806699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97062d62b2d9869f928fbd70095c94a1dfdb304910e7df1f890e2eab5b7d3bd`  
		Last Modified: Tue, 17 Feb 2026 21:41:52 GMT  
		Size: 19.8 MB (19802837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc7f8650602efbd2f377c6b04b47043b7fef0f5c6a411bc9b4dcd1c040fc660`  
		Last Modified: Tue, 17 Feb 2026 21:41:51 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:809a2fbfee5fdd6176d77de6314f284d38f59efa191300254cb521864e17fa88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4318253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e197e84b22564594375951fedda05feb945c1cba56b23692f0e3aec3a1f03cf8`

```dockerfile
```

-	Layers:
	-	`sha256:32197e664485d26d9d55294cadd5ce54dc1d91cf2b6540c6a196ff892d65d02f`  
		Last Modified: Tue, 17 Feb 2026 21:41:51 GMT  
		Size: 4.3 MB (4301872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9eb96c3127d0beb7923bff9ba40e2d576fda47a1faeac7f7133b454b63e91ee`  
		Last Modified: Tue, 17 Feb 2026 21:41:51 GMT  
		Size: 16.4 KB (16381 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:89ac76c230c4dceb9b42e684e5f6aedf8084e51dcf1d4741c3215b440e20f892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215017986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbcf2903649018b546d1d055ae26cea595a4cd782b3282d96ec63adfa602965`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:41:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:41:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:41:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:41:16 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:41:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:41:16 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:41:30 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:41:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:41:30 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:41:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:41:32 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c4325184fc1b13b747ced72eb99405263ad8af1a57fe9b0528cef416aa403b`  
		Last Modified: Tue, 17 Feb 2026 21:41:53 GMT  
		Size: 142.5 MB (142501423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bbcfe408c38618c13e48e350d0dc19dfca2a3713c5673013272d7c68078de7`  
		Last Modified: Tue, 17 Feb 2026 21:41:50 GMT  
		Size: 19.6 MB (19632817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a5da019b8b8c69482b50f3bb252ee3bb612576bc0ecb53fb8c2e203f168558`  
		Last Modified: Tue, 17 Feb 2026 21:41:49 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a2c4f4cf113ed0479425cd43aab84bb74af422d020ac9435c5e375c523c95772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4318608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e190fcb95ec0222fe239cf93105e6ff690ed8c4116eafbe4317e6c3d813432`

```dockerfile
```

-	Layers:
	-	`sha256:8b517c1a50fb9a2170afff5b48b18d058bcbc50ac9783bc1ba567322a361c3b6`  
		Last Modified: Tue, 17 Feb 2026 21:41:49 GMT  
		Size: 4.3 MB (4302105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55e52b25d06bf2b91d0f1ab3ae8c90f6c5eb82fd0212dca29905f528e89fb955`  
		Last Modified: Tue, 17 Feb 2026 21:41:49 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:0a403eaf7cd7ed6683c7cb17caa020101e790d36d892f9564f3e6123206d7965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209866685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad698ac3eb48b462f9128e633df61c5c8dc845847a1471535e121c119b32fa6`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 23:33:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 23:33:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:33:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:33:16 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 23:33:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 23:33:19 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 23:33:55 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 23:33:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 23:33:55 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 23:33:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 23:33:58 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b47947f163eae116857a151bacee4e62eeef47f193f3d24c01851afc3df70f9`  
		Last Modified: Tue, 17 Feb 2026 23:34:52 GMT  
		Size: 133.0 MB (132997795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7962d0521c05e34b28a3149a5da467fb5ff0a71c958768c4f396c98e6d9dccc7`  
		Last Modified: Tue, 17 Feb 2026 23:34:49 GMT  
		Size: 20.0 MB (20023815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c842ce407912a2bd8b86d268d5c8da50e28ace45a51800e8cc55a43860eb11f9`  
		Last Modified: Tue, 17 Feb 2026 23:34:48 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1bdc9f6c5c94c11689f6a57e6f5691312c403deab00476739855ebfb98270ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26759c61b3540d674a7845b4ec855cc79ecf4a81e89d2fdeb10230e1b124bb73`

```dockerfile
```

-	Layers:
	-	`sha256:7d96cd4b54b1bce3499d3bb8f536ff125d4334e3372f64793878f91f5cec1057`  
		Last Modified: Tue, 17 Feb 2026 23:34:48 GMT  
		Size: 4.3 MB (4303118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4be2cd6fb3a40f2e0fb1b415e28410990d81197d09a63d6d98cd5c8273f63462`  
		Last Modified: Tue, 17 Feb 2026 23:34:48 GMT  
		Size: 16.4 KB (16426 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:b39f5d663850a0f74689149cd55185bd94d69701f3004a3b835ea89dcd3602fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.7 MB (197681473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a5a85b154c9635c9c183389ae7837afb06a867fab2e511cdd66522176bab9b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 22:00:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:00:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:00:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:00:48 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 22:00:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 22:00:50 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:01:22 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 22:01:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 22:01:22 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 22:01:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 22:01:25 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e20b53c4756131e0afe8226f902291e2b2414a41626908c5000715a6ed3f93`  
		Last Modified: Tue, 17 Feb 2026 22:02:00 GMT  
		Size: 126.6 MB (126562021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffda87fe009e4751469a71c4e7999ebb575cd4c748f3606e7ba4732053a4c5d`  
		Last Modified: Tue, 17 Feb 2026 22:01:57 GMT  
		Size: 19.5 MB (19463309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a31ca02ee93be09d51cd7edc66dd9b5a6cfa5e8c83f08e28e618950c78d2fa5`  
		Last Modified: Tue, 17 Feb 2026 22:01:57 GMT  
		Size: 4.5 MB (4517768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f25386f99172adcecd759f9d1e352c0a02faac2fe67fd518c849793f59cfd71b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4310072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a880058655f5ae8430524b8e0703900e52e90b52d9ffc1600dcb478d7d9e02`

```dockerfile
```

-	Layers:
	-	`sha256:e288377dd8c789046640db33c3a73509f5c76b337287bb5932d8639a3d4a82c4`  
		Last Modified: Tue, 17 Feb 2026 22:01:57 GMT  
		Size: 4.3 MB (4293690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:863ff9c70bba78814bedfd3845f9627b46462843d1e9b0965533a4d874f8c7ad`  
		Last Modified: Tue, 17 Feb 2026 22:01:57 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json
