## `clojure:temurin-23-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:096eb2b04cd8ceac872064465384a62300e54ceb9486f41990af1557d01cc096
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:898aaf112c831bfcd918e449a0f3b966d9814a0a3acad63464f97812e163d569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243126468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626b20a71ab3b2ba5da5d98963ef73b822afe6bf800e6b1cd66c2f382b7bae32`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_ROOT=1
# Mon, 06 Jan 2025 23:07:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 20:33:08 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1799f531d1754254c28415983f365261135c4386cc429966d6f46712808965b`  
		Last Modified: Tue, 14 Jan 2025 02:45:20 GMT  
		Size: 165.3 MB (165295091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4077a3fb06d9726d1c6ac4ba10430216250a7d5d1e7a3084022fabfd039b5b78`  
		Last Modified: Tue, 14 Jan 2025 02:45:17 GMT  
		Size: 43.1 MB (43064148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad1f140885d79bd078f66ca8c7d9b2273d3d0039db57ecf024fa6f62d4d8018`  
		Last Modified: Tue, 14 Jan 2025 02:45:16 GMT  
		Size: 4.5 MB (4514137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ce413a5fa3832ae5ff7cb27e3b4c315db9ec31712ea6d9f6364bf9b53ee368`  
		Last Modified: Tue, 14 Jan 2025 02:45:16 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5203f761476fbae8c0d968f22ad02d491117ab288ed318613334738f4deef712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d89ca2a1e95d4f75cb0095bba2d32b360d7f798dbc064e1d00faa8939b6baf88`

```dockerfile
```

-	Layers:
	-	`sha256:ba38a61de1fb9dcbe0257ab657552f712202e1c5665351a027ad2a848dc20865`  
		Last Modified: Tue, 14 Jan 2025 02:45:17 GMT  
		Size: 4.6 MB (4573176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb5d357cdb56fc3ed4f32a7631b157155848a2cba765f8b3570041fbbc2a60b`  
		Last Modified: Tue, 14 Jan 2025 02:45:16 GMT  
		Size: 18.5 KB (18457 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bfaabe35343bd3f30a43024985b232e5e2f30acf99e6df2c7e079791cbb88156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239651545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d05d2922c62df041333f80d5d391d13999d8f64403067ed05a4e885dc2c9bcf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_ROOT=1
# Mon, 06 Jan 2025 23:07:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e206b6fd86d16b339586be06a284d97aa652cd2602791ae8ae2346212f045696`  
		Last Modified: Tue, 14 Jan 2025 12:41:46 GMT  
		Size: 163.3 MB (163281785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac1b7463f708c4d8a57142b4c90d95bbc0575c2307e189cef3a95ba671e66a6`  
		Last Modified: Tue, 14 Jan 2025 12:41:44 GMT  
		Size: 43.1 MB (43110233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3e18bfa901ce59e0087015027b5cd51c3c2c2449d61f363202a9d22521695a`  
		Last Modified: Tue, 14 Jan 2025 12:41:43 GMT  
		Size: 4.5 MB (4514187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ada01fdcadc30d02f0dc562fea08382014bc7a7c04b0220de773bcfaa00cfe`  
		Last Modified: Tue, 14 Jan 2025 12:41:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:985ddbe9af8fd45974b6500422a7af2bcf1bd7daa57f4abb47cf752b002d2006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4596797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09fa2baa3560870bca4e8cd6ef7b21644dd504c552b07cea6bf4f6dccaf323f1`

```dockerfile
```

-	Layers:
	-	`sha256:7aa80b52c865ea78d753f63eee950259513e3b77e2c39550593acad54c254e68`  
		Last Modified: Tue, 14 Jan 2025 12:41:43 GMT  
		Size: 4.6 MB (4578219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04d63dd905b47cb6a2472271ff15f32306ba725e969abb5f4ac2657435d8d219`  
		Last Modified: Tue, 14 Jan 2025 12:41:42 GMT  
		Size: 18.6 KB (18578 bytes)  
		MIME: application/vnd.in-toto+json
