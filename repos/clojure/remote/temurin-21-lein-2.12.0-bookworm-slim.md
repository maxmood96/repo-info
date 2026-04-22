## `clojure:temurin-21-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:a3019099b8efc3cef53b6db314577ece0f4dc51eb70d1c867f81b3879dd6b5e9
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

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:163bf3b7c8fdca1b9cc03742b676f9c8727002d948ad7568b02a7ad2b4486daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208371015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a5323b879fd53ddc301cc62cb615cb2fd989b32738f9b6e5524fa51998751c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:19:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:20 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:19:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:19:20 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:19:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:19:33 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:19:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:19:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:19:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:19:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db037240f6e869a5e70af768a322ef23ba92e76b5e681c0416845741eb15c13`  
		Last Modified: Wed, 22 Apr 2026 02:19:55 GMT  
		Size: 157.9 MB (157857060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b43907fa6aa36c9109b7cc379d9297294e7824efcb7cf36251d86b6ddac57d`  
		Last Modified: Wed, 22 Apr 2026 02:19:52 GMT  
		Size: 17.8 MB (17759560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674cb928edf29daa9fb00c5959f7c5c47cc8186eaccceb7ed9ab911c8ddbd1a1`  
		Last Modified: Wed, 22 Apr 2026 02:19:51 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85f119a6b7547b17c6ffc73d81b2b5a527661adf264dcabbf6a883baa2cb660`  
		Last Modified: Wed, 22 Apr 2026 02:19:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7d695ded365941ce4e0dbf8d8f2e0e81c22dda0012d91dde4a05d105850df691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f855711fc75375f555ec4b004233b82ec9ee45b9e2ae0d7b99a0792e0c5c6f`

```dockerfile
```

-	Layers:
	-	`sha256:0e71edfad8f268b317f83efde38c1b97fced996c432d4a6acb5b5bb9f26a18dd`  
		Last Modified: Wed, 22 Apr 2026 02:19:51 GMT  
		Size: 2.7 MB (2731902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4de559a963061da1c9ecdd290bece18656e0d5ad231c666de13e1cbce3494a41`  
		Last Modified: Wed, 22 Apr 2026 02:19:50 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c04fbbc0334aaefdcb3534023b225ead82f7b3e18b3519c1c3920ce27cb946ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206360359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469d6b8f2bbeaf10d50fad54798d83f52dc4cdee1c3c41c0032781744c91c3af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:22:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:31 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:22:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:22:31 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:44 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:22:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:22:44 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:22:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:22:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e88e34f10e7fe995dc90a8c9f41dc854a055440ba9ed83521b81a795ee73ed`  
		Last Modified: Wed, 22 Apr 2026 02:23:07 GMT  
		Size: 156.1 MB (156133067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe47b317fc9637e80a967e94f038c442e02962358b9d9c468ae4af4d4b8955f2`  
		Last Modified: Wed, 22 Apr 2026 02:23:04 GMT  
		Size: 17.6 MB (17593006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c6d67d519143e177a01e3eec437705cd0d5dd3e4e1b2b99f51ad004d1e86aa`  
		Last Modified: Wed, 22 Apr 2026 02:23:03 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebcd46c3bee577d872a04e222c263a6c9f189a3d2325080cd406a62a8ca3fd8`  
		Last Modified: Wed, 22 Apr 2026 02:23:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b3934c5dd4d8d00a1efcd1d97ab304a0119812b10c6242ca06aba4825fc13e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ce56ded0bba58550decaaa6660fee477c8f1a72f0150748af0024fd0b5ae5f`

```dockerfile
```

-	Layers:
	-	`sha256:64e5a542a4e2052bcae780d50b12ecda86edfade773d985bf94e27b13088d231`  
		Last Modified: Wed, 22 Apr 2026 02:23:03 GMT  
		Size: 2.7 MB (2731517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a0b4fd77e518516a35e625a74f1393f921c8a368878555ba9d1967dd4724ec2`  
		Last Modified: Wed, 22 Apr 2026 02:23:03 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f91f61adf2d0fd5f1e201d84d22f04e8f20b4a0cbfd96b92eb5b1b1af9c59e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212535544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752e8b20acbcd6ca27a28ee4d08c774cd43a3152da86f2e5171edca6036078c6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:58:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:58:33 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 02:58:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 02:58:34 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:59:11 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 02:59:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 02:59:11 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 02:59:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 02:59:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 02:59:15 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 02:59:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e203b9caf09504a0524431e8715aa89e01133d5345e0098d271b086ec7c0ab87`  
		Last Modified: Thu, 16 Apr 2026 02:59:55 GMT  
		Size: 158.0 MB (157977487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43f95a639453ccd66fb5c58feb04e97a5e681d65a18ae7adbda245dcabc8fbd`  
		Last Modified: Thu, 16 Apr 2026 02:59:52 GMT  
		Size: 18.0 MB (17961444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa9044f8970c20a23da30cb1533655da2ff702ba72a59ab0319f89a4359c490`  
		Last Modified: Thu, 16 Apr 2026 02:59:51 GMT  
		Size: 4.5 MB (4517719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6fe0f9fed63e8b92d31ce3a4b82c41db549cbe01ca3a1e983bdf3e2b0c7727`  
		Last Modified: Thu, 16 Apr 2026 02:59:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cea27833f9b0a32d5c23d9f37e6f076fceb895cd4956100741044bbb302f6fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b0e4a1f7dec832c0c5ccf493de71ed44d97c2d122ac0913fc3fbcd6f39d9907`

```dockerfile
```

-	Layers:
	-	`sha256:6674070752644c2a47825163103e9c675f580922ad250f95340204dfb0792e9e`  
		Last Modified: Thu, 16 Apr 2026 02:59:51 GMT  
		Size: 2.7 MB (2733735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02d43db3649b9825ba4de53f1d31d8864a3af3845abdb5e9a00b276060dfe928`  
		Last Modified: Thu, 16 Apr 2026 02:59:51 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d145bcbc15daf4cfd5df36bc048281d74723ec4d29e02b4f241425a761085854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195936924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cafec20c8837832e9b6a85185c8ba051b3997a0a4ac6cc587d299cbbfc57721e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 04:03:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:03:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:03:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:03:03 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 04:03:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 04:03:03 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:03:14 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 04:03:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 04:03:14 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 04:03:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 04:03:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:03:16 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:03:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d069b53a2035ccac2b1dbb1b89e27ab2bf4d9e50e2e3be41b5c021b21dcc2c`  
		Last Modified: Wed, 22 Apr 2026 04:03:43 GMT  
		Size: 147.1 MB (147105212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e169c1789bbf9b36a329125a9df7b300a0af41672240b35aac2e82ed81cd832`  
		Last Modified: Wed, 22 Apr 2026 04:03:40 GMT  
		Size: 17.4 MB (17422000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9a2cd4afb72d95caf0e41199132b3eb809580e44aeafc6afe86ef68e285fc2`  
		Last Modified: Wed, 22 Apr 2026 04:03:40 GMT  
		Size: 4.5 MB (4517721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64c9298be84b3eff4fe2cce8f8130cd953139756333cb02f4cffa7c4bc3d199`  
		Last Modified: Wed, 22 Apr 2026 04:03:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:230010fd5718ef1da5efa4ad3510cd9ede9649c1919f0429aa68097bd42c56e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc36d16bc7d8710c85ef1145e7a47a115b3dd353db88432cf57aee902de8777`

```dockerfile
```

-	Layers:
	-	`sha256:51802f1197dd18542d2a6df3adc71cce05fe56c28127189e3512e22f4b94b4e3`  
		Last Modified: Wed, 22 Apr 2026 04:03:40 GMT  
		Size: 2.7 MB (2723716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93c0919112734b195eb110cbf14a0013a63ba0dff97914d7883d6e0b22c5653e`  
		Last Modified: Wed, 22 Apr 2026 04:03:40 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json
