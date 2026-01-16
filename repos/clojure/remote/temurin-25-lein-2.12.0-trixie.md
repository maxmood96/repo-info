## `clojure:temurin-25-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:2217648c3c015b1ee667bafd84d0aff63f3423f21282236adc18a8fb96ce62d0
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
$ docker pull clojure@sha256:d04f2b3791361e5df08a25085af286352f305a84dba8c8af5b2aba9998a3375e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164428715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b891b0ac91d17e2aeb282bf5ff06929b20bba3fe2f96457982dd2965f34542`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:38:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:38:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:38:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:38:52 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:38:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:38:52 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:39:10 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:39:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:39:10 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:39:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:39:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:39:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:39:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631898fd0375fed42769ec5bc5cde060d7c2f9905ed01f1e10f0e4ffd34c4898`  
		Last Modified: Tue, 13 Jan 2026 03:39:46 GMT  
		Size: 92.0 MB (92045300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9ca40805e324f41a400f71b80356bca3f466c0938244f8ce38cece862870e6`  
		Last Modified: Tue, 13 Jan 2026 03:39:41 GMT  
		Size: 18.6 MB (18579667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be51fe825b5db6c91d95b64717ba1e2234a9e6971ac9cdeef024049e97532f0`  
		Last Modified: Tue, 13 Jan 2026 03:39:38 GMT  
		Size: 4.5 MB (4517699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d1bf5b5a26f7f82778d223d9c39e5fbf2af0dd31123686f880364c5723cb4`  
		Last Modified: Tue, 13 Jan 2026 03:39:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0e10c766c8d01c13104af99689b1676700304ea180ca757735b002b53698617a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9462b3acdb7dab60f1729a7814f5cbfee629bbdcb8ee14fda1282e1a6abd6293`

```dockerfile
```

-	Layers:
	-	`sha256:2c77252f9e4ca12819f9871da5be3db19fb215bf0f896c5f533df24404f0f35b`  
		Last Modified: Tue, 13 Jan 2026 07:35:53 GMT  
		Size: 3.8 MB (3765535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ebc52f91ce5aee9e80c2c54c8567420ccdb8a2cca33ba6ab069dd860ed8a32f`  
		Last Modified: Tue, 13 Jan 2026 07:35:54 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:439b6836bcee82583d35b3d85a8abcc24a93958e9931d4ce71c5620889afeb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163759527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f038a91e5caf8854481acd0b88777e76895526cbd907a7e671e25d77d5cf7640`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:42:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:42:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:42:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:42:13 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:42:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:42:13 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:42:29 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:42:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:42:29 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:42:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:42:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:42:31 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:42:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089f6c093e77fccb44bb012e85e6d310164a8a05364edb4d067070f7aab13fa0`  
		Last Modified: Tue, 13 Jan 2026 03:43:04 GMT  
		Size: 91.1 MB (91052481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb6c9af8e60826e55366f00efc8d0c56008d27488e5d9b2deca0ddb8b7908fe`  
		Last Modified: Tue, 13 Jan 2026 03:42:57 GMT  
		Size: 18.5 MB (18540780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8d6a99ecb78cc11cbebfad52c87e3861d59e432292eabd0e67f81e30609f6c`  
		Last Modified: Tue, 13 Jan 2026 03:42:56 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f585400d2b2de269621b635e208866406aefa3a204b257b55b480b7fcbfd5bd2`  
		Last Modified: Tue, 13 Jan 2026 03:42:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ffef0d607489a2b2e53f0ec758f6b9b8b0682fd81cb859a0348f801ada190fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c85de94ef83b87c737a66490141b72b5a9b7a0f3440b8982ff3a6f45f3c371f`

```dockerfile
```

-	Layers:
	-	`sha256:7896b4353068cd6fdf0aa8ae283d53cf50423492cdfb1b2ef677e8685f11f353`  
		Last Modified: Tue, 13 Jan 2026 07:35:58 GMT  
		Size: 3.8 MB (3766433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:947882e00acb7d0077819cb4afe76b8b407f159c15ffef6b71966fdb0efa0360`  
		Last Modified: Tue, 13 Jan 2026 07:35:59 GMT  
		Size: 19.1 KB (19124 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:c405b9af6f7d6593e22613ae74cf29f9223d270420aa160595f5b25be5785921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167873057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041cdc0c0aefe7b545bd44e449964d985aaad3a509569ba94f3bb935bd876ab2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 12:26:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 12:26:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 12:26:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 12:26:49 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 12:26:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 12:26:50 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 12:27:46 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 12:27:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 12:27:46 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 12:27:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 12:27:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 12:27:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 12:27:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:58 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae7604a3d1e42b32c72cfbaece977af9dcd293cc1c09fffd678e719e4da5230`  
		Last Modified: Tue, 13 Jan 2026 12:28:49 GMT  
		Size: 91.6 MB (91610745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70dd8e27590ad4e1022a346d25ae031be2a54e5b0e444a5764695149cab565e6`  
		Last Modified: Tue, 13 Jan 2026 12:28:40 GMT  
		Size: 18.6 MB (18637212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab813614bb70dba3dff4b21bee05421d1a6bc5ca5dad07f523bd8fe18ee4d1e7`  
		Last Modified: Tue, 13 Jan 2026 12:28:38 GMT  
		Size: 4.5 MB (4517709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febca6c384866096a2a45850f95d5265ee23232edfd4cda761d312dcf8ad31e6`  
		Last Modified: Tue, 13 Jan 2026 12:28:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1bfa76640b85f7f63a36925b39788c5d5d5c2eebe687712909b295b8daac89ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86af892725c8c6259fde2a48380fcf062fad196dc0e67d1bbbdf2e9cffde7dde`

```dockerfile
```

-	Layers:
	-	`sha256:7a630a88682b4f4f3aaf64703f54c65dd8165ac3c161f99bbec7b8680cfb764a`  
		Last Modified: Tue, 13 Jan 2026 13:34:32 GMT  
		Size: 3.8 MB (3767845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74bfeed71ab3f929204a3e8d49c5419339532b86a496b133e1cfb2302f3b9b73`  
		Last Modified: Tue, 13 Jan 2026 13:34:33 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:7d3beb28017b32f2bec89adaa52edd88ff7487285f0e4d7193a3835ac7018027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161573955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d7896431c5a438871f78be2ac2b109b669073da0117f7a422c9f7cde6f9123`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 07:24:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 07:24:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 07:24:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 07:24:27 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 01 Jan 2026 07:24:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Jan 2026 07:24:27 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 07:25:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 01 Jan 2026 07:25:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Jan 2026 07:25:59 GMT
ENV LEIN_ROOT=1
# Thu, 01 Jan 2026 07:26:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 01 Jan 2026 07:26:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 07:26:15 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 07:26:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:aaf3ef12aa0c431a6203a456b21b1e30e26cb56dfc257b8bca2efe1ba7c531de`  
		Last Modified: Tue, 30 Dec 2025 00:51:33 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e72db194620f93f57207f61aa544e094761861bb8fbdbf65160d1e1594a9c91`  
		Last Modified: Thu, 01 Jan 2026 07:30:30 GMT  
		Size: 90.8 MB (90752893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578a725406d0222a0bf716fbc6c412a59b379add08b579b0f52661319f9d7926`  
		Last Modified: Thu, 01 Jan 2026 07:30:22 GMT  
		Size: 18.5 MB (18531712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f2f88cea93c0c8393673eb3323f2fbd3e6018f4174e602a2db3723f6c72c93`  
		Last Modified: Thu, 01 Jan 2026 07:30:22 GMT  
		Size: 4.5 MB (4517767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3accc15121411f29d0f0ea48151052f15acb2d0e86d47d3cedd606e0ea652d4d`  
		Last Modified: Thu, 01 Jan 2026 07:30:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c545cdc29e233638050236122a869cdbfeb250c8a42010cadb4f8ec4f3c3148f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92526daa2701e44923f18530ea5502ecc1e44190dbf79dccf90c5cecb416d1e9`

```dockerfile
```

-	Layers:
	-	`sha256:b41e981f2201942c5e1463c6b2a34018151d49fc0697456cceaeeedd5e0f2d57`  
		Last Modified: Thu, 01 Jan 2026 10:35:04 GMT  
		Size: 3.8 MB (3755160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2508d55783bc7450628b328666c52bbe4595f38a44e43311673860bcf0d1d3e9`  
		Last Modified: Thu, 01 Jan 2026 10:35:04 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:efd218827aeef2b3ec6aadb9ba583d0810ab3b186acbf2b9aeca5827770c327f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160698285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58dedaeb79ded95d09b2b9590b9dfb056a83e2d3bc0c88e05e41d0b5095e6fe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:22:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:22:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:22:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:22:58 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:22:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:22:58 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:23:10 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 15 Jan 2026 23:23:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Jan 2026 23:23:10 GMT
ENV LEIN_ROOT=1
# Thu, 15 Jan 2026 23:23:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 15 Jan 2026 23:23:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:23:12 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:23:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9da15375349ed468c4d395178dea5e2fe711fa01064413f4605f3f47af67086`  
		Last Modified: Thu, 15 Jan 2026 23:23:51 GMT  
		Size: 88.2 MB (88210648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87663d8736bc88f37169881f97d4b06cd465ea23476fe5932b4634922906a22f`  
		Last Modified: Thu, 15 Jan 2026 23:23:46 GMT  
		Size: 18.6 MB (18620747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec099c7074d38c6f711e40ce47ff97f5239cdf18cdabb98f37469a9e9cfb87d`  
		Last Modified: Thu, 15 Jan 2026 23:23:44 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced5d24eccc92fa0722be1bf7e484856266bc403e431299d2a9e508867967b61`  
		Last Modified: Thu, 15 Jan 2026 23:23:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:36fa61fa02489ce448197773dafc131166c6794b413754891463009d276b184d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7360462a5ffb707c4329d016451b38ae038de70c45042456b6135ef03d89d515`

```dockerfile
```

-	Layers:
	-	`sha256:950e286bb921887041628127fe32ae86c7bc22d7f1a25ba606b3b214a7ac684d`  
		Last Modified: Fri, 16 Jan 2026 01:36:19 GMT  
		Size: 3.8 MB (3764510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5de2507488f3435093e50e6c061058e82fc79d9151ca3bdd6dff86029a4c6230`  
		Last Modified: Fri, 16 Jan 2026 01:36:20 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json
