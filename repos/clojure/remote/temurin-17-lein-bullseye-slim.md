## `clojure:temurin-17-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:fe116f7bf6b15f114daba976c2f42eafc4460d17307550d238165d1ffb5fb321
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:45c43c4898b33543935a3407c5aab09b050c84e7f759202ed84598e0e1fe0e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195723880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9693760709eff3da4b304c546a3806e2760ac582f5351236175ccb79bc03b044`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:42:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:42:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:42:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:42:51 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:42:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:42:51 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:43:07 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:43:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:43:07 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:43:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:43:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:43:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:43:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a81b725004aabe02fd6691c9a33b9e675d76298bb7c60df4941e6022264df9b`  
		Last Modified: Tue, 17 Feb 2026 21:43:28 GMT  
		Size: 145.6 MB (145628752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f36abf84cfdcc19e0984af054bf692ed2c6d17055a1dae269b0a7ffc069e231`  
		Last Modified: Tue, 17 Feb 2026 21:43:26 GMT  
		Size: 15.3 MB (15318711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3965edef1119bceb2f5cf2bbfc8836992cdb7d57548dd6ffc87091e81050dae`  
		Last Modified: Tue, 17 Feb 2026 21:43:25 GMT  
		Size: 4.5 MB (4517703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000e111a2284efa43e2400919e206b816ac9154cb4702095f2af54b5dac29d32`  
		Last Modified: Tue, 17 Feb 2026 21:43:25 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:398dce72bfb86b0090264a557a157257814d3e28db7fe550ae143fbe06cf1482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3037564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b1c9309fe78d09577e8e24b482f7c0e3f375e37f7d1dfe2185962e9b9856de`

```dockerfile
```

-	Layers:
	-	`sha256:8816a43f46f35683b48892f183025a4529cd6db3d24c2c877c0b338092caeeba`  
		Last Modified: Tue, 17 Feb 2026 21:43:25 GMT  
		Size: 3.0 MB (3019162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b59267aad25c4b6a957cdd5af14d83a8eefb930de559614d33abab77ccc7e56e`  
		Last Modified: Tue, 17 Feb 2026 21:43:25 GMT  
		Size: 18.4 KB (18402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:716ac6e823999f4e2c155105895af2e8d49f75efe8a61835d401fb815abff0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (193004623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88c05b6320175348146e3717a1c4cee23b6e8cbfe0a4cb1176df8e18c3a6677`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:42:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:42:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:42:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:42:38 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:42:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:42:38 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:42:51 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:42:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:42:51 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:42:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:42:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:42:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:42:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46548bb5228bdd97fcc60fe6752d8d08f53857faadfabc36cfe36408fb069447`  
		Last Modified: Tue, 17 Feb 2026 21:43:13 GMT  
		Size: 144.4 MB (144436250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07196f066ddce00fc745b8062f44aa40938b3908f355637ea58f0fde39922af4`  
		Last Modified: Tue, 17 Feb 2026 21:43:10 GMT  
		Size: 15.3 MB (15305792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ab7705c4080de6d7ec0c7d014724f6cb0d887f1cd88fcf4e568f9f7fb788d3`  
		Last Modified: Tue, 17 Feb 2026 21:43:10 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4e577ea639d8e3b77384c85db0f21792439f58ce3fdfa26f0d6f47ff73f2dc`  
		Last Modified: Tue, 17 Feb 2026 21:43:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6e9af0dfba990c36756510dc86f6cf602736c6cf7527f06d4400a8600a2fcb6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3037295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1b132754b22fb43220be8fff6a45c9051752a63d842cef450790557f9ee1db`

```dockerfile
```

-	Layers:
	-	`sha256:9770bef63c54d9c5ddc670155e114569424290946329cf5bf2c07b42ecdf6134`  
		Last Modified: Tue, 17 Feb 2026 21:43:09 GMT  
		Size: 3.0 MB (3018771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9cd49c8e279d61af6769896a9002725b50d5f65e1af74707d62529454a58a72`  
		Last Modified: Tue, 17 Feb 2026 21:43:09 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json
