## `clojure:temurin-21-lein-trixie`

```console
$ docker pull clojure@sha256:c257d346dde230efd7638b89c6baeb16a28882454fcb58fdad7976889158cc26
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

### `clojure:temurin-21-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:146537a49285d42a2411286728cd93a70ddc1e51683f49121dde25d70f5ab0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.9 MB (277928673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c78a671dff717d9cbab169c8d0ec4b937b1d3c76e12e09c2ee711a1c85eef19`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c719da888e213c555e1c16ccbb9aa18f72c873d16c3f5c706154a7a254bac3f`  
		Last Modified: Wed, 02 Jul 2025 16:09:09 GMT  
		Size: 157.6 MB (157634517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a505b680d321798414bee7f0a73301b159955dc012a33c50d3e19906655c5e`  
		Last Modified: Wed, 02 Jul 2025 04:17:21 GMT  
		Size: 66.5 MB (66515701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659475a7a240cb95e741a248cb00474d8f8cd2b97b5faf9a311b23c016b837d2`  
		Last Modified: Wed, 02 Jul 2025 04:17:12 GMT  
		Size: 4.5 MB (4514150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e455d35f67a6ed453e5fb12d6054639f0d5a97ef963b7533e8378fe9eae55690`  
		Last Modified: Wed, 02 Jul 2025 04:17:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a1238b32561f4d8c7aef0d187c31a0459cce00093e9b8666d601337b524b508e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6470679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b1037cdfbd7b84f1791337bf386b36ebb28367b2646e733258fac1d2831109`

```dockerfile
```

-	Layers:
	-	`sha256:2a8811319b2edee2bcc04252039048421853b2606a388e43281f4d9941cc22d1`  
		Last Modified: Wed, 02 Jul 2025 06:34:46 GMT  
		Size: 6.5 MB (6451643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb47b46fd1b85c59019ca0bf31eee5f4757f2ac8b5f783207569b24f9756291`  
		Last Modified: Wed, 02 Jul 2025 06:34:47 GMT  
		Size: 19.0 KB (19036 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:882979465383b05ef1f1a4dca39abebb4c678fd49b37bb2fd5596aa8a041876a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.5 MB (276535232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa79dd237bcd76643275023006b455d0cbf9889053670e12f0dbb2f0e96b022d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2581a046e315a4b3013d50a17da46bcffbba144014a55d733fa55c3bafc6b7ab`  
		Last Modified: Tue, 01 Jul 2025 01:18:05 GMT  
		Size: 49.6 MB (49630154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c102048348f860ce1e85405e32ca456a52a441757b642ead74c7b79f92ea6f5c`  
		Last Modified: Wed, 02 Jul 2025 15:51:56 GMT  
		Size: 155.9 MB (155928830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8329e8306d8cc3ea493ecd7979fdd018686ba4eeeabd386920bdd5ed226ccc4`  
		Last Modified: Wed, 02 Jul 2025 12:47:09 GMT  
		Size: 66.5 MB (66461619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9597e14139137cf3d0b795af8369de66bc0619505d54b426be182774162c117`  
		Last Modified: Wed, 02 Jul 2025 12:47:03 GMT  
		Size: 4.5 MB (4514201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a123c9a632e1686ecbb7bc81ee58a9e0c840940a1db396a73aeeb31a88ac7c`  
		Last Modified: Wed, 02 Jul 2025 12:47:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:136f8cf7da9fc2f84296724cba5bbd0e8bc14722bdf8ba265af6e964f26bacc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6477812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d863e064cc8a7fa0271b0cdb24e0ade075854f010f9e7bb5fc0c23e6eef5a35`

```dockerfile
```

-	Layers:
	-	`sha256:bd1cea535e0f1f81dfaca6097301476fbd7634d663f632d6b3f5c2040faecdb4`  
		Last Modified: Wed, 02 Jul 2025 15:34:48 GMT  
		Size: 6.5 MB (6458630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8282b8f80b9a461bf56e26c311d3ea38cb9bac48e543a9df079f2b09106d885`  
		Last Modified: Wed, 02 Jul 2025 15:34:49 GMT  
		Size: 19.2 KB (19182 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:970485c3d09d8a209725bce2b73f84e3f560f09330e14e2d4e15f86eae20a386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286937767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61610dbf33f7a730f762e4110660c81ff1398aa640f9969b21a2eb0eb42e10bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ba674ba1404593b1a6a59d0974b4549e6f5655bdfdb982e660021a4e42c0fe`  
		Last Modified: Wed, 02 Jul 2025 10:49:42 GMT  
		Size: 157.8 MB (157804888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df75390f69990ee0ea10888712dc5f92c3a8f6f37cc74d51b7e6c9a37252e67`  
		Last Modified: Wed, 02 Jul 2025 10:50:03 GMT  
		Size: 71.5 MB (71521011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd46632258b8a14054573ba5c267d898269ddd6212a1d01424c5737bafc8495`  
		Last Modified: Wed, 02 Jul 2025 10:49:58 GMT  
		Size: 4.5 MB (4514202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1d8cebd6b8f0900717615bb4d02e9d9cde24a8b60c431ffa968d4ae8660d9d`  
		Last Modified: Wed, 02 Jul 2025 10:49:57 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:eba9cdbff16a86acc6cd5a85387364d0c34fce6c458231e935122fdf7faee917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6474856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6cd792bbba66af4128816d20320a2e2b60c0ab76cb5a9d2613c2e37efc2443`

```dockerfile
```

-	Layers:
	-	`sha256:29ad5e6984883cf51778959b967a78c33734a61a6ce49279561cf6de4ccb6099`  
		Last Modified: Wed, 02 Jul 2025 12:34:49 GMT  
		Size: 6.5 MB (6455763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d75219cc2c287c7438066519d55a0ba96b36a884cc798b5b19653f60959eabd`  
		Last Modified: Wed, 02 Jul 2025 12:34:50 GMT  
		Size: 19.1 KB (19093 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:c30524ebbe5d728027a053073878beb68fb663a40ad23630170e0a91272b64f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.3 MB (271347995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d307b3a649acd1a52571c5e6c6aadeb8cd12aa2a2a40e9cacd153077599d09`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a19cda6d0aca0ae93b23898ddaa4518ab5077c7011f945c7a7e4a2cacb08ca5f`  
		Last Modified: Tue, 01 Jul 2025 01:23:18 GMT  
		Size: 47.8 MB (47750158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e076e085e4924513404df674a4b5cdd11b691d0a99549b6d4e3c46e86877f1`  
		Last Modified: Tue, 01 Jul 2025 03:02:40 GMT  
		Size: 153.4 MB (153449649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64236ec3b9693317967042b3c1ede01da19a17437e6494410b123df37020b359`  
		Last Modified: Tue, 01 Jul 2025 03:03:06 GMT  
		Size: 65.6 MB (65633518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1115b73ce5915fa77da467b56694929a37e1589dab3b91dfef0344b2516507`  
		Last Modified: Tue, 01 Jul 2025 03:02:54 GMT  
		Size: 4.5 MB (4514241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83c5ff0e0b54a76fa01935570b3364c7450fb82ed978f3974123b011b4099bc`  
		Last Modified: Wed, 02 Jul 2025 09:04:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:11c654c298877cf2cc48b7d56b4ae01956aa0a0cd855bd8793aa116a770371c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6458570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e70e65cf967a11c3ae115a5b3ab09c9a2a5eff8f10bdcb6e793b91a187feec5`

```dockerfile
```

-	Layers:
	-	`sha256:386fa7033bd9e21b56bedd844821243e85543a5630215f6e8359ea70ff3b09bd`  
		Last Modified: Wed, 02 Jul 2025 09:34:52 GMT  
		Size: 6.4 MB (6439477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80d2fdecc1cbdacd279b75fbd22f7ee4eca36a454ee2ebfb3e535fee207553cf`  
		Last Modified: Wed, 02 Jul 2025 09:34:53 GMT  
		Size: 19.1 KB (19093 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:87fa335106bec052cb6ad16af177d018f01de6d1230082502cf667f5bf1c085b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.3 MB (268262777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76205c0f7df2700cd19867ef9986af5a05f6e737816df57935255bbfd79a81cb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:48de1d8f52c0a2a00375babc11bf69628b8225862d3b6ebbb2205e4ae2f3e96a`  
		Last Modified: Tue, 01 Jul 2025 01:19:00 GMT  
		Size: 49.3 MB (49343660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bc60726a2f3745d54c0dd09294d4451be8392d24b90a4488a0071b6ed0b78a`  
		Last Modified: Wed, 02 Jul 2025 06:48:19 GMT  
		Size: 146.9 MB (146910935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b025732db3b233b027c4a5c61b3ac1d60539f2b68d32a74fd75b1e09a81e347`  
		Last Modified: Wed, 02 Jul 2025 06:48:35 GMT  
		Size: 67.5 MB (67493558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0e7db6af8c1e7e3ff8394c8acecea6977289d6b67b4eba076771d59222a694`  
		Last Modified: Wed, 02 Jul 2025 06:48:25 GMT  
		Size: 4.5 MB (4514197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a237220b21ab2973899a73904011de8f7d3fc5630a5e3a3ec53ff651a682f3d4`  
		Last Modified: Wed, 02 Jul 2025 06:48:24 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8108f8eaa766500d42f2abbb9c232c780dcf39de3b14b4c8daab74bae1c7c102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6466657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898ca7d803d2149b37cda80223bc811d8bf44009b1a9726f385b4ee4f8ed4f2d`

```dockerfile
```

-	Layers:
	-	`sha256:789902fedde969ac1dae2c73d9ea6d83485f57c9ae0f54b7fde46e9a97e4e588`  
		Last Modified: Wed, 02 Jul 2025 09:34:58 GMT  
		Size: 6.4 MB (6447620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ad5f1cf37970da4179132fdaa4800b31a87a71773b8079ed2567a4a8e8299f`  
		Last Modified: Wed, 02 Jul 2025 09:34:59 GMT  
		Size: 19.0 KB (19037 bytes)  
		MIME: application/vnd.in-toto+json
