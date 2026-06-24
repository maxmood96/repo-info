## `clojure:temurin-11-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:9cca3c4ff05d369c01ee427245d038a0f247164836961feb39e4bb9a87eac8eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f083759dc2447b32c357fc06ccc2d2b76058e1a32b99f35286bf0996460dd61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196291856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d7755aad8f17fe2e5e4862cb910b29d84a2735b9360e727e57f06b2464f0a0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 01:44:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 01:44:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 01:44:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:44:17 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 01:44:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:15:37 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:16:42 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:16:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:16:42 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:16:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:16:43 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0251c4232e4025b51352f0bb7119fd866d4a6a62861f09baea6fe5af4c6eee59`  
		Last Modified: Wed, 24 Jun 2026 00:28:14 GMT  
		Size: 30.3 MB (30259447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdff644a2a6eaeabcb6a4aa4b59a460e93274b872610564de322f9b83950a47`  
		Last Modified: Wed, 24 Jun 2026 01:45:05 GMT  
		Size: 145.9 MB (145886223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c5e544181148ae372d3382e6e8132518a7926ec7646d929170213b78d38e29`  
		Last Modified: Wed, 24 Jun 2026 02:16:52 GMT  
		Size: 15.6 MB (15630984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d841ce91c01ad19cba201b6e57dd3f95a9c8d73271191fa2b8c2c27ffe7afcf0`  
		Last Modified: Wed, 24 Jun 2026 02:16:52 GMT  
		Size: 4.5 MB (4515170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d6c85dd23618c7a076d92dcbe4717475307146d2ed9865c68aabbb12ad1b839e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3071451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac636293e70729c939e83c8ca5dca8b94903c0d3dd6a274e531a40df0967a16e`

```dockerfile
```

-	Layers:
	-	`sha256:6703d54bd585383a6b570d2bc835469ebd341282026d0fab7dbfa9775b6a55c8`  
		Last Modified: Wed, 24 Jun 2026 02:16:52 GMT  
		Size: 3.1 MB (3056628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:910088e7b2a0e165fb7993088dcbd4e0cd5a49a98289993a80647595ad0d83f0`  
		Last Modified: Wed, 24 Jun 2026 02:16:52 GMT  
		Size: 14.8 KB (14823 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a7a96d89d1c7bc87e68bda081fa87e915252ef26a0e0c470d4ea88a764810974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191463759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed636598af849761be50127ea115dc99de8c04c7311bbd0e56c69b377417d1c0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:22:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:22:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:22:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:22:23 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:22:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:22:23 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:23:32 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:23:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:23:32 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:23:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:23:34 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:58009b48fe731a10341c4f5f98dfa280afd10fa34cc71961411d37e306120dd0`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 28.7 MB (28746926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f45e7b1ee7e0ca4e3d52869f1802a7246d2daaa0635e3dfa797af6957ef7c6`  
		Last Modified: Wed, 24 Jun 2026 02:23:54 GMT  
		Size: 142.6 MB (142582142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533d974af9cdfe1049855bf86111664be4a2f84891ee2d0ac03eaa5578ce9b4c`  
		Last Modified: Wed, 24 Jun 2026 02:23:51 GMT  
		Size: 15.6 MB (15619440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967aad8f8e3e3351c175701318c06d982ca20edb67fc090476039712e3df00f1`  
		Last Modified: Wed, 24 Jun 2026 02:23:51 GMT  
		Size: 4.5 MB (4515219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ea2e469038c7dcc26364e255fd2c7a229b3c915197e7e7ecf495448f9f4303f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3072753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e51682b0180ae353be3f89a8d0afaefda3ccea9f7040cb93c8080032de0577`

```dockerfile
```

-	Layers:
	-	`sha256:b851d95d8d5e0418f56ddb180b22c96a58b9c72b5157faf93671a254e89f7b84`  
		Last Modified: Wed, 24 Jun 2026 02:23:51 GMT  
		Size: 3.1 MB (3056855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bfc765c62a33bbebd80d6ba1e98bc893529c775c33c1b1b07e97f1fe0552c4d`  
		Last Modified: Wed, 24 Jun 2026 02:23:50 GMT  
		Size: 15.9 KB (15898 bytes)  
		MIME: application/vnd.in-toto+json
