## `clojure:temurin-21-lein-2.11.2-bullseye-slim`

```console
$ docker pull clojure@sha256:8e427d456134441ca3c502d76b46adb334db843a194c068a59af1e216d858a27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.11.2-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1accc2f523525a2dafaf16345b21fbf4e00f10ff753ab466158adeaf1e27a47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235636489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0b9833ad48d1d2eecdb0c08d5549b2b499fb4b1e167ca827d5d491b6c1792f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340568302177098e131e6bad8350e922db580818728e05509c105e20e4bbfdbf`  
		Last Modified: Wed, 09 Apr 2025 02:19:13 GMT  
		Size: 157.6 MB (157585883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955f6b6406334831b608af6bd9fdcd288bac9c8db0eac41ed70228ebabfe6947`  
		Last Modified: Wed, 09 Apr 2025 02:19:11 GMT  
		Size: 43.3 MB (43278610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8e2128a07898ad489d6c4f5d6f7ba968fb2e0d28aa84935e977f5225360132`  
		Last Modified: Wed, 09 Apr 2025 02:19:10 GMT  
		Size: 4.5 MB (4514147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e98066f802c0b49d7b1687e8d34b1ae79d6a540b166b18b6e95d600dac59e37`  
		Last Modified: Wed, 09 Apr 2025 02:19:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:54db4ef1b1bf4abc0a414749801af82128d5190186b1b6db5e6dbe2304bed291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4592999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81896e27a2bead4f0c359adba67a7953d67ac4172ffe78936a4ebfd72e32858a`

```dockerfile
```

-	Layers:
	-	`sha256:6d5563b4ed71220bac856c4ab9bec843247a19ebdc20580a67cce2d29ae89cd5`  
		Last Modified: Wed, 09 Apr 2025 02:19:10 GMT  
		Size: 4.6 MB (4573879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4a9e145aa9e1fd137b05bca5c911c8676f44619bc45cf2a2e783397efeb1704`  
		Last Modified: Wed, 09 Apr 2025 02:19:10 GMT  
		Size: 19.1 KB (19120 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.11.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:78c38c53849892f8ed357e49da539ede817cae04eb1a8d557244b419746e1ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232437520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019b619d8f0bfb72285d800bf681da97b7a006c787be489d29f596b697ef5a0e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3092970dfc6ff6b5baaf45f0ff4fdbdd2c181b6e2eb0565cc8b269a2c08eb8`  
		Last Modified: Wed, 09 Apr 2025 15:16:05 GMT  
		Size: 155.9 MB (155859263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ea9ea1011946e0559e734853d3d5b75bdbd5b1ea6ff8c9375a1017a42347b2`  
		Last Modified: Wed, 09 Apr 2025 17:40:51 GMT  
		Size: 43.3 MB (43314138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677e3664bca73845d88bbb8751492c1300a3accb534757b25b638d56f2ecf4b2`  
		Last Modified: Wed, 09 Apr 2025 17:40:50 GMT  
		Size: 4.5 MB (4514191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc7657c5a8caaf3b98de931acd4300c98dd4fd0d5c4f5b98aeb622ed130c64f`  
		Last Modified: Wed, 09 Apr 2025 17:40:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ed227a4a33434a3702ce1b9bae656e73b22d446fd7fb2e2fd5ce12cf4761495d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4598832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5743a878c655e6271f1bc062ff3946b9ced84c612c284b60bc917507ff9413`

```dockerfile
```

-	Layers:
	-	`sha256:e75a2265447db2ffb4ad2695a8437ca5af80cc04c3dbbcdff4339b55088493e8`  
		Last Modified: Wed, 09 Apr 2025 17:40:49 GMT  
		Size: 4.6 MB (4579567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7565b144e81777f84e36f40832c26dd68dbe5e07ab111a6c2e4aab71a7b10e18`  
		Last Modified: Wed, 09 Apr 2025 17:40:49 GMT  
		Size: 19.3 KB (19265 bytes)  
		MIME: application/vnd.in-toto+json
