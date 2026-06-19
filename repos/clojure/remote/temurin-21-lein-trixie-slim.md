## `clojure:temurin-21-lein-trixie-slim`

```console
$ docker pull clojure@sha256:86e0ebbb7f17ce90fa3fd0c17c27c428b1d2504e3eb432ceae7db0f621fe9a17
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

### `clojure:temurin-21-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:73325bc297028e6f206ed4f6683205713b6f289ab1293dfd29b211b9a4b0701f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.2 MB (209211146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dfef85b371deab4d77adb8f8e36fd57c57ea64862edc5f23f77120cfa7bdd6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:18:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:18:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:18:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:18:37 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:18:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:18:37 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:51 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:19:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:19:51 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:19:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:19:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:53 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db1a6e0e6591a4bb90ad99c14d09a14421b9a83d79f7eb2778ec6bfd0dd0dbe`  
		Last Modified: Fri, 19 Jun 2026 02:20:12 GMT  
		Size: 158.2 MB (158166967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69763692d1378b630b26d5f3233b7df564a61cc72ff391906678abeba379586`  
		Last Modified: Fri, 19 Jun 2026 02:20:09 GMT  
		Size: 16.7 MB (16743148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21197f7ba035dea98d926e4178f521dc4c86cd0185d1e56fd82f4ec333cedc31`  
		Last Modified: Fri, 19 Jun 2026 02:20:08 GMT  
		Size: 4.5 MB (4515186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fa4b9d10bda9d1953a917b811043d5a15195724bb152888f7a9daf39e5f10e`  
		Last Modified: Fri, 19 Jun 2026 02:20:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7377677c6dc1ee60f81f0d05dca52a1c26c99b1618650904fb670d7568d87886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b85b5caafdf180c8690eebad20513d256304c6fbe473ebc02d2cf51c761079`

```dockerfile
```

-	Layers:
	-	`sha256:f886639193509351c69f89b311c54d6cd2dd1eb7b5aef7c7bdd14f2d1057f309`  
		Last Modified: Fri, 19 Jun 2026 02:20:08 GMT  
		Size: 2.4 MB (2368933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:014c0b133a6d3edea164b2a0008d1f64f51c4f95b3b860c0708a90ff1cf32b42`  
		Last Modified: Fri, 19 Jun 2026 02:20:08 GMT  
		Size: 17.8 KB (17753 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:630d33b2c0e86383fbbdcd916e6ceae4a30ae7c1ee1719d70d927f93a31f1d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207836957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7156d02548e88e9e296c3e874ad81e11802651861df3fe0a0b1ad2b440e14110`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:18:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:18:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:18:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:18:54 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:18:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:18:54 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:20:10 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:20:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:20:10 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:20:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:20:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660a2a4817dba3f2dcad876da76b1899f1ca3606eb8b52c95cb4a7dc7533665e`  
		Last Modified: Fri, 19 Jun 2026 02:20:31 GMT  
		Size: 156.5 MB (156461275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4215bec19918abde568c4a484467755688b9bed71450a95bdf579c12b45529f2`  
		Last Modified: Fri, 19 Jun 2026 02:20:28 GMT  
		Size: 16.7 MB (16711548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfb126b590ac36cae91b07eba8b655f9a10cb918e4fb1741542f4babdacf912`  
		Last Modified: Fri, 19 Jun 2026 02:20:28 GMT  
		Size: 4.5 MB (4515174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7134681397319f16d6e1088e12e58386097194bc1cf6baa17ca6e9d114903e`  
		Last Modified: Fri, 19 Jun 2026 02:20:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:888533f08343a7c5175a27b83381c2ccfa3c02dc3734ec52f343dd4601bb54b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d6e7c1c8bda1f02eabbdb10ecf9a5c04795e64f4f32d211e45dbf0abf791db`

```dockerfile
```

-	Layers:
	-	`sha256:aecdfcd144b49949aac734b97b9963befcf9976e80e6f7716154b9d945e41126`  
		Last Modified: Fri, 19 Jun 2026 02:20:28 GMT  
		Size: 2.4 MB (2368543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ca406df372b6dbc6227a4e3125e5486f0d9c0bb32b6c7af94830dbda2cb4a17`  
		Last Modified: Fri, 19 Jun 2026 02:20:28 GMT  
		Size: 17.9 KB (17874 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ca9f1d85bf4dd3270795906adbc3768bb7d091aab3cac18d9ed0c25933f1fa22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.2 MB (213247590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0dae320f65ea2e165e33a21f74c0cd964133416c8ea39d69d3bca18819856fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 00:00:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:00:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:00:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:00:47 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 17 Jun 2026 00:00:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 17 Jun 2026 00:00:47 GMT
WORKDIR /tmp
# Wed, 17 Jun 2026 00:03:27 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 17 Jun 2026 00:03:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jun 2026 00:03:27 GMT
ENV LEIN_ROOT=1
# Wed, 17 Jun 2026 00:03:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 17 Jun 2026 00:03:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:03:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:03:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cae30f60cd0ec6ba95234bc9baf8b715de9cca5a8c7483a3f4eebc08e9456b2`  
		Last Modified: Wed, 17 Jun 2026 00:04:10 GMT  
		Size: 158.3 MB (158343250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecab9349ceb2918e3b2fb0e2a1b9bf4bc3113ebdb9f963e67d351f15e9835c9`  
		Last Modified: Wed, 17 Jun 2026 00:04:06 GMT  
		Size: 16.8 MB (16782386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc85fb5220f648344b5a97a51eda13fd644755fb75eafdd40b1a03353c9f5fe`  
		Last Modified: Wed, 17 Jun 2026 00:04:05 GMT  
		Size: 4.5 MB (4515185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1132a529849969ec5395c2ad6eae1493086320b0c51cb6cab5f46bc82318cb`  
		Last Modified: Wed, 17 Jun 2026 00:04:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3d7ae192d531927d07479b3493722f0311ac0ef00660432b2e3a4222ca706173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a167a8a3f7feaccfa7473691e0c485f88f1de577bac45ba90b6a4a2a86f89d95`

```dockerfile
```

-	Layers:
	-	`sha256:7c1691c05d4dabb3b777bccf65fc52ffd6c6b5c89cdab954031be24e4dfec246`  
		Last Modified: Fri, 19 Jun 2026 02:49:51 GMT  
		Size: 2.4 MB (2369913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9bcba48519054cb51f96c99343c7573230e603b696ff7bc53e5881b60766a96`  
		Last Modified: Fri, 19 Jun 2026 02:49:51 GMT  
		Size: 17.8 KB (17796 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:520ab8bb2c7fe804e301e336b2e69eed84ff5be5a25da10c252738b09ba50809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198535018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695212a4f4b938a7d61f0a95291b67b7f1c6b795b72c795be987b17366a3a3c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:38:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:38:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:38:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:38:51 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:38:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:38:51 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:40:04 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:40:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:40:04 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:40:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:40:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:40:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:40:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66d9375a62e658d5255a5581f80c6f86b82e7d20e6a5c6878c2e0220d54700`  
		Last Modified: Tue, 16 Jun 2026 23:40:34 GMT  
		Size: 147.4 MB (147388338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a591815a1c96260572f72ad9e7b60e296717e36c2a433c0da2a45d40931e6f5`  
		Last Modified: Tue, 16 Jun 2026 23:40:32 GMT  
		Size: 16.8 MB (16779695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ee544c84d46e11562e572ece00dd9d3a2ba7dc62be33f607f6cf9647d62bd7`  
		Last Modified: Tue, 16 Jun 2026 23:40:32 GMT  
		Size: 4.5 MB (4515201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e41e633d46d77d12113b18c609b64884cddd36e1eb7c1fd2ef3b8e1d820a1c`  
		Last Modified: Tue, 16 Jun 2026 23:40:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:74a64eb96361a11dd2d135ea4e505e5208ed3f9d36a107bd0ae4e59ee48bd4f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e5e940ecd789b758b192c63b11d518fb0ee8f5d908f34d7dd721b97dac8a3f`

```dockerfile
```

-	Layers:
	-	`sha256:977eb0d74d9d91fa7287aa015edc1ce9c7a361d8a46d1d991f1f8df72ef817c6`  
		Last Modified: Fri, 19 Jun 2026 02:20:04 GMT  
		Size: 2.4 MB (2365360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:becbfee478c2dd1483d8eb3c339e815742a211441bceea4fcb9baeaadea0a336`  
		Last Modified: Fri, 19 Jun 2026 02:20:04 GMT  
		Size: 17.8 KB (17753 bytes)  
		MIME: application/vnd.in-toto+json
