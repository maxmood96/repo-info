## `clojure:temurin-11-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:b25c4898dad0655d679175344889c3477651b8e01afd138128ac98eadcfabcd8
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

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6c51fe95e75eb3e2d9ff70206474352dffca9d92526bf258b22dac268bcf77cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196632260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947f7acaea4668aca95a92b027809a30ae793226700dfcd0a2d4cf014f4fc7df`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 29 Apr 2026 23:14:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:14:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:14:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:14:45 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:14:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:14:45 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:59 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:14:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:14:59 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:15:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:15:01 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a8a81099969d61585481dcecd6319e9f9454b8abd2cd3b3e99913f6d932979`  
		Last Modified: Wed, 29 Apr 2026 23:15:19 GMT  
		Size: 145.9 MB (145886252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925dee80f8173054d41351dc031d695eb5a9cf3700c15558df7090f78b17178`  
		Last Modified: Wed, 29 Apr 2026 23:15:17 GMT  
		Size: 16.4 MB (16448060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442bb8871a0d2852fac0016adea8d114cde88d6c884f00e88fa10ccb579ce7c3`  
		Last Modified: Wed, 29 Apr 2026 23:15:16 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:623bab4207ffcf75dc484cc0c829f93fcdb0a513770842d540c2d23aeb381c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c8a4dc7b87c9b6d03738a2649d0f7004da4f75346ebd53caf3c15bf803839d`

```dockerfile
```

-	Layers:
	-	`sha256:0975363e6243977a2d84cdf8616bab856c6d3b84adafcd733c65b8b8c3ab3c5d`  
		Last Modified: Wed, 29 Apr 2026 23:15:16 GMT  
		Size: 2.4 MB (2384931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fe6a8b26c206e5597f90985907da8e6d3af3a3f23eb2905309da89b672afa68`  
		Last Modified: Wed, 29 Apr 2026 23:15:16 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d3b520537bfef516b3c1097084fadd50181cdf758a444fae3e393d160c3e3e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193659234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6fa2569f1be16b05519c4f29b6ec9d99c3662783731caea1c2640622741f2e5`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 29 Apr 2026 23:14:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:14:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:14:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:14:22 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:14:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:14:22 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:37 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:14:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:14:37 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:14:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:14:38 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1847c42d906610f4e7f0da970361c9f6503c696326e0a4cfa91a57474cf05c47`  
		Last Modified: Wed, 29 Apr 2026 23:14:58 GMT  
		Size: 142.6 MB (142583978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8fd99804820edf86ba2596956d033218bc4486ed7cd7fce84dc2e6193ed37a`  
		Last Modified: Wed, 29 Apr 2026 23:14:55 GMT  
		Size: 16.4 MB (16413903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e145ee1a3e846cb48dc293b92b663c7b11ea9c39ad1295c777e3f52b594ff8`  
		Last Modified: Wed, 29 Apr 2026 23:14:55 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:058d7b40623e6f01ce4de95b64246fbd766936939a211914aea4a44a966735d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84030eaff374c46a0dca37b0cdc2d18ce15e899cafb31176a93939feee19a1c8`

```dockerfile
```

-	Layers:
	-	`sha256:915ea97daa93de2e96ed7c9f023ce3834e5a343819c4a8063e89e3bfe28505cc`  
		Last Modified: Wed, 29 Apr 2026 23:14:55 GMT  
		Size: 2.4 MB (2385167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ea2559454241226605c47d45a0a3210edf9b0cd47c5c3d4fbd2ccc442815fb8`  
		Last Modified: Wed, 29 Apr 2026 23:14:54 GMT  
		Size: 16.5 KB (16515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d0dc7b05a176d14f4f86524ffc047aa4909cd1a873c6bba1c6cb7866ef2ba1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187710853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3760c57d68707c925d1df9f4e59282573d6f04d879fa759f70fc8b760b37145`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 29 Apr 2026 23:27:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:27:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:27:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:27:00 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:27:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:27:00 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:27:55 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:27:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:27:55 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:28:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:28:02 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f7d7f9877c5bd685e55ef47de15acae7a1f615c5c4638a9366725a00badfd3`  
		Last Modified: Wed, 29 Apr 2026 23:28:51 GMT  
		Size: 133.1 MB (133109605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb437e01468b49c677b2a98ea0820286fb03a5b3910066cea27b86ebe5b05724`  
		Last Modified: Wed, 29 Apr 2026 23:28:48 GMT  
		Size: 16.5 MB (16485414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86505d848e502f0daacc429d19aa04aa4280529209b64ac9db01986c401f1455`  
		Last Modified: Wed, 29 Apr 2026 23:28:47 GMT  
		Size: 4.5 MB (4517770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cfad7e7927d5386a9ae342b060eb228e489253763c2f7b5758254f7faa6ec8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5f1fb58a88059be0b87683506bd45e851bfa8c8c25ae6236efd9f08dbee20b`

```dockerfile
```

-	Layers:
	-	`sha256:62eab40f213475bbdc736bd0b139376b39b4bd103cd40b5c6ea37dbc18bfcc74`  
		Last Modified: Wed, 29 Apr 2026 23:28:47 GMT  
		Size: 2.4 MB (2385296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19571612089b5328b1e43ee3237a7daef2df7161bfafdf7ed090db3b057d4e95`  
		Last Modified: Wed, 29 Apr 2026 23:28:47 GMT  
		Size: 16.4 KB (16438 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:22f4dd8ffef843c9ed7c2465f047b2b2d62a8bb648162ee4391df70cb813fcf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177494563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6befc61ee1dbced99f15a5de0bf78936921b852d95badac006995fb5b20bc449`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 29 Apr 2026 23:14:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:14:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:14:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:14:16 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:14:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:14:16 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:29 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:14:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:14:29 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:14:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:14:31 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aeee4edd1f5d8f782b9436601ddf2ffd14dd561b9e9b8c4a9f500a1b6f712e1`  
		Last Modified: Wed, 29 Apr 2026 23:14:54 GMT  
		Size: 126.7 MB (126652695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0613421a39959cfc96d3a1d7085c1c232af1ef646e83e5df429387aa5acc52`  
		Last Modified: Wed, 29 Apr 2026 23:14:52 GMT  
		Size: 16.5 MB (16483797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa433dc4593173915b5b5e9a7a0659302b2f4f5cb04d57a8b29ca2ce360b982c`  
		Last Modified: Wed, 29 Apr 2026 23:14:52 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d39214292ee313df7a4d57cd1d966fd199d1a6dec4d1bdc7e9cd1720d51bc206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99982e2f9e33dc553fb842b3fe24acc05b90db3aabbbc6d45f27b94b79c463a0`

```dockerfile
```

-	Layers:
	-	`sha256:2e0ed808629a47b63ad7080285b03174f40bb4461753d060cc752ab12b7e1ce7`  
		Last Modified: Wed, 29 Apr 2026 23:14:52 GMT  
		Size: 2.4 MB (2381362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f10658b286bc9042f4432786d23dc492dcb67de1bfeda98fe25f6d0a369dfafb`  
		Last Modified: Wed, 29 Apr 2026 23:14:52 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json
