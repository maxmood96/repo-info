## `clojure:temurin-11-lein-bookworm`

```console
$ docker pull clojure@sha256:f251e690228404e7099bc7fc73db1da013274928eebc8ddc7853d446fd988d7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:b3281c25a3e2e1e5e07f3ff3b0863fdd8a671535821ac3a6d249122f4081c266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (219011701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489d5afe3d83d2cd7d84a0002d5751f2ab19ea00c828e894ffea5ad853e46f2a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:15:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:15:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:15:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:15:06 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:15:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:15:06 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:16:12 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:16:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:16:12 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:16:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:16:14 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c5ba858e556e4d905c5c0e7a143d23de000c2de49b3ec2f8b3187127d14610`  
		Last Modified: Wed, 24 Jun 2026 02:16:34 GMT  
		Size: 145.9 MB (145886208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01c2f64a8ff7b6f32360c003efe10ebee8a91797023dabba24266214ed66112`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 20.1 MB (20108027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61364c9309d681d772d4af07a20e4f8660056eb615e4330b81b713bb230421b9`  
		Last Modified: Wed, 24 Jun 2026 02:16:30 GMT  
		Size: 4.5 MB (4515224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ca56b83c5f0c07b71741b5893128490ae6d369ea2947e2492b5f1db437c7e98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d569e6220cff1a9d2047e1f8c08e19c79c4d76937cadf05b43dbf618bb36f82a`

```dockerfile
```

-	Layers:
	-	`sha256:5f6da9036293072a20b63093f20b00386278422eaabfbd59cf386cd4b63ed5f9`  
		Last Modified: Wed, 24 Jun 2026 02:16:30 GMT  
		Size: 4.3 MB (4303534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:554532f81ccca8c1a73353776471b35710a34b39439ab5b56bf0eaf0b786adaf`  
		Last Modified: Wed, 24 Jun 2026 02:16:30 GMT  
		Size: 15.7 KB (15748 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b280dde5ee9d601cf59930e231ba896e54bc95465a655e3693a465b6e5640498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215426647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89061e2a11c5a6661891b94beab9572d4c8931928322410481b72be410df7f6f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:21:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:21:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:21:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:21:36 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:21:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:21:36 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:22:44 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:22:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:22:44 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:22:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:22:46 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e5c73d9f3e3fcb7a5b9be3456ee8088201dfab04f2c5bad69535ada8384f77`  
		Last Modified: Wed, 24 Jun 2026 02:23:07 GMT  
		Size: 142.6 MB (142582159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88e75d412bced70d2cce9e842ff3685fe0234de6360a545d20d3e5b857ec0a9`  
		Last Modified: Wed, 24 Jun 2026 02:23:04 GMT  
		Size: 19.9 MB (19940044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99fd36e82ae325be3707e34f966d2e9a1231d81ea1153fc851148930091956c`  
		Last Modified: Wed, 24 Jun 2026 02:23:03 GMT  
		Size: 4.5 MB (4515211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c4e565b9c0341529dd6328c8a165265019bafcf7a070862731ecc076890a1cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2023b736034e1a4033089f30bb6b002511e7c17c1df225501d280f9a2c18b0c0`

```dockerfile
```

-	Layers:
	-	`sha256:5bd172c37cb8a563ba9d32dc5406d56de839df17babc3a3ee0c76077fdcd2305`  
		Last Modified: Wed, 24 Jun 2026 02:23:03 GMT  
		Size: 4.3 MB (4303767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d197b62caf81cf1cb5147c11a3167ba3657c81a251cb9607430c68f9bf1c642d`  
		Last Modified: Wed, 24 Jun 2026 02:23:03 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:25836bde1dce43263a8b18df2614937dc1443fbf0c964b6f5df12ac9aa8c4161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210304543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4384e4dd70f06e0a280ee9f85b3f8f728344967724b820a1006ada7c8c48c595`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:24:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:24:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:24:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:24:25 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:24:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:24:25 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:27:46 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:27:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:27:46 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:27:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:27:51 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fc64daf9c9f118fbcba656767bc8dbba78b223045b626eb61d82cdc3a433d8`  
		Last Modified: Fri, 19 Jun 2026 02:28:29 GMT  
		Size: 133.1 MB (133110739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc85b9e1ec0d23773963d5ecc2fd33f11242ce5e5959a8f1deaaca08521a3f3`  
		Last Modified: Fri, 19 Jun 2026 02:28:26 GMT  
		Size: 20.3 MB (20331864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26a3d1cac191f049dea600f0e191f736278f738f222cdc99b2ee5f04b4fe2c7`  
		Last Modified: Fri, 19 Jun 2026 02:28:26 GMT  
		Size: 4.5 MB (4515238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:017799ee5e164e9fec5fce5f156edec0e46113e0007d41f766409fefb7363d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4320572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2065137edd6437e32b9ea08630419229258c9c232059940ea7d8b980865bb5`

```dockerfile
```

-	Layers:
	-	`sha256:4a6c270b4f8f4bb93e3e63f440ebb42b8c91879421e6c4965daf4a7642784e75`  
		Last Modified: Fri, 19 Jun 2026 02:28:26 GMT  
		Size: 4.3 MB (4304780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43375b6cbcaacea554df3798b38f95c1450d0bf67f0de25b9769d1ac4b8c59a`  
		Last Modified: Fri, 19 Jun 2026 02:28:25 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:483101a8b30a980130817cb84606a6f3f2e6fad1584ec58c72dd3de62fde711e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198099675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba62c57352f9801d9afbbcef183f81ce67463322845f32244f18325ffd85c102`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:07:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:07:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:07:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:07:54 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 04:07:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 04:07:54 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:09:01 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 04:09:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 04:09:01 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 04:09:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 04:09:03 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:bdd2e9d83d68023204331dd445067114dbd3500d2d496368624fa7ef81743d4a`  
		Last Modified: Wed, 24 Jun 2026 00:27:09 GMT  
		Size: 47.2 MB (47161675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894f0ce15fa11bb3c6ca37e7d0ec532b71cf5687d8bdbe22e95582d18a8c14f2`  
		Last Modified: Wed, 24 Jun 2026 04:09:28 GMT  
		Size: 126.7 MB (126652580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7ab71c47ac0513b2d1b37a53de8b98b2aff8e568d9efc22f11c8d1562eb8d9`  
		Last Modified: Wed, 24 Jun 2026 04:09:27 GMT  
		Size: 19.8 MB (19770162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3b0c80e7191d22b98c07d8920053dc213648575774def4b5d687038abd287b`  
		Last Modified: Wed, 24 Jun 2026 04:09:27 GMT  
		Size: 4.5 MB (4515226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2041f3c658a2c64c07294bb85a03837460ec294da09891968d0364cd79da418e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4311100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b384a0b04c136f3855f684279a99a2b5c9453e2c54ef4dbe3b6ad2b254c7e1`

```dockerfile
```

-	Layers:
	-	`sha256:9cc3f96806b6542df594cc7211cd563ac4612f588a5b2ff6ee70f87f9c35f293`  
		Last Modified: Wed, 24 Jun 2026 04:09:27 GMT  
		Size: 4.3 MB (4295352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0323038b68cc86cab949974f3963b264144a974eaa283f92d3d1dcefd3d811de`  
		Last Modified: Wed, 24 Jun 2026 04:09:27 GMT  
		Size: 15.7 KB (15748 bytes)  
		MIME: application/vnd.in-toto+json
