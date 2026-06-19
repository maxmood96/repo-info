## `clojure:temurin-17-lein-trixie`

```console
$ docker pull clojure@sha256:638a2beb3a25491a6fe4750e5beca46fc34ee36944dd42dccf7225e3bb6fa2c9
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

### `clojure:temurin-17-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:1115458069bc3ba5cb08416683edef6b44fb62ca14c6a82ddcb7d6135539ead0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218618151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95845038566df2fae279a4324ce4c5a41622f8c51e59097a05d2a31866fc83ff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:16:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:16:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:16:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:16:55 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:16:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:16:55 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:18:07 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:18:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:18:07 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:18:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:18:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:09 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a59815f07d195238fbc5411c5f60523304f0417ce5c51ede29a900843da00b6`  
		Last Modified: Fri, 19 Jun 2026 02:18:22 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d725c657a9bab2b6c440e782b1cd02831af2fe059717ee04c9e1dfcf4e6228`  
		Last Modified: Fri, 19 Jun 2026 02:18:26 GMT  
		Size: 18.9 MB (18879968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a276cfece5f1c9415f56e5ce18e8514d285d27a11c3e3a5cd48c1d7d294115d`  
		Last Modified: Fri, 19 Jun 2026 02:18:26 GMT  
		Size: 4.5 MB (4515178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bdc5bdf966a89c8992a296657a55412ed4f53a76d8d9a0dfbaaeaceb3f42f5`  
		Last Modified: Fri, 19 Jun 2026 02:18:25 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fca1e83b4e9a4afc96214d6c272d8c33fa0a7dd3e0bfd9ebbc0dfbad7448ab88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1bb59ac293010b4ae9270933ad55b15efb8f9be328942a267c6ac1fc2edc88`

```dockerfile
```

-	Layers:
	-	`sha256:9f571899cee435c2a2f3de030426d210e3f1addf1f880df9bf6255540db8fdfa`  
		Last Modified: Fri, 19 Jun 2026 02:18:25 GMT  
		Size: 3.8 MB (3817820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0382ab25f7058225704073cb14e80db5ac75e0e20fe01e81f51d2ff3a21a61a2`  
		Last Modified: Fri, 19 Jun 2026 02:18:25 GMT  
		Size: 17.7 KB (17717 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c2c687d1e6c14f01fa2b3202e5b5d39619d709defb99add88bb727b38cc3fdb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217757733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f99ff1ff0577e921371e337b4bfa89880b2185f1de93520762df9fb9088d5be`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:17:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:25 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:17:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:17:25 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:18:41 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:18:41 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:18:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:18:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa2a4971a145162dee290fd0c41bdf60433a78b7ee956f0531e12bd04609e2b`  
		Last Modified: Fri, 19 Jun 2026 02:19:04 GMT  
		Size: 144.7 MB (144724303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77658d9f0b9dcf4d8dd22cca825835bd0f8f5561e97be9b45e798266767c4b5`  
		Last Modified: Fri, 19 Jun 2026 02:19:01 GMT  
		Size: 18.8 MB (18839637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7fe45453895c4820c6a1679525c351c8d2d5647d09d019f2ba7061f0d21a38`  
		Last Modified: Fri, 19 Jun 2026 02:19:01 GMT  
		Size: 4.5 MB (4515195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd5b5880b059a005a1af9dfda015e71e88c914093d4cb7e9ee1c8cc6d2908f0`  
		Last Modified: Fri, 19 Jun 2026 02:19:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a845a08ddd29c655f0068667473b9f2962e56bb328397de113f28c553c4d77d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3276cb02bd6ffb29e9ba5103f33f0519c145ce313b25cf1a0b6ff68d89767856`

```dockerfile
```

-	Layers:
	-	`sha256:71bb2b19ca979c7439001534e70c106a4d98ba75524323938ae421e5c8626033`  
		Last Modified: Fri, 19 Jun 2026 02:19:01 GMT  
		Size: 3.8 MB (3818060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3df3f73398011b780a419a40a6095204c463040357a10a8cf2f623ae768d3a1`  
		Last Modified: Fri, 19 Jun 2026 02:19:00 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:df8e9dc40857c3f980459bf8e73b053da3ddd751afa8d715e35c4b5290c7017d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.4 MB (222356447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001ec24b104d058da3b41b786b5c830f3072dba17fb59a586a4c65654b1f0b71`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:40:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:40:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:40:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:40:48 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:40:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:40:48 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:44:06 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:44:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:44:06 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:44:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:44:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:44:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:44:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4c522651359f2b9382194c5170132137b32f6d0214c41d2c39ba3ec770a8cb`  
		Last Modified: Fri, 19 Jun 2026 02:44:52 GMT  
		Size: 145.8 MB (145766191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd274513b420e4bb3a0ecb58544c5242815ebed9ed6da61d5bfea5218b8f7db4`  
		Last Modified: Fri, 19 Jun 2026 02:44:48 GMT  
		Size: 18.9 MB (18936669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f329c88d6e76266b37eadf4693d273775fd1d92445c57e2df132c84e9061e6ce`  
		Last Modified: Fri, 19 Jun 2026 02:44:48 GMT  
		Size: 4.5 MB (4515218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e16c408a81fb540b5029c73f97c3042d48349864073f488b7eaddd8e535668`  
		Last Modified: Fri, 19 Jun 2026 02:44:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c392c3a400788c6eb6a81b8813948b7cee4e5a7a3512ce586b83d884aaacec90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba206f20a93d01872f287803c4a4bb4e6064cbb91d385477e860449debf292b`

```dockerfile
```

-	Layers:
	-	`sha256:0de40abeabe438a5fa8ef4946a361b0339580868efb3e2163873394bcab2386c`  
		Last Modified: Fri, 19 Jun 2026 02:44:48 GMT  
		Size: 3.8 MB (3818820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1361fd3fafae2440e8a9c044ffe7a0aa626d8fb3ceb36d3d2be7b09b48444746`  
		Last Modified: Fri, 19 Jun 2026 02:44:47 GMT  
		Size: 17.8 KB (17761 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:2f817ecfc24c7b1fd7242361049946777bdde26ebb32695211f93d7505a878da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 MB (208733613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b537847f88c54047854582e5b2851f0be53a962a69323037835b4969d35bac09`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:17:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:08 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:17:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:17:08 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:18:13 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:18:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:18:13 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:18:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:18:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:15 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918861cf680bf2b5b17504c84afdec10f9b09d3eb5a7a38387c5b5ff00597b16`  
		Last Modified: Fri, 19 Jun 2026 02:18:42 GMT  
		Size: 135.9 MB (135910421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0d0860299cc28b2ad7db9c66dcc3942a643846b0bfa4866351c0513871e343`  
		Last Modified: Fri, 19 Jun 2026 02:18:39 GMT  
		Size: 18.9 MB (18921657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f994c9831527e3e8b51f92035e8377fea6c30c14b517a517e478b7a9cd214a5`  
		Last Modified: Fri, 19 Jun 2026 02:18:39 GMT  
		Size: 4.5 MB (4515208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e411343b561ee7472ab46c33bc6da45effe1f2e2ca4b23a4f94d84600bbd21`  
		Last Modified: Fri, 19 Jun 2026 02:18:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:72f1062be14c8476f451118a973c1e3af2e3e4a0a08cbdc57cba149cc6c77d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec00a3b51e0c46e8200e3dbf8072f61b0ea041e15531b949e8061b984602b4ad`

```dockerfile
```

-	Layers:
	-	`sha256:7be6b085f0539098e513d73a14d3ccf9db84911c2904e94835d34468cd2217d8`  
		Last Modified: Fri, 19 Jun 2026 02:18:39 GMT  
		Size: 3.8 MB (3814247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e35b492aeba498d165e86196cb89391592ac25d43456e09424b26c2133a629`  
		Last Modified: Fri, 19 Jun 2026 02:18:39 GMT  
		Size: 17.7 KB (17718 bytes)  
		MIME: application/vnd.in-toto+json
