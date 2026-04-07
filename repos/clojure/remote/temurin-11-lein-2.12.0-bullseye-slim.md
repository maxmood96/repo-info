## `clojure:temurin-11-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:2b644bd6716157e671e3d49e31a064a0e89646a7f32eace1b1f2e62eb99dd628
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a85fd1fe967a22557265077180acfd3429a738ff79adb12c34765de87293b58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195921583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4a8eb630e8acf0780074b1eff1c85ae89b34a91ea9f69eb24af297e51c5705`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:58:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 02:58:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 02:58:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:58:44 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 02:58:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:13:22 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:13:35 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:13:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:13:35 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:13:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:13:37 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021150f9fb3c64ec9d05eb82cff69efb46c53664b5fe16cf16e18fde100652a8`  
		Last Modified: Tue, 07 Apr 2026 02:59:28 GMT  
		Size: 145.8 MB (145806958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d0e3c58621f2c182c117dc9876b4c72ec6e53292225cc39ebc598ef260217f`  
		Last Modified: Tue, 07 Apr 2026 03:13:47 GMT  
		Size: 15.3 MB (15338859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d918f075da0f455acc6e97afa7b0a795ebced515b36bb5d23ea731c4999bfd97`  
		Last Modified: Tue, 07 Apr 2026 03:13:47 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a00e31b0fbafd03c508e4f0e50fb2816924602375940caa5a34cfc076c53cbbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3063334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c0568d49fbb16c94596748c53188d44b6c331639761364ab408efaac11c5ea`

```dockerfile
```

-	Layers:
	-	`sha256:eb1bfbb6d8c70718749a0b47b0236e004dfddd48a7b3b004d866c0420ab00bf1`  
		Last Modified: Tue, 07 Apr 2026 03:13:47 GMT  
		Size: 3.0 MB (3047723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d55ac5d26592449725905cc38b13f077e270aa85c55f05c9b08d75a52c5ef7`  
		Last Modified: Tue, 07 Apr 2026 03:13:47 GMT  
		Size: 15.6 KB (15611 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b5d9894d816816c26f746b20dd76be6c36840767dd0381072d8a3ffd6252ebf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191089727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3e6341536f47c5ac3704e6381c9596d474578034b9e41a89ede8612de892da`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:24:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:24:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:24:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:24:18 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:24:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:24:18 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:24:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:24:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:24:32 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:24:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:24:33 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d663882bc53a14eec439225311da003aaddee6d3ebe2061f9cbc4adf8c3cef26`  
		Last Modified: Tue, 07 Apr 2026 03:24:53 GMT  
		Size: 142.5 MB (142500056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c02fd361dfaf14a3a20df8fa3b3d9b5ca14e18ac7c60ca51c65f1e20e8c1f10`  
		Last Modified: Tue, 07 Apr 2026 03:24:51 GMT  
		Size: 15.3 MB (15327222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08979d81ffd05296638939a76c2e61b0aaa7383009bd2159bf39b896b8a68f5`  
		Last Modified: Tue, 07 Apr 2026 03:24:50 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9f67e594dd34d1e0556ca413fb071bf80d0e6ac2d7980efca19610289aeb2ad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a0c9dfa4daa101dd2e05ef6829c6cc2ed68c4a7080f47b956c744d7323afef`

```dockerfile
```

-	Layers:
	-	`sha256:ceea82667180cb3a253714a3c958639f219d7d6cf4aefd1d8db74db33a437ae1`  
		Last Modified: Tue, 07 Apr 2026 03:24:50 GMT  
		Size: 3.0 MB (3047950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e8ecd62b63b91466a3ac3d8c48d0526837d7c8e69d2d1043006a4b1e2b37c79`  
		Last Modified: Tue, 07 Apr 2026 03:24:50 GMT  
		Size: 16.5 KB (16532 bytes)  
		MIME: application/vnd.in-toto+json
