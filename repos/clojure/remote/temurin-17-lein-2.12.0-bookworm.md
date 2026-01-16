## `clojure:temurin-17-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:b88f1eda2a3c75d7a22d6033ee7c096880b3e569466d9f6cae23f74b69759817
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

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:96f31b4c173abd6d1ebb5313950ac490262f2d5b81087edf6140a802e06afb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217650297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f607c9b9f6dc9c7f9d0736f1f949abcff11e954685fa6324772ac4575b76c5f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:29:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:29:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:29:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:29:30 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:29:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:29:30 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:29:45 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:29:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:29:45 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:29:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:29:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:29:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:29:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9878220792f6359931cab302edc178e3b7fdef1f4b210ae11805cd62138fb7b3`  
		Last Modified: Thu, 15 Jan 2026 03:35:02 GMT  
		Size: 144.8 MB (144847951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfad7d11f90e1f5aef3f2490c532011613205ff17a956cde233735700ae50dda`  
		Last Modified: Tue, 13 Jan 2026 03:30:18 GMT  
		Size: 19.8 MB (19802537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69bb7e4df4980107fa301f0943a9e87616f656f0ff74ae986fd768a2c5f6917`  
		Last Modified: Tue, 13 Jan 2026 03:30:16 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71cdd30871ea952f07ba6098188e07991ee31522f45bd268d0c9b52fed88b55`  
		Last Modified: Tue, 13 Jan 2026 03:30:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b660c9f9e895a6e60b00a3c7b80c9e20462b1f4fc1f5964ba1f1a6c37a74ca7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4298847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f52f77fd833fd2dea6742892eaf598e3085fb2a3ac915f872b1e0ce9528f66`

```dockerfile
```

-	Layers:
	-	`sha256:9e6962e5d95e8f84ce858415b95dfbab82d84581311f61d3db879efdc05ffe6c`  
		Last Modified: Tue, 13 Jan 2026 07:39:58 GMT  
		Size: 4.3 MB (4280479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ef32f1ddf42fdac31dab8af23f1efee8515246b7cf04b44e4cfc18f12789ee4`  
		Last Modified: Tue, 13 Jan 2026 07:39:59 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dd7bd979b7fc72f3f8b406af87b12b5349cee3d699fd2d13035cc37fe5af722e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216196802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f843a4829cccdb79c107cace3765def6781d0d98d73185320130c98f277af2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:33:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:33:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:33:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:33:06 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:33:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:33:06 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:33:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:33:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:33:20 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:33:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:33:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:33:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:33:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd037e8e598bab2bff12fe99dc314546db776820515e396a519ec49308c03bc`  
		Last Modified: Thu, 15 Jan 2026 14:05:52 GMT  
		Size: 143.7 MB (143679920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25fe566a7080cfae4685ca75a7562b4bcdf591824c9356899948373362f6543`  
		Last Modified: Tue, 13 Jan 2026 03:33:49 GMT  
		Size: 19.6 MB (19632657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2fb4580152eb9450a711080f4b7a5bfb2bc34b3b63d211a66c2031389c3835`  
		Last Modified: Tue, 13 Jan 2026 03:33:48 GMT  
		Size: 4.5 MB (4517724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389b604463ac772d04e06fdbb9661d5fd47987b512113a7ef8c98fdd0ddb8ccf`  
		Last Modified: Tue, 13 Jan 2026 03:33:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d630b32be388a8ff60555137738170dd63167563964823e4c95baf3de162aa05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4298583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3a0e37a7ef0c56f38d3dd16705677402db7cb60ab3d10717df8977dcc8d515`

```dockerfile
```

-	Layers:
	-	`sha256:02f200a48641ad21181ef486b50e5b60635335d0c4f79aa24b2de44936558de0`  
		Last Modified: Tue, 13 Jan 2026 03:33:38 GMT  
		Size: 4.3 MB (4280094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b0a07b05be60b36d66b55ae2e47a476adccb831640332e7aaf034a72052be04`  
		Last Modified: Tue, 13 Jan 2026 07:40:06 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:3ec867161e4320e2f1fd7af8cc2ff80546fd7db02a5eb1be6847afe5813d996d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221393364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddbe66dd23fb44ac5251027ede4907e4aa5969bdc7aab0af1b7b4c3402a61eb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 05:40:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 05:40:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 05:40:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:40:49 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 05:40:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 05:40:50 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 05:41:30 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 05:41:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 05:41:30 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 05:41:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 05:41:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 05:41:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 05:41:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:39 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd3caecfdd7b6952c5561a9744f7d3d4cbbf3ec2c42a80cea345e4dce59f22b`  
		Last Modified: Tue, 13 Jan 2026 05:42:17 GMT  
		Size: 144.5 MB (144525182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750d63f93f4ab199273957b839d6c3cef6abef30558fad2e6e82f87a6240c459`  
		Last Modified: Tue, 13 Jan 2026 05:42:25 GMT  
		Size: 20.0 MB (20022610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf9d76cc627cfd1d09bda715eb99f17142da72ff657d62bee90f7ed9040feb9`  
		Last Modified: Tue, 13 Jan 2026 05:42:23 GMT  
		Size: 4.5 MB (4517767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c32f556ad1c431dbab08fdbc93843f3a091634ca14f9c8cc7384affbd2cd1bd`  
		Last Modified: Tue, 13 Jan 2026 05:42:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3b6eb5bcfbc2976842e7e5a6915013725d503bb84f16a8716cea347331153926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d6e20abd6ba837eeaabdc93aa76e57f46b71164b5f712dfe22461562fb227b`

```dockerfile
```

-	Layers:
	-	`sha256:76ab1ff4cad2e37cff46ac652d8f2b7f399ab6946e3818922c7ab623ac991672`  
		Last Modified: Tue, 13 Jan 2026 07:40:10 GMT  
		Size: 4.3 MB (4282340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b86837036fadae16dc1a7ccfa41a21532dcb2bfd76703fc8793d8f1404369d99`  
		Last Modified: Tue, 13 Jan 2026 07:40:11 GMT  
		Size: 18.4 KB (18412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:df645424094ade0db46c3d50984c5f31349287fc63bbd52a170e097298a3d7d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205977724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba305631f1287ce6621bf3747de817849cac92eb5e04a8713009ed195c516c1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:02:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:02:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:02:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:02:05 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:02:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:02:05 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:02:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:02:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:02:15 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:02:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:02:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:02:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:02:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377e101c17ebdce9c73b4b044ea0633ed12041cc83ca9e8b72b3585c8ea37029`  
		Last Modified: Tue, 13 Jan 2026 03:03:00 GMT  
		Size: 134.9 MB (134859065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6594db14b4b01ac7a8c5a078e3be785d8d6b4037827cb1828cd8eb4e4e5092e`  
		Last Modified: Tue, 13 Jan 2026 03:02:52 GMT  
		Size: 19.5 MB (19462050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7620172d68ede34d41aa010f6c2d53adbf9c9814a3e63b0d2de417c462f55b1`  
		Last Modified: Tue, 13 Jan 2026 03:02:48 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa91d9872c316752736059ae891f73d8a3af66934b8fc72fc37f436051b46aaf`  
		Last Modified: Tue, 13 Jan 2026 03:02:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:68a5cfc0a3502f48164ddc047858f7ced229c3e7c4d72ee036395829edb8156b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4290661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59818b3e52dc0594031fd5f0da458ea62c427ab84fdc5863fd8765e4e55dd002`

```dockerfile
```

-	Layers:
	-	`sha256:2b5dab3e03531ab0b35d487eabc58efa89ee8cc3d45a8dc88768a082dbb31bdb`  
		Last Modified: Tue, 13 Jan 2026 04:37:31 GMT  
		Size: 4.3 MB (4272293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c63cc414a23d9d97b443dc269fcd8360cf2457d2f195fa9e960c739f803a59e0`  
		Last Modified: Tue, 13 Jan 2026 04:37:32 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json
