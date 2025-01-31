## `clojure:lein-2.11.2-bullseye-slim`

```console
$ docker pull clojure@sha256:6890a3c1c05c61863fefe51b13821486cfccf8c9308a05674f0d316b02c9994e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-2.11.2-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7d6d9d84f3928b5f56a9bdd35639f4805cd731ec288c4b57c577a4e66dcae317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235427272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59436aefcce8b91c0ec4949f1f2cb682b1d721d3e2cbb1200b9a03494cc3372`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_ROOT=1
# Wed, 29 Jan 2025 19:11:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82b40830ffc205bba3699afea8ec09e2e1da8ca457c5f68b820c737f3416d60`  
		Last Modified: Fri, 31 Jan 2025 02:18:06 GMT  
		Size: 157.6 MB (157585864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50e42e646c227e2deeff4ba51b98786129eb0d7421cf90da4bd4f5f101009f5`  
		Last Modified: Fri, 31 Jan 2025 02:18:05 GMT  
		Size: 43.1 MB (43074142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceefb4582a49cefaeeae189f61dfb02d756b30d4a638e9932dc52b8bef227805`  
		Last Modified: Fri, 31 Jan 2025 02:18:04 GMT  
		Size: 4.5 MB (4514173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efac3c6f58ecba1097ede308114e7ac2b6523d8c210ed33e44c75253684cf03f`  
		Last Modified: Fri, 31 Jan 2025 02:18:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cd0cc415a5a683f273fb0187b9d64e843d9320b51a44b5f9b8e37502d764a355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa56f2640c1b89ce6f102193e45fbf56fd8a78e36046b1e9915fd304a83c166b`

```dockerfile
```

-	Layers:
	-	`sha256:9d212c7b5657f60ce78879b2239753c2e9d258f5604c2bb8ea7a3574b8a84a8b`  
		Last Modified: Fri, 31 Jan 2025 02:18:04 GMT  
		Size: 4.6 MB (4571933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc5baccd8961f7d7c5901cb4c34cb91a0b6f478ca4f8ad3480b97fb14c0fafba`  
		Last Modified: Fri, 31 Jan 2025 02:18:04 GMT  
		Size: 19.1 KB (19120 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.11.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5b9920f4132c78c9443df9d64a63ad29dcf93735d0d144b31f23f072a1531f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232229838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c008e6460e20e8514a9d22c1eed0d3066e971a547382119921eb497b01fa1a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_ROOT=1
# Wed, 29 Jan 2025 19:11:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc3ea4febeac18700dd0fad07b719e7b913376667b87dc7052c14b9ab784817`  
		Last Modified: Fri, 31 Jan 2025 05:21:51 GMT  
		Size: 155.9 MB (155859332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e46b07332223cbf55a3de0402b0978454fe396d967d7c676624ec15483a5f7`  
		Last Modified: Fri, 31 Jan 2025 05:21:49 GMT  
		Size: 43.1 MB (43111029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e0883d974e287fecc033e62c02e916f372e91d39504c06746c5bfcea2715a8`  
		Last Modified: Fri, 31 Jan 2025 05:21:48 GMT  
		Size: 4.5 MB (4514135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468027e8d5e31f93760a932e8fcd9e604a99936b5f174a48dc219f3580519ea4`  
		Last Modified: Fri, 31 Jan 2025 05:21:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:87e78be16bfab69250fac503a3e9ee82739af451c44ce8941cd3bc9f95742638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4596886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe9fabafae13c0678eea8501d8a83476e624e3f4f117054b3b25672eb5dcfb2`

```dockerfile
```

-	Layers:
	-	`sha256:0bf2606c24af3b99b831fa7cafa4a788ba5eeda76f2f63b3fd664736ee1960ee`  
		Last Modified: Fri, 31 Jan 2025 05:21:48 GMT  
		Size: 4.6 MB (4577621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c922f6d8bd0ca99deacfbe685ee2a1b25233962c94f6a254f46b958054c0001`  
		Last Modified: Fri, 31 Jan 2025 05:21:48 GMT  
		Size: 19.3 KB (19265 bytes)  
		MIME: application/vnd.in-toto+json
