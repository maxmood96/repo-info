## `clojure:temurin-21-lein-2.13.0-bullseye`

```console
$ docker pull clojure@sha256:5c251c5d649d28a2f92186ddf47188f1b8cde28e4c3121f794eaf8070c7ff7b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.13.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0f465ad5c0b26f93166ecc8f3a73ad8ba9860c580cd867901f972190c498e267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.4 MB (233383076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132099b564b4417f7ca46b7f0dba4d8b2336057d83d1b837b743f3689d8b04e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:18:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:18:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:18:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:18:30 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:18:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:18:30 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:38 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:19:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:19:38 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:19:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:19:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:39 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad3a6aaa5161f44c08bb8d6bd149f45e858d22491010f32841f048680e0ba0b`  
		Last Modified: Fri, 19 Jun 2026 02:20:00 GMT  
		Size: 158.2 MB (158166940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2f7b16dbfc7de430bce57d7075805650b482433675917f5756982fbe1cde49`  
		Last Modified: Fri, 19 Jun 2026 02:19:57 GMT  
		Size: 16.9 MB (16928774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85d97f8d1a97a54ed06da2b1120b8c0a4328e263bac0e2a49a687e9b6f8c1e1`  
		Last Modified: Fri, 19 Jun 2026 02:19:56 GMT  
		Size: 4.5 MB (4515164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646c6b0230cb2e492627ac4c1d60b78afc8ceae3a55d2c2cf159513aea53731c`  
		Last Modified: Fri, 19 Jun 2026 02:19:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c389acf0bd4ec193d1b252c53db09e64be625626a064cd537876bf3f29c3add5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03fd566fe1097e0ffc011352a19e230c1e015ebbcf7f6eb935afe99639ffa508`

```dockerfile
```

-	Layers:
	-	`sha256:5abb93ad6583fcc00c5a076bfc61abd783a13a9a76474569c56ed081766045b9`  
		Last Modified: Fri, 19 Jun 2026 02:19:56 GMT  
		Size: 4.5 MB (4504503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e43fa13a4478b91ba8920c1b2ddcd3fea47d108fabb3316cdf6a30a4ed22e5f`  
		Last Modified: Fri, 19 Jun 2026 02:19:56 GMT  
		Size: 17.7 KB (17738 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5cc44ca8d15e6db9aa93515a9fe5b45688df40164a748124dda80cae4c020f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230158581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c914dd5e119652552560486c52d0d4b86a1be8e0fae21bbcda36d52911ffef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:18:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:18:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:18:36 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:18:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:18:36 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:44 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:19:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:19:44 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:19:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:19:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:45 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c71250be0f3c27f079c50f4271a10654bed182a4e93ec6990a50111d368dc3`  
		Last Modified: Fri, 19 Jun 2026 02:20:07 GMT  
		Size: 156.5 MB (156461276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0de35bcb33b640b1189e5a00903f07e79209e0700f6bc97a26b154e90ba036`  
		Last Modified: Fri, 19 Jun 2026 02:20:04 GMT  
		Size: 16.9 MB (16917575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ec38df45564f9a3a6453e8c0e340d9ba6710b5c1357de9a2d869c3278e2d69`  
		Last Modified: Fri, 19 Jun 2026 02:20:04 GMT  
		Size: 4.5 MB (4515186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f5c65bfecb3d7f28b82a7684a4edb6f75ad9e6da37891c286e5ead0f3e04b9`  
		Last Modified: Fri, 19 Jun 2026 02:20:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e8c65c2b1c1b4c3f58fd362e403afc4dd6684ecf23fa6066cdc41e775c99e0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb32a962d340bc4e58e57a8a13ade2c67543b201329211bf5f0813d1d10ba18`

```dockerfile
```

-	Layers:
	-	`sha256:d1f96425a9bad6f2a5ea9125a44be861c1b50971821d8b54a9bd1cd2596bb6db`  
		Last Modified: Fri, 19 Jun 2026 02:20:03 GMT  
		Size: 4.5 MB (4503477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c67e642f4eda50ea35b4ef306972d0a779643e1c0a1292d84c3985541167cc9b`  
		Last Modified: Fri, 19 Jun 2026 02:20:03 GMT  
		Size: 17.9 KB (17859 bytes)  
		MIME: application/vnd.in-toto+json
