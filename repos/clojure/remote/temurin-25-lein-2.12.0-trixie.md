## `clojure:temurin-25-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:6d80bfa9b6093c854ce39d9a2e58c2ce67b36d7c28fece27b5090b97f85e8ab4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:be3318b84c7163b602b01ed720eeadf0affb4a39fa474ff079b70d5eb191067a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.2 MB (168161543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d64d51c38d7eec3ca4b1c54cf862aec04021c7bac3f9d30de2c489e6e7358d0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:06:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:06:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:06:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:06:25 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:06:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:06:25 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:06:43 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:06:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:06:43 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:06:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:06:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:06:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:06:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376181d63be168965b88eb70c505dd3939be81b1ab933211976377db7b7937bb`  
		Last Modified: Wed, 15 Apr 2026 22:07:03 GMT  
		Size: 92.3 MB (92256337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77c5e5529509a354bccb022ef43357370f398f8217d16420b96d1e07002b35b`  
		Last Modified: Wed, 15 Apr 2026 22:07:00 GMT  
		Size: 22.1 MB (22089193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0915720f9d4f32414b6adc459e4cd7634d45741afb87833cc087dcb9eae3e5`  
		Last Modified: Wed, 15 Apr 2026 22:07:00 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000af5470e43c9f95a2990cce79f9c321f794e55b9652e2ca10ddeecee8b0d77`  
		Last Modified: Wed, 15 Apr 2026 22:06:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:013a6afd7a2f8f9e3374759ff919fe73a1754d3b416de967ff13d51628caecb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3802538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f6bb9195628469141f3a60403a6b48a990ea230e111f466a7ed9cebfe6e903`

```dockerfile
```

-	Layers:
	-	`sha256:031b9d819648bb6acf2125fdcd0099507bc36acae4ff624342d909c5e47ce914`  
		Last Modified: Wed, 15 Apr 2026 22:07:00 GMT  
		Size: 3.8 MB (3783559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ddbafb84bab121236e6266c8a634d607edaed45c10a0c6caadbd03a5f63e26f`  
		Last Modified: Wed, 15 Apr 2026 22:06:59 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e994aa0ae7c1c7e86c3fce0c6d69f4c2c8f4035cfdb85aabd555e71d6b7414c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167895922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723f92d52ae97098e582a9cc7b48aac5c645ccbe5baced081e817e2f58372065`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:18:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:18:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:18:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:18:02 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:18:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:18:02 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:18:19 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:18:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:18:19 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:18:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:18:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:18:21 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:18:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da5f66862c80aa3016287b05d9450ada5d3ee50d306b9c350e852a1647d0ca1`  
		Last Modified: Wed, 15 Apr 2026 22:18:42 GMT  
		Size: 91.3 MB (91288271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778b65668a6a40ca25a074c34d6b0f893f7e17762ea17e44b8d8bbbf8a6a4864`  
		Last Modified: Wed, 15 Apr 2026 22:18:40 GMT  
		Size: 22.4 MB (22424250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b647db5fb366dba1329a6c11459bec2c58861a6ee92d002cdd2d30c1bc347070`  
		Last Modified: Wed, 15 Apr 2026 22:18:39 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7653a9090d1e3bf5db7e00ad15a92b7573d187c8feeedf3211838fef8bdca75c`  
		Last Modified: Wed, 15 Apr 2026 22:18:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b08af58d2ef69e7186258504894ca916ccbe7b0ad7d94be00c7dc752275c22cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aed117b7f41001585b1aade97b02c16ce826acdbc6da2d1cc712661685600cf`

```dockerfile
```

-	Layers:
	-	`sha256:ed8eeb2903189a4ea92fd37ce0c0f74e7443d9a7dacb6c51c3913ebd8801131b`  
		Last Modified: Wed, 15 Apr 2026 22:18:39 GMT  
		Size: 3.8 MB (3784457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea2a195adc8b2d254873d8515a4259e878e00d32b51d7792e5941a32bba63d8f`  
		Last Modified: Wed, 15 Apr 2026 22:18:39 GMT  
		Size: 19.1 KB (19124 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:77336e75da62daccbb2f72a0bfeb1d2179cd9d25642845318c8ced898fb4d589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167910708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b57a62eab1e09ea30ce026c8248b49b70f1e63d48e5c91af66309ebe600e1c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:55:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:55:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:55:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:55:46 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:55:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:55:46 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:56:27 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:56:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:56:27 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:56:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:56:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:56:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:56:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3326c6b4216bde98266a981f1f1fb92f86315b90e8c006d1aadb7310dd7d4f`  
		Last Modified: Tue, 07 Apr 2026 14:57:06 GMT  
		Size: 91.6 MB (91633006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eaf73ccf363dc5d7e17b6f8ea485aeadda89dd8be7835e22357db372361009`  
		Last Modified: Tue, 07 Apr 2026 14:57:04 GMT  
		Size: 18.6 MB (18640848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dfd6a4d46d38cbf23175c56eab1146bb55fec1cf47e53d5e6e7fca111383b4`  
		Last Modified: Tue, 07 Apr 2026 14:57:04 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e197b634a019470f3b59a99faf0cd40862cc41660290141059b4601b776400`  
		Last Modified: Tue, 07 Apr 2026 14:57:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ee93fbd79dcb4a62f7e51b35bd10428d0bb2ccedd10a5b754e3b32a3df9d1a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a56f751a59196cc5a5f424fea5202fea94e0c78c40e3029ad5293abb5396d73`

```dockerfile
```

-	Layers:
	-	`sha256:6f10cf71430827e85a6cc3c2493ed0ca0684e3dfa2d04904a6eb97325d779dc4`  
		Last Modified: Tue, 07 Apr 2026 14:57:03 GMT  
		Size: 3.8 MB (3767883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d000359060b419b618749956428de3011e907e2f0eb79f2264ad3d86ce43d02e`  
		Last Modified: Tue, 07 Apr 2026 14:57:03 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:65e004b7b404793fef4fefd47b1f1be89638bb2e7d19c5f4ceac411e8dc83f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164780419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95425362c462b6d3fdeb0b1d4307602ff9ba155b3bd6bf6ee0dcb4c1e858305`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 22:33:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 22:33:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 22:33:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 22:33:17 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 11 Apr 2026 22:33:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 11 Apr 2026 22:33:17 GMT
WORKDIR /tmp
# Sat, 11 Apr 2026 22:34:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 11 Apr 2026 22:34:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 11 Apr 2026 22:34:52 GMT
ENV LEIN_ROOT=1
# Sat, 11 Apr 2026 22:35:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 11 Apr 2026 22:35:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 11 Apr 2026 22:35:09 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 11 Apr 2026 22:35:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7224fd307fae2068f62ccce22d637a96c5204dea7af1d7b9116b5323460f86`  
		Last Modified: Sat, 11 Apr 2026 22:38:56 GMT  
		Size: 90.8 MB (90773425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3cee8b7858b6e47a6142136700e3a8c00971ca2899b3e905d79cf95926ef27`  
		Last Modified: Sat, 11 Apr 2026 22:38:46 GMT  
		Size: 21.7 MB (21696155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca377022b8af3a58916923f4fdd929aa705a15a0725212b93712ff7be44a253`  
		Last Modified: Sat, 11 Apr 2026 22:38:41 GMT  
		Size: 4.5 MB (4517783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4899f012572b5a96438d13f91ee2fc973c7f36c565fcfbf1e72cf05a02ba0b45`  
		Last Modified: Sat, 11 Apr 2026 22:38:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ade6fcb3d67049d0a3c5bc90050def8e7352c218c423833cbb6a3a966784e5da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ccf68ed424dee997b234c9aab2bb8faaf8fe13b2716b9da1811e5f27834da6a`

```dockerfile
```

-	Layers:
	-	`sha256:7b92c7045a34f98036522ef013f25497e4e9478ca2e367c87366dd82ec91d533`  
		Last Modified: Sat, 11 Apr 2026 22:38:41 GMT  
		Size: 3.8 MB (3756059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce5c4511cc11635b411c9071f1f590820b3d03c011f5ab9c3d3d07cb09d9ff65`  
		Last Modified: Sat, 11 Apr 2026 22:38:39 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:3abee8c35d4712f34de9d4486f58b96a3721d5c61e9b6e2723763c21fef82cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.9 MB (163899313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba5f9d6900852692b383a204a6d720216a6b4bbe16d3e248183696a2c7a08e6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:44:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:44:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:44:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:44:04 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 00:44:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 00:44:04 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:44:19 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:44:19 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:44:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:44:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:44:21 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:44:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af85e16ff2a5e4ef4e7bca442eaf789074eba5dae2548a5309ae1cc069f92daf`  
		Last Modified: Thu, 16 Apr 2026 00:44:45 GMT  
		Size: 88.2 MB (88233823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8a10788c992ad2a15c6b837b8f02cf3b9493ad6ce66fe94ca1a10846bb9ce6`  
		Last Modified: Thu, 16 Apr 2026 00:44:44 GMT  
		Size: 21.8 MB (21782216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfedf9bfa03913f7768467ecd7a5f175b546a4c287711f6f60987543d110e42`  
		Last Modified: Thu, 16 Apr 2026 00:44:44 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54248441a45a7a3609e83ffe632d3a0798dbb64f87eddb461ae55f6261a4860`  
		Last Modified: Thu, 16 Apr 2026 00:44:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a26d265139c9975cf38a24bf81829c00f93da71d7693703ac2bbbc68e2672b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f818415d6f718bc3fcaa72bfd97d055bca4bc73505d1f246a1b11f41c1ba8e8d`

```dockerfile
```

-	Layers:
	-	`sha256:0f3f902eba7f21f9dc86a7ac6dba3fc141a87b321557c08ee787f1b23dd3f142`  
		Last Modified: Thu, 16 Apr 2026 00:44:44 GMT  
		Size: 3.8 MB (3764548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:353bfa886d97203a41b66ead1912fee372fe94689399f5e2e431bf5ebaef4ee7`  
		Last Modified: Thu, 16 Apr 2026 00:44:44 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json
