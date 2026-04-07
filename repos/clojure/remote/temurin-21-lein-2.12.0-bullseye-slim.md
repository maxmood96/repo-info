## `clojure:temurin-21-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:1e99efecfb1cfe56b7e342fa604d0aa718fa53c992f78e40be31e0fd987ae8c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0c3821c0e6085a3e67dcd90eb9a3beaa9d14ccd7d078b5ed1f3a93bd4d053245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (207972140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6bff9930452b2cf5bcede090b5310bdf3bf4343c48dbe829b90c9cac1c141aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:57:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 02:57:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 02:57:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:57:51 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 02:57:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:15:41 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:15:54 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:15:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:15:54 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:15:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:15:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:15:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:15:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db30d2ef0ad2289c1d82855f014bf8c760f3231626d6c7a2f09be579a1db06b`  
		Last Modified: Tue, 07 Apr 2026 02:58:46 GMT  
		Size: 157.9 MB (157857084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d313174c132f4549c403f79c4729fe95ca066df97cbfcd4c453be6a1b5bab71`  
		Last Modified: Tue, 07 Apr 2026 03:16:08 GMT  
		Size: 15.3 MB (15338856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeed57dee1cda8985bd3e301bbb309f3f770afa825d3f6fdd9d8f615f9d2b360`  
		Last Modified: Tue, 07 Apr 2026 03:16:08 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5f69123dbddcf4240db4ad2ea71ba8f3e74aaf9998db209381071ecfd1f628`  
		Last Modified: Tue, 07 Apr 2026 03:16:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0c614bddb389d8bfc5676d95db56d747c718f5d670127e8e46f64890ccfd28a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5344862bca4fde36636bc23f38dee9f974360a577b5fa30d369bd72e47fa75`

```dockerfile
```

-	Layers:
	-	`sha256:164b3c0bccbdca54ff0e9f5a994a5271ea1a5ffe220b7aa1f120c5279c5f15ef`  
		Last Modified: Tue, 07 Apr 2026 03:16:08 GMT  
		Size: 3.0 MB (3029434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79898657e97a364bd534b630bb1797026d6b4e8e5d77e951bd6b630ab63e97c0`  
		Last Modified: Tue, 07 Apr 2026 03:16:08 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d725bbcc6657f38acf720980efe05e9c656f3c79460c9159986887060327960e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204723031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3710feff3b4371c68f13f0eaea664df53c74da3a3596a39781c7a81fd01fc9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:26:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:26:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:26:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:26:37 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:26:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:26:37 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:26:51 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:26:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:26:51 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:26:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:26:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:26:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:26:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4579411e57ee0506e8648d8c5403a219ef2786295a9cfbeea9f042217c7c564`  
		Last Modified: Tue, 07 Apr 2026 03:27:14 GMT  
		Size: 156.1 MB (156133049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2043e4e19b9b76cf2782d3e5ddd21f8aad12228df7097db57bb17e768c344e89`  
		Last Modified: Tue, 07 Apr 2026 03:27:11 GMT  
		Size: 15.3 MB (15327166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab6a8a5e34e39de84d83e00efa17852a6eaabb4d9b7e2e92da39f531e24e2d5`  
		Last Modified: Tue, 07 Apr 2026 03:27:11 GMT  
		Size: 4.5 MB (4517701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372a11b70381ff41e639bd277272238fe50cbb7d601392c924ff8896618ddec2`  
		Last Modified: Tue, 07 Apr 2026 03:27:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c02b1aeab238433ff1bc88f92998d14e8e016de8da8744b0ceee2aaf81ae6570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637c1dec065c55aed3fa6f9ffd47efd632eec71146a918aa7a8c957200eeadc8`

```dockerfile
```

-	Layers:
	-	`sha256:dd57e1dfed0738c5ca5173ee47bdb9353ff4892624157d434b95d1632fda444f`  
		Last Modified: Tue, 07 Apr 2026 03:27:11 GMT  
		Size: 3.0 MB (3029043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417ae6450fc670b83637de1689225ad3bcd83df147e3f3a6a86512e1b1bc0b3f`  
		Last Modified: Tue, 07 Apr 2026 03:27:11 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json
