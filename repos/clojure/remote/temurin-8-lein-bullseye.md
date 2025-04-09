## `clojure:temurin-8-lein-bullseye`

```console
$ docker pull clojure@sha256:918a8a13aa28670bdcc26370451bf9ba7f79ed75543d15b8d4807ae13f541933
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:435e1f750cc3183a284e4efe8c87a887f378e7590b5fc5f0386eaa519eb4f4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165775592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0e08b092a09ed5d444252277f23c4cbb395b7863274eefd9b469151fbd2387`
-	Default Command: `["lein","repl"]`

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
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159bfd7fc5f0b1c5aab02f41965f2362974d6a596b9ed6bbb863083667605c02`  
		Last Modified: Wed, 09 Apr 2025 02:18:01 GMT  
		Size: 54.7 MB (54721244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8725437ef3b3bc8fdbe6ac994c92e0bebc7fe20c8c94e36e5edf423cfdc913fa`  
		Last Modified: Wed, 09 Apr 2025 02:18:01 GMT  
		Size: 52.8 MB (52791580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977ae917d397e70a995df732f0a708a9f8e66b253a9f740e4b124a5bdb919ed0`  
		Last Modified: Wed, 09 Apr 2025 02:18:00 GMT  
		Size: 4.5 MB (4514207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:52048b202127b5f434c8e31e5ce694fbd7f703747a07f261464b4d99f072fc4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6759735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46770b388df73aba141a5e01f004bfe3ab560b5e7ff1791f07a8e3c18c258f1d`

```dockerfile
```

-	Layers:
	-	`sha256:66fe65a552094ffe0a890a51711c6ba88cb6f9c749e4dc8dc70edc145a46b3a2`  
		Last Modified: Wed, 09 Apr 2025 02:18:00 GMT  
		Size: 6.7 MB (6743314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b181ff41e174b2960e82d77fb5a53844f48a1a2aeabedf8f8a7a4e5027dbdee9`  
		Last Modified: Wed, 09 Apr 2025 02:18:00 GMT  
		Size: 16.4 KB (16421 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:63fae287450d980429362f70b382dbfea1fb0a21b3109f47121a31b71ce00de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163422182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ccedd5afe81bf1b1ba586f805c6b9e65050f350c4e1f642e978f366c749fe5`
-	Default Command: `["lein","repl"]`

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
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ed3c3095e037dcd3f9d0412720b3f9d97adc708c3eb9bcf47590225cb6ba6f`  
		Last Modified: Wed, 09 Apr 2025 17:13:13 GMT  
		Size: 53.8 MB (53822769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ce9a46a9ec8ee7fbc71e51fa69bf5d832c7dce4e42164ef28a81e52dd7c2d`  
		Last Modified: Wed, 09 Apr 2025 17:13:12 GMT  
		Size: 52.8 MB (52830967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108d1d7af6c893d7d17d8f34ab9388aca88083626a7e5ff21d0b7c01d3b4631e`  
		Last Modified: Wed, 09 Apr 2025 17:13:11 GMT  
		Size: 4.5 MB (4514192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e1da3c48eb8f8ac20f94a76775dad76b2496531dfca6a53956b5f6e7ecd0c3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6765585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f88957a35416b95bd4079d130de9b233571b8609a4ba90407e50c4626c4f35f`

```dockerfile
```

-	Layers:
	-	`sha256:ac9efd6ba1594704d730a164aeca7d996607fbc6b99fbc1b7d41ff4094ad42d5`  
		Last Modified: Wed, 09 Apr 2025 17:13:11 GMT  
		Size: 6.7 MB (6749043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b84657ca8e284055d76630e8f07cf3d6fea5dc2d219da4ed3f289cc4e7168b28`  
		Last Modified: Wed, 09 Apr 2025 17:13:11 GMT  
		Size: 16.5 KB (16542 bytes)  
		MIME: application/vnd.in-toto+json
