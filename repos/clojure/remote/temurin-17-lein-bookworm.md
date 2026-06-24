## `clojure:temurin-17-lein-bookworm`

```console
$ docker pull clojure@sha256:ccfc68df266d9f51caa4310fc3b5e08b51a27c6477397b3107ff8941db97de18
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

### `clojure:temurin-17-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5e7056e52aff254c5fe190d9190e5b94f5705deaeab71d4978c295148d6b8554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (219030864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628e185af9cee2ef9206adcff7395a496132a8862f2d06fe94038c32c5c8ec1d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:17:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:17:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:17:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:17:03 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:17:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:17:03 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:18:10 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:18:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:18:10 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:18:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:18:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:18:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:18:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412d86f8fd0f4ac4bd7b9d1c0d2a334b34f10ad21b4e8240d3ebf334bf9f4743`  
		Last Modified: Wed, 24 Jun 2026 02:18:35 GMT  
		Size: 145.9 MB (145905441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48311ccbe60d0455c42921534cd47385e2df77d84f85f4729a17f832616c9eee`  
		Last Modified: Wed, 24 Jun 2026 02:18:32 GMT  
		Size: 20.1 MB (20107576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9656ff19ef68b6ccbfa74e535c9f336b388142f46b83af362b181aa938ff42`  
		Last Modified: Wed, 24 Jun 2026 02:18:31 GMT  
		Size: 4.5 MB (4515208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa4f43deb7968f3435a7906b50f47cf4a6ce60465e257932a732cacda375294`  
		Last Modified: Wed, 24 Jun 2026 02:18:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:128c78e609fba5f0017c8537a30142b9524ba8097f9cd3c801ee738e7bd235f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4301756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64557ebfa8296add79a9b1557d76b23d66b1235c624b61583614496df76900f8`

```dockerfile
```

-	Layers:
	-	`sha256:7f5d92b81f3cb3edee2be624920d0675388ffba59d2d654b4e0de4713a9e93f0`  
		Last Modified: Wed, 24 Jun 2026 02:18:31 GMT  
		Size: 4.3 MB (4284018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc7cab3c17bb68efc704f6dff9f81ba774b6cf054701feb300d79dc6d7fb1cf7`  
		Last Modified: Wed, 24 Jun 2026 02:18:31 GMT  
		Size: 17.7 KB (17738 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2918a69c8efabc08226b43affb669a8f3c241d7a42495bd0dfc133e837dd8b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217569499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e902d108d9c00d5280e546fcc527e107f70f62a13935cf32474c39ce199817`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:23:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:23:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:23:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:23:42 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:23:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:23:42 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:24:51 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:24:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:24:51 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:24:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:24:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:24:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:24:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571b52bca0f840624be41445ee2c4db1420453b47427970c3f5519024a14579a`  
		Last Modified: Wed, 24 Jun 2026 02:25:13 GMT  
		Size: 144.7 MB (144724312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a604724153a368f558e5ef689397b60daa133f5cf5cea8e46cf46e1c1148d435`  
		Last Modified: Wed, 24 Jun 2026 02:25:11 GMT  
		Size: 19.9 MB (19940344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c81f82eb72d22122b14b148f3cf6f62c52fda959562692beb38220ddb06ea64`  
		Last Modified: Wed, 24 Jun 2026 02:25:11 GMT  
		Size: 4.5 MB (4515213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32d1b8209480d7160bf5e4b9fd2d8fa47f20c6daad953f24a3e2527361d1198`  
		Last Modified: Wed, 24 Jun 2026 02:25:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:56a7639e31b7639e9e62f267fcaff4038f04490300a3b5e2ac3eb99145f56240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4301492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b8e5fe0cda8e95e00e05246c906bfd3edf87aef041bcb36064d11fd53a9522`

```dockerfile
```

-	Layers:
	-	`sha256:01acc9fcf96d6c4846985c834c5f77da6194508bd0bc0ecc5562863fe19c728b`  
		Last Modified: Wed, 24 Jun 2026 02:25:10 GMT  
		Size: 4.3 MB (4283633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a590c6f85478c70f2e4e20d1f5d788f44a7d3cbf0b31e0d36ec96487e7cbbb1a`  
		Last Modified: Wed, 24 Jun 2026 02:25:10 GMT  
		Size: 17.9 KB (17859 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:71b9d305b77381d6dfe74bb5183c78dc8af61ce03f707b52d4aa4593e08c0d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222960741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b393095b34adc40eed075e53c5c0e6c95f7a392a67386b7599d82236e8d90b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 08:01:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 08:01:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 08:01:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 08:01:31 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 08:01:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 08:01:32 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 08:03:57 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 08:03:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 08:03:57 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 08:04:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 08:04:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 08:04:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 08:04:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:55b0e891f4e8dc14bf4bc7e853254fcf1f3ba5a8e8e3c07c21e7dd5bd6d87882`  
		Last Modified: Wed, 24 Jun 2026 00:27:34 GMT  
		Size: 52.3 MB (52346847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc3303405f604b9119feae76c1964b8d7cd671be00851817c5db88d3df2f4fe`  
		Last Modified: Wed, 24 Jun 2026 08:04:41 GMT  
		Size: 145.8 MB (145766195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0014ee9b78f1f70f5127925387af4df1e692f3fea5c5b99a77a31f072917cf5`  
		Last Modified: Wed, 24 Jun 2026 08:04:38 GMT  
		Size: 20.3 MB (20332051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9850f92039c7740698618a9ae208b79aa341ca6089bbb45a60d26045f090caa`  
		Last Modified: Wed, 24 Jun 2026 08:04:37 GMT  
		Size: 4.5 MB (4515219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44ce5a196300533e1746726fa25599e35f99a034b81b531ef29fba364ba4473`  
		Last Modified: Wed, 24 Jun 2026 08:04:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:793a88846bcc0107593bb5392991ebeab96d163f26b4b5df8870c5389f94b012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93e0763f3197aea149432ffeeb2d7f220c2eac5477f21f70307643ff7b794edc`

```dockerfile
```

-	Layers:
	-	`sha256:16a0f875975c4792db061c0c51813c165f842c73fc20659abb7671e9a7399f72`  
		Last Modified: Wed, 24 Jun 2026 08:04:37 GMT  
		Size: 4.3 MB (4285879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71b7e55c656f66bb83e1a9f08f3871a0acdd6dcd366e20a5f5a59da0849ca942`  
		Last Modified: Wed, 24 Jun 2026 08:04:37 GMT  
		Size: 17.8 KB (17782 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:c87864e133645dfcdc881b8382808056e34c79bc1a7534bbd7d89ad9ddb6068b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207357754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064def4acc7ce60a3fbb08b0d024ce6a3e60fb61d65c397a0a53893c4199eff3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:11:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:11:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:11:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:11:02 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 04:11:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 04:11:02 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:12:07 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 04:12:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 04:12:07 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 04:12:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 04:12:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:12:08 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:12:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bdd2e9d83d68023204331dd445067114dbd3500d2d496368624fa7ef81743d4a`  
		Last Modified: Wed, 24 Jun 2026 00:27:09 GMT  
		Size: 47.2 MB (47161675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163a00859d47f645890acf4472c5048a743eac0767215dce1944e4a6c0c32b13`  
		Last Modified: Wed, 24 Jun 2026 04:12:35 GMT  
		Size: 135.9 MB (135910426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75450bd3c78fca6ecd81ea66593225ae43d49041e6279ec2e1ee3180d5b651d`  
		Last Modified: Wed, 24 Jun 2026 04:12:32 GMT  
		Size: 19.8 MB (19770022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67eaa1f6e2af76dda1836adc42ddebf2fcbcb3a2f68aeb5273a1a2e365911333`  
		Last Modified: Wed, 24 Jun 2026 04:12:32 GMT  
		Size: 4.5 MB (4515202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715aaa8252e6d026ffdbbbbea254f5e5c2e5370cd4a688946ad269284096120e`  
		Last Modified: Wed, 24 Jun 2026 04:12:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6ee698b215f21a8c28392a57cac8454d1adaf477d4b17eb79255d59a7a3f172b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4293570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440833321558a2d33cd9a49b946fa3074b37bead7be6b78b260e547081898750`

```dockerfile
```

-	Layers:
	-	`sha256:fb18d5609f2e25db04e86ae2dd0796242010fc526dd4b2b826e44e80dca154b6`  
		Last Modified: Wed, 24 Jun 2026 04:12:32 GMT  
		Size: 4.3 MB (4275832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cf15b41eb84f8770609d32a219a4b78ec8077807dc58f675506d0ad6ec6e142`  
		Last Modified: Wed, 24 Jun 2026 04:12:31 GMT  
		Size: 17.7 KB (17738 bytes)  
		MIME: application/vnd.in-toto+json
