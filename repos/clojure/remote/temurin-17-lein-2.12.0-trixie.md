## `clojure:temurin-17-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:4fb240297c006d434636bcb3c6ae1c47070cf439df25133e9a80c44aa6e560ac
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

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:ee352d2ad7c739c02aedb753ad1ac4d186ff01c040a7a2b7bd331de814a27c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217235279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd28e4280f1e6336fd2de429fd6f6d5fe291b2a1ffcbe0a87a4046fdd935ef94`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:58:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:58:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:58:45 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 00:58:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:58:45 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:59:02 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 00:59:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 00:59:02 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 00:59:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 00:59:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 00:59:03 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 00:59:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d878cca90d3a82da8d61e5124f6e229332cebf887ec79acfa479658514652c33`  
		Last Modified: Tue, 30 Dec 2025 00:59:44 GMT  
		Size: 144.8 MB (144847979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01405f54f8a1487c2ffff294516d53fce0b04f4e4cd6f430e6ad0b89bda81560`  
		Last Modified: Tue, 30 Dec 2025 00:59:29 GMT  
		Size: 18.6 MB (18579552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16feaffa35ecd803834a9997a21f7e7e558ad14e482117bdc024880a2de3b154`  
		Last Modified: Tue, 30 Dec 2025 00:59:28 GMT  
		Size: 4.5 MB (4517732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be918a5a2a814f8cbe0b443aa6c476a46601762d387d68a9ed7cbd821b553e11`  
		Last Modified: Tue, 30 Dec 2025 00:59:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4dd7d162a2240968562d91dba1f8608a191c3296ef793a030aa9f20ca842414b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c40f14c54aefaca7dd372302d35e9206c7571b676f4922bd06787dc3d32859f`

```dockerfile
```

-	Layers:
	-	`sha256:db68ad5f2559891724f2dd64348deb9b629b2a19b87b6eba0e0e2b91eb086199`  
		Last Modified: Tue, 30 Dec 2025 04:40:55 GMT  
		Size: 3.8 MB (3813380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12796b5cbc21a371002ea76b45dccde833c6a414f3493b6db3c9c40dcee8b5b2`  
		Last Modified: Tue, 30 Dec 2025 04:40:56 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:31a7a358ac7e46127ad66ceb9dd40be969cabde8224716e0a7420e18aa3a7d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216388885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8e4a5e65d9d8b071e7f0b70fe34d8a98139358cb13735dc2fdf6c92bb1b549`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:59:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:59:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:59:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:59:56 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 00:59:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:59:56 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:00:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:00:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:00:13 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:00:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:00:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:00:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:00:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe7737574531ce47a995a8039d085e29478f2b3e5a7403262cc2034e2d7a7e5`  
		Last Modified: Wed, 31 Dec 2025 02:46:14 GMT  
		Size: 143.7 MB (143679885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e779e515e5a1a304657b38d8603c02d16522f36c3944f7d6fa8198947071f6`  
		Last Modified: Tue, 30 Dec 2025 01:00:53 GMT  
		Size: 18.5 MB (18540642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17305d6ca5fe09fcdfcd622d50bbc9aeed1c1141db490007db95dacf5b1f78f6`  
		Last Modified: Tue, 30 Dec 2025 01:00:51 GMT  
		Size: 4.5 MB (4517735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3ea07aa0cc0190b3c774b82fd93838cabb966fdb926911828976a90f9e4944`  
		Last Modified: Tue, 30 Dec 2025 01:00:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2a09d6651f2b9579736603aa3e2e5bcbf6c981477cfbce8240054a915e8fd8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c06037a76151c9346d2fef8036c97366094ef8391171c23addea766921ef579`

```dockerfile
```

-	Layers:
	-	`sha256:bb7806c925b8e99fb105d7cf4b4742e0171706e02a593355240889716c894915`  
		Last Modified: Tue, 30 Dec 2025 04:41:00 GMT  
		Size: 3.8 MB (3814257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebecb478f110cff225cabae31b027f904638b9603cb9ed9a14ad8d6e9b82654f`  
		Last Modified: Tue, 30 Dec 2025 04:41:01 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:418a2fa141ee814f0f770c9e5bbefc158d529ebda3d3ee3eb7179720cecbc209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220788928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488a6627b96f1c28e84e2e327a5123c52b93f0f3cb08e403b2448162c8ed3355`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 05:19:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:19:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:19:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:19:32 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 05:19:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 05:19:33 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:20:12 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 05:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 05:20:12 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 05:20:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 05:20:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 05:20:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 05:20:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ec9bbe5a1b4841d627859808d06aee03b4bc59e675f245c14fd66a059d46e3`  
		Last Modified: Tue, 30 Dec 2025 05:31:37 GMT  
		Size: 144.5 MB (144525256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a438d889aff3afdc7ede1e63984eb65af0548d3038a957e93cce3c503123551b`  
		Last Modified: Tue, 30 Dec 2025 05:21:05 GMT  
		Size: 18.6 MB (18636999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e063746ae83259bfa4b6398a138bf28fac60cd4167c9bdfadb0572b7d01427e2`  
		Last Modified: Tue, 30 Dec 2025 05:21:05 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c202d15712a75ec77a9d582da0f2702e888cd54121b3bc6da94752c654688f3`  
		Last Modified: Tue, 30 Dec 2025 05:21:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:651c312e8e3b58126e970f176aa833b52ee7ad04c479d7b9ac31bfd4e9bbba50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9517199b3ff143a0ef4bb14e9f15538c1f14501bd28160b4bbd9b6fffcc7a93`

```dockerfile
```

-	Layers:
	-	`sha256:805c4ff8dd2264c8429ee5ed67fdbb6d10fbd8d442580225986e8427ece5ba4e`  
		Last Modified: Tue, 30 Dec 2025 07:36:36 GMT  
		Size: 3.8 MB (3814378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b9d598c83e7ef1782e709e4abf2a0a3de9043d64ed2e0fbe93a7fca6bae01c5`  
		Last Modified: Tue, 30 Dec 2025 07:36:36 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:9b8e5ba2a1d364c028ea751e8121858b6b77c794bde8c5874de3dbb94c52f575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 MB (212710650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37209781956c784bb522718204253dc1c6482911719f178f8dc8ffd792df4120`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 06:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 06:28:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 06:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 06:28:31 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 01 Jan 2026 06:28:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Jan 2026 06:28:31 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 06:30:01 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 01 Jan 2026 06:30:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Jan 2026 06:30:01 GMT
ENV LEIN_ROOT=1
# Thu, 01 Jan 2026 06:30:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 01 Jan 2026 06:30:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 06:30:19 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 06:30:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:aaf3ef12aa0c431a6203a456b21b1e30e26cb56dfc257b8bca2efe1ba7c531de`  
		Last Modified: Tue, 30 Dec 2025 00:51:33 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84137287e78b3f369929e5abc1e6ea708f5c823ab4a3f6ddfafc4335289f5a85`  
		Last Modified: Thu, 01 Jan 2026 07:09:39 GMT  
		Size: 141.9 MB (141889568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfd199ecf7fb41a1a45bce9595e421ffb738a0af48c36ae1a3d7a0e293d117`  
		Last Modified: Thu, 01 Jan 2026 06:34:40 GMT  
		Size: 18.5 MB (18531688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb787233811cdf4051a609cca9a891a979fbd71ba28b5b02ad99c3522d09bf0b`  
		Last Modified: Thu, 01 Jan 2026 06:34:39 GMT  
		Size: 4.5 MB (4517813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d97e68ef895c020aa53dbaa74e81d0c48c585aaac075e10a46baa3113a4087d`  
		Last Modified: Thu, 01 Jan 2026 06:34:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:24b0e7f7bf782ad3acec9f9130ef9eab64621c4aa99d92e22ae00f8e8fe603b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3820332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6214eb446e2f52e41d973533b328082b349b7ab2c186161208989675a708c421`

```dockerfile
```

-	Layers:
	-	`sha256:ff4dc4d741f282dae487599d8fc63ef70b592dd5bac723fa4a24f91db7983028`  
		Last Modified: Thu, 01 Jan 2026 07:35:25 GMT  
		Size: 3.8 MB (3801936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96df7bf256bdb5230a7f091e976d37fa27dbb7b063971b398e2c21744724da83`  
		Last Modified: Thu, 01 Jan 2026 07:35:26 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:c6726ca1eead0b98c02bd5b1d6a8442d4b4441988999dc9f5dfb6d58eaf17649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.3 MB (207343867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8741519d91f05876698b0b973bf8b09f27c338dd8bbbb0a3e373bf3383474d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 05:47:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:47:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:47:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:47:46 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 05:47:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 05:47:46 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:48:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 05:48:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 05:48:00 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 05:48:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 05:48:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 05:48:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 05:48:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:85bc4a4d1f4e52a33d42907057e0ab87c5eb2560b332d94f6e9d7da79c0c76b8`  
		Last Modified: Tue, 30 Dec 2025 03:26:29 GMT  
		Size: 49.3 MB (49345959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08732a2dec916be0d8bc9d2fcfb21b347835cad2dc44d9206ba4d8ebdc9ded05`  
		Last Modified: Tue, 06 Jan 2026 06:49:01 GMT  
		Size: 134.9 MB (134859063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d2587dc7f233c0ed2c9f13c0695eb6ff7170197c7d758467be8f3d8da2a0d1`  
		Last Modified: Tue, 30 Dec 2025 05:48:43 GMT  
		Size: 18.6 MB (18620657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a51bc99c9f31eac8d9b9dade7e6ca1297ec28a433bc018e6b80dde17ec5496b`  
		Last Modified: Tue, 30 Dec 2025 05:48:39 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2886fbdf4ff5af8207275d92c43c9e17cfec9584220cf8656e11f2e371d57bd`  
		Last Modified: Tue, 30 Dec 2025 05:48:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b86a07ce2e56c863dec7f5aaf834e85bda64000efa3a1b8de4060c9f4567fc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3828159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8075f2a762ebbc4b359e19212a38f82098b2bae6ae426e0e0a48c3f361e1bae0`

```dockerfile
```

-	Layers:
	-	`sha256:2b78d770ccd2e59a328f886e78bbb148e47016d62ef6e001bc2616d6e17d8f3b`  
		Last Modified: Tue, 30 Dec 2025 07:36:43 GMT  
		Size: 3.8 MB (3809807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0354c101bbcd831cee4a46af93e6c12a7628c569b34dc14fe3a317fe534d3846`  
		Last Modified: Tue, 30 Dec 2025 07:36:44 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
