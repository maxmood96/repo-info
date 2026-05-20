## `clojure:temurin-26-lein-bullseye`

```console
$ docker pull clojure@sha256:5d88f9b0205051ed4e5a289097cacdd20f039a526313452e559e26b9d7e2931e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6e6b7a16b556a7e53015e3c5cebf1f3bff17faf21ff85e0e2d5cbd6e10e59747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169440901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa68de3cce39cf535486f7b47ae321f9f970883f4d45e60c9aa3c725468cbad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:02:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:02:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:02:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:02:05 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:02:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:02:05 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:02:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:02:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:02:18 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:02:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:02:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:02:20 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:02:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7759fd3681093a76fe9fbf9997eb2d1d3d002bdd7f1db21395ebb4425de5a9ad`  
		Last Modified: Wed, 20 May 2026 00:02:38 GMT  
		Size: 94.5 MB (94524344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1016d75c856cde5108557e7cbaa8f7adea99bb6769bc2fd79f929fb58c27b32`  
		Last Modified: Wed, 20 May 2026 00:02:36 GMT  
		Size: 16.6 MB (16629535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d8c0f60a1ca218bed40f5dd6e247ca0e443b4d5b56b39144e905605651a121`  
		Last Modified: Wed, 20 May 2026 00:02:36 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1974b286724a2074c2f397e62a8fefbd17588c31c6153aa29037e57032365`  
		Last Modified: Wed, 20 May 2026 00:02:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d90d7f6a101f4fff3874f0d07c09544df6b57046ab5d927f2bfb4c7d6d23861b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4469894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ed9ad98b73172d0cde31a1cd64f17ddf1bc453a5daf8abec9ec394fd6e5b83`

```dockerfile
```

-	Layers:
	-	`sha256:966e887b208b6f47715c2581af9fa9b39da3f76938c7068dd11d4fd4bb377cee`  
		Last Modified: Wed, 20 May 2026 00:02:36 GMT  
		Size: 4.5 MB (4451380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6acfe5e36ffac092acb527650040c0f857de9444a39cffba634ffcbcd07ba74a`  
		Last Modified: Wed, 20 May 2026 00:02:35 GMT  
		Size: 18.5 KB (18514 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:358ac73690ba5798a6f5eb320367476d492bbdfdbe6a4d1e3e0229d95a5006dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166895649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ba21f086a4686ccd64b6cac4b1ff95f881f53d176f42a2f77cc805d3e43d9b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:08:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:08:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:08:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:08:43 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:08:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:08:43 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:08:57 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:08:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:08:57 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:08:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:08:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:08:59 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:08:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d5e2199769bc7c8aaafdcef7768cb51841c656f185577782a7eeeae44bb87f`  
		Last Modified: Wed, 20 May 2026 00:09:18 GMT  
		Size: 93.5 MB (93504373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d508956dfced2af1f3dbe00e2fbfe56294ec292f3d286398baee831aa71ef223`  
		Last Modified: Wed, 20 May 2026 00:09:17 GMT  
		Size: 16.6 MB (16616530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ad835003f2c3ce71c06eb0c870febd1715660ce5a9d0bbf3923046f71f4d35`  
		Last Modified: Wed, 20 May 2026 00:09:17 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a850a682c2a60788bd81dad06796007baecb2a4eb489028f3e5eacbb7d2e1b`  
		Last Modified: Wed, 20 May 2026 00:09:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:83ee6c8d2db2e35c60b93659fa6a72abcd9cbf54c3cf7f8a204b02618af05987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab5ceabf22113a02725bb51531612827c095b0d322db97752750ce885eb43c4`

```dockerfile
```

-	Layers:
	-	`sha256:f27bd22fb9138e354d12967852bc1b81fc292aafe319a9ac4ba6f86aabefae16`  
		Last Modified: Wed, 20 May 2026 00:09:17 GMT  
		Size: 4.5 MB (4450351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a635bf384b938e18a776ea9e483e1dc7305ab4d7cf6b0d115247b7795e1053c5`  
		Last Modified: Wed, 20 May 2026 00:09:16 GMT  
		Size: 18.6 KB (18636 bytes)  
		MIME: application/vnd.in-toto+json
