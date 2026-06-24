## `clojure:temurin-17-lein-bookworm`

```console
$ docker pull clojure@sha256:c770a97f191948fc3bec03cb9cb7c0e68b58397f365d4c8d98a674d93a095d72
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
$ docker pull clojure@sha256:766facdc9e7e35dcbd8ec01304f0980db49b37a9313e19d7c2bfac4cfd81412e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222961141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a153e1eb13761fe624bafe7faffcdf12a66ac62efbd018c04a6d573be965c2d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:36:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:36:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:36:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:36:44 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:36:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:36:44 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:40:04 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:40:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:40:04 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:40:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:40:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:40:09 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:40:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011a8b1fe08cbca6cfbf84dcf1035227586f8c0a013a520d08ca8f1bb6f1baa7`  
		Last Modified: Fri, 19 Jun 2026 02:40:33 GMT  
		Size: 145.8 MB (145766212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde958ec6996a952c04f47df124758d009d89f9b25f8e0d7f5aae426a3606476`  
		Last Modified: Fri, 19 Jun 2026 02:40:48 GMT  
		Size: 20.3 MB (20332596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48b6988151fb5eda532aa3c25b1509e309ce338a4f79d6846fc8a2d91484179`  
		Last Modified: Fri, 19 Jun 2026 02:40:47 GMT  
		Size: 4.5 MB (4515233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f974549e4cac06ff039cdf5017785fac4a2d7aedae6e607b61fe439b66e845`  
		Last Modified: Fri, 19 Jun 2026 02:40:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3cdefbf2cd47b32f89cbd72fe822a867de35a2932484247fffdb7bea090e1fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a8f283dc7337c872c9f65b84d56645184ad1cdbcdfbf72fa3ef7d16d437207`

```dockerfile
```

-	Layers:
	-	`sha256:fd4a795d1779707031964eb7af2a92af00f7dca12dde99a9acdd8a050c751ad2`  
		Last Modified: Fri, 19 Jun 2026 02:40:47 GMT  
		Size: 4.3 MB (4285879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:323aa560ba19d5c3429ab5cf495e150f51712da318be73c311f07b5d3481a20c`  
		Last Modified: Fri, 19 Jun 2026 02:40:47 GMT  
		Size: 17.8 KB (17782 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:a7e4a90a2d9d79b6ba406d4cca5eb284470631d813acf08c4850ea40728d616e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207357786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efaae53e1ae2494649e187c8430a8b969a78a74114ab5d3496db5f6720ac0424`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:16:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:16:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:16:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:16:23 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:16:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:16:23 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:17:26 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:17:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:17:26 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:17:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:17:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:17:28 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:17:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467d2d4124b27f04294aa8517fbb889a4ab8a600258034f2ee7ff580572fcc74`  
		Last Modified: Fri, 19 Jun 2026 02:17:55 GMT  
		Size: 135.9 MB (135910421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2148cb2af586f495a3e346f298bd2d7f8bcdff55e959b5dddc110247a54744f3`  
		Last Modified: Fri, 19 Jun 2026 02:17:52 GMT  
		Size: 19.8 MB (19770225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a502a7397a46fffc03fb0a2027f06e8f4420fadcc7d22643aa44c4633bc8ce`  
		Last Modified: Fri, 19 Jun 2026 02:17:52 GMT  
		Size: 4.5 MB (4515211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d011decccfa32bd23331e272c77f5647b53a5a79a7a0d06f5b83f3535857fb1b`  
		Last Modified: Fri, 19 Jun 2026 02:17:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7402df28b00d21091d8eebe3b1015091a93a287e048ddf5abaf5918e88eca011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4293570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8ddc08a061a87dd33ed377927a7e6b8e252112210267f74eb85303e8951828`

```dockerfile
```

-	Layers:
	-	`sha256:92f0feec8a639ae9fb1940e8d8eff2b6e812dc92b0ed3a54d6d1e48ef26f1067`  
		Last Modified: Fri, 19 Jun 2026 02:17:52 GMT  
		Size: 4.3 MB (4275832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:143649db6a0bd326b518df3293b59dfd2a3728a65bbc207fe684b5077cc1ce04`  
		Last Modified: Fri, 19 Jun 2026 02:17:52 GMT  
		Size: 17.7 KB (17738 bytes)  
		MIME: application/vnd.in-toto+json
