## `clojure:lein-bullseye-slim`

```console
$ docker pull clojure@sha256:c272e70f912c5543761a4074413ae9dea98c5fcd3a2dd0828567951418fa0397
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d87460c2dc2e510738124beabfae0a5cfdc4e726a44fbbac9c592f2001ebc5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (142981665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e93abc84a2f72d3f8f22dcbcc9dfa22ec124a0dc8db6c18a5d47c67d6ec547`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Tue, 16 Jun 2026 23:37:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:37:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:37:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:37:38 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:37:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:37:38 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:38:48 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:38:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:38:48 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:38:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:38:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:38:50 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:38:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dac36b25fcfb79e24fbda30ff451f95d246c3760d230585cf8697f79365e2e3`  
		Last Modified: Tue, 16 Jun 2026 23:39:08 GMT  
		Size: 92.6 MB (92574585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ed72b588caef4e458f593ecf540efd342178bd28ea97a9257e57a6b220f5fc`  
		Last Modified: Tue, 16 Jun 2026 23:39:06 GMT  
		Size: 15.6 MB (15631222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d13e72de99170232b8073332e0103560a9121b724f25c468cf00972eec7aad`  
		Last Modified: Tue, 16 Jun 2026 23:39:05 GMT  
		Size: 4.5 MB (4515173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46338f7da3933e04cba45e8a6a5b649b78fad82503ce87baa7c2097afaa90f0`  
		Last Modified: Tue, 16 Jun 2026 23:39:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4aa9663dfe9c2895d4a92b08f2357ab603be8159b5b8ee0bfcd6748ffb287113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3025220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbeab5e855fc438688b98b4c902e9725cfd4e83897ccd8cdc36fde9b2562502`

```dockerfile
```

-	Layers:
	-	`sha256:43fbed6f23b6f9a2136ff1b70c2ced7222c8758fd5df4a7583f192aca2262b58`  
		Last Modified: Tue, 16 Jun 2026 23:39:05 GMT  
		Size: 3.0 MB (3006792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190021ddad41fc9f3bd2909a3be85aec90c80cf307549f1d4371f8b7bd0fb591`  
		Last Modified: Tue, 16 Jun 2026 23:39:05 GMT  
		Size: 18.4 KB (18428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a59a004529486ee3fc32ac612cf6094787b764a2ece81c4fdd70be08dfcb12ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140423643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b10e63724c1626d2e90b389a973dd2c236ae50a19c54e17733ae78a8790ab52`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Tue, 16 Jun 2026 23:37:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:37:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:37:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:37:27 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:37:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:37:27 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:38:38 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:38:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:38:38 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:38:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:38:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:38:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:38:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bd102da43afcd41f1fc87a85d2949db22d67f120961d78cc113e44e3f0823c`  
		Last Modified: Tue, 16 Jun 2026 23:38:58 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546757402d17dd4e2395735c0a60983f92ce2bc26dc5489777851c1eec8b1b3f`  
		Last Modified: Tue, 16 Jun 2026 23:38:56 GMT  
		Size: 15.6 MB (15619620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd5da32f81ea8e214ee2cb026cf5c860b5fd8d5bd18511a3ac97e420a03846d`  
		Last Modified: Tue, 16 Jun 2026 23:38:56 GMT  
		Size: 4.5 MB (4515186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cf110a28a332cdf310d65dfd6afb2327622a59da6f2be1c5e44825f06ede80`  
		Last Modified: Tue, 16 Jun 2026 23:38:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:227ed663447b48cd2521d8050d73b31ae2c54b1d92a11ee73aae9035c8e62ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3024995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bccc27d9ad3f2b1ec96fd6f2317be07faf331581615a567e41f8d73c60082d3`

```dockerfile
```

-	Layers:
	-	`sha256:974176acc631e966e3c87fc1490f90d73086ec6cde77ce3ca53763e67005ecb5`  
		Last Modified: Tue, 16 Jun 2026 23:38:56 GMT  
		Size: 3.0 MB (3006422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:401eeae4d1097f882fae0f1e43c906343c0768e3995ed9973043f1661c18fb60`  
		Last Modified: Tue, 16 Jun 2026 23:38:55 GMT  
		Size: 18.6 KB (18573 bytes)  
		MIME: application/vnd.in-toto+json
