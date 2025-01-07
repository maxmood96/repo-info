## `clojure:temurin-17-lein-bullseye`

```console
$ docker pull clojure@sha256:36ad550c6aae7260055a65a3c4ff412fa6a6a83452014e9d642af32d7ef0058d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8cf45d2530a0a5b6a008d114a4229a12338463b9703cc0a05deec4711b0f48d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255368842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf44624a2710af87491fe0b3aa80d953fcd7081bda78150eca4bc7c7f70764c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_ROOT=1
# Thu, 03 Oct 2024 17:49:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a88f3772504022bd259bbaae2b8fff9d49e07ae76cd84d2aa85296972ca01a`  
		Size: 144.5 MB (144536665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e444af464df737fa78497fa5845764025b29fdecaa295b58ed322d9bd76782d`  
		Last Modified: Tue, 24 Dec 2024 22:38:11 GMT  
		Size: 52.6 MB (52578644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1f113722dc956c20585c8bb5007306b02a3b5a7c27e71e901d55f8bc5f9737`  
		Last Modified: Tue, 24 Dec 2024 22:38:10 GMT  
		Size: 4.5 MB (4514150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e5f4c9c0e7a76c6c972c7a87de0394aa59931713839dd70abda9b8bc253d5f`  
		Last Modified: Tue, 24 Dec 2024 22:38:10 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3affa038f60ae60fc6bb1ee293add30583da47a1fdc5b1ff60d806c1f3428e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6638181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2aaf6d42cca5749bf28e6a45145289324831fd55c95dc4a7bad823369c7220`

```dockerfile
```

-	Layers:
	-	`sha256:6efa3fadb5ea6076d0e1a7064225c5c595404232aab340c5e823912be0ba85d8`  
		Last Modified: Tue, 24 Dec 2024 22:38:10 GMT  
		Size: 6.6 MB (6619758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0882613d262c37d27104857115e410401c7f8052e23c272de6c551c04be524e9`  
		Last Modified: Tue, 24 Dec 2024 22:38:10 GMT  
		Size: 18.4 KB (18423 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2745440c4b648ac7ba829b2be8b176ade63bb054278b0754ae210e6ea0985820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252745840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5205fa8d4661cc02f5e22be9af94768676479ee3a928fbc26c84f4ab0fd0a4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_ROOT=1
# Thu, 03 Oct 2024 17:49:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dce462c22105422e138f6d754df187041f54e682066c38e939203fda7d53c73`  
		Last Modified: Wed, 25 Dec 2024 07:26:24 GMT  
		Size: 143.4 MB (143360983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ccccefc785caea146fbe086146c74904c669f070311b05d4778ac72b7d00b4`  
		Last Modified: Wed, 25 Dec 2024 07:26:22 GMT  
		Size: 52.6 MB (52624539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363a6c50c6200026a2c651b1c40baa2d86c42dccf9f57c0175d87b701a52f8e8`  
		Last Modified: Wed, 25 Dec 2024 07:26:21 GMT  
		Size: 4.5 MB (4514192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb814b4e611e77a44b436ee1934f10d21cc7c6e84fdd64305256c9a8d4fbfecc`  
		Last Modified: Wed, 25 Dec 2024 07:26:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c02a0325433d64a0e9f80c2dfb2bb4a539c732d2d36b28642ca0a54984026c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6643333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5044d619b0e8763bc47b3ecb4dc246e60216c9a74f1e93314f1be08a91d0467a`

```dockerfile
```

-	Layers:
	-	`sha256:70e5ab7f45ce02f60eec67b676a4ae230c25024c51d0b22ae78d18d167b20b3a`  
		Size: 6.6 MB (6624789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03d79a2f22d59e29998ebc7c1f08aeb54760885e9db3cb6c72ffc694c34b1067`  
		Last Modified: Wed, 25 Dec 2024 07:26:20 GMT  
		Size: 18.5 KB (18544 bytes)  
		MIME: application/vnd.in-toto+json
