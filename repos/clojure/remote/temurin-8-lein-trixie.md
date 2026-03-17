## `clojure:temurin-8-lein-trixie`

```console
$ docker pull clojure@sha256:e8de1f895e02764141df02f28df586ec7af02ed9930311dd01803a1ec0306a10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:56d8a5fd04093303a072ff0ecdec0ec48b90415ebc597b45645b08d45890c902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127570532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae1a56809a87c00faaabf26ffc0e89495b0f575309371f227c661f4e1f2934f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 02:56:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:56:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:56:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:56:01 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 02:56:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 02:56:01 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:56:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 02:56:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 02:56:18 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 02:56:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 02:56:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979dc3905b70bcf79ffc2331c696fb2bad081a65dd9dd83a62f320bbbf89c0f2`  
		Last Modified: Tue, 17 Mar 2026 02:56:34 GMT  
		Size: 55.2 MB (55170194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aedb16c3f31f9390ae86e730bcb8808a7ac3bdd5ee366c92686359696734220`  
		Last Modified: Tue, 17 Mar 2026 02:56:33 GMT  
		Size: 18.6 MB (18585054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82895e9ba880e83d1eed3ddcde2777c8228eac6f9097ea1dd34cedc89499499e`  
		Last Modified: Tue, 17 Mar 2026 02:56:33 GMT  
		Size: 4.5 MB (4517722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1430b8b22b286c74b406eac46598618d8b2378835822fb40fc689f9ee8a2a38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5702f65ade57811954ecb41653d4c63ce8a60714dbdb15e825c04fceb3d33b47`

```dockerfile
```

-	Layers:
	-	`sha256:b7ad424fe7258c53bb165daf457e1dab8d8200aa27a6a0c49c4525de8c5df752`  
		Last Modified: Tue, 17 Mar 2026 02:56:33 GMT  
		Size: 3.9 MB (3936516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e05a5e26749b24d953fabd82235b8ab6210bf31fa880961a9e4f220dd272abfb`  
		Last Modified: Tue, 17 Mar 2026 02:56:33 GMT  
		Size: 16.4 KB (16352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1ad97811fac11e85732cf2055d81644678199fe114c801a48ca8e29a760f9531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (126979035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603a0a047ec365a307b20f9ff28a2e260941c4156dca561e963de0829f48dbb3`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:00:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:00:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:00:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:00:22 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:00:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:00:22 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:00:40 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:00:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:00:40 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:00:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:00:42 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69afafbe568edb8ac7f5b1a3599c31e4b121a2780b0c73b76db977db8f7d3fc`  
		Last Modified: Tue, 17 Mar 2026 03:00:57 GMT  
		Size: 54.3 MB (54251611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fae4ef6f7131cdc3d8c5c5a2d0fc658bbc3767907ec2cfd356edb9a1a873bcc`  
		Last Modified: Tue, 17 Mar 2026 03:00:56 GMT  
		Size: 18.5 MB (18544735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a701a19ad7e3678633bfdef04892d1e877f715af4883ac42c900d88cccbb4483`  
		Last Modified: Tue, 17 Mar 2026 03:00:55 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:978076b859d0213071796fbc2650d47a590d2250c9478c5b63c1c3a442325fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79caff729f0c5086aacbb3822358747427faabea79a3ce7e39c5545b3602f6d`

```dockerfile
```

-	Layers:
	-	`sha256:639e983fa76ea3338494ead47570de9980d34d7a5af8cad2fb49af7c9dc77e32`  
		Last Modified: Tue, 17 Mar 2026 03:00:55 GMT  
		Size: 3.9 MB (3938093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2eade4b6d9203951e9541cab078eebecb4b894d91dfb96c432ba88ca177abf5`  
		Last Modified: Tue, 17 Mar 2026 03:00:55 GMT  
		Size: 16.5 KB (16473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:b828b5a4b62059c922dd7d66c1cdca1e4cae8810012c0f142c9d0c3ff4559b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128917959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a82d0c7d0b7bb58c12524dec2f291eb604f11a0cb68ad7562b4c847d41fb01`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 01:43:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:43:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:43:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:43:24 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 01:43:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 01:43:24 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:44:09 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 01:44:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 01:44:09 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 01:44:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 01:44:16 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdef948f7a075c7ba090915db8bdf444c4fd6f03737e0d659d8563f21b69755`  
		Last Modified: Wed, 25 Feb 2026 01:44:45 GMT  
		Size: 52.7 MB (52650395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27675fddd81bcc6928cb0f24d8c463677bb122c90ae6bb5390128588c3953283`  
		Last Modified: Wed, 25 Feb 2026 01:44:44 GMT  
		Size: 18.6 MB (18637516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3210e59924e879f181f590f4fb5d7324b881cb48837b9d54b7a95ef9a24d32fd`  
		Last Modified: Wed, 25 Feb 2026 01:44:44 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c485aa5b6f873a6c1264e1083de023e639a1aca942ffb619a94ed0db1d63f599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921e74b0d3eb703fbbe91b70159e7557d3b3939e9235598426d9862da60440ee`

```dockerfile
```

-	Layers:
	-	`sha256:ad6f42f56dd5d22f7dfc9525e2ede96a20e778a2abb67b9bf12dc012ecace298`  
		Last Modified: Wed, 25 Feb 2026 01:44:44 GMT  
		Size: 3.9 MB (3938075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fad4bda816a6f93edb0652a33fc51c5f60c7e87773d43f884cd86f1139da3936`  
		Last Modified: Wed, 25 Feb 2026 01:44:43 GMT  
		Size: 16.4 KB (16396 bytes)  
		MIME: application/vnd.in-toto+json
