## `clojure:latest`

```console
$ docker pull clojure@sha256:2eb95d5f2f857ccf9d8af801e305a923ebf2e9932f8508156956e5135291f4a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:latest` - linux; amd64

```console
$ docker pull clojure@sha256:6b1f35c599fb1661c575e582e71acb4015f86d1abc0dafa4d15f9e1a4f9d3254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240511209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e77a5417ee61aac9d7c9db96c7066a50cceb087061fd0e2c63a47a28429f511`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:33:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:33:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:33:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:33:15 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 14 May 2026 23:33:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 14 May 2026 23:33:15 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:33:29 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 14 May 2026 23:33:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 14 May 2026 23:33:29 GMT
ENV LEIN_ROOT=1
# Thu, 14 May 2026 23:33:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 14 May 2026 23:33:30 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:33:30 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:33:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:33:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:33:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:33:44 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:33:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bcdc8504277ffc1c492da7bdd0db99a4d4cb73d300397c02367164c22915c4`  
		Last Modified: Thu, 14 May 2026 23:34:07 GMT  
		Size: 92.6 MB (92574586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422379fa0115faa88ee4a4fcda4b4047c2b3e15ddd43be97f47d5b45f10fb44c`  
		Last Modified: Thu, 14 May 2026 23:34:05 GMT  
		Size: 19.8 MB (19806628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b133a82e05843c09638a44900df66fb447d22876799a70cc291712646193af0c`  
		Last Modified: Thu, 14 May 2026 23:34:04 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a934a1f7a725e0bbf112220b74c673a27a5acae700852fed46504e8807613524`  
		Last Modified: Thu, 14 May 2026 23:34:07 GMT  
		Size: 75.1 MB (75122514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641beac3b4d094cc70ff347ec12d313f69200e0ea6d61912b4a016e6fee65f41`  
		Last Modified: Thu, 14 May 2026 23:34:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d3f901ccdc6e49870db7475448a1c2a9ca189e91f8f27a8d64166aff83c9d8`  
		Last Modified: Thu, 14 May 2026 23:34:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:26ba6b8b54c6a9e7830abb77c68cfbfe6245c98ed526dc7a8599e98bbedc1273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7465255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39eaec2d06883e28ff0a817fee9bda659281eca52eabbb639b22e3110e6006b8`

```dockerfile
```

-	Layers:
	-	`sha256:78e07195858d385f9b5de8f36d09e2508deacd1fd56e6210ffcfb5a5cc903fbf`  
		Last Modified: Thu, 14 May 2026 23:34:04 GMT  
		Size: 7.4 MB (7439492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf80546d4b7421072ceba45932868494d3275c4ca623c3fb5dda06c00d1e3f37`  
		Last Modified: Thu, 14 May 2026 23:34:03 GMT  
		Size: 25.8 KB (25763 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:74241d49107a40286b57df86e463983226116aa1dd5c43fd312efe3bf44dd7e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239351880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7edc16f660f55e33ee002d1c8b2f23b84f20e52b31ee323c5c7dc7ca377964c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:33:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:33:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:33:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:33:12 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 14 May 2026 23:33:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 14 May 2026 23:33:12 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:33:26 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 14 May 2026 23:33:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 14 May 2026 23:33:26 GMT
ENV LEIN_ROOT=1
# Thu, 14 May 2026 23:33:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 14 May 2026 23:33:27 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:33:27 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:33:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:33:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:33:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:33:41 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:33:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41fc1731591d1bb05ff9c1da99c263b34ae72ffcf679362fb8b0c43a6e2862a`  
		Last Modified: Thu, 14 May 2026 23:34:04 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b64dc2c68dbf5e7fae8d2ce8650d392a1c95e425f83566578ffd3a3b2cf721`  
		Last Modified: Thu, 14 May 2026 23:34:01 GMT  
		Size: 19.6 MB (19637151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b78ba8c7122af9605d5b1da8d8636e371de765da4d9147fe9e35ae6ef4811f6`  
		Last Modified: Thu, 14 May 2026 23:34:00 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018da0585b8dade6a4f807707757783e83d0f4c8eb5b8ec1753095f54d94b6dd`  
		Last Modified: Thu, 14 May 2026 23:34:04 GMT  
		Size: 75.3 MB (75280547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee9a28ca48eeee5a1c47f0f01c290f6b8c300f11830fb5190c4d8ee19a74c47`  
		Last Modified: Thu, 14 May 2026 23:34:02 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690ef9b14925e92b8931230051331e8bda7b0aa124f3bbaa2ad2fb629f597d87`  
		Last Modified: Thu, 14 May 2026 23:34:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:0eb25276bb0137f42034ca3061f307c697083ac795d8d11d85e7343cd55840c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7471115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1292fabb50e8f9f95c79212f2a0454ec70d90b2127b16baefb426d62c5bf4a1b`

```dockerfile
```

-	Layers:
	-	`sha256:8da062615311b2c92ae97eab706c0cfe4c873627182d77dd21d230288b5070c0`  
		Last Modified: Thu, 14 May 2026 23:34:01 GMT  
		Size: 7.4 MB (7445228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fcd12b40e39bbce5d244e5f7f6322ec68eb81c1456361052672bc0662bc23ac`  
		Last Modified: Thu, 14 May 2026 23:34:00 GMT  
		Size: 25.9 KB (25887 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:ddcb9148a76f968b7d56350763cd42b9767805f7afe3e2e0cf8afc98ea5c021d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249522514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6e7e81780b77bc05e97647d11ee70bf647256625de7431821af414754efdb1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:18:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:18:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:18:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:18:51 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 09 May 2026 02:18:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 09 May 2026 02:18:51 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:19:17 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 09 May 2026 02:19:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 May 2026 02:19:17 GMT
ENV LEIN_ROOT=1
# Sat, 09 May 2026 02:19:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 09 May 2026 02:19:21 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:19:22 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:32:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:32:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:32:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:32:45 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:32:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5de956b7a11284f1a158aa4d174299365ba072baa5eadc5c41d537c7ba7509c`  
		Last Modified: Sat, 09 May 2026 02:20:31 GMT  
		Size: 91.9 MB (91914029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7c27935ce89344c9f2063adaf35463730e2c3db3cda2b4435240ccf8a48f5f`  
		Last Modified: Sat, 09 May 2026 02:20:28 GMT  
		Size: 20.0 MB (20030513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8435cb421dfc3e57ae86315bbfd20609e9a621d5a198bd965880b6dcdf4018b5`  
		Last Modified: Sat, 09 May 2026 02:20:27 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f31e1f9a8d6f33e69f68fbf97751e8c70dae4fb1b7cb523e6c212ba4328ab1`  
		Last Modified: Thu, 14 May 2026 23:33:27 GMT  
		Size: 80.7 MB (80722364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cca3fa26f64fbb4482eeb134b24779c8fdef40608b9e82527d02e333a06f4b`  
		Last Modified: Thu, 14 May 2026 23:33:25 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674c4668a849c6b4ff7f768889414dd881859acb8bd73076b4c8e7271074e2fe`  
		Last Modified: Thu, 14 May 2026 23:33:25 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:1f5af3378abafe1ade5b91b3c770d841a9a16163252052fe3b9399263816794d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7452858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eaa33a55138414eba566d46e30baec4ee4949104a2ea52c92dbe7a905b5f7ce`

```dockerfile
```

-	Layers:
	-	`sha256:e43c8b78524b15878fcba1c58f5828838ecce60b3d997cc3e95377a7919d3661`  
		Last Modified: Thu, 14 May 2026 23:33:26 GMT  
		Size: 7.4 MB (7428008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeeb24164a6d7fa31d76b88a077f09012506894ed688f91272e13842246f406b`  
		Last Modified: Thu, 14 May 2026 23:33:25 GMT  
		Size: 24.9 KB (24850 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:6d3665599b094c605349e9cb7d95e0407cf134ef4ac0b7c52cd4e79b260e611f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233824003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79858da4fa8c54f18fb397548f20976c27abd773004b01b4049c5a61e96e0ba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:32:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:32:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:32:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:32:13 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 14 May 2026 23:32:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 14 May 2026 23:32:13 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:32:26 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 14 May 2026 23:32:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 14 May 2026 23:32:26 GMT
ENV LEIN_ROOT=1
# Thu, 14 May 2026 23:32:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 14 May 2026 23:32:31 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:32:31 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:32:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:32:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:32:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:32:44 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:32:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b6df7c9202b34e5001f1810110d9cec30a4c24152183a755a378cbd2825b9a`  
		Last Modified: Thu, 14 May 2026 23:33:14 GMT  
		Size: 88.4 MB (88420318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea434e4bdaff060dd5d86848dd71f8fef7178355b899145cf2fcc6ca8551dbdb`  
		Last Modified: Thu, 14 May 2026 23:33:13 GMT  
		Size: 19.5 MB (19466847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302e9e28690038c8afdfe1a08c88ca42f5db41d05a25ae8720270cd48ac7cbc4`  
		Last Modified: Thu, 14 May 2026 23:33:12 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6840871ad8a9ce79250ca754e0b9798393c939dbf9b204d301e68e4f02cf1ace`  
		Last Modified: Thu, 14 May 2026 23:33:14 GMT  
		Size: 74.3 MB (74269996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10addcc23f315326f603e51004c07fe80a9186920746ec58bb60f852205b4e79`  
		Last Modified: Thu, 14 May 2026 23:33:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a922b147bd2c2123c698ec4f36bc99247f8999367271ccb8fcc89290f69db9ce`  
		Last Modified: Thu, 14 May 2026 23:33:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:cb29de6a7578cac2c5218771b6b4029a0f026dba705135416be0f9f59821a4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1997cd1f1ecda31f5001bd107a9b95de78f7aaa39ba0e6db4996a98c4b2c3295`

```dockerfile
```

-	Layers:
	-	`sha256:bec2f84a616ed5389e98549c4d1c49df6b183b08c267de14019f09282b381b06`  
		Last Modified: Thu, 14 May 2026 23:33:12 GMT  
		Size: 7.4 MB (7415373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6e1aa2875272204a882b3c8dea308bbf4d4b43e8dc3406a1da433ec85aee0e5`  
		Last Modified: Thu, 14 May 2026 23:33:12 GMT  
		Size: 25.8 KB (25763 bytes)  
		MIME: application/vnd.in-toto+json
