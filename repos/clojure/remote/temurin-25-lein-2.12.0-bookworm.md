## `clojure:temurin-25-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:a7dcabda82b14970f66b884899c55aafe385ff0f45c55a6e36f6bd2b1f16829f
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

### `clojure:temurin-25-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:b9a24a9b0a7c4b21adc13f96318672f0609865bead8f21e22e7f1385de3c0f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165399917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cab362feb7a14e1cd1c9dff79491767909f1b19233d05d8644c6d5e41c5d5bc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:00:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:00:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:00:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:00:37 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:00:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:00:37 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:00:51 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:00:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:00:51 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:00:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:00:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:00:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:00:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778b180785b8db011aa334089d3a97da98986ea6dc5000981b2b86b5fc2acf21`  
		Last Modified: Wed, 20 May 2026 00:01:19 GMT  
		Size: 92.6 MB (92574585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1573dcefab1aa2f150ca25c1373c278ef44808ccec15fa1fff9193c416e876d0`  
		Last Modified: Wed, 20 May 2026 00:01:18 GMT  
		Size: 19.8 MB (19811718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f3da6690d72e79e22c3e0e7646ff44bfbb388850e7f7a5cf57511ee9ddd84b`  
		Last Modified: Wed, 20 May 2026 00:01:17 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7be0d7d98d1f44a7778c1ca27fe2b4d3db2ced6a67da8532118fa21749d36ae`  
		Last Modified: Wed, 20 May 2026 00:01:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c6d192a8f9754229e97a17d4558b147076a434fe9aafdfb337543af1f0556f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4687ba00da2ef1f6b6c971d258cb2b2dae9c69793d6576324b46047fe769a747`

```dockerfile
```

-	Layers:
	-	`sha256:5a967b692804328ff6609761af134f2f99b063e0dfb12e66098d94486d66fc8d`  
		Last Modified: Wed, 20 May 2026 00:01:19 GMT  
		Size: 4.3 MB (4251668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdb97a9590e87a8f028c13f4bbad4d0fa5d10fcb2e84d3d18eb496fb9835c9fe`  
		Last Modified: Wed, 20 May 2026 00:01:19 GMT  
		Size: 20.4 KB (20413 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c160d20d37ca6b211d92f4946e52dcf311126ba91f092b9876d974b66bb47ff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164081630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2521f7433eb8dc88544bf832032e4d89e05d0b6391ed6c0af6628cc14a678ce8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:07:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:07:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:07:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:07:15 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:07:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:07:15 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:07:30 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:07:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:07:30 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:07:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:07:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:07:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:07:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b80a37e284dcb6180825d8a8cae0925e3b5f62c9939024cbb94f6110887851`  
		Last Modified: Wed, 20 May 2026 00:07:50 GMT  
		Size: 91.5 MB (91542261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582f96e376c493c4c23db7d3758885dba93c047c2d2ba3ddf0fa3a18da49bec3`  
		Last Modified: Wed, 20 May 2026 00:07:49 GMT  
		Size: 19.6 MB (19641808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7e63c4e02e1ce5197a2b0142dd13c99b6de33fdbb7564153b3b9394f89d40c`  
		Last Modified: Wed, 20 May 2026 00:07:48 GMT  
		Size: 4.5 MB (4517701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91622645c5aea3fa6f5105abdfe887b7089109a683f39b48d6ba04e70e61bcba`  
		Last Modified: Wed, 20 May 2026 00:07:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:31ef4a3a615cfe132b02145f7bab9e2353d46a24aed1ce048dfaee9e7b94b72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6383c029dc8a4c13441ce796124b9aba00a8cb45b45b4460046417e3db0c5e`

```dockerfile
```

-	Layers:
	-	`sha256:49e962c0fdd43c876f352996e73b3c71ef1d4c97c0a218fa4010712e488e34c8`  
		Last Modified: Wed, 20 May 2026 00:07:48 GMT  
		Size: 4.3 MB (4251352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:987d48e6327f89e33825cd60f16ad0ee309767487e0192c437afd71564ad409d`  
		Last Modified: Wed, 20 May 2026 00:07:48 GMT  
		Size: 20.6 KB (20606 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:0169ecb500640882809bd8fec8a2f844563d40009aac5f7aeeedf8f9ac2ed316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168799500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50f4fe00ef7c5d4fa7305d34149bce60098faf1374395061beaf30fed594a84`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
# Sat, 09 May 2026 02:42:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:42:12 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:42:12 GMT
CMD ["repl"]
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
	-	`sha256:b6c5a7a80bc073448cd4e81bddcd50f7d37d237a1a71bf0ae87ab9e0de092df2`  
		Last Modified: Sat, 09 May 2026 02:42:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8c7dabf8bfc49fde486b870d5aefba9fb5428e72c963025062866b48679ff23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4256399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dba11dd9e1773793549394aa287278e0a5bdb92712ec9e372988a20afe00e74`

```dockerfile
```

-	Layers:
	-	`sha256:d5b388595c9c0368ea81247b1f1028721590c538be54c02d23f4985e168a16f6`  
		Last Modified: Sat, 09 May 2026 02:42:29 GMT  
		Size: 4.2 MB (4236859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b468c4b106348935eba14afc3c7973ac0f095cea071eb464457524d399618d8`  
		Last Modified: Sat, 09 May 2026 02:42:28 GMT  
		Size: 19.5 KB (19540 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:687b6dd0f5182b6b0380166567fed2c983ed74bf96f9f985f7cc2cd643d6d7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159567840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ccd42ec24a88a9eaae69f0763e98a2a3f058ce2073ba26493273b64c3a4388`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:40:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:40:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:40:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:40:39 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 01:40:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 01:40:39 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:40:55 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 01:40:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 01:40:55 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 01:40:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 01:47:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:47:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:47:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a934554ab57d2fd5986adad7cd7478af54f0d87c944e186bd166c53ad21467`  
		Last Modified: Wed, 20 May 2026 01:41:43 GMT  
		Size: 88.4 MB (88420319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdd88ea48242c31c3879754e78c6bf8e58100cb6a81ed18f4b20caeee46d46c`  
		Last Modified: Wed, 20 May 2026 01:41:41 GMT  
		Size: 19.5 MB (19473757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9ae8639f45bbe737a5ad3c701692aedd0f3a28c0cd34dfead8ea724c82fee6`  
		Last Modified: Wed, 20 May 2026 01:41:41 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456d6aa2bf7eadf75f73f5e673b88e4c4ac868bcb4bd9bfbd623c9a3d7ad5217`  
		Last Modified: Wed, 20 May 2026 01:47:12 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e934fe3ff3fcba678a5604da053c7a05aabce96e827982e81f76b068cb44ccf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9307ccd9706f6e94c0703e278d5f8a51b3b1365a21e5977e368792c0a2c68b0`

```dockerfile
```

-	Layers:
	-	`sha256:d4a8bdafb08eb5caaf8a47474d6659540a8a6ce4852a2c8a25c6c27654cc29f3`  
		Last Modified: Wed, 20 May 2026 01:47:12 GMT  
		Size: 4.2 MB (4228044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a54f75c0373c5ec268798b41eca6c56fcf0e26a41ac3419e3908263abc43b98`  
		Last Modified: Wed, 20 May 2026 01:47:12 GMT  
		Size: 20.4 KB (20412 bytes)  
		MIME: application/vnd.in-toto+json
