## `clojure:temurin-25-lein-bullseye`

```console
$ docker pull clojure@sha256:0e175c9624f7d4e82e6e61ee04f6af904ee8548f7617af4e57ae8d6245e06518
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:65a96d6932dfab1b0b65c239c6af505b904ef9c3252fb3e3c2861595cbf1f1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167791816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a305ed4345e2cbbfa97151cf9af9132cad598bbedc69c2f5b843551a8493c78`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:20:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:53 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:20:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:20:53 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:22:00 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:22:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:22:00 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:22:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:22:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:22:01 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:22:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c67cddb4b9fcdeefaf829aa012f0ccaefcfa862a558064326104b95b8849cd81`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 53.8 MB (53773009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c76eb968458a6692ba618fd61f237ad4cebb1c23c462a9ba4de2ef86f52271`  
		Last Modified: Wed, 24 Jun 2026 02:22:22 GMT  
		Size: 92.6 MB (92574568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bb40adac3467d25df28a83edb32cd5ad25cfc0c4195987f58b0e54528818a2`  
		Last Modified: Wed, 24 Jun 2026 02:22:20 GMT  
		Size: 16.9 MB (16928637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a666647ae50bcaf157a3f9cfd30ee8b1155dd39ad1ac842ad8d50173c961e7b`  
		Last Modified: Wed, 24 Jun 2026 02:22:19 GMT  
		Size: 4.5 MB (4515174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37d47768e59579d1ddf25cdea32b3a78c22a2e81341686ff958df09b7d6e5f3`  
		Last Modified: Wed, 24 Jun 2026 02:22:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:060098498861064e3dcadeb7a02c3fedf88004326c72e1ed176fe92e1a1738f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4487436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623aa70b3ffc2841510f24141cba99b8996c378af1a580f0ac90af711e24b74e`

```dockerfile
```

-	Layers:
	-	`sha256:1e6d6336947843bda20128a74c25af1637a430328e11c0a3558190f62b98da82`  
		Last Modified: Wed, 24 Jun 2026 02:22:19 GMT  
		Size: 4.5 MB (4469063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d31e977d9f3f3d698b410e7aac0dbdb313fa16c7a02901437610d896c886af`  
		Last Modified: Wed, 24 Jun 2026 02:22:18 GMT  
		Size: 18.4 KB (18373 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:339be1123da076121e7bd16ccb4bd12ec0f44b7cadd0702dd9c2f8ccee4011c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165232902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3440cb33cf15c755704273250d60c554e650f76c36c4e2cb747b646ee60a85ac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:27:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:27:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:27:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:27:31 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:27:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:27:32 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:28:42 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:28:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:28:42 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:28:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:28:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:28:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:28:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:35157acdff35db21da73141f382d0dca0f6bc6d183c3a816d283fe39f471e539`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 52.3 MB (52257219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a28b9c6baa70efa1e69b06d54ef4e0a1a5857750fe46b00690f7d4531191c83`  
		Last Modified: Wed, 24 Jun 2026 02:29:05 GMT  
		Size: 91.5 MB (91542250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc6339350575987a7ac1c2aaa4cd1592ecff85855b1768bfdbb7266ca398a1e`  
		Last Modified: Wed, 24 Jun 2026 02:29:04 GMT  
		Size: 16.9 MB (16917791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a78e73128c5b9fdefe00d6931c58e9cbd24eef23d62b5013351e590ad2a2c0f`  
		Last Modified: Wed, 24 Jun 2026 02:29:03 GMT  
		Size: 4.5 MB (4515214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7436dfe32e1cd6ac2c0175ac4d15bb529be08dc6f497d18444ecde819e4a9f8`  
		Last Modified: Wed, 24 Jun 2026 02:29:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4a5d8f9187401573397f39f1c7463db5ed56175755e9feb2b33e71e3792bbc80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4486576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff3aae96a6dcc4229c87c287d34a4767c4e601d7660b07905f458c97c477c74`

```dockerfile
```

-	Layers:
	-	`sha256:fa2d7780b0eec4fc1d1c13ad90c97e931e7d88f15ae5720375523cff986d77e0`  
		Last Modified: Wed, 24 Jun 2026 02:29:03 GMT  
		Size: 4.5 MB (4468058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dfb4d185893d25658cdbeda3eda3863e2b0ad17f7453a29dd0df0579b00e8ad`  
		Last Modified: Wed, 24 Jun 2026 02:29:02 GMT  
		Size: 18.5 KB (18518 bytes)  
		MIME: application/vnd.in-toto+json
