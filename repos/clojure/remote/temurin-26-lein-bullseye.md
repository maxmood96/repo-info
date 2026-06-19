## `clojure:temurin-26-lein-bullseye`

```console
$ docker pull clojure@sha256:85373b61e683fca8e2f5b6dfa23087e2f80325de56c59ce6fa37bb10c6fb7060
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:878cc1a00a2ad5bb312839f0edfce58d9eb00209cf82d14951d541ba3b263c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169740905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb2b49c8143c0ce19b0f5f5b226d441d8388c20793bc2d6163421741d12d08b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:21:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:13 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:21:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:21:13 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:18 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:22:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:22:18 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:22:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:22:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:19 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a365a46cfcf06029aea3002c2178b324b1394445178f474303bd1fd816b9ef`  
		Last Modified: Fri, 19 Jun 2026 02:22:37 GMT  
		Size: 94.5 MB (94524351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b469fde20cbd63c0edc25e596c66dc3d7af2cc892119e99da75836daa7c3780`  
		Last Modified: Fri, 19 Jun 2026 02:22:35 GMT  
		Size: 16.9 MB (16929153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a80105819971efeffae6a79d5b8705276edf23c4269310aa39cfb97d45e1404`  
		Last Modified: Fri, 19 Jun 2026 02:22:35 GMT  
		Size: 4.5 MB (4515202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9156071fa12f06410a8f89a612ffa6d89220c68048e6d8dd0e7b7ca28f28d548`  
		Last Modified: Fri, 19 Jun 2026 02:22:34 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:efdc9c36f37db2bc02de00dcd84367cf201144824ef2855fcfb603f9b75b1136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4485273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dac9c43181fdd00d77c50489c0f08bf1a9b76cb9f031b37bd351ee7551278ed`

```dockerfile
```

-	Layers:
	-	`sha256:bc8239e67e5b45e781192170d051644fb0c8cdfb4223baf256b75425ae48b638`  
		Last Modified: Fri, 19 Jun 2026 02:22:34 GMT  
		Size: 4.5 MB (4467542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e41b54ee3c4dc844bf6f382e1ecc60a848c602a7050874b7e41bd3092845fb78`  
		Last Modified: Fri, 19 Jun 2026 02:22:34 GMT  
		Size: 17.7 KB (17731 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5b2f078b8216ec2a2f08d053e8a0e41220a6f2b065ce7aecfa50a017ef352d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167201773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5774d2c6ee5c48f4dbfa6078c2b69b4a0068347f22e06712854b129e3f1943`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:34 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:21:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:21:34 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:45 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:22:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:22:45 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:22:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:22:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:47 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f603e1cc16a3270f82da8682d253df0526c2da50ccdda6eb97ee0f10cb0d2532`  
		Last Modified: Fri, 19 Jun 2026 02:23:06 GMT  
		Size: 93.5 MB (93504322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d44f9ae7aa870194f9243e86e8122a90e9990a5e503a47e80db2d5dddcd2326`  
		Last Modified: Fri, 19 Jun 2026 02:23:04 GMT  
		Size: 16.9 MB (16917745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64899ea5505a5f11f7950065e128c4a64f1a9a6142ebe5df39c049868f15f93a`  
		Last Modified: Fri, 19 Jun 2026 02:23:03 GMT  
		Size: 4.5 MB (4515162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b93eeaf115c16d3b9b77e7e8204259f8ac93df048c90a5991c912fa1708eb6`  
		Last Modified: Fri, 19 Jun 2026 02:23:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a6e2003089f21b3d2b6336c8bb1588abd9dded95650464e1f6fcdb5a2ec47a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4484364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8511a2c10d2d60af01151c1947799180eb8c4464a270789262754f0c1fd7f9`

```dockerfile
```

-	Layers:
	-	`sha256:afb7ef7eaea5aeb1eaef2e7ad03710e902997fd5fe9b743798c1baec155465b3`  
		Last Modified: Fri, 19 Jun 2026 02:23:03 GMT  
		Size: 4.5 MB (4466513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00436c3b227cc3ed51aacd216a43908da9ef054bfde9cc631b8f407e17e6751d`  
		Last Modified: Fri, 19 Jun 2026 02:23:03 GMT  
		Size: 17.9 KB (17851 bytes)  
		MIME: application/vnd.in-toto+json
