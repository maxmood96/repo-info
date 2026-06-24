## `clojure:temurin-26-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:9347914a7646f3ab44575d02621a1af3404a9449d8df6f5efae0fd8e43600b90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c0478888bc280adb6e0bae680fe6469da863c6637ef41170493b30be4a381146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144930642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd078ce318a9a37f8058494e014b07abf2ea19fbbfddbb4a245ab08f59d5ffc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:22:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:22:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:22:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:22:29 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:22:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:22:29 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:23:37 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:23:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:23:37 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:23:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:23:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:23:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:23:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0251c4232e4025b51352f0bb7119fd866d4a6a62861f09baea6fe5af4c6eee59`  
		Last Modified: Wed, 24 Jun 2026 00:28:14 GMT  
		Size: 30.3 MB (30259447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f67d2aeb56732708c3b8cc5b4fcdb3b3cd9f074fe9156d1eb1dc9e3e804272`  
		Last Modified: Wed, 24 Jun 2026 02:23:58 GMT  
		Size: 94.5 MB (94524352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77690108b4a343f8be9c458da255618345becb0e2311b430a9f900fc0300509`  
		Last Modified: Wed, 24 Jun 2026 02:23:56 GMT  
		Size: 15.6 MB (15631191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a5f6fba31e6589538f600834351edeb42086c25173d69bc3b7514f9ca6c325`  
		Last Modified: Wed, 24 Jun 2026 02:23:55 GMT  
		Size: 4.5 MB (4515222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036ff80a9955ab4b8f286c226c5c9de30c25f30ca13a843bcfeed6548dc9bc23`  
		Last Modified: Wed, 24 Jun 2026 02:23:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:486ca6f8c41040b6cd9aebf3203680e57ef168c2b9442124c103ea34aab2b0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3019769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859e43eb4c9e3d98b61f199f692ce205adee74b98d22a2309f8a254ea5ff62d7`

```dockerfile
```

-	Layers:
	-	`sha256:69715e787982cfef36e560801f19539113aadf4544986618896e34157d0dbcec`  
		Last Modified: Wed, 24 Jun 2026 02:23:55 GMT  
		Size: 3.0 MB (3002003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6011989b243a3a13fec2e447750c9a4b6dc1216ff484117910fb50154aca52c6`  
		Last Modified: Wed, 24 Jun 2026 02:23:55 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3b95e02151fd2bdde6b66fb49d6ed2e1baafeee6a5586b4bb9c10210312eee37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142386691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1da723486b4feb0c29426f89b669bc952c249b422d8397223e425e733be6a03`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:29:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:29:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:29:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:29:01 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:29:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:29:01 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:30:09 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:30:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:30:09 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:30:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:30:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:30:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:30:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:58009b48fe731a10341c4f5f98dfa280afd10fa34cc71961411d37e306120dd0`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 28.7 MB (28746926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1214e2de5cb054ba68ad9a60fa76113d52c5d887bbb5d138de8fdbb9130162b`  
		Last Modified: Wed, 24 Jun 2026 02:30:32 GMT  
		Size: 93.5 MB (93504363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74361cec819d0759e0aeef3a17d999058338c2dbc8d8a18f20cc365a9a0d8e50`  
		Last Modified: Wed, 24 Jun 2026 02:30:29 GMT  
		Size: 15.6 MB (15619765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354800ae3120761dab4a65124709301ff3cdb8ed500398d03fda72eb00066d9f`  
		Last Modified: Wed, 24 Jun 2026 02:30:28 GMT  
		Size: 4.5 MB (4515208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8987322d20fc5f2c2338f493e950b86a47f0421e386f06f47d3b1a3092d88f1`  
		Last Modified: Wed, 24 Jun 2026 02:30:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:92bf4d26d3453440d66f20f1fea0d960afb46bc2402f5d48732a3f2185cd7d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3019496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a998f969b696c756ec06dc512fb277d233b7a9315437d9537355bba63d0971a`

```dockerfile
```

-	Layers:
	-	`sha256:c1d71cebfa6b225a6a963c9367b2d11c7144070d6df6fdd5c4e7c32c3e9e7cd5`  
		Last Modified: Wed, 24 Jun 2026 02:30:28 GMT  
		Size: 3.0 MB (3001609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b81fc411477448ab261a0d351e76f601f48d3039969d8e93a793212a384da5`  
		Last Modified: Wed, 24 Jun 2026 02:30:28 GMT  
		Size: 17.9 KB (17887 bytes)  
		MIME: application/vnd.in-toto+json
