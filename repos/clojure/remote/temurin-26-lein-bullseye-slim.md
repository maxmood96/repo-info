## `clojure:temurin-26-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:fe3f9bea26591be65d1201afe8021e62e3cc2328db62aa11fca9b13c3f9e8145
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:46079549af5a495d26c642a0362c203738fc516330de1bd56f690f22577d7b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144570547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed0c39b94ce8a632b1fb00d506ec2390c2ca594454e8dd5f7de33dc31c1aa45`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:49 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:21:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:21:49 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:02 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:22:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:22:02 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:22:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:22:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ae0071b177c3b9d3e864a56362d5ae9a6c98db5f7771f53d32928ace9e3da5`  
		Last Modified: Wed, 22 Apr 2026 02:22:22 GMT  
		Size: 94.5 MB (94455690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88f3ab2f616dccf4e93a4e1c67546fa546b4fcfd5bbfa1c228d62f89ad3502b`  
		Last Modified: Wed, 22 Apr 2026 02:22:20 GMT  
		Size: 15.3 MB (15338746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3858a721d91bd090c2ccb6836ff1a9bb1b8b5ed4719082f24a3bb0850158fe7e`  
		Last Modified: Wed, 22 Apr 2026 02:22:19 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62813c9ff15a4d7589d2f73c8c0657ca291bc7b347ff0b7e47d22b88a156e0fd`  
		Last Modified: Wed, 22 Apr 2026 02:22:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:982a52f284accad5818dea12dcd23944271e4fb0b20802178cbd440a20b78732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2723d58f315f91f086f843442fddbe046bac9f47d5d3ff15ae1777bc1c8d030f`

```dockerfile
```

-	Layers:
	-	`sha256:7e17f220c60c396b853c828122fde86192a7aa935165b1c138159e961e5b147d`  
		Last Modified: Wed, 22 Apr 2026 02:22:19 GMT  
		Size: 3.0 MB (2993086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f800e1457a9c5ddf45f920a07ba139459633dea35646d37eaf3b9c46ed365b1`  
		Last Modified: Wed, 22 Apr 2026 02:22:19 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ffbe9fca1b1cd3458373a5cf5a74374fc8c7de24ff616cf46337d7e7a63991c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141983158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e4f21db599e3a03259dc8e1b1100b7d9cb01dde95fdaebbb51b582d037ded5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:24:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:24:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:24:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:24:39 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:24:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:24:39 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:24:52 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:24:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:24:52 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:24:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:24:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb5cb142e5332c68b04339cd11b5a67a58acb5c2ef97e105c9cf0c54ba0ce77`  
		Last Modified: Wed, 22 Apr 2026 02:25:14 GMT  
		Size: 93.4 MB (93395200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a14673207a6d1649fd7240a0c7e40d16158c2023d21f4c037fbc2cac5ab1f6`  
		Last Modified: Wed, 22 Apr 2026 02:25:13 GMT  
		Size: 15.3 MB (15327261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e033fff4491fe17d929a1f32389b2779318dc5dbbf0723a8eda81d4e8537d927`  
		Last Modified: Wed, 22 Apr 2026 02:25:11 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e7c5cfb713ee634b7ac9d679001c3da682230f260d7a7fa44f5266493c5813`  
		Last Modified: Wed, 22 Apr 2026 02:25:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:34cc8bbadca8c0a589550abc5f488130a3324f9d0b242fa79ac4e3a0930fcaaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc8b49fc4783741548e97e56a41db950351f2fe765ff16980c9de308cb75e3b`

```dockerfile
```

-	Layers:
	-	`sha256:8bc582d1d32f1b0ce50e35244389a143641675e6430b19b72eaae61d43fdb455`  
		Last Modified: Wed, 22 Apr 2026 02:25:11 GMT  
		Size: 3.0 MB (2992692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9124642a5fdec9bd0f27926284852d945213577847b953423f2029a3e7fa9c40`  
		Last Modified: Wed, 22 Apr 2026 02:25:11 GMT  
		Size: 18.5 KB (18517 bytes)  
		MIME: application/vnd.in-toto+json
