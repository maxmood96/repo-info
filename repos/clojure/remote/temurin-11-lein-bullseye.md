## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:b7f1b2567c5a99ba37da020834a32b668d56bb3bef5c33473ad6c9af6efa9784
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:39e1e8f31072d6060795823b5bb4b38a3d5320b932fcf7613bd755f96e33ae72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221102272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96dacdd6741ec28d940aca88e0103b3f24ac5b92d152df3bf354280f5d31f772`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:15 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:15:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:15:15 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:21 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:16:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:16:21 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:16:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:16:23 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742fc8616c20f77be46f85c60b4984b7cd4412202b56f04cea345eed62b4863a`  
		Last Modified: Fri, 19 Jun 2026 02:16:44 GMT  
		Size: 145.9 MB (145886162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c8033a1ab9b3e7590ad8af461d5267d49b900086a5dbeae30e535cb035fbf6`  
		Last Modified: Fri, 19 Jun 2026 02:16:40 GMT  
		Size: 16.9 MB (16929093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daccbd78f31e491e38bc63fd49983f228cd20581f2835671a63a9d0fc8e1cfd`  
		Last Modified: Fri, 19 Jun 2026 02:16:40 GMT  
		Size: 4.5 MB (4515216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3d4e77939420f76729d6e15ff03478b4900f96ed6100601be5a2e67f25bcac24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4537914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0dc4a7f5456c53689a71cf7d926515eb5be5cf6c4ba06efdbed313403050c0`

```dockerfile
```

-	Layers:
	-	`sha256:d7abaa9b0be79e7cebdfabcfc83700a8e70ad78059cdee60e0490078b1b34b53`  
		Last Modified: Fri, 19 Jun 2026 02:16:40 GMT  
		Size: 4.5 MB (4522167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a1534e18c010fe75d856f93a4269d84014eeea91b059fd135b1579ce270ffc7`  
		Last Modified: Fri, 19 Jun 2026 02:16:39 GMT  
		Size: 15.7 KB (15747 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fc93fd8fc36657971ec5083dac5f9d9e0e899b102744befe1d19c33e6799f0d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216279630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93fae22ef7cb6dd2497a332067838a2d4414fb716ced43b42d6d954a57cc28b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:15:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:36 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:15:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:15:36 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:47 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:16:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:16:47 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:16:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:16:49 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734db61379015831d1988a60d9941ac2ebfbd2472e8cd6ee04571c2f57c471ab`  
		Last Modified: Fri, 19 Jun 2026 02:17:10 GMT  
		Size: 142.6 MB (142582140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48eb870833cd132c16f17f907ff954d2a1a0ce54a8089b144238711fa46c16f`  
		Last Modified: Fri, 19 Jun 2026 02:17:06 GMT  
		Size: 16.9 MB (16918132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37e2c34d1b8cd6e88b68cf9b4d2c288c4527ef3666c38b70829aac95515b00c`  
		Last Modified: Fri, 19 Jun 2026 02:17:06 GMT  
		Size: 4.5 MB (4515212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e5927c6cc2444fa5a3efc07e3ded36846eb0d6c4062e9e5baabd82628637398c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4537628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2009e0266ca4dbdbc395b205ea2c6607304da75b193e43a8dd8ede9d7be07495`

```dockerfile
```

-	Layers:
	-	`sha256:494da5efb52ccd92ad8382b45aaa510e080d3ad6fbbb61427a0b3b5e1d9d194f`  
		Last Modified: Fri, 19 Jun 2026 02:17:06 GMT  
		Size: 4.5 MB (4521759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:337511ce9889c16412bb322efb0a606cb45ce68a693152d0878538eea83c2ac0`  
		Last Modified: Fri, 19 Jun 2026 02:17:05 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json
