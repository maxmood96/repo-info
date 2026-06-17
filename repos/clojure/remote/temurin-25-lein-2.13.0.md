## `clojure:temurin-25-lein-2.13.0`

```console
$ docker pull clojure@sha256:dc7f42bd652096ac8e857945a7e657583e128bd02b4f7b9d29c0c4692793e833
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

### `clojure:temurin-25-lein-2.13.0` - linux; amd64

```console
$ docker pull clojure@sha256:7e290266ae7086ce3f7bfb4041f3aa069af84423c465a889f037916d6703b7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165700021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3851c50426cd385bddbd8930178abd6f19251f836b91ac7af5d7c8bfbbb0ad9c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:32:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:32:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:32:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:51 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:32:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:32:51 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:34:03 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:34:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:34:03 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:34:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:36:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:36:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:36:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be82348757715d0824b3486736b0e007b9002574e5621eebd1aff9f87b48fe3c`  
		Last Modified: Tue, 16 Jun 2026 23:34:41 GMT  
		Size: 92.6 MB (92574586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5677f7d9d3f5624e23ada669aabcba708cf7a009f5d3a020e2cd8e6ac885a248`  
		Last Modified: Tue, 16 Jun 2026 23:34:38 GMT  
		Size: 20.1 MB (20107789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabca998214597d6497c4affc9e50ba0951e6e4000e950b4c6257070a90ae37a`  
		Last Modified: Tue, 16 Jun 2026 23:34:37 GMT  
		Size: 4.5 MB (4515179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90f810dc0fb1e16996f1832fee637aad7902aa4ceb6ff9276b5c4a7568a31cc`  
		Last Modified: Tue, 16 Jun 2026 23:36:47 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.13.0` - unknown; unknown

```console
$ docker pull clojure@sha256:7be221fe921950aaf7036b52760320ce8af96439bd3cff93bdc2f50ae1193baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2197d504104379d21fee29bd4908971b68958d75a686e02052d47b62995a2b91`

```dockerfile
```

-	Layers:
	-	`sha256:fef0a2ceafe609b26bbdf7fe5376e65245073408434b207a1f921c391ecc83bd`  
		Last Modified: Tue, 16 Jun 2026 23:36:47 GMT  
		Size: 4.3 MB (4253310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fec06291ea67584c17217479d3f561d87bbc0e9caff16954ff90b722c5a53fae`  
		Last Modified: Tue, 16 Jun 2026 23:36:47 GMT  
		Size: 19.6 KB (19629 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.13.0` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:091e98704ea94c60064a2a40d2d693f654e40e68d22ddb0f1d2692c62d4c24bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164387353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0a11a0780be9f122251ff091d8635eedec5509bb6886786f760e9e6485b3fa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:36:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:36:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:36:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:36:37 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:36:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:36:37 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:37:45 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:37:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:37:45 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:37:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:37:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:37:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:37:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81949e404cfc766dc585e8ea060cdf3d0c8dec6b9c5c1ff0cc9a8e9be077944a`  
		Last Modified: Tue, 16 Jun 2026 23:38:07 GMT  
		Size: 91.5 MB (91542299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef95f7fa988933075a6a12227f3ef1786e1feca903bd2cda097aeccf53f6656f`  
		Last Modified: Tue, 16 Jun 2026 23:38:05 GMT  
		Size: 19.9 MB (19940409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5161f871dd00f14a09e58cc01135de03a0b142974f9dca3ec8bafdff6079961`  
		Last Modified: Tue, 16 Jun 2026 23:38:04 GMT  
		Size: 4.5 MB (4515198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a4aa592ea3284f8e6d1524985258de3742cfa2cc4d544053ad97848e18bd86`  
		Last Modified: Tue, 16 Jun 2026 23:38:04 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.13.0` - unknown; unknown

```console
$ docker pull clojure@sha256:cffca4db87c1d639b63e891c4ab974da9f3b783125e361ea217d03c85928492f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad16fb1be88dfcfd7f5f5a2800328b8336c33309ef8f1d0b5928f54a45735ec0`

```dockerfile
```

-	Layers:
	-	`sha256:dbfb481a66e839d7304109a038a9ca2b25ea39e5c664a84079572ce5f9623478`  
		Last Modified: Tue, 16 Jun 2026 23:38:04 GMT  
		Size: 4.3 MB (4252994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2edfd4f370ee4e33c6b7c924256c017f506d64317ed638a0b57c3d47019db89a`  
		Last Modified: Tue, 16 Jun 2026 23:38:04 GMT  
		Size: 19.8 KB (19822 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.13.0` - linux; ppc64le

```console
$ docker pull clojure@sha256:4da034921df9d899d361ec009218dd36c776f42b8617d4994c55d5280c389d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169108168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0946dc73b9cec62a85ec1814ad55485ea17f60420920f3824e70b66d7cc323f9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
# Wed, 17 Jun 2026 00:02:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:02:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:02:47 GMT
CMD ["repl"]
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
	-	`sha256:bf89a28de7a2761db3b1d45bf3c00b21c7ab706a0db5122da20022d327e92acf`  
		Last Modified: Wed, 17 Jun 2026 00:03:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.13.0` - unknown; unknown

```console
$ docker pull clojure@sha256:2059a9cf469725fbec9f71d91fcc4c7f0e03e803c660d1c205fe55ba9c8dcd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4257275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1978c223120aa6d5646d74fd0739e0040d3be10a626ed23ff80e317649e01f`

```dockerfile
```

-	Layers:
	-	`sha256:298ed10cfc4833fdfd25f9ce908ff5cfcaa4a6c0892762203bf64ee52105eddb`  
		Last Modified: Wed, 17 Jun 2026 00:03:02 GMT  
		Size: 4.2 MB (4238519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dba0416b7c4a7bd6059aec98db409d0280f2bf11924756ca19bbc81985699fff`  
		Last Modified: Wed, 17 Jun 2026 00:03:01 GMT  
		Size: 18.8 KB (18756 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.13.0` - linux; s390x

```console
$ docker pull clojure@sha256:9e0ac7592d933449fd1244c97d88242bb0641b25bdcec4817701aee37a9926a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159867870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae46281fa59190c12319f86c5fb35729d021afbd7e36f64ea02f5c4115220b52`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:38:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:38:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:38:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:38:59 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:38:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:38:59 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:40:08 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:40:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:40:08 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:40:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:40:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:40:10 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:40:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4520e3ce17e71abaf08ea3cba3cab2e79d57848b6df7e253340b469c20e61608`  
		Last Modified: Tue, 16 Jun 2026 23:40:38 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119882721c41add10c6dd4ffd46e2c62596ff1ee22a59841fe02b3a0aa9dc680`  
		Last Modified: Tue, 16 Jun 2026 23:40:36 GMT  
		Size: 19.8 MB (19770405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3639e13fce2ea10ea1123b5120760f22a9db7c9525b263677dbef41c7e09965b`  
		Last Modified: Tue, 16 Jun 2026 23:40:36 GMT  
		Size: 4.5 MB (4515215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5cb5281f58fa8e79801cd1b57a6cb16e8324e760c1b4bbaddb3c799950361a`  
		Last Modified: Tue, 16 Jun 2026 23:40:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.13.0` - unknown; unknown

```console
$ docker pull clojure@sha256:0e2e8f8a3a70bf2956fd7e573c357178a77ef332f96299378eab5bb0ae18a2e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a77c25734d085654df3886e1997dad1460dd5f5d2030add2aaa72497aba3362`

```dockerfile
```

-	Layers:
	-	`sha256:a29ee05d89577bbf3f71875d291f9b3d30743ae6191fa72ddb333ca24d0ed050`  
		Last Modified: Tue, 16 Jun 2026 23:40:36 GMT  
		Size: 4.2 MB (4229686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83f2a2656cc890129ca6dad16f9b386c13e41ccd83780885b263bde7abdc8729`  
		Last Modified: Tue, 16 Jun 2026 23:40:36 GMT  
		Size: 19.6 KB (19629 bytes)  
		MIME: application/vnd.in-toto+json
