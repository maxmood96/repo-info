## `clojure:temurin-8-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:b8e6730b68654760c1373e663d6ac624f7a859dc76d344cc1ed119563a6f8874
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bd0c21bdde1b210defdced4b285d2868179ae2516086b9f647b39f7a3dd0a7e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105683739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647f1f9fc5d5e08afeabf2d3261a6038fe363f584ce240e1080cf173295af0a4`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:13:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:13:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:13:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:13:55 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:13:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:13:55 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:14:08 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:14:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:14:08 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:14:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:14:10 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f185b22cd1303114f216c75437e3de345c7f86ec81637302bb1911e6a3bca89`  
		Last Modified: Fri, 08 May 2026 20:14:23 GMT  
		Size: 55.2 MB (55170118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1651c72318f16d903c252a567782ed148aa73b04ba59ff0483fbd974e8770e`  
		Last Modified: Fri, 08 May 2026 20:14:22 GMT  
		Size: 17.8 MB (17759551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b80513468faa197cb66f61a9272cd195ff694251f32234cd1e3997d71981a3`  
		Last Modified: Fri, 08 May 2026 20:14:22 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d2e05af9954edc4131bd7febff1466c3e022e711b2f4f9ac84449a1f0bc7462c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40934c5cc6970810056255de37dc3487f75003665d2195510c4a19d5449d1a05`

```dockerfile
```

-	Layers:
	-	`sha256:7af395f1b6d3fe20a681f7974f49b962b4f292158c3d3137d817bafde559cce3`  
		Last Modified: Fri, 08 May 2026 20:14:22 GMT  
		Size: 2.9 MB (2851039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b96eacd128b1e36f84d14d509c490e9be3ee87f314ab219e94770f906c693f1e`  
		Last Modified: Fri, 08 May 2026 20:14:21 GMT  
		Size: 16.4 KB (16399 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a6c310324cdee97f6951d87a50ed387d042bdea5c1dce007646527a64f29967b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104478538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b15b9a5f606d54df2cbf6eb558e5135b9b42fcbe8667323feb772d1d17259f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:18:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:18:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:18:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:18:14 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:18:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:18:14 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:18:28 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:18:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:18:28 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:18:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:18:30 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d3fc2979e5e360a31f9c76b1ed6dc7fe19f9743a5e50f739a5848268e42445`  
		Last Modified: Fri, 08 May 2026 20:18:44 GMT  
		Size: 54.3 MB (54251615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8004b3aa29d9b4b4cdbe9f2ca8122f4981ebdccb8753584b6c13c1eb07ccb7cc`  
		Last Modified: Fri, 08 May 2026 20:18:43 GMT  
		Size: 17.6 MB (17592998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e687eab3c336512436f3534340a3b684d18dee05dba702c989076d6187e8eb`  
		Last Modified: Fri, 08 May 2026 20:18:43 GMT  
		Size: 4.5 MB (4517728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f32dd62231741fdbe538ff675031ae6d22424f22dbcbf6db846620bb30b011fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d29693e4c000aa2f1fc15dd23eddf0011b35de477dece7975030cba237869da`

```dockerfile
```

-	Layers:
	-	`sha256:1542b0a15869a594868f8892c5e467052f6b1d52136960d4d6730290f29e012e`  
		Last Modified: Fri, 08 May 2026 20:18:43 GMT  
		Size: 2.9 MB (2851354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:801752b790d77b8683ee69a4e2e25715d14a5df54366faa517e1b4175795937e`  
		Last Modified: Fri, 08 May 2026 20:18:42 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:36e6db692ebc59394a36930b14acc426c43744a792c6dc202699624465132189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107207974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78da68283d64934b30eb0c2b360706f8cb5bc8659b5ca07e821be0c4e30312f9`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 08:14:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:14:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:14:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:14:52 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 08:14:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 08:14:52 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:15:28 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 08:15:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 08:15:28 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 08:15:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 08:15:34 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b356cbf5e863ec8292624dee180661bf4ceafce1ae834eda77f2b34cc77d309`  
		Last Modified: Wed, 22 Apr 2026 08:16:00 GMT  
		Size: 52.7 MB (52650390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce5dfbb6aa8b6512299fa3d3ff08e37a9eaa080643afe39840503093391db23`  
		Last Modified: Wed, 22 Apr 2026 08:15:59 GMT  
		Size: 18.0 MB (17961397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fbfc5806cb22e8171c25b2eab3bc97bf6c7dc6e1213103ca51bd8cd7566520`  
		Last Modified: Wed, 22 Apr 2026 08:15:58 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e984581120a16ddfdd80eb52d1bae88006020ecbffd8b6d7f09acf3a34507be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7233909be707725b9c9cb0bf3cf803d3e4a37aed56ceef6ae6f7785891c259be`

```dockerfile
```

-	Layers:
	-	`sha256:33a9f25c489f78321ea46fb51421babca04ccdff41dd880fa5af2fa60334f929`  
		Last Modified: Wed, 22 Apr 2026 08:15:58 GMT  
		Size: 2.9 MB (2853467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70054ac5773d2d0db2e94c6f4b884ef7ec722f1f03e855b33753c695f7834b1a`  
		Last Modified: Wed, 22 Apr 2026 08:15:57 GMT  
		Size: 16.4 KB (16444 bytes)  
		MIME: application/vnd.in-toto+json
