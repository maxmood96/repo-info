## `clojure:temurin-11-lein-2.13.0-trixie-slim`

```console
$ docker pull clojure@sha256:cb78171cd09150288abaf857541a5ddd0754117d4f374eb93af68c1daeac0713
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

### `clojure:temurin-11-lein-2.13.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:eccb77d69451122ac2299bbbb008723a5d1b7b0b56b2dac91290a5592d565c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196929682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c447b99144ac47b77acea702f9218f6549c5b8586cfa258cb6578570406065`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:33:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:33:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:33:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:33:34 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:33:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:33:34 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:34:53 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:34:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:34:53 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:34:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:34:55 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9992eb1ce3395490f03bd6456c845112c2f000988d222deb324f8fd2e0b2f885`  
		Last Modified: Tue, 16 Jun 2026 23:35:14 GMT  
		Size: 145.9 MB (145886263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0867b0b6771baf9e3fa3363185b2a26bdd40ff813976ddd8b8b9c2ffc494c1`  
		Last Modified: Tue, 16 Jun 2026 23:35:11 GMT  
		Size: 16.7 MB (16742758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112a7b979b48d58169a4ec076b139c0a808ffd92d7606626a16d105bedc83167`  
		Last Modified: Tue, 16 Jun 2026 23:35:11 GMT  
		Size: 4.5 MB (4515214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:30a2ce80998eed5e7de51f159bbe626c7f30cad4d0b16047d40f50040a166b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1587df3ade2bcdab345cb37cb70d02607d6699bbcb3a4c2edb436c6ee96bdd9b`

```dockerfile
```

-	Layers:
	-	`sha256:3ac28b968aae7391791e34e7e51da89ccbd4e66ce57d8292e5dd13a9cf93dc8e`  
		Last Modified: Tue, 16 Jun 2026 23:35:11 GMT  
		Size: 2.4 MB (2386597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8128333d2c9cee3c31257789ba5fb597f9dbd4593c415e9c015094c275e4ac4c`  
		Last Modified: Tue, 16 Jun 2026 23:35:10 GMT  
		Size: 15.8 KB (15764 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.13.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1c4312ba4d8b18924e9c90b01534b392e251be1a8816d65bda993696b21b7c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (193957327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea10ae7bd073bc0aa8b425b15e644a8bbb66179907dd813803004c303107ee19`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:33:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:33:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:33:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:33:14 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:33:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:33:14 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:34:33 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:34:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:34:33 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:34:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:34:34 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfcff2f835840f10727f839d599d89eb86426b2738d139cf166e6800c70c05a`  
		Last Modified: Tue, 16 Jun 2026 23:34:54 GMT  
		Size: 142.6 MB (142582200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0c7f843b5289b27ef44e8bf809ab668ca81e49b9755262d117f05b004de305`  
		Last Modified: Tue, 16 Jun 2026 23:34:51 GMT  
		Size: 16.7 MB (16711379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5f5f1807f8b80c5374d9ba4b0cb0834be24cfecdbda62151ffc098e72a83ec`  
		Last Modified: Tue, 16 Jun 2026 23:34:50 GMT  
		Size: 4.5 MB (4515186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:17def81b5fe43d192b708b1f1a2d531d464b60ac8162b6654d9bec4c21bd5c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e35231c718a99e5fea809aff8883a1ae151836ffaae4168cb58420932c94bc3`

```dockerfile
```

-	Layers:
	-	`sha256:d970e2800955970040236abf0c81f9295a5de510947956d284cba0d0a1bcdb5e`  
		Last Modified: Tue, 16 Jun 2026 23:34:50 GMT  
		Size: 2.4 MB (2386825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bac003f9c0e8e6f5b084c5050b072f2d57a1fd16de6083c8ba6b5acc0799d471`  
		Last Modified: Tue, 16 Jun 2026 23:34:50 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.13.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:84211a6233a36fb4dc3fc1b8397c0d237d53d1763ebba731c1db96f5376d5c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188013735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8b1a9e73fefee4c1a2f243b60dde74ae8e725a67c85a878015cc5d656655f9`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:41:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:41:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:41:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:41:00 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:41:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:41:00 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:44:01 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:44:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:44:01 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:44:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:44:04 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3943f8bbc6fdcb6836564ab0edeb292a8256bcd9f0f493c987dd19dcccbd8d2c`  
		Last Modified: Tue, 16 Jun 2026 23:44:36 GMT  
		Size: 133.1 MB (133110125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076deda243a7a48ff579e0119d4db248eaa8dbcfd14cf968dd22f514161b8319`  
		Last Modified: Tue, 16 Jun 2026 23:44:33 GMT  
		Size: 16.8 MB (16782014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a522fac140c3a4800ed22e7be6d7d88edc9f134d17e83fbf43ed790540d7a6`  
		Last Modified: Tue, 16 Jun 2026 23:44:33 GMT  
		Size: 4.5 MB (4515224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b49245ba5c6c9747aee41f5c2f55caad31b1ad24ea3404f699b5026802bf55d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ec50500393d817f18d19c7ef9d2a5cb83e2c9bb6685e826cc89bb545cd5996`

```dockerfile
```

-	Layers:
	-	`sha256:42406da00838a974019e1c351dc5609722018809e117be2f76b2b73638827174`  
		Last Modified: Tue, 16 Jun 2026 23:44:33 GMT  
		Size: 2.4 MB (2386962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e55f1972b56763b98da33b1a5fcaa06b12b874308a57abdbaece9e6d346211a4`  
		Last Modified: Tue, 16 Jun 2026 23:44:32 GMT  
		Size: 15.8 KB (15808 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.13.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:74283f73610e07cc34480995dfa2e3257639b9f28a046dabc097dc6530261761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177798442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c687efe6884bd2df7031c2f94e91815e3210c55253eb2f8b8c6aaf65bf3eb8`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:32:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:32:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:32:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:31 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:32:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:32:31 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:34:13 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:34:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:34:13 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:34:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:34:15 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b37f7ca2620fa8034b4c758473d8f6dab5ab72faa3511f54f5250cfad8fd1f`  
		Last Modified: Tue, 16 Jun 2026 23:34:40 GMT  
		Size: 126.7 MB (126651739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66171aee5e186413b63e3c2c8c2cd4c30da9b5efadce6fbd3d9165fd29e961d0`  
		Last Modified: Tue, 16 Jun 2026 23:34:38 GMT  
		Size: 16.8 MB (16780109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b10776c4b80e1998d866ffbdf6c571606753702b104e82003409277f7d9c8f`  
		Last Modified: Tue, 16 Jun 2026 23:34:37 GMT  
		Size: 4.5 MB (4515208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:baee2f3b8232e67826d7f8ee02b1524e1985eb94acc62dff9b67b4d5e4b7ba6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4305158aee4f8965c11593c450d3cd7fc575f877efe17818486c28f64468832`

```dockerfile
```

-	Layers:
	-	`sha256:8c5b2d961f9ad26b11f42de7a5ce33ba5a3ea38e2f4a88a1930e6baeb3bda41a`  
		Last Modified: Tue, 16 Jun 2026 23:34:37 GMT  
		Size: 2.4 MB (2383028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d223a19df3755d486f84962346d95a571eed0443d8c85d5e86ba58e5f3ec6875`  
		Last Modified: Tue, 16 Jun 2026 23:34:37 GMT  
		Size: 15.8 KB (15764 bytes)  
		MIME: application/vnd.in-toto+json
