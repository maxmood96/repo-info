## `clojure:temurin-17-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:4a82294a2141e038170568e588cd4106cf41d5930e1c331f760c334007d66e44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:cf64656ee665910bfbbc2ee75306884ac1c98a80c2cba833fcddd12d20fb4ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220821963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770aca5348d471403032cb99c35e2919e0039d27d3ae1eb599c84e5925b27769`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:58:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:58:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:58:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:58:25 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:58:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:58:25 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:58:38 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 19 May 2026 23:58:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 May 2026 23:58:38 GMT
ENV LEIN_ROOT=1
# Tue, 19 May 2026 23:58:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 19 May 2026 23:58:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 19 May 2026 23:58:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 May 2026 23:58:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069817fd8fc4c30c5d6101f41cb2922c0605cdbb201f895b518140f14dde517a`  
		Last Modified: Tue, 19 May 2026 23:58:58 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89833918124a959ac79f5aa8c9a140189304e2401e965e5590cefef7be4dcaef`  
		Last Modified: Tue, 19 May 2026 23:58:55 GMT  
		Size: 16.6 MB (16629501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07367d3cb46d44ce492e6f173ca79db11fc558e2eb5c82abf660818d077395d5`  
		Last Modified: Tue, 19 May 2026 23:58:55 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4beee356dc6ddefc4c82badd57f97268aa638f7c3c30c78c915cadcaa73f17f3`  
		Last Modified: Tue, 19 May 2026 23:58:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b7945aef2d9e1a7c37da2df5c6b2d5f6ad79e866e0c3a03aae4f2a7caa113108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4505010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2b9bf49e221cff91da73020cdf94a5211c97ce6f05d4eaacc370f435bae5b0`

```dockerfile
```

-	Layers:
	-	`sha256:820cbd597323e72d72b82b9447091d5e3df0bebba21b7495f338c2de15f8133d`  
		Last Modified: Tue, 19 May 2026 23:58:55 GMT  
		Size: 4.5 MB (4486489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22a3871cade766d48d2bf8de73e1ef227d1eea56703753f3f3102960a3ea18e3`  
		Last Modified: Tue, 19 May 2026 23:58:54 GMT  
		Size: 18.5 KB (18521 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:13ffe627311a6c061f463be2f6ca3d4eec0316802e45de26cd4df1f5033aa10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218115660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6de43e42f7b531f56b52fdb92f89cdb148bf6d62d0449a966f57b396ae0b955`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:05:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:05:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:05:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:05:29 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:05:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:05:29 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:05:42 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:05:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:05:42 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:05:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:05:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:05:43 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:05:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e4c1d83c81bbebe27d7812f3dfec1f53ba191406e982bbfee3c0779d3f9e88`  
		Last Modified: Wed, 20 May 2026 00:06:04 GMT  
		Size: 144.7 MB (144724360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba862f94a8dd90b1cdabed581c569a9655ce700bc210cc9c20519457cce4474`  
		Last Modified: Wed, 20 May 2026 00:06:01 GMT  
		Size: 16.6 MB (16616579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfe55d7da6107a459c122519bd946420f3b31f11e75b25c2b89f92da17700ce`  
		Last Modified: Wed, 20 May 2026 00:06:00 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38dade414b2e21e98db623214f8729e67a1ba5ab6059447be8f6a7011b3432cb`  
		Last Modified: Wed, 20 May 2026 00:06:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ab951bb27b3fa1965d6f23dd739305a35ab3163cd21b0ebfabe1faf757abf0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4504106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764d4aad1266dd4b037111d4c221a4cfd9f9fcf49e331499ef9cdd5e6849e17c`

```dockerfile
```

-	Layers:
	-	`sha256:83431bf368b2bdfad96d4f80dd3a4bf6e0fb30716ebc071092eb491dab0b3c28`  
		Last Modified: Wed, 20 May 2026 00:06:00 GMT  
		Size: 4.5 MB (4485463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:453fb50c4f8797bfd9decb869b28cbe746fc0de36386ffc776a46868c36810c2`  
		Last Modified: Wed, 20 May 2026 00:06:00 GMT  
		Size: 18.6 KB (18643 bytes)  
		MIME: application/vnd.in-toto+json
