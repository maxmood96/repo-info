## `clojure:temurin-17-lein-2.9.10-bullseye-slim`

```console
$ docker pull clojure@sha256:a7bfe202318b7010832a5a8614bce8717043eec6525b9de3f1340c9f237ecf94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-2.9.10-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ffccbf62e269d522538fcd4f170be78ba10c8f614d375b922addba16476e19e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240938202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59bf717d440a03987261d7b4f1e1967e1cee2b4455de70cc9665134bfcf672f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:56:40 GMT
COPY dir:09afbf947759009c57336c17f70cd71239c5d8b0170793151aec66483cdd0976 in /opt/java/openjdk 
# Thu, 06 Oct 2022 03:56:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 03:58:11 GMT
ENV LEIN_VERSION=2.9.10
# Thu, 06 Oct 2022 03:58:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 03:58:11 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 03:58:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 06 Oct 2022 03:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 03:58:27 GMT
ENV LEIN_ROOT=1
# Thu, 06 Oct 2022 03:58:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 06 Oct 2022 03:58:30 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 06 Oct 2022 03:58:30 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 06 Oct 2022 03:58:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef3d95ee3a8969f154e4e82981119ffbe3fb6d2183d260566ed8ba03b8fc6f8`  
		Last Modified: Thu, 06 Oct 2022 04:12:33 GMT  
		Size: 192.1 MB (192137622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6226079265b50168b248205d85a4ae51a589dec3c2af4ac33842caf02b01533`  
		Last Modified: Thu, 06 Oct 2022 04:13:38 GMT  
		Size: 13.0 MB (12981420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7bbf9e58d6e4dbd25d1113d9648e52bdc59131b90f5b82607fdc6279a3fc28f`  
		Last Modified: Thu, 06 Oct 2022 04:13:38 GMT  
		Size: 4.4 MB (4398658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aafcba117c43f08799622d6b851a5a300c72c40da995bc1c91d30f71d5f5854`  
		Last Modified: Thu, 06 Oct 2022 04:13:37 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-2.9.10-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f127327b430df405997dd4136699ed438f6778677ec19cc01f38782ac37909f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.1 MB (238131824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4ad661fc1b19527a5f047e4e43b7d1db7f1f2a9239fcc9f797ff083cf63d3e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:39:47 GMT
COPY dir:dc2bc1e50ab42c5231433386b6bc2a9cff04b310112464fb4909efc66be10627 in /opt/java/openjdk 
# Thu, 06 Oct 2022 02:39:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 02:41:53 GMT
ENV LEIN_VERSION=2.9.10
# Thu, 06 Oct 2022 02:41:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 02:41:55 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 02:42:10 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 06 Oct 2022 02:42:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 02:42:12 GMT
ENV LEIN_ROOT=1
# Thu, 06 Oct 2022 02:42:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 06 Oct 2022 02:42:17 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 06 Oct 2022 02:42:17 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 06 Oct 2022 02:42:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd853b0df38079bcf0a5945a7e8ed2935d92b2270210148614164b9ddd8b48b`  
		Last Modified: Thu, 06 Oct 2022 03:01:36 GMT  
		Size: 190.9 MB (190904238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b288d37d3f91256b0f22d539a09207c32538ba1f83514d483bc7c2e7fc94fb6`  
		Last Modified: Thu, 06 Oct 2022 03:02:54 GMT  
		Size: 12.8 MB (12764189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7b3b6dbbf7e933fe425a6efc7bbeaef534eaa7df7b2615a47dfe75046e4949`  
		Last Modified: Thu, 06 Oct 2022 03:02:53 GMT  
		Size: 4.4 MB (4398602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4549a5e91d6dea343676b262be0704cf143c3a89c24854d02eb23215a94d810f`  
		Last Modified: Thu, 06 Oct 2022 03:02:52 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
