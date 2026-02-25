## `clojure:temurin-8-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:5df0bcabc954e50f81e06e4ec56913336905fff43600f886bf814fcaf428dba0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:458ba055a10dd239a369e77274ff85a8e9f6437e711e7d77e70f97caa21c7e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127979531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0805a96081065f99c7445168664c13d1d32e1ec1419b73285cd6f910279db26a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:52:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:52:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:52:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:52:04 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:52:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:52:04 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:52:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:52:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:52:18 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:52:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:52:19 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226332ea3f9c564edeb3bbde63b3c9d476d133dc336dbb442852ec2fdae2ddb`  
		Last Modified: Tue, 24 Feb 2026 19:52:33 GMT  
		Size: 55.2 MB (55170133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af1440739d35f46541db93d175fea092c3fdcad1a7352f7635c60fd89503236`  
		Last Modified: Tue, 24 Feb 2026 19:52:32 GMT  
		Size: 19.8 MB (19802877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da097a8598a3459d04398ece9567e28e5e8489f9672795ae1580ea048fcf40`  
		Last Modified: Tue, 24 Feb 2026 19:52:31 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1dd18ab685290d59630f4636f647231b679c1ed481f49789ab21f0ad13c03118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5914ad13dc7ae428ccf0f9c107e93ddeeef929b2789082210845925f731f785f`

```dockerfile
```

-	Layers:
	-	`sha256:f273d96f20ab173ae4cb6e29265fe86a520802aae9c57c2ec3cb2ee6c4d2acf9`  
		Last Modified: Tue, 24 Feb 2026 19:52:31 GMT  
		Size: 4.4 MB (4402720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d521491d53d967bab7107693c2d173c9cdb5f7d72ef966ce3820c3e54cef7fa`  
		Last Modified: Tue, 24 Feb 2026 19:52:31 GMT  
		Size: 16.4 KB (16370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:455f989c27eab011695a04c3c7cecca66ffb32a6d7aaa15516f4ae11a0e86330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126775359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f330d051690894c4be0d8076f4e3ed2b8cb112687679259b742688c3825c167`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:02:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:02:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:02:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:36 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:02:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:02:36 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:02:49 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:02:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:02:49 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:02:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:02:51 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5899fd4281eb802180094cd7248a180de2d7f4dd4fadc1ad27cbfc97e09414b`  
		Last Modified: Tue, 24 Feb 2026 20:03:03 GMT  
		Size: 54.3 MB (54251619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4f68512df7c028ce372c196f900addfea782f8e2d1defb57f03a8e63cce0f8`  
		Last Modified: Tue, 24 Feb 2026 20:03:05 GMT  
		Size: 19.6 MB (19632775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941aec6e367467fff43b02e2b8433373fec5e1f364bcf8f484e281765a847481`  
		Last Modified: Tue, 24 Feb 2026 20:03:04 GMT  
		Size: 4.5 MB (4517723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b0386967459a8f6db4529daf754e0e28d1982686053871c16c309104e20a803f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e2cf921a687f5bcf33dc8b33c1ad1d57e6b67df894ad56295a6b5f642b9f11`

```dockerfile
```

-	Layers:
	-	`sha256:59fa4e0427608a6e361bc6a1d12c60eaba163c1c62bf88279085b82749fdc99a`  
		Last Modified: Tue, 24 Feb 2026 20:03:04 GMT  
		Size: 4.4 MB (4403035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1efa51a8077d278fd464ec2ffa05760c604421d444d909542be28b1f0f2ad36e`  
		Last Modified: Tue, 24 Feb 2026 20:03:04 GMT  
		Size: 16.5 KB (16491 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:a3828f668af44c3b082e6ca62a3b80d21b8a3646f1dee0fd4bae9dcffc3bb130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129528922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c017573174081bd0c345914f1ec97dd199ce401748aabd0c814c182ddfae474`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 01:40:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:40:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:40:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:40:50 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 01:40:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 01:40:50 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:41:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 01:41:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 01:41:28 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 01:41:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 01:41:33 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758957e39a5342d475126ebfd163d16c39ac530ed3ea794d3a28465b8deb3059`  
		Last Modified: Wed, 25 Feb 2026 01:42:09 GMT  
		Size: 52.7 MB (52650389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69d62614090347551990439ad653c24bc219e7d80330b13da44d11f60ea27b7`  
		Last Modified: Wed, 25 Feb 2026 01:42:08 GMT  
		Size: 20.0 MB (20023938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4464611eb01e12f2120488a242466b448c937fee9280616743809fef114612a`  
		Last Modified: Wed, 25 Feb 2026 01:42:07 GMT  
		Size: 4.5 MB (4517766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:52a474b5a1c5de7d496c27fb7a99ce92348fe677fdb560c15ceef6984e1cdf75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4421590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c283745f680f263f226f4edb0492868e9727f0da97f443a15d52dc9601adfdbd`

```dockerfile
```

-	Layers:
	-	`sha256:0d27b6c716f2beb2bca217d39952b2c750157fa90cb2eb5096bd518664665723`  
		Last Modified: Wed, 25 Feb 2026 01:42:07 GMT  
		Size: 4.4 MB (4405176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a39fd3110f9aa1f28a068510a077d69a2fe3a530485f911319c208c49700f78`  
		Last Modified: Wed, 25 Feb 2026 01:42:07 GMT  
		Size: 16.4 KB (16414 bytes)  
		MIME: application/vnd.in-toto+json
