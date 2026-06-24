## `clojure:temurin-26-lein-2.13.0-bullseye`

```console
$ docker pull clojure@sha256:fb1b76c58613cf3fc25dd9ebad6ffb5fb2dedc3951e2e5cd44db0c6f70dfb7fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-2.13.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:002116270138395452cbc3ae3a73dbfbbd2dba1f267bdaf8a743152266bf9123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169741905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0eee787350e738a6b4653d4cf0d1688eba0aa8ddee50c7caceb065e6ac4cc53`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
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
# Wed, 24 Jun 2026 02:23:33 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:23:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:23:33 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:23:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:23:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:23:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:23:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c67cddb4b9fcdeefaf829aa012f0ccaefcfa862a558064326104b95b8849cd81`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 53.8 MB (53773009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35c5027f9ce29fc33c7e72ed9a6fa4e654226dc399772750980caf31fa5e765`  
		Last Modified: Wed, 24 Jun 2026 02:23:58 GMT  
		Size: 94.5 MB (94524331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a88add40cac8b304cf91523b1d02ab9098e80b8ef1100bf1ebc5cadfeda96d2`  
		Last Modified: Wed, 24 Jun 2026 02:23:55 GMT  
		Size: 16.9 MB (16928914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044066f55b0ee12be6ad3bc3860ea541075ede76061bc40c61b71fe367d8e669`  
		Last Modified: Wed, 24 Jun 2026 02:23:55 GMT  
		Size: 4.5 MB (4515222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e3995a675e299d8781bacc5f8fe6b0a75df1ea145ad1a41a93dfe4a82a11cb`  
		Last Modified: Wed, 24 Jun 2026 02:23:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:08eb4e549725739b5a325837b5c330aec2ca69b25a5238de3621ab5217dab495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4483649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb68558d00f6707fe94889cd98f6acbb58cbb811952578a4d09eec01f0342f2f`

```dockerfile
```

-	Layers:
	-	`sha256:266fa59e16f5543a4400f8f345f1dc5cfc789d6e37a9e85444ca4057f2022277`  
		Last Modified: Wed, 24 Jun 2026 02:23:55 GMT  
		Size: 4.5 MB (4465918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66bbf6710b38e2785e8f4d05fb56dd41eb24acce65ffe9a1e47f248d761adfb9`  
		Last Modified: Wed, 24 Jun 2026 02:23:54 GMT  
		Size: 17.7 KB (17731 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:beb1f797677492b000715a3404d2643bae6f8913dad7768309bf2f9da59ac292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167194903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf76a1b9c398a2062facba2d4f939f457b8322dcdadcf222f62c113faaed932`
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
# Wed, 24 Jun 2026 02:30:11 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:30:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:30:11 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:30:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:30:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:30:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:30:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:35157acdff35db21da73141f382d0dca0f6bc6d183c3a816d283fe39f471e539`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 52.3 MB (52257219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1214e2de5cb054ba68ad9a60fa76113d52c5d887bbb5d138de8fdbb9130162b`  
		Last Modified: Wed, 24 Jun 2026 02:30:32 GMT  
		Size: 93.5 MB (93504363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d128ef33019c065d5fe43ae69f0a7a0054220ad1fec0a53576c51678be388250`  
		Last Modified: Wed, 24 Jun 2026 02:30:31 GMT  
		Size: 16.9 MB (16917685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f7f87d5dda8fb300d8ae1ce411aff74f5de52c7cad7daccae95c7bfc14ad20`  
		Last Modified: Wed, 24 Jun 2026 02:30:31 GMT  
		Size: 4.5 MB (4515207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fbb251d82ab90c1da4e611d64f68175d10b0c6434ff5855572ad4cbcf18c03`  
		Last Modified: Wed, 24 Jun 2026 02:30:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a1b3ab8f85970cab35cd0afe8b899ea4baac626a9d5679ed82939107b69fb46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4482741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a113d5fd306ccfd5a7e24424daa63fa0687f9667d76d534f763c5669a48b2a`

```dockerfile
```

-	Layers:
	-	`sha256:53c70c52abcde043cf31a0e46e2f60aded9717a9e8971b5f6e698fc2007e4bd6`  
		Last Modified: Wed, 24 Jun 2026 02:30:31 GMT  
		Size: 4.5 MB (4464889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27b66de21e6fbec35e41f5e91a9bd602e18abae56498949be87fb45125d0a5c8`  
		Last Modified: Wed, 24 Jun 2026 02:30:30 GMT  
		Size: 17.9 KB (17852 bytes)  
		MIME: application/vnd.in-toto+json
