## `clojure:temurin-11-lein-trixie`

```console
$ docker pull clojure@sha256:7286d873396c0fd0edee066c1eb1d82079fa7b38e9de8580b0bdcccc5216a33a
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

### `clojure:temurin-11-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:7448238e7e77c36c39e57d8c86758ad74d5f85239cd171f6a85636752658000c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218598833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993363ad0a907cce73391aea7c2c3ca67c1abb319ed1def5270259eb2764a916`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:33:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:33:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:33:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:33:23 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:33:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:33:23 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:34:39 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:34:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:34:39 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:34:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:34:41 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea298e6806ecf96faa70e607f40f6347ba840f58062fa49710743a379f2fcc6`  
		Last Modified: Tue, 16 Jun 2026 23:35:01 GMT  
		Size: 145.9 MB (145886219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c9daffb9137f0a55280672037d4d307139f10acf341cd856c605dc82e7a964`  
		Last Modified: Tue, 16 Jun 2026 23:34:58 GMT  
		Size: 18.9 MB (18880228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0ad1e23b6cb91209dbc14c8a8b6c4e8cacb30ad8e34a28c7c24d16aebae1ea`  
		Last Modified: Tue, 16 Jun 2026 23:34:58 GMT  
		Size: 4.5 MB (4515233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:62c03c513e6714e92d65df69ff701bf6e6837ee54d3057b0905d7f928fb82142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e509ee43e4744eb8926c5095bf194cd6d1275d98f1a447ed3585dac5b37bcf`

```dockerfile
```

-	Layers:
	-	`sha256:268262dd3f735a1f832d5ceffd068077820d703d16fd641f84553f41924a1448`  
		Last Modified: Tue, 16 Jun 2026 23:34:58 GMT  
		Size: 3.8 MB (3837336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d89dfea0743c5521def0839c028cf320ca28a540185c1d1dfebbb26ee0ecb34d`  
		Last Modified: Tue, 16 Jun 2026 23:34:57 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:82e7114f6ce8ad0233879ff757cc93114ee5c5ffc29a21bf1b330cddded242ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215615288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2892ee95d8589df7e3fda6f8844dd3fcf0def7c1fcb51c5eddadde65956ae6f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:33:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:33:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:33:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:33:03 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:33:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:33:03 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:34:21 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:34:21 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:34:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:34:22 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5bfa5ac058759b44f0f4a53651553615fe39fb1d52817df4919b7e23d1a739`  
		Last Modified: Tue, 16 Jun 2026 23:34:44 GMT  
		Size: 142.6 MB (142582228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb03f848f702f9407a654cf202c5875b3dd8e0aa0d5a01a293dc89fd498795e`  
		Last Modified: Tue, 16 Jun 2026 23:34:40 GMT  
		Size: 18.8 MB (18839677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cda1d099243a1ba4e16e0b7801c19c0986a70ab41bb984ab683ba12bffdf34`  
		Last Modified: Tue, 16 Jun 2026 23:34:39 GMT  
		Size: 4.5 MB (4515182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ee81eb512c82d1f3ba9500a8d57858e6a24cfda2e3d75f575acaa0cce4378a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3854049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9f63bcd03ea5f1f0dc0b51504efe9055a6123dbc532a9974a15f50e7d4a835`

```dockerfile
```

-	Layers:
	-	`sha256:210bf755fb64c5900a4d15ed67cfdbffdd71185ba61629056579e3a2a247c10f`  
		Last Modified: Tue, 16 Jun 2026 23:34:39 GMT  
		Size: 3.8 MB (3838194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41766eb57777f3493d026ae4f9693fd52966d58d6da293719f43a2a5491a3c71`  
		Last Modified: Tue, 16 Jun 2026 23:34:39 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:6e0401e12aa8129c62a3e1c276831ed994c8b21336800558408d6ae85d6fe13c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209699763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b7023afa849d83463fe9cad8cdb3077450a480941c5dbd5d8845699e16e4ed`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:38:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:38:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:38:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:38:31 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:38:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:38:31 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:41:33 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:41:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:41:33 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:41:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:41:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9aeff07095489e34872cfdfa559818f67e228c151dff7dfd27b88564211aa95`  
		Last Modified: Tue, 16 Jun 2026 23:42:13 GMT  
		Size: 133.1 MB (133110132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011e1ddf2c4571eda2f53babbdf8b614e03975068bbddc7897b87362b627df88`  
		Last Modified: Tue, 16 Jun 2026 23:42:10 GMT  
		Size: 18.9 MB (18936441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabdf4bd17b981bf0b60bc129239cdd58e19d3dbd305d50de9c2402e9505d599`  
		Last Modified: Tue, 16 Jun 2026 23:42:09 GMT  
		Size: 4.5 MB (4515219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:95cafda4859c717017392162ca25adf94178bb90e0a5393c77b3f9150d446d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4e83533689a1670711c75656fac0131fb23ba022fece0f9b81d782afc8e794`

```dockerfile
```

-	Layers:
	-	`sha256:6ea7dd097075afd715f6efd68b355c755274ec51f4df8c1ae0333d96e5479d4a`  
		Last Modified: Tue, 16 Jun 2026 23:42:09 GMT  
		Size: 3.8 MB (3837721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d360028a7a1e27ddde3226a2ab45f5634cf8b120c73f9a44dcae9c318a0abdb`  
		Last Modified: Tue, 16 Jun 2026 23:42:08 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:aec1c1596d59fb1ccde06b4b5fc29a9b75733189ba666e9fe2b8ddf3f23f0f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.5 MB (199474984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335e6fe07a3a11886ee0ccdaafbe6a6b5357959b53a5d1e1ddefda341878a50f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:32:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:32:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:32:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:29 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:32:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:32:29 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:34:14 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:34:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:34:14 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:34:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:34:16 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee59824b0dadbf20c14b9970d2181e7709e36cd5a52575ea50299c74207d4c8`  
		Last Modified: Tue, 16 Jun 2026 23:34:43 GMT  
		Size: 126.7 MB (126651735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fa11fc218e3e6c05a2874c519c694e1bc0fde7c9f9cbd7857c42de8ad1edd5`  
		Last Modified: Tue, 16 Jun 2026 23:34:41 GMT  
		Size: 18.9 MB (18922138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7eafae0b5324423366bd5f22f4ad05970aad807760f2d52466a6bdf4673d76`  
		Last Modified: Tue, 16 Jun 2026 23:34:41 GMT  
		Size: 4.5 MB (4515182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8b39b792e8688b5c47b066198da0ea02113fb9a2dd96f31707a765efed3e75cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ff6e6d1a2dd5b93c6e7bed6a016bfc36c7471c7cd8597a3d04672c3497498c`

```dockerfile
```

-	Layers:
	-	`sha256:23efbe9600a40fddf9423afc358550a0df11459461c6e9b65b9783a56154840b`  
		Last Modified: Tue, 16 Jun 2026 23:34:41 GMT  
		Size: 3.8 MB (3833767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fb2b3bec144dbca34d3f699ba567a7f970da50e0d3811b43defa4753f76030d`  
		Last Modified: Tue, 16 Jun 2026 23:34:41 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json
