## `clojure:temurin-8-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:6dec3200a419b41db141092a72d06889b49b7f914660ba3b2d5892927e86fdaf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cf3361ade9ea92d1d55f41814401adc8ab259e3e2245a503ca446da735338ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104828334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2495a836f178c3c9477b73dfdca77a310790e113b0d9b5f827822ef976db70de`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:49:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:49:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:49:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:49:24 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:49:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:49:24 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:49:38 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:49:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:49:38 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:49:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:49:39 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3d9c03134e5d164dc90bb2623c46151699b3f5be229915e024574d57f80fe6`  
		Last Modified: Mon, 08 Dec 2025 23:50:12 GMT  
		Size: 54.7 MB (54733389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042d384b78de229e5b6d854f7d274db51ffbb63121dd14b9dfd8d8b71da88606`  
		Last Modified: Mon, 08 Dec 2025 23:50:05 GMT  
		Size: 15.3 MB (15318734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b7d47946c1a8e9b1e301aed42dc69ec7edcc8a29e97b2684bfd78e8a49e1f0`  
		Last Modified: Mon, 08 Dec 2025 23:50:08 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e1059579683e17e59c55761ac86c75f38be9f6c03b9cd29a51ce781b48bdd89b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f676ed1096ed563c95b7ae94a002f1751fe4eecc1acffe3b3c110a5f39646240`

```dockerfile
```

-	Layers:
	-	`sha256:6d18268e7e871b6e8590ef461501cc3562488578440f40ea6b9c473cbb4b3f0a`  
		Last Modified: Tue, 09 Dec 2025 04:48:43 GMT  
		Size: 3.1 MB (3139520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d40b2e07572d2a0e88d2e9d741f98956207ef76bb03ce046ad0114dae162ad1c`  
		Last Modified: Tue, 09 Dec 2025 04:48:43 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3971550aa6e39059fa5d868b13e17bd8d985adbacd3a9b34e8023e2c4b946920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102387061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307d2dd500cd0171abcd90d8fcf959ccdc6c0688cdeb5ae47868aaa09e1c31fb`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:57:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:57:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:57:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:57:32 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:57:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:57:32 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:57:45 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:57:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:57:45 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:57:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:57:47 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51290555ee3100897419a250bd2dcc2e8cf6c0ab52b9dd3b88f5be7d5b37e240`  
		Last Modified: Mon, 08 Dec 2025 23:58:14 GMT  
		Size: 53.8 MB (53814992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb236bfe82a174151886cd6476174a54b367c4115ea839e33fef78fc5af19e12`  
		Last Modified: Mon, 08 Dec 2025 23:58:08 GMT  
		Size: 15.3 MB (15305820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491a4b46d2e4a898f1f4eb9444dc145ccae6c541a1b44213785330fbd4ee1de9`  
		Last Modified: Mon, 08 Dec 2025 23:58:08 GMT  
		Size: 4.5 MB (4517735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1854762a093e25325946e7227aa3d554cab9cb49d6a9a0381ff461641a854c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a29867edee0e285df2fd8e956e1615b64c467c66f06c657c8ee9aef1498196`

```dockerfile
```

-	Layers:
	-	`sha256:33f3d4407717a036857e5b0636878cb21e7fa06e51d115dd154e0d5f14bef5ef`  
		Last Modified: Tue, 09 Dec 2025 04:48:49 GMT  
		Size: 3.1 MB (3139827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cee427bcc84880f1301f51090d99c7a4f1aa0a7cf762c0b99e716aa6a1eee034`  
		Last Modified: Tue, 09 Dec 2025 04:48:50 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json
