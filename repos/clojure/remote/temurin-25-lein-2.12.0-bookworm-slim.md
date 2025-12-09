## `clojure:temurin-25-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:4cb8f979e6a0a087918e873be23fb1fa3a93f19c7aae9a659e7cc01791cbf696
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

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:694602fb8dd75059d4620351629675a51036404192f85779171b7b18994f33d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142549968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1763681f9a801dfed3e3ccdd73b1863046584d81b406b931d130e78e51d684`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:56:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:56:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:56:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:56:13 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:56:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:56:13 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:56:26 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:56:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:56:26 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:56:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:56:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:56:28 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:56:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7286ef26c0552096dc49aa4e990a34f20dbb1c4584b6ba14297403d7159046`  
		Last Modified: Mon, 08 Dec 2025 23:56:59 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f19f14c7f848abdbac107d0af5452166e8e77e1dc3e33ba2e2b562b30f419a8`  
		Last Modified: Mon, 08 Dec 2025 23:56:54 GMT  
		Size: 17.8 MB (17758068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4db8170e549ca29cf435163baa577069fadd54f3937c73bb5e362f82b41be54`  
		Last Modified: Mon, 08 Dec 2025 23:56:52 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0423f90ee118140bb76a45cceafb3243870832d9f911f5c02511ed1f40b5a59`  
		Last Modified: Mon, 08 Dec 2025 23:56:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:902bc6652d711c7a09892c25166be608fae749acc44f305cba36cfa9c7521bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c65eb4a4029d36e3f1e6dc89a1d273e449cb889d2bd3c514c83e29329379fb5`

```dockerfile
```

-	Layers:
	-	`sha256:15ef90ffee69161159492e177c5618cb91315ed88c2875e348292eb1707d703f`  
		Last Modified: Tue, 09 Dec 2025 04:35:01 GMT  
		Size: 2.7 MB (2680112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c86fca0a4ce966b42aca1cf341e6c6531d43659adf2e36457db36b56cf780506`  
		Last Modified: Tue, 09 Dec 2025 04:35:06 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3ceddbff278d5f25a469cd981967e3a6c3442bfb187023c3bcaa5cbf350349eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141263975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818d6c8f02330b0674538c37b1f36875d1296ed7320fbb6cbaeee43631f9995d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:03:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:03:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:03:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:03:00 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 00:03:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 00:03:00 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:03:14 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 00:03:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 00:03:14 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 00:03:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 00:03:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:03:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:03:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fcc13ba01dbcaa7b7c5aee49e7030beb0764a0c5165bfa63136047ad0b55a8`  
		Last Modified: Tue, 09 Dec 2025 00:03:48 GMT  
		Size: 91.1 MB (91052516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfdd19813b993dd4ce408cdffc75485ca28895251ae82d27346def071c5e1c9`  
		Last Modified: Tue, 09 Dec 2025 00:03:41 GMT  
		Size: 17.6 MB (17591093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088c4af405b372f27baa9797d69e4e661ef5ba865774828ba232e7f666511090`  
		Last Modified: Tue, 09 Dec 2025 00:03:41 GMT  
		Size: 4.5 MB (4517708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff6e6cd7b6c83fe38a768972059874947a73bf9dc901dfed2cfbb31d6f126ab`  
		Last Modified: Tue, 09 Dec 2025 00:03:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bc34a7d348bb2dc9a6f3f65de5b02e6c28840e564656e76da37bb2aa29476bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3853b8760c79abafd15ee47cedd03bb6589d3a85265db711701a747a6bc48d0b`

```dockerfile
```

-	Layers:
	-	`sha256:09579819e823ba94a56070fd21f9ef30626f14f392de167df62dac0f92311178`  
		Last Modified: Tue, 09 Dec 2025 04:35:09 GMT  
		Size: 2.7 MB (2679748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dbc2cd8b2d7deddac003ca751bba0c5d33f7b112603b31c2e868e2e12d3a5ef`  
		Last Modified: Tue, 09 Dec 2025 04:35:10 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:dce23870731a6102c49c80734eb0ea1c11b96ac7e94804322f1ce6749d9591e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146157453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae9c4e306197896a0de905337ce063cea24bfd41a38fc64b1ca049f4ae2b400`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:24:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 16:24:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 16:24:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 16:24:10 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 16:24:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 16:24:11 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 16:24:46 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 16:24:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 16:24:46 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 16:24:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 16:24:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 16:24:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 16:24:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d34f3bc4e2e28ed95aba8ec4d91b1f2ea595dcea02126d32ce2f47b884268f0`  
		Last Modified: Tue, 09 Dec 2025 16:25:49 GMT  
		Size: 91.6 MB (91610770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a82c6c4f4e3833d77632d179dc4255834b491270ee2a5428fe95600050ddcab`  
		Last Modified: Tue, 09 Dec 2025 16:25:42 GMT  
		Size: 18.0 MB (17959666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0024e8898832e691d159dabfe69808c4d9c4e7725f2ea139969817bf7a339d1`  
		Last Modified: Tue, 09 Dec 2025 16:25:47 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b95cfb59aab3937a0555a525d4adf0b5fc51a04381ddb720a0855b175b271b`  
		Last Modified: Tue, 09 Dec 2025 16:25:40 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0a6190e6d90309b3d299effd6b8576665da1b98b6772a6cda58b4881943f1443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2702369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac37fc2ff4eb4f56d487542e462429a09a337d06a94ed460380a8aa22059cf39`

```dockerfile
```

-	Layers:
	-	`sha256:1b8ce66a9ef4a810b522596bca61d36e962998db3e250f8155d86a631208a9fc`  
		Last Modified: Tue, 09 Dec 2025 19:34:33 GMT  
		Size: 2.7 MB (2683255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:300c43d5e2a4d330160f228ac75350398ce8e792fb13471967661ac79f1d0bee`  
		Last Modified: Tue, 09 Dec 2025 19:34:34 GMT  
		Size: 19.1 KB (19114 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:41397a28921f93c160f82467f58ee94ff6d1732e4000a1425d23dd1e99bdf0a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137033142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa16bf15127707cad687f4c4f00e618c672af799ac74a12d0d051c6fec79b173`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:33:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:33:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:33:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:33:07 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 01:33:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 01:33:07 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:33:17 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 01:33:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 01:33:17 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 01:33:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 01:33:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:33:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:33:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709c0e13614b718d0c3c4ac64648d2daf3ff575c31cced0f8f9a4e0d7b37e36`  
		Last Modified: Tue, 09 Dec 2025 01:33:55 GMT  
		Size: 88.2 MB (88210730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ff1b438f40420e10369d7d8eb5336858bfba313084d73916debed2036a21bb`  
		Last Modified: Tue, 09 Dec 2025 01:33:51 GMT  
		Size: 17.4 MB (17419802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736e70b00b13a5877ae9a7ba67c6f591e104b877f9ec0e1f67b48795cc2fff5b`  
		Last Modified: Tue, 09 Dec 2025 01:33:50 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a348e0e52528808032377891c12a37282d5b174d8c0cfc2d50734d9715f7ed5a`  
		Last Modified: Tue, 09 Dec 2025 01:33:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:04586db4ebd6ce0e8c6121fea6d2dc35b56712e5b9bb00eab4481c572d1c925b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09711d0f7df8ecbceae3f388a0bb3921307089a26a01212c33105858b25b1b09`

```dockerfile
```

-	Layers:
	-	`sha256:009a72629227745fb8d6ccfe89a33857aa40c916e9cea9dc6ebbc851edcc7ab1`  
		Last Modified: Tue, 09 Dec 2025 04:35:17 GMT  
		Size: 2.7 MB (2674474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df5d14e170916758c296210e438145157322f0f55018b571f8af65ef80388e95`  
		Last Modified: Tue, 09 Dec 2025 04:35:18 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json
