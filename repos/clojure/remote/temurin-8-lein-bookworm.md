## `clojure:temurin-8-lein-bookworm`

```console
$ docker pull clojure@sha256:4aef9f117fd9441a1ce4c7197ba7f6ccf7f7dc2c3f9b96b6ad7e8955280c3bd4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:dd59af3ec9d02cc67b354bda60760734d31a4aa03322383955b240158fd0d2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128023572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6579d490abfbdd494f1d20c41a65ffb2dabd01b070e951118a216ac7c20dca70`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:55:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:55:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:55:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:55:32 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:55:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:55:32 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:55:46 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 19 May 2026 23:55:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 May 2026 23:55:46 GMT
ENV LEIN_ROOT=1
# Tue, 19 May 2026 23:55:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 19 May 2026 23:55:47 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3648f3291a4d25e2bb51f0f1669282bedc7fcae8d94b6e98cdf3b987afa8012c`  
		Last Modified: Tue, 19 May 2026 23:56:02 GMT  
		Size: 55.2 MB (55198702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8353c6c0163131aee14ac6d9b3dd8a56a57e15c6bd94f76fb26d09dcf4e54131`  
		Last Modified: Tue, 19 May 2026 23:56:01 GMT  
		Size: 19.8 MB (19811694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c0dbc56c0b8c5006b6eaefabd48f974ccb58f4b37276efbddeb085fdb73b2d`  
		Last Modified: Tue, 19 May 2026 23:56:00 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e55b5581898e4991a26fed1cdac05e5bcc1aece9fa66119e9a38f73c1b4c66e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9832f3a4a1a0e8f2e375431ffa5e89849ee6f6cea8cc905d02b658a70a0fe779`

```dockerfile
```

-	Layers:
	-	`sha256:768de37be3af08a84d2c8982eb7bdc8be27a0626ccfe698722830d607f7359bf`  
		Last Modified: Tue, 19 May 2026 23:56:00 GMT  
		Size: 4.4 MB (4402738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:432dd46cac3ab673a74b5fd8f53d1dc7a10925db2afab4c617a2cfbe24490930`  
		Last Modified: Tue, 19 May 2026 23:56:00 GMT  
		Size: 16.5 KB (16524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:83891c6ae868e6916ebfda719d34fa4637d4b7d232d3b04277667fe61255315b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126811989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcca099c7d748ff4ff2ef815e4f37f7124de6bd462790bcf7876a9fe485d5fe3`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:02:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:02:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:02:32 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:02:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:02:32 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:02:47 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:02:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:02:47 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:02:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:02:49 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbba7b18bc91607811060b6bd72e21eadd0e91cbdf2842519c780a53118b46a`  
		Last Modified: Wed, 20 May 2026 00:03:06 GMT  
		Size: 54.3 MB (54272922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0672c90b10e860cc7b9ef721976d1e1756a79cc7d7815ca9d8a75523a175e`  
		Last Modified: Wed, 20 May 2026 00:03:05 GMT  
		Size: 19.6 MB (19641845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b95797b81607b5bcd4ddc674aa7ee8aa09e3999b560c642086281dbaaa6e008`  
		Last Modified: Wed, 20 May 2026 00:03:04 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:38ed76e18b8c39b5c423dce84cc0fcc97cad43f50900083c7bcdadf524e4ecfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93e3e4d2f101426eb5780672b6e6304483f42cc252d5042ea366d0cfe0a5da7`

```dockerfile
```

-	Layers:
	-	`sha256:a216200a6a11e75830d575ab4309784f158ed514ce0482b801eb1c37c5e36c22`  
		Last Modified: Wed, 20 May 2026 00:03:04 GMT  
		Size: 4.4 MB (4403053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5fbc68c16c8f4431f7f9a0c6a32324fa62981035f8304054a81445a811f3268`  
		Last Modified: Wed, 20 May 2026 00:03:04 GMT  
		Size: 16.6 KB (16645 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:dd092e501f490a7d083dc2829708c26422286d4540dfe8f8a5a1d5eb86a9798b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129560345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b77aa6a594c14ae268f2c11b633a8ccfda0bfdec63e0b26e8e385295a42431`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 05:41:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:41:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:41:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:41:57 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 05:41:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 05:41:57 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:42:27 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 05:42:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 05:42:27 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 05:42:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 05:42:32 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b865ce015782198efd3fb681f99e5929fef916aa774999d18b087fba22a996`  
		Last Modified: Wed, 20 May 2026 05:43:04 GMT  
		Size: 52.7 MB (52669123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f95bc8589d6b7084902dd0f089795f753032bb773d08730dc51b84c5831855`  
		Last Modified: Wed, 20 May 2026 05:43:03 GMT  
		Size: 20.0 MB (20033260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fbdac74c6d787cb985fdb438c055787077a7203943a29093764c9bc1f5a5c7`  
		Last Modified: Wed, 20 May 2026 05:43:02 GMT  
		Size: 4.5 MB (4517731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3ae6efe3f52973bbe416913a55ddc10476e3ec0b52715a1cb314fb95b737a7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4421762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6c1b156e4079a59bf86cf4e52aa23675d3d1c31a3f5e215245a3d8788f523c`

```dockerfile
```

-	Layers:
	-	`sha256:f8cebdad6db470f21fd8b1061f7c98cc296373fba377f9f1c2452d90a9fb9d70`  
		Last Modified: Wed, 20 May 2026 05:43:02 GMT  
		Size: 4.4 MB (4405194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d898a8035fc8104774aeebd50cc23002e17036661f5eb7b13ab184eb5519ce23`  
		Last Modified: Wed, 20 May 2026 05:43:02 GMT  
		Size: 16.6 KB (16568 bytes)  
		MIME: application/vnd.in-toto+json
