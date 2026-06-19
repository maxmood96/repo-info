## `clojure:temurin-21-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:dee6b750ed1c1ce8c35fbd9cbe244a7fdd963f39ef240a5152c71c555fad4850
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:91a013a66c2b32290d1402c18b8b21d2a5aa681a6f487779c1c5111b63cb0239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208574243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f850e6872d5d8617c842cf510e9144a0a1dc788d60786a6bc0f3f48fb2098376`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:18:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:18:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:18:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:18:35 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:18:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:18:35 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:47 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:19:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:19:47 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:19:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:19:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:49 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a151fe1cfea00a8dd29c576b1f8dd7141c36b5ae19d0d5622950285d951a4a3d`  
		Last Modified: Fri, 19 Jun 2026 02:20:10 GMT  
		Size: 158.2 MB (158166919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699e745daa62bdccd21c10941d900c517ddca5974ecd0efad72530391d953629`  
		Last Modified: Fri, 19 Jun 2026 02:20:07 GMT  
		Size: 15.6 MB (15631431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742ad021835f27f0a178aaff18703d118bd3887095a2f3adcd8aca41356ecb0f`  
		Last Modified: Fri, 19 Jun 2026 02:20:06 GMT  
		Size: 4.5 MB (4515209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9943656f4b83890faa6793a303507c6d378ccc0972cf92a9efcaaf8d5c9a4c80`  
		Last Modified: Fri, 19 Jun 2026 02:20:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8426a8b177888b61c50730a7bd7954b4259ccc36113decb102a78c5246ec993b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3058361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592f7f15c1bcce39f15afdb4311d92eb60f4dc19f45f7fe6cc1cec5048881dbb`

```dockerfile
```

-	Layers:
	-	`sha256:c384e4e9da669bbbf0000083ef7ee5f5166f72477dbad29ca7f2855332de7e63`  
		Last Modified: Fri, 19 Jun 2026 02:20:06 GMT  
		Size: 3.0 MB (3040588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:032806343d79bccc6048edd35ab50783cee3a19c8f60c83b0de5354eb19b1dfa`  
		Last Modified: Fri, 19 Jun 2026 02:20:06 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:624e26d6740615ac8d04a7d8ca5bacd7f57db6ce016c1b7c673e05e34ae2da60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205342776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8bd1eb6c62ce81861307f713ed199a08f14b29e5d7d1ad668f2fcc5a18c857`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:18:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:18:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:18:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:18:43 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:18:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:18:43 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:50 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:19:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:19:50 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:19:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:19:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:51 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a039836440a361214925b78aa1ab5991806648ff009b8314c176c22320aca44b`  
		Last Modified: Fri, 19 Jun 2026 02:20:12 GMT  
		Size: 156.5 MB (156461268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178c7363b8dd12f9c8387c3069d521356e29502a8136130c4f73315284024de7`  
		Last Modified: Fri, 19 Jun 2026 02:20:09 GMT  
		Size: 15.6 MB (15619756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0a8edb2a5c28a3df9768f1a32601ecd92be18c313797859b2b21f346a49243`  
		Last Modified: Fri, 19 Jun 2026 02:20:09 GMT  
		Size: 4.5 MB (4515169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1577b466bd0f238ac916f659bb0b72f2258c6e093429cc6370fa647ebfb05072`  
		Last Modified: Fri, 19 Jun 2026 02:20:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:08de3e841c758ad25dbb7c13548a688f8b6ae84dd2e310edf3faafb927ee06a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3058090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd08e30947ce940fc56e9b7a09bf5214344d444a4eb5e3cb2bea22fa3b936cd`

```dockerfile
```

-	Layers:
	-	`sha256:10e24ae6619069daff2b414885a1735a640e05f17734d97bf9779db06603e23c`  
		Last Modified: Fri, 19 Jun 2026 02:20:09 GMT  
		Size: 3.0 MB (3040197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde0c656a76ee75c7a99719ea5ff773d0e11a6e9aa991a374fbbe9f7e70c741c`  
		Last Modified: Fri, 19 Jun 2026 02:20:08 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json
