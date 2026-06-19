## `clojure:latest`

```console
$ docker pull clojure@sha256:501a5b88779a946fd3f0a231f75a176d7215ba532f9a55cba340674756ccbdc2
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

### `clojure:latest` - linux; amd64

```console
$ docker pull clojure@sha256:78d8a885521968597e996003c8aa60285751cb2f0b1158f8e66a816abe053bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233911521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68ed210a4701c92e3cb801f681def780ffae478d00432e0bb5b0d488a4674a9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:14:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:14:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:14:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:14:36 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:14:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:14:36 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:15:45 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:15:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:15:45 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:15:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:15:47 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:15:47 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:15:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:15:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:15:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:15:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:15:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cc1befffdc7ebf8161b60bd4f8575b3aac52995b408f168af884503096f9cb`  
		Last Modified: Fri, 19 Jun 2026 02:16:22 GMT  
		Size: 92.6 MB (92574584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aeb46754edabd3efb401630946d2355b1540f6bce4ef2e7dfc46ea1f1d7790a`  
		Last Modified: Fri, 19 Jun 2026 02:16:19 GMT  
		Size: 20.1 MB (20108182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3493466818269e2edded89b339cda816f60505e74d8fc35d1754be3a004e76b8`  
		Last Modified: Fri, 19 Jun 2026 02:16:19 GMT  
		Size: 4.5 MB (4515180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cf3664d7ad10c43f923a9ff8384129911eb9d0e0b56de7c48511a2dc02e420`  
		Last Modified: Fri, 19 Jun 2026 02:16:21 GMT  
		Size: 68.2 MB (68210459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d623f0bcbb7fe67d96bce7abaf8771baf871d8dea4252ccde12f272e738d8f`  
		Last Modified: Fri, 19 Jun 2026 02:16:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d146555fd59de92a44c0f16d0d8941ffc9e4528a1a653784414ef51955ce8be3`  
		Last Modified: Fri, 19 Jun 2026 02:16:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:264063237e91c11a6bde6647184e9c02c6dcd45ead4835cc824a09eabccb4869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7460886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1872c634251e7699f87a7f8670e93047a1c0fa31c8af58e91b0f9098c6ba6d2`

```dockerfile
```

-	Layers:
	-	`sha256:e61a1e2bac47e3e7a178b94247c4e13ccac67bea6f11365b48e6526660556214`  
		Last Modified: Fri, 19 Jun 2026 02:16:19 GMT  
		Size: 7.4 MB (7435911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0b331f99bb89d86e21454b18c9fc6894912eefe8595aebe8af2ac99fc89119f`  
		Last Modified: Fri, 19 Jun 2026 02:16:18 GMT  
		Size: 25.0 KB (24975 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ec21ad3fc5396501658bce5b6c87c877a3d9d551bd9fefc151802e685631add2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232741745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b137fd8c8878230c64a5d57f4efaf2eea8562517a21899a55edaa591a745b9cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:14:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:14:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:14:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:14:39 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:14:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:14:39 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:15:47 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:15:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:15:47 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:15:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:15:49 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:15:49 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:16:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:16:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:16:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:16:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9403891d67e1401d668b8a82f359cd7e2b122c6a957c5225435b27e2dd007c06`  
		Last Modified: Fri, 19 Jun 2026 02:16:25 GMT  
		Size: 91.5 MB (91542250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ba610ae37b075f51dee929048718ab44872c60b4805808e35cf2d24f8402c`  
		Last Modified: Fri, 19 Jun 2026 02:16:22 GMT  
		Size: 19.9 MB (19940404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65aaacdd6b9a95c2ff9e783864d0998999986f6e4d088575a487c8a12bfd9338`  
		Last Modified: Fri, 19 Jun 2026 02:16:21 GMT  
		Size: 4.5 MB (4515217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3f4290403526b52a02dd4c99925961c7e3583b7418d16e17d7d665b651a732`  
		Last Modified: Fri, 19 Jun 2026 02:16:25 GMT  
		Size: 68.4 MB (68353786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddec1f915aef0fc835d39f8a4509f056923ad2730c9e73073eba35a7442fa3c4`  
		Last Modified: Fri, 19 Jun 2026 02:16:23 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e111aab50c4ca82d50912bd2297c741c2c9867ccb8b4a00b38d1a3b98e62a07c`  
		Last Modified: Fri, 19 Jun 2026 02:16:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:72d8d9a36212c4b36c775f9b783a8804f51cee6f9dd80f61c3a33ed2ed4afd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7466746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85b8421f05823d5bfb315a1594e9e048fc7f23574a79dc8359e37ed437bad2a0`

```dockerfile
```

-	Layers:
	-	`sha256:f275186fb976c354b6c5752f3d5a4e88ba4ccf8d668f93e46203a478e2d92163`  
		Last Modified: Fri, 19 Jun 2026 02:16:22 GMT  
		Size: 7.4 MB (7441647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39b24887fdec055877e4a0f6bc65fa27e522046c7f1542ae97b21a06fa9d4d43`  
		Last Modified: Fri, 19 Jun 2026 02:16:21 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:9f776d596afe3cbf652635270972a95a9588bbf9fa915ffc8d713e11c4f655b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242920865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9b110ac059606dad89cfe16fa0b1f0ffc1f400f7fca7df54d7b44895fbd203`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:30:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:30:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:30:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:30:21 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:30:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:30:22 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:33:52 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:33:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:33:52 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:33:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:33:55 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:33:55 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:34:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 16 Jun 2026 23:34:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 16 Jun 2026 23:34:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:34:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:34:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af2d7bc5e0f6f23b949f449ec38352dcc13ff43d0d262dab584e4f344eec386`  
		Last Modified: Tue, 16 Jun 2026 23:35:12 GMT  
		Size: 91.9 MB (91914009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68947c24a5e1c48feb5dfc5d4e28fe4f56550fcd7d0ffdaf1322d3ddb36f090a`  
		Last Modified: Tue, 16 Jun 2026 23:35:09 GMT  
		Size: 20.3 MB (20331869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7f1d5b8d6bc4ae48b7364827721c152758155257cfff4b80279cd72f3d6bf1`  
		Last Modified: Tue, 16 Jun 2026 23:35:08 GMT  
		Size: 4.5 MB (4515191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681ca53a2ea5923857d7bd3046b8635776ac9327e93b8476b7862b1690ae8527`  
		Last Modified: Tue, 16 Jun 2026 23:35:12 GMT  
		Size: 73.8 MB (73812052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ce5bc08975d0e839671137a7c2bb51320b950433317790cdd8ac9cb14ca325`  
		Last Modified: Tue, 16 Jun 2026 23:35:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb72dd97a652b682ba689394204a9a87d775b1aba31696034959d9216435764`  
		Last Modified: Tue, 16 Jun 2026 23:35:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:482b0cb47789ba3acb6369cd32c1937c328bcf80b3291764d636c6ca47f4ba61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7449442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55fc002db4352b59ff325a0cb2c315ee618054f28b5cd48cdc471b2a04592db`

```dockerfile
```

-	Layers:
	-	`sha256:aa8ba60eaf34e6e37a39d62b7ca53296bdd9bf57983acea1d0cca0dd7696ea81`  
		Last Modified: Fri, 19 Jun 2026 02:21:08 GMT  
		Size: 7.4 MB (7424427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a786af90727536f6091ae493bc5f1f7cbd2abb4b6f0f2631c25fa8970c9991b9`  
		Last Modified: Fri, 19 Jun 2026 02:21:08 GMT  
		Size: 25.0 KB (25015 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:49421dd2cf457e2766316964bb8f405e0790cca723be7316d091ac2bbaf8ded4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227210559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8673ac24da0d14e6373cffba27e31babb54dae8001b287ee52809a5c60cc9c7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:30:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:30:16 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:30:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:30:16 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:31:32 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:31:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:31:32 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:31:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:31:33 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:31:33 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:31:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 16 Jun 2026 23:31:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 16 Jun 2026 23:31:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:31:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:31:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14907b0f682b8ecfba5edca7e3ae44505f908a9f5163eb33cb4b2d568ad948ea`  
		Last Modified: Tue, 16 Jun 2026 23:32:19 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e7043565b34b7284c7fa5d693843e5ece45dbcaec9986711d409c32de70cec`  
		Last Modified: Tue, 16 Jun 2026 23:32:17 GMT  
		Size: 19.8 MB (19770336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987739cc204bb874386b889d6cc4fae0c385eb47a370889b6f322604802cc162`  
		Last Modified: Tue, 16 Jun 2026 23:32:16 GMT  
		Size: 4.5 MB (4515179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239e28d22a1e75898438fb4d297728c2d631c2883ae1d15ce3b7d46f425022cc`  
		Last Modified: Tue, 16 Jun 2026 23:32:18 GMT  
		Size: 67.3 MB (67342149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa7723bbcb6af52be23c5a8f10e46e6f1317a9bbf758e7657ac0120a5d394c2`  
		Last Modified: Tue, 16 Jun 2026 23:32:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bfe914b9c07ae24c391891d24921e99bb988de49652c90400a151f02ee92b1`  
		Last Modified: Tue, 16 Jun 2026 23:32:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:61ebaa550ced044b0a071f40e82e4c04958e7479d00549fcc294129a15c83c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7436767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e527625630538ea18a9ccf4a3b9d2e8ebf5bf1900b274f7031535cc83ba1a68`

```dockerfile
```

-	Layers:
	-	`sha256:eef745897f2a3016318273e57bc92326011a0a1720ada306d16b508a9ee88d78`  
		Last Modified: Fri, 19 Jun 2026 02:13:31 GMT  
		Size: 7.4 MB (7411792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9be77baf7f9d0815fbd83b4f6b79e09f9b794408b88d442dec09199df42f3f1d`  
		Last Modified: Fri, 19 Jun 2026 02:13:31 GMT  
		Size: 25.0 KB (24975 bytes)  
		MIME: application/vnd.in-toto+json
