## `clojure:latest`

```console
$ docker pull clojure@sha256:77c7d63a8387b0d4e538e364b156dbcf0cab197c5310cff2d10f7628275b4290
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
$ docker pull clojure@sha256:29e9085530178c18ebd2db3205a2f1b19430d77894f1667272886eee4806b92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239920304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd755b24b7933ef3be04b997cd97073b4b8475cf790ad29117ec452c85a412c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:17:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:17:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:17:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:17:15 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:17:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:17:15 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:17:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:17:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:17:31 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:17:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:17:33 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:17:33 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:17:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:17:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:17:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:17:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:17:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881678cd63841dd6b8330c52c04cbf408e8458eb009c9e276219b07b29a5bb2f`  
		Last Modified: Tue, 03 Feb 2026 03:18:11 GMT  
		Size: 92.0 MB (92045314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7fa46f66c956280b195f9695a63082fa00b694d7700d18963c0e232bd14991`  
		Last Modified: Tue, 03 Feb 2026 03:18:08 GMT  
		Size: 19.8 MB (19802869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb33a8eb106e3985a10efd8454ecc1b3384c110b648b9f835ac8762fcebfa19`  
		Last Modified: Tue, 03 Feb 2026 03:18:07 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a8e04ef61b72b78d70a46d7a0e434a3095ae8badc4d30cf400377918324eef`  
		Last Modified: Tue, 03 Feb 2026 03:18:10 GMT  
		Size: 75.1 MB (75071821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7622b3b113d49a019a18ac65b0ed40b6e475bdcba543d7ec796c94bab0a6df88`  
		Last Modified: Tue, 03 Feb 2026 03:18:09 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d12626abda5863454625ce6dc1fd23ba8562736d1c849a214a910dc35dfaa2`  
		Last Modified: Tue, 03 Feb 2026 03:18:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:9a1d3e4a5e40c63d09da1b68d879708e7c591a5108ec2e74cff31afe97d163fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62afc28756fc38b7c30a9b8ed28a6cebee3ed03c8b7d4692cb8bacc1f9a4f36`

```dockerfile
```

-	Layers:
	-	`sha256:4755eb1228374f54adbf6b1703b27e3316c8ae97d4935b9155dcf8ae46d98bfd`  
		Last Modified: Tue, 03 Feb 2026 03:18:07 GMT  
		Size: 7.4 MB (7419370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d15ae3094018e455b5f9a1e9e6401c00928e6d17956cef36df6473ef6c009f6`  
		Last Modified: Tue, 03 Feb 2026 03:18:07 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7bdf5b4139bcd462fc9fec2ff5daba001e9ae54b3b27e408c9730302e95170dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.8 MB (238801119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8afe22478eb865c617772e6c4ceb18a474d80e41118fafb67acfc7380802499`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:20:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:14 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:20:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:20:14 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:20:29 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:20:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:20:29 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:20:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:20:30 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:20:30 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:20:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:20:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:20:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:20:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:20:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65c0c29d2b39cab1c4f4eee185fbd089baec7505063c168a86e13212df3c4e7`  
		Last Modified: Tue, 03 Feb 2026 03:21:06 GMT  
		Size: 91.1 MB (91052507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fb306bb3d625ab5dede89363b05bbfa5a14bfe701cf67a3aa9d5e6b13de26c`  
		Last Modified: Tue, 03 Feb 2026 03:21:04 GMT  
		Size: 19.6 MB (19632797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298b86513b25dc5892544c214af3bd37f0e6c9af09f66a0b2c3b37620d82e318`  
		Last Modified: Tue, 03 Feb 2026 03:21:03 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da6d903aea7a1f04533d604ad994890492620abb2894e8e183c256bcd388d6e`  
		Last Modified: Tue, 03 Feb 2026 03:21:06 GMT  
		Size: 75.2 MB (75231066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70148471abce8edbab4f5acefdfc4933814fc82d3e11aafedbe4936eecf91b7`  
		Last Modified: Tue, 03 Feb 2026 03:21:04 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50fb6f8956cecfcaee0b174a8addfbb5a6416bc4dd15ab34ac1e7a1d223d16d`  
		Last Modified: Tue, 03 Feb 2026 03:21:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:017d8a3bc61e44f4196b065b0e87f7a9aae6f1c71d61e90e510eff0cf7874d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7450838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ce9b2733560df3c0a2932745ae0d6d9aaa953895434950b5670887ceed7ce8`

```dockerfile
```

-	Layers:
	-	`sha256:43e44bf40ab53c40491440d04e48d769eefeb0ed2c301eba7f97ef21a52c80ee`  
		Last Modified: Tue, 03 Feb 2026 03:21:03 GMT  
		Size: 7.4 MB (7425106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bb1c0c307e9639be95f7d57e96c03915c0f03d1f7f7007f86d70f7db7ce14c5`  
		Last Modified: Tue, 03 Feb 2026 03:21:03 GMT  
		Size: 25.7 KB (25732 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:b0c03e96b220b6ce8f1fc1f3ce4e85eb7f428c6d04c9240ac3175062e5e1f126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249155059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75cb65cfc8a9e60da95495245072102e9c632ccbf13159bf1d7b68a6b00b0444`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 09:26:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:26:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:26:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:26:41 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 09:26:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 09:26:41 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:27:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 09:27:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 09:27:14 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 09:27:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 09:27:18 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 09:27:19 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:28:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 09:28:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 09:28:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 09:28:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 09:28:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f0540c2771fa9506db24965044fb39bf9f36f0c2c7623c568dcfe6110ba393`  
		Last Modified: Tue, 03 Feb 2026 09:28:50 GMT  
		Size: 91.6 MB (91610788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd357cefacc043eedf21b15f2a7f468b3d011c964ed0a2951b21e13cf9f521c1`  
		Last Modified: Tue, 03 Feb 2026 09:28:47 GMT  
		Size: 20.0 MB (20023671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d6b059c6e75f55dba21aadda71cdc7ec70f30258f7a6d24e126eda5915065a`  
		Last Modified: Tue, 03 Feb 2026 09:28:46 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120f010332d9fb1969fc2bdcb47745b7fe6e4d28e88ff82a0f1a4d72463f9cc7`  
		Last Modified: Tue, 03 Feb 2026 09:28:50 GMT  
		Size: 80.7 MB (80674482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d510d35ce85997908f825814e4b50f126274a8880de2cae45ff551a14ebde1b`  
		Last Modified: Tue, 03 Feb 2026 09:28:47 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23db96fda7524c5719ea35e31a49346707ba6d415d7e6b1d2b72ee94ab301ef7`  
		Last Modified: Tue, 03 Feb 2026 09:28:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:887715eddc541b69bb95378c61b1632883c8f2c2a57ce84e67c3ae854a74a3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7451521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61950728b704aa18dc8891fd46e8f725f94b61d8055725bd78f72adb2171fc31`

```dockerfile
```

-	Layers:
	-	`sha256:fcbe5bdd77017ed7b64385d9a8983f2f3777bc3564dc3713a28388ac7421a6be`  
		Last Modified: Tue, 03 Feb 2026 09:28:46 GMT  
		Size: 7.4 MB (7425872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14779d6f645e4bd5de8ebb53cfa99edb8e1829297eed97a7a4cbfb3d0e8de442`  
		Last Modified: Tue, 03 Feb 2026 09:28:45 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:0f78d99fb2b3e01b2a81c887e041fd879ac4b7bcbf699b66b0105f95d6218f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233552686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd9fe7ea98a265348683d632f8b974dd21118f51aa108fc18896877c43af466`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 04:59:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 04:59:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 04:59:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:59:30 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 04:59:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 04:59:30 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 04:59:42 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 04:59:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 04:59:42 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 04:59:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 04:59:44 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 04:59:44 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 04:59:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 04:59:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 04:59:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 04:59:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 04:59:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdef57afedce759031aec2d24c0fff4c7e6f222a37d2f21fec7f3a9fa7818efe`  
		Last Modified: Tue, 03 Feb 2026 05:00:27 GMT  
		Size: 88.2 MB (88210680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dcaa56ef88ade0a292848fc88fdf40a42d022a832819281d71aca24b922530`  
		Last Modified: Tue, 03 Feb 2026 05:00:25 GMT  
		Size: 19.5 MB (19463171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1368acbdc7a6eaab11c831e35adaeab66006541b564334b620ad19ac5039993`  
		Last Modified: Tue, 03 Feb 2026 05:00:25 GMT  
		Size: 4.5 MB (4517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154f6c971ba2e7a486ee6904ffda2d49ccb8535e6a4d4bebab2139003dbb7286`  
		Last Modified: Tue, 03 Feb 2026 05:00:27 GMT  
		Size: 74.2 MB (74221678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9364e40a64ffc20c46912e209569d2834fda155e08eedf7bd929797dcbbcfeb`  
		Last Modified: Tue, 03 Feb 2026 05:00:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfab8e6f6c1610f691aa5c182084f67629c6a7fb15c8df920b1965c788bf38f`  
		Last Modified: Tue, 03 Feb 2026 05:00:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:1d0b07aeb96d61cac3624c5bc5c95b15f7039cd70cc8278418319661ada0988f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7438845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51add68f43af49cfd2a86c3f7c66358267d4595d2bd73d6147e51bfa1acdff5d`

```dockerfile
```

-	Layers:
	-	`sha256:18c1778f155a24caa6fe11aaf5f874bc2bc406284a345568002fbd4975c70195`  
		Last Modified: Tue, 03 Feb 2026 05:00:26 GMT  
		Size: 7.4 MB (7413237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8352974dba47fd8e356038ce5a5ff22807017ba80720bb8f163dc8f80664e9f5`  
		Last Modified: Tue, 03 Feb 2026 05:00:25 GMT  
		Size: 25.6 KB (25608 bytes)  
		MIME: application/vnd.in-toto+json
