## `clojure:temurin-21-lein-bullseye`

```console
$ docker pull clojure@sha256:c569ada25ec983fbb7b2c4f8b0135f2f10fd1947471990250919dcde3dc305d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:de73398d33a88ca210a6f348d1b0dfc6e86d320729642924b6c1c3940ab4ff2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233083510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6962f7ac00f916bdfda5500ac710ce00fde08da5bfa858c36a11bb046aaf83f8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:59:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:59:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:59:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:59:34 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:59:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:59:34 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:59:47 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 19 May 2026 23:59:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 May 2026 23:59:47 GMT
ENV LEIN_ROOT=1
# Tue, 19 May 2026 23:59:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 19 May 2026 23:59:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 19 May 2026 23:59:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 May 2026 23:59:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96eaa80252e9649b67c656ddffbfd6413a661b44f1023ffe8e48082a3ae15a8c`  
		Last Modified: Wed, 20 May 2026 00:00:18 GMT  
		Size: 158.2 MB (158166966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7cad7c0e6d6d931b4f759f9de1d2eeb28947531f4110602bf74d428f0b069c`  
		Last Modified: Wed, 20 May 2026 00:00:12 GMT  
		Size: 16.6 MB (16629543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ad89e7ef4679163fb70671e43dcd0b72ff180409f00893cf33fa35dda6efce`  
		Last Modified: Wed, 20 May 2026 00:00:13 GMT  
		Size: 4.5 MB (4517721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3cc0eff838feddd1e42d2ffbac7f25f93be3773e4bc5c87f3535adb3efa8a0`  
		Last Modified: Wed, 20 May 2026 00:00:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:26d826d394d8d20cba6a76fdabf01e9bb6724b42825b56481336d2931d4835b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b65ec46532fb0dacfa464bc85c7699467e840eb57b8959c8f2167c3c719e9a5`

```dockerfile
```

-	Layers:
	-	`sha256:dfa6efadba914ae263694101178848d1c7719665809e8ce400b18aa1dd3b9c37`  
		Last Modified: Wed, 20 May 2026 00:00:15 GMT  
		Size: 4.5 MB (4488341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce11507a293be9bfc811ca76a0950ee3f532908541b84b9b1f5c6dcd97853448`  
		Last Modified: Wed, 20 May 2026 00:00:12 GMT  
		Size: 18.5 KB (18522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6eb4ca850f1ede0b379baeb1c24d8f814c818eaf7a5e0da636d819fad31f4ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229852582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7207155e5d7152b00e1e1a84d2f3a082a74db0e710bd1824f2cd6f5b43db5c0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:06:39 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:06:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:06:39 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:06:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:06:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:06:53 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:06:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:06:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:06:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:06:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb384d7378c07c18b5a630fce8072a2313163f8224ffa54520dba12f3099d33`  
		Last Modified: Wed, 20 May 2026 00:07:17 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237e82ef12412b7ef434b671c8d30e73da20e4788dc0253fb7e88cd836b91384`  
		Last Modified: Wed, 20 May 2026 00:07:14 GMT  
		Size: 16.6 MB (16616523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6520dbcdc130db5dd6ae660bcdeba29184a546c7057a82ebb4bacf4d5b012`  
		Last Modified: Wed, 20 May 2026 00:07:13 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f58139bd668e0260947f0cc52fc018e94eba082ccc770fffe2f479213a12f5b`  
		Last Modified: Wed, 20 May 2026 00:07:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bb7a3dd127ceda26ff2b011ec46b7835154dfcfcc1bfd3183593d7a58b0ce77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4505957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5849539b8c6b5ac71952f539f572b5dae8577edc12d899372efc06c47cf65ef`

```dockerfile
```

-	Layers:
	-	`sha256:a762670b64e68683fe3e927e500d19bbfeb884177b9e867c0622ca0aa3b21c08`  
		Last Modified: Wed, 20 May 2026 00:07:13 GMT  
		Size: 4.5 MB (4487315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e33f813a6137f719e87a7b7a6e70406a87f0f697d2fbe465d529553045c4b3ab`  
		Last Modified: Wed, 20 May 2026 00:07:13 GMT  
		Size: 18.6 KB (18642 bytes)  
		MIME: application/vnd.in-toto+json
