## `clojure:temurin-24-lein-2.12.0`

```console
$ docker pull clojure@sha256:5401149338e45f24c2c02c2eb082b2ca7e2e96a29871db05800c6590aa7d4034
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-lein-2.12.0` - linux; amd64

```console
$ docker pull clojure@sha256:a335232bda33f988f2692b1c3fac76ebfa9ba93b0f5dd95293c66eec392ae5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162773901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d38d4a479c0b54726cdb3403ffcad8d42d66a23c9356310fd82db38dea4ce7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e270b91fc58d47e2bfbc5e8671ca695eb69147e8bcd0a0a55cbd165f48ebd768`  
		Last Modified: Sat, 13 Sep 2025 00:10:59 GMT  
		Size: 90.0 MB (89975233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2622de2a2f6bdd133e358970b6c0b3862fff98b25293e54389e96c9ceb9841`  
		Last Modified: Sat, 13 Sep 2025 00:10:50 GMT  
		Size: 19.8 MB (19799915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199d7aabd6111dc4a894b4ac0d20198f493569f9e3e702a0cc25d15e3380e96d`  
		Last Modified: Sat, 13 Sep 2025 00:10:50 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cbc99ec2164484189674774293a7a33720138c1f31174a1e89e156e7ecb3f8`  
		Last Modified: Sat, 13 Sep 2025 00:10:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:68a15f8c449e256b7991259807313b0e2e4c6b5dec280f2f6c3e6fde67e0781f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8631efd745b77731a890ffb3dfc5894ed6b404de72259fad43127b01181e38d6`

```dockerfile
```

-	Layers:
	-	`sha256:102b466f5c76348e741c47e0ee80de9bf2c514d107be938d46e3297902378b06`  
		Last Modified: Sat, 13 Sep 2025 00:41:52 GMT  
		Size: 4.2 MB (4231132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3f621d99bc2b59ea44220f06baeee65f0fe2518caf20a1653ac511fd43a66db`  
		Last Modified: Sat, 13 Sep 2025 00:41:53 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.12.0` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:864aeebfb1628ccfaef27a4c2653f88c365a8898c3914d75713c26c64a8c865e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.3 MB (204305810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43e617a93ff52f51f39800f5eaf67a20e8ec91becb2a1d61038c99777fe33f4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 17:48:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 17:48:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 17:48:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 17:48:33 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 17:48:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 17:48:33 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 17:48:33 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 17:48:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 17:48:33 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 17:48:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 17:48:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 17:48:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 17:48:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97557ab76eb32a92f78923623c8d42db0317fd0fad7d2aacc1d0aff975d94f23`  
		Last Modified: Fri, 12 Sep 2025 23:44:33 GMT  
		Size: 89.1 MB (89092530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc37f4f0fca8702e8f99d8740caad2c28478ffec3709cd10d7c8959ab413440`  
		Last Modified: Fri, 12 Sep 2025 23:44:41 GMT  
		Size: 62.3 MB (62339675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce8902f1db76481b42dabdf33bfc6e3e3d6eda4c46390be8b21a7e0dbfc3923`  
		Last Modified: Fri, 12 Sep 2025 23:44:30 GMT  
		Size: 4.5 MB (4514157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47dbfbe46d8ae971c1ad4878da2807bd95e836a06a5e7c53f54c64333c879ba`  
		Last Modified: Fri, 12 Sep 2025 23:44:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:3daaedb1f208df38da1a77512489d3d6713ded9d0018a35d4f8b327af949cb19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c54611793b1b559a6c0419542f9752a44ee35b54a8a6f9b61f330296c40403`

```dockerfile
```

-	Layers:
	-	`sha256:34c3f737ab212005a5cd53c08c1a3777422929d57b08da107df76fcf3405fe7a`  
		Last Modified: Sat, 13 Sep 2025 00:41:58 GMT  
		Size: 6.7 MB (6665749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f37df2dee5a23e9f61c45248e2938e6c630eff6bf5d2c1922a1ca40d1030068`  
		Last Modified: Sat, 13 Sep 2025 00:41:59 GMT  
		Size: 19.2 KB (19211 bytes)  
		MIME: application/vnd.in-toto+json
