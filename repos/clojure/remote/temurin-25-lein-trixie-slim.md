## `clojure:temurin-25-lein-trixie-slim`

```console
$ docker pull clojure@sha256:8fa80eb0d29396590c7b86921948d03695d69ff22706749091ac487891930374
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

### `clojure:temurin-25-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:aa58ace8ceb8faf451721afb1ea08b75d4c964d99a2c75b9a022248a1c021226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143619068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2674ce776a18ef756df9786faccb1cc38b00214a107284efda56e0cfe75035`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:43:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 01:43:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 01:43:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:43:26 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 01:43:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:20:50 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:22:04 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:22:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:22:04 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:22:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:22:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:22:05 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:22:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542e6d11ff1562bdaecf08153eacd5e05cc4683dfdb22cf950d5b45b99af2554`  
		Last Modified: Wed, 24 Jun 2026 01:44:21 GMT  
		Size: 92.6 MB (92574577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04be1abb5d0e704042eeb1f5d536ccb27c0030b1a428f2404e45623c8aa3c2e1`  
		Last Modified: Wed, 24 Jun 2026 02:22:15 GMT  
		Size: 16.7 MB (16743464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0fa544988b23c15030ab72e6de851c410047151f6765b0d071ca35f2652c13`  
		Last Modified: Wed, 24 Jun 2026 02:22:14 GMT  
		Size: 4.5 MB (4515178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6a35455734c4d570c7870e3ae351686b4814a722bc5e7ee5ec03e514333aca`  
		Last Modified: Wed, 24 Jun 2026 02:22:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ef725b9d795da9d0633c7c7b789506f03b00c1dd0d80049e6a5e09849309f8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2352576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2b188c67309eba51d961f231411d2b5ed957535823ab2fdf35001c7093836e`

```dockerfile
```

-	Layers:
	-	`sha256:bc03858dc9af64c5e9e4398309b85de932a48cf25247bdae6728de13b86bba71`  
		Last Modified: Wed, 24 Jun 2026 02:22:14 GMT  
		Size: 2.3 MB (2335129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fa9dcdcb871ff76226f37d6aaa8a70606679c85ec588b0e171641b8826c88ce`  
		Last Modified: Wed, 24 Jun 2026 02:22:14 GMT  
		Size: 17.4 KB (17447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:79666957e43ecab13400483943956d3392b89cf0f15114744d72e2c0d7b5bb38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142917874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8e6118f4ca1ef772038b026cabb14f48d55d47ea1340f3502a8fe438705bff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:27:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:27:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:27:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:27:40 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:27:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:27:40 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:28:56 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:28:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:28:56 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:28:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:28:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:28:58 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:28:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fdcf5e0ce5cb83e0feebbfe96049b691bf38d771214561b002dbda2fd15b56`  
		Last Modified: Wed, 24 Jun 2026 02:29:16 GMT  
		Size: 91.5 MB (91542238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44769ddc34488eab678df01ea761cfe419ab5b218029d7161d2828ef35d035d`  
		Last Modified: Wed, 24 Jun 2026 02:29:15 GMT  
		Size: 16.7 MB (16711444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0755a522a308983aebe688c34fdd93a78da82cf89b1a6aae8b69af53a595e546`  
		Last Modified: Wed, 24 Jun 2026 02:29:14 GMT  
		Size: 4.5 MB (4515211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02846e63b793b88d4bae72d625e781e3e4f56b3ef3287d08c37262e905a3c940`  
		Last Modified: Wed, 24 Jun 2026 02:29:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0376491f4f357135af3aeaf4c8aac4457303a50438e0135f262a2eeb44bdc612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2353305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca58b3705cefc24fbf464c149b1ac8398f65ac7980d4607fc57748db540bf814`

```dockerfile
```

-	Layers:
	-	`sha256:65e8dff47e1805d5c319c05a87fa366ae23c7c4920ad777bb7f2cfa2e4605215`  
		Last Modified: Wed, 24 Jun 2026 02:29:14 GMT  
		Size: 2.3 MB (2334760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fde1b7bdedb151c831d99fe051b2e1bf6089c856e08f27f68acddea029d50e7d`  
		Last Modified: Wed, 24 Jun 2026 02:29:14 GMT  
		Size: 18.5 KB (18545 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:5d8d6dfeff1c60ac64ad31e756318e3af0ebcba694101a08f669c29797759474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146818032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1d4751e895eb6794b08dff4ce5c5061b054206f82ada29e49c11e754d738de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 00:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:06:39 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 17 Jun 2026 00:06:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 17 Jun 2026 00:06:40 GMT
WORKDIR /tmp
# Wed, 17 Jun 2026 00:09:21 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 17 Jun 2026 00:09:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jun 2026 00:09:21 GMT
ENV LEIN_ROOT=1
# Wed, 17 Jun 2026 00:09:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 17 Jun 2026 00:09:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:09:26 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:09:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d2e9d705b633c31ee18ff0b56f7ec3ad425fb9e720182ee7a6e0f18d85842b`  
		Last Modified: Wed, 17 Jun 2026 00:10:02 GMT  
		Size: 91.9 MB (91914009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3988b62f6dd5c16c60ee94f04dcead13d040bed1810bbf54c9907675c924824`  
		Last Modified: Wed, 17 Jun 2026 00:10:00 GMT  
		Size: 16.8 MB (16782071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f8d12b51dd2c6f9a710a18a1f0946a97b2523fb8e369a2f5b33d0235d12650`  
		Last Modified: Wed, 17 Jun 2026 00:10:00 GMT  
		Size: 4.5 MB (4515183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf5612caefc5410b0abbaa5d6ae3595e18033ca3bad791686e4baaf114524f7`  
		Last Modified: Wed, 17 Jun 2026 00:09:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9610db639ab710362803c8652183232d53e30e533a5ef9b3b2a9d383e2fcad0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2337889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58bfd436dee6daf89b6de1938f0f1830c2fd4b56063e18bbb964d6bf726cc2ae`

```dockerfile
```

-	Layers:
	-	`sha256:02e403082a3367f1fa414425dbc67156c393600c3db9a1920bab119dc3ce43bb`  
		Last Modified: Fri, 19 Jun 2026 02:54:48 GMT  
		Size: 2.3 MB (2319433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:662fa6604b9b4b1e8362855b68ed993bcf2e1e8ac4e845c9f4a409c54cadbc3b`  
		Last Modified: Fri, 19 Jun 2026 02:54:48 GMT  
		Size: 18.5 KB (18456 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9fd517535c950259cee7f17959b60f1db687c789d0777c5b82052fec6acdbff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139567601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6cc15e7be28f848ccac9944e2171e5f473b0f978de9cf6bacec556ba23ca058`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:41:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:41:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:41:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:41:05 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:41:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:41:05 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:42:20 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:42:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:42:20 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:42:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:42:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:42:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:42:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e141af4c3ca44d66006c21b5229d05180427e764c0a36b8e43c72eabd028a0d`  
		Last Modified: Tue, 16 Jun 2026 23:42:49 GMT  
		Size: 88.4 MB (88420336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9482dc5ca9b3004f09343d4ce9ae3958ee894228c4da1f267f4fa53ae4abfa99`  
		Last Modified: Tue, 16 Jun 2026 23:42:48 GMT  
		Size: 16.8 MB (16780293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caa99a45afcafb0138e9d3acc27e1bfe26dbd1ad2e3e852c0a7d799975b000f`  
		Last Modified: Tue, 16 Jun 2026 23:42:48 GMT  
		Size: 4.5 MB (4515188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb688b5872adfb62fd1e33e9c76623052ce9fba6e98aa98107e73969a471bde`  
		Last Modified: Tue, 16 Jun 2026 23:42:48 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dabdcad02945efa80e6a17d320493e67ee016abbb66cdfd1121786485dca9025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207625bd68e348d9a9521eeb4854111384439bd87ff55d45c00d1ef021711f0d`

```dockerfile
```

-	Layers:
	-	`sha256:8a7963e074e4de31f786e63a1aa8f3f11debc72ff7ded49964ad6abb518e0558`  
		Last Modified: Fri, 19 Jun 2026 02:21:34 GMT  
		Size: 2.3 MB (2316118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b37f8445c407549cda68db25e4bc8180b41c19d3a66036e37556141793b99d8`  
		Last Modified: Fri, 19 Jun 2026 02:21:33 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json
