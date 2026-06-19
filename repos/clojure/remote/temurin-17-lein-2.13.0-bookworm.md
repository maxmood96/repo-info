## `clojure:temurin-17-lein-2.13.0-bookworm`

```console
$ docker pull clojure@sha256:c7dd41abdb8d27b5cc4e3a3b11cb9ef3b169f210e28c30ce97953b7cd539c52f
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

### `clojure:temurin-17-lein-2.13.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:3090ed128957f13d5adb2bbdf573d1ff50545a799ed99f2f5bd32281094691c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (219030549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d2065305592aa7237092279b1ceb6a8dd5dd38342a186eb327e8832c39a207`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:16:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:16:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:16:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:16:45 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:16:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:16:46 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:17:52 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:17:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:17:52 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:17:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:17:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:17:54 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:17:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f859d1c7ae0704a62e9f294bb0683b8cee90530ff3675310c7a42085d3d092`  
		Last Modified: Fri, 19 Jun 2026 02:18:14 GMT  
		Size: 145.9 MB (145905426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f977cade78cad898b9355ca9c26159d338e8a6571a7f1436ece98aa5bcf2a04`  
		Last Modified: Fri, 19 Jun 2026 02:18:11 GMT  
		Size: 20.1 MB (20107436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c19927ba30d61ceb3581d28b58e96f8fc42517fa6da050b430ef46ec3c8dc76`  
		Last Modified: Fri, 19 Jun 2026 02:18:10 GMT  
		Size: 4.5 MB (4515215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adece955e2db5d4d43b854f535a8ecb3252eee505e55d657c826e540dd08f116`  
		Last Modified: Fri, 19 Jun 2026 02:18:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ee7d896cf4b40cff81a999a5265e15a481516d33a383b2a9aa7a754bdca9c3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4301756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff56b4724bef75e526c52e455e9c2965799fe48bc4ceb780df4d9901a233f4a8`

```dockerfile
```

-	Layers:
	-	`sha256:725449fd1ad1a53d61805904829e992282e591d84569c54d4f87f37f85c5046c`  
		Last Modified: Fri, 19 Jun 2026 02:18:10 GMT  
		Size: 4.3 MB (4284018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6210a82cf4639dfc672cebffbf9cb4bfc7bfb7cfce0e11c96d5e6b28b7316f44`  
		Last Modified: Fri, 19 Jun 2026 02:18:10 GMT  
		Size: 17.7 KB (17738 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8c6af54d580847c0bd4ba0be5b1c9f318c703f5a04de736addadc536b65020b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217568895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b06d9915b021c6d3c356fbe6245eff61969eb2bba6f58f92ae0a1ae3149105`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:16:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:16:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:16:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:16:51 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:16:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:16:51 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:17:58 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:17:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:17:58 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:17:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:17:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:17:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:17:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261c4d9511247b730cc59c1f2d8f4263a82ad48df23abd9174667861e699a5e6`  
		Last Modified: Fri, 19 Jun 2026 02:18:21 GMT  
		Size: 144.7 MB (144724298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3523b384ed243fcf66111211797fb3f4f4c345ffed6e0c01f8115486233fa4`  
		Last Modified: Fri, 19 Jun 2026 02:18:17 GMT  
		Size: 19.9 MB (19939971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae16a6edafbeb3e58e10115e3361cd15fa39713082af15c72c63799e8a9b684`  
		Last Modified: Fri, 19 Jun 2026 02:18:17 GMT  
		Size: 4.5 MB (4515181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79998f99bc0b1aa97ba64857546bb063766895262b5eee5671948b99075433c4`  
		Last Modified: Fri, 19 Jun 2026 02:18:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e7277a1d9b669884f28a025015b45c288d2072706df38dc419f862afd2da8c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4301492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49429728dd46a19ce1846943f57b7b7eafe1f434eddf3e95d357643abaa9d319`

```dockerfile
```

-	Layers:
	-	`sha256:ec5f63ace04016c3e4cb3d1e3d7ccf9dd47aee03267ef8823aa5f7e8a328d7a7`  
		Last Modified: Fri, 19 Jun 2026 02:18:17 GMT  
		Size: 4.3 MB (4283633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe79acaf3c1928688f218853cad98f84eb2dfd96ec352d9d13ffc650309bdfe`  
		Last Modified: Fri, 19 Jun 2026 02:18:16 GMT  
		Size: 17.9 KB (17859 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-bookworm` - linux; ppc64le

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

### `clojure:temurin-17-lein-2.13.0-bookworm` - unknown; unknown

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

### `clojure:temurin-17-lein-2.13.0-bookworm` - linux; s390x

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

### `clojure:temurin-17-lein-2.13.0-bookworm` - unknown; unknown

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
