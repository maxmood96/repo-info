## `clojure:temurin-21-lein-bullseye`

```console
$ docker pull clojure@sha256:e1fdc267f72cdbe7c4cb06d901c7076ac0edc0acfbeba3fe7f97d1d8d10d5ad3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1a2d89dac6ad6302c12db4098dbed8198cad51ad93492a086266aa4ced3dc925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232708491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775be65d23267cd4ec8f4621a1a5575556bdac793ba2d686c8bb05d1f3870ea1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:44:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:44:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:44:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:44:01 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:44:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:44:01 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:44:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:44:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:44:15 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:44:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:44:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:44:17 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:44:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a866ae1a4bdf7578169288bf92a9a3393192dce7b59ef06967f975d200ca54`  
		Last Modified: Sun, 09 Nov 2025 04:14:20 GMT  
		Size: 157.8 MB (157825964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd85ac0a387186a5072c2e8f748f9a9f91889e1fa6322f6b539c347ca51a90a3`  
		Last Modified: Sat, 08 Nov 2025 18:45:15 GMT  
		Size: 16.6 MB (16607651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fdf338ca8e02bd92b31d5b6abaf82b62216528339ea9ed034e224ab4c0f4c1a`  
		Last Modified: Sat, 08 Nov 2025 18:45:14 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3534584fb60bf554a67716c5ae664c86e8b5ce158bac9d61725acfe554c025`  
		Last Modified: Sat, 08 Nov 2025 18:45:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:40bdca589d5abee5a3cd1e2683c6f9ffdda23f3f027a6422990e7da881de9601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768371ae6ec2ce031ece43e2f0eef577334152ac2edb2419eae47d819b8aade6`

```dockerfile
```

-	Layers:
	-	`sha256:e961fe5fa0292ea6cb9a54eeccac19cd3accd42b29a4033258bff73a193e3500`  
		Last Modified: Sat, 08 Nov 2025 22:47:32 GMT  
		Size: 4.5 MB (4479292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52070dcc8a638654c9415b53add9618f5d6827726b1189535dba5660376ecd8c`  
		Last Modified: Sat, 08 Nov 2025 22:47:33 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cb2fda540c2b91740b288cd64054bace9cf54bb48179b4eae160b1a92de3b8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229478781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1551717cca1422a8e53573ee7762bcf38ab09f16c6e9104dbddbf3fa2f377d1e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:43:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:43:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:43:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:43:32 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:43:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:43:32 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:43:46 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:43:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:43:46 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:43:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:43:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:43:47 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:43:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1157830f8bd0081931b19e6afb21452a22166e22161414c8674fcd509dd524`  
		Last Modified: Sat, 08 Nov 2025 18:44:10 GMT  
		Size: 156.1 MB (156107663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23df1e5a4d6f0b0e3d22eee28c6439e6ea7505c2316accb822d142a94bb51765`  
		Last Modified: Sat, 08 Nov 2025 18:44:42 GMT  
		Size: 16.6 MB (16595018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962a96cf562712bcfacafc753d48e19fa55633b1d885e7ab10ec9847f2eaad6b`  
		Last Modified: Sat, 08 Nov 2025 18:44:41 GMT  
		Size: 4.5 MB (4517703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79116765dc1e050d024d648c37353576db54d6876c14ab9adb55181a0eb8448`  
		Last Modified: Sat, 08 Nov 2025 18:44:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7f713f13ebe91522abda799e8c662dba217b77ae5b62b769447b97f84744742b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4496754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b91ecc452c179e4baae7d26425d447060b42d4af11c81dc4423c53563f071fb`

```dockerfile
```

-	Layers:
	-	`sha256:314c0c857234365a3beb34bce883f9623d7cd882c794126a3f67757578dd5243`  
		Last Modified: Sat, 08 Nov 2025 22:47:37 GMT  
		Size: 4.5 MB (4478266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea988c8a6953c5afb1670b7156f9db562e64fc50b68934fcb27ac2cbbdeb54ae`  
		Last Modified: Sat, 08 Nov 2025 22:47:38 GMT  
		Size: 18.5 KB (18488 bytes)  
		MIME: application/vnd.in-toto+json
