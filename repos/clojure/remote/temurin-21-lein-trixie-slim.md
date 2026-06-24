## `clojure:temurin-21-lein-trixie-slim`

```console
$ docker pull clojure@sha256:1a914842f87f6f3a7ee3eed4be3a336445ff2c3fde0480340fadb7a30316969c
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

### `clojure:temurin-21-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ff452c60f42ebe2954c43c2c068868215ee555fc81bfcc7de87ba21dd34f8d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.2 MB (209211120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d2a0f77a2a267d05dc7459451103c156ff9493bb7498b18faef816e579a8af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 01:43:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 01:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:43:42 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 01:43:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:19:24 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:20:42 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:20:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:20:42 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:20:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:20:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:20:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:20:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7473c91b88d5eb633f18a6a19dc16a1174c9959796e98bd7a022ab10b75c41`  
		Last Modified: Wed, 24 Jun 2026 01:45:17 GMT  
		Size: 158.2 MB (158166926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db25e66c8f1c91c15e8fd71acb9bf9669655d97c8c17362147d66f5d2f60f948`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 16.7 MB (16743127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e5c2537acf932dbc6cab1101303512ae13e0104bdeaf2ec3455fec4657284c`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 4.5 MB (4515219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151e8bc201f3d5a20c3657dd29f4ed6d3cba38c50ab29570d9d55a666bfeffc9`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:69c235c0dceadd9d29857a81d0a9e8a3573a6bbc0955a40519d814affe1af786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e3199a5b266a257866ac8b016cf852c00d038be4e7a55e7b82ab122629f175`

```dockerfile
```

-	Layers:
	-	`sha256:0b5a996d1036aed647862b1e0acac8872c4b88e648a6c2579aa188d44ddb8b58`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 2.4 MB (2368933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:816d44f121fdcc5dc15b87d55b93ad1916e835e7a09f33cf66fd65fb36105aef`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 16.8 KB (16798 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:73460206934bdd8868115b7e7c010b60264c7015e6e170ba4ef295b6f24ecd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207837062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b002010c1f8bd5001d8507f5a3ccaff0d95fb6dcbc4d8280c3ed92b4439734f8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:26:01 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:26:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:26:01 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:27:17 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:27:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:27:17 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:27:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:27:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:27:19 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:27:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1738deb2880d5c7ada0d6868777c9e272a1887c111d1656d8e23281e2c278a`  
		Last Modified: Wed, 24 Jun 2026 02:27:40 GMT  
		Size: 156.5 MB (156461287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2b7d99aade0dfc7966e2f723324013bde75061cbe42ea08991de1814ac3e8f`  
		Last Modified: Wed, 24 Jun 2026 02:27:37 GMT  
		Size: 16.7 MB (16711603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f3baee3b94b2feafb3268ba831885fffbd281e5c2d476d87f175f9977a42f7`  
		Last Modified: Wed, 24 Jun 2026 02:27:37 GMT  
		Size: 4.5 MB (4515192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200c9369ec377924d4ffb986e9688e1fb3a5ad26f7e857ed0eeb3c727868755e`  
		Last Modified: Wed, 24 Jun 2026 02:27:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7a3e1eed46f717a8542070752ef647cff8cbce11526659131b241a7d24a74aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc526de6cd12475fa03e128706835e7f6f001294b3100838f46093f4e4315b13`

```dockerfile
```

-	Layers:
	-	`sha256:f1a6d4babe90a309e4c4e479c642501bba916dd07f926d6efbe2b7b51f4203f7`  
		Last Modified: Wed, 24 Jun 2026 02:27:37 GMT  
		Size: 2.4 MB (2368543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d9d86f9a0673d76e9804eac97f9073b910bc300f4bf580939f1402c3bec7a14`  
		Last Modified: Wed, 24 Jun 2026 02:27:36 GMT  
		Size: 17.9 KB (17874 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ca9f1d85bf4dd3270795906adbc3768bb7d091aab3cac18d9ed0c25933f1fa22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.2 MB (213247590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0dae320f65ea2e165e33a21f74c0cd964133416c8ea39d69d3bca18819856fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 00:00:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:00:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:00:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:00:47 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 17 Jun 2026 00:00:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 17 Jun 2026 00:00:47 GMT
WORKDIR /tmp
# Wed, 17 Jun 2026 00:03:27 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 17 Jun 2026 00:03:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jun 2026 00:03:27 GMT
ENV LEIN_ROOT=1
# Wed, 17 Jun 2026 00:03:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 17 Jun 2026 00:03:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:03:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:03:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cae30f60cd0ec6ba95234bc9baf8b715de9cca5a8c7483a3f4eebc08e9456b2`  
		Last Modified: Wed, 17 Jun 2026 00:04:10 GMT  
		Size: 158.3 MB (158343250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecab9349ceb2918e3b2fb0e2a1b9bf4bc3113ebdb9f963e67d351f15e9835c9`  
		Last Modified: Wed, 17 Jun 2026 00:04:06 GMT  
		Size: 16.8 MB (16782386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc85fb5220f648344b5a97a51eda13fd644755fb75eafdd40b1a03353c9f5fe`  
		Last Modified: Wed, 17 Jun 2026 00:04:05 GMT  
		Size: 4.5 MB (4515185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1132a529849969ec5395c2ad6eae1493086320b0c51cb6cab5f46bc82318cb`  
		Last Modified: Wed, 17 Jun 2026 00:04:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3d7ae192d531927d07479b3493722f0311ac0ef00660432b2e3a4222ca706173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a167a8a3f7feaccfa7473691e0c485f88f1de577bac45ba90b6a4a2a86f89d95`

```dockerfile
```

-	Layers:
	-	`sha256:7c1691c05d4dabb3b777bccf65fc52ffd6c6b5c89cdab954031be24e4dfec246`  
		Last Modified: Fri, 19 Jun 2026 02:49:51 GMT  
		Size: 2.4 MB (2369913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9bcba48519054cb51f96c99343c7573230e603b696ff7bc53e5881b60766a96`  
		Last Modified: Fri, 19 Jun 2026 02:49:51 GMT  
		Size: 17.8 KB (17796 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:520ab8bb2c7fe804e301e336b2e69eed84ff5be5a25da10c252738b09ba50809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198535018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695212a4f4b938a7d61f0a95291b67b7f1c6b795b72c795be987b17366a3a3c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:38:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:38:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:38:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:38:51 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:38:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:38:51 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:40:04 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:40:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:40:04 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:40:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:40:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:40:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:40:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66d9375a62e658d5255a5581f80c6f86b82e7d20e6a5c6878c2e0220d54700`  
		Last Modified: Tue, 16 Jun 2026 23:40:34 GMT  
		Size: 147.4 MB (147388338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a591815a1c96260572f72ad9e7b60e296717e36c2a433c0da2a45d40931e6f5`  
		Last Modified: Tue, 16 Jun 2026 23:40:32 GMT  
		Size: 16.8 MB (16779695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ee544c84d46e11562e572ece00dd9d3a2ba7dc62be33f607f6cf9647d62bd7`  
		Last Modified: Tue, 16 Jun 2026 23:40:32 GMT  
		Size: 4.5 MB (4515201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e41e633d46d77d12113b18c609b64884cddd36e1eb7c1fd2ef3b8e1d820a1c`  
		Last Modified: Tue, 16 Jun 2026 23:40:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:74a64eb96361a11dd2d135ea4e505e5208ed3f9d36a107bd0ae4e59ee48bd4f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e5e940ecd789b758b192c63b11d518fb0ee8f5d908f34d7dd721b97dac8a3f`

```dockerfile
```

-	Layers:
	-	`sha256:977eb0d74d9d91fa7287aa015edc1ce9c7a361d8a46d1d991f1f8df72ef817c6`  
		Last Modified: Fri, 19 Jun 2026 02:20:04 GMT  
		Size: 2.4 MB (2365360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:becbfee478c2dd1483d8eb3c339e815742a211441bceea4fcb9baeaadea0a336`  
		Last Modified: Fri, 19 Jun 2026 02:20:04 GMT  
		Size: 17.8 KB (17753 bytes)  
		MIME: application/vnd.in-toto+json
