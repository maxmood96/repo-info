## `clojure:lein-2.11.2-bullseye`

```console
$ docker pull clojure@sha256:6462ca451ba3df64db9e032dafe91683527c9ab1cc72a6883c224f5080d74bfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-2.11.2-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c27de3d3a5b9e8f182f4a03d7e44512ef7e3f8aa88f1127ca0a023f67d576530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268688193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24c6f175c0f5ddb527fe5e495c1f250c5d7031a78917eb6a3888019245ce899`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_ROOT=1
# Mon, 28 Apr 2025 17:24:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887e98ed3dd60314734e51c5e91d4de59f7458b1e1a237319b937380d15283c5`  
		Last Modified: Mon, 28 Apr 2025 22:08:01 GMT  
		Size: 157.6 MB (157634520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c10e05b4aa5ea5902739e0b009693de8c8b7890ead0937096614dafd374b79e`  
		Last Modified: Mon, 28 Apr 2025 22:07:59 GMT  
		Size: 52.8 MB (52791341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3f8b513602d03fa579499aab28f511fc283ba8c9d3ab2fd5450175ebe2c3f0`  
		Last Modified: Mon, 28 Apr 2025 22:07:59 GMT  
		Size: 4.5 MB (4514164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3c201fd699c1fb6d4d02e73192bcc715cae0e3398c4040f45590818d17b726`  
		Last Modified: Mon, 28 Apr 2025 22:07:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8eed6a215767c0c317f2d45a40951e2c2b8e7d310a0e9e3dbc73eb372b9160df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6506224e5e05d9520dd661d96d4e24b957bbc82ed0ed0b512adddbdd607c8b`

```dockerfile
```

-	Layers:
	-	`sha256:ec99810126d3f555591d8b802c8c94cf3bbfc90a3dbfe22dfc4780010daf6404`  
		Last Modified: Mon, 28 Apr 2025 22:07:59 GMT  
		Size: 6.6 MB (6625500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207d0e00851edc41608045108ea985edbb60e73952c366cb78c7a5c300877808`  
		Last Modified: Mon, 28 Apr 2025 22:07:59 GMT  
		Size: 19.1 KB (19065 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:df94f44d8435a7fc9780e1b19297d522cf92973342aae89968bd09ca8f4ea4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265520565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5977ab305563eba771a9df9ba9f4867f7b4e8d503412da9deb5e1ab660bf7ab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_ROOT=1
# Mon, 28 Apr 2025 17:24:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c157ab8eb81c07fbfae63cd9fe879f3c276295291ce0524b491f7a359eb662`  
		Last Modified: Wed, 30 Apr 2025 01:46:35 GMT  
		Size: 155.9 MB (155928834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e40bd2f922450240406f703adf623e4b28f1dad501bb279ce1a9580b1c9535`  
		Last Modified: Wed, 30 Apr 2025 04:48:34 GMT  
		Size: 52.8 MB (52831179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa073ba513f0b4594285df0739cc8343a237a3f3017c567849a3b5e3e37bf81b`  
		Last Modified: Wed, 30 Apr 2025 04:48:33 GMT  
		Size: 4.5 MB (4514144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df01e608b57ca57c2584a12377fe3d00860d970728717e026de4db0dce56c154`  
		Last Modified: Wed, 30 Apr 2025 04:48:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d11266f566d72faa3519629fa588ff122d629499184ff46a0779295a4ace2b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6649765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1b3f00ca74337899d53b42f7af4e81debf834782baa93196a0a5be89a3d6d7`

```dockerfile
```

-	Layers:
	-	`sha256:031e066aeb7b6ad60535eda80b6e3920293ac4efda9c866b0719bfa560e93afe`  
		Last Modified: Wed, 30 Apr 2025 04:48:33 GMT  
		Size: 6.6 MB (6630555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80145761e414b52e8b12d978b97054c059a3dbd35c1f0796492ebaa1420d553b`  
		Last Modified: Wed, 30 Apr 2025 04:48:32 GMT  
		Size: 19.2 KB (19210 bytes)  
		MIME: application/vnd.in-toto+json
