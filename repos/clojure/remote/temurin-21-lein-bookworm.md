## `clojure:temurin-21-lein-bookworm`

```console
$ docker pull clojure@sha256:fc1b0d8ba522dd6acdfb71197aba389ce84c3926688492ae4fc24e94a741508a
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

### `clojure:temurin-21-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f5ef76151930464b31b97d518469b802de1c82507d6205d6ecf96cf6cb6d17d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231292611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95888015b60d37fbde647c099a74cdbec7a3199ff811731d8882ffbac19446ce`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:18:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:18:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:18:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:18:58 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:18:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:18:58 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:20:04 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:20:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:20:04 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:20:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:20:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:20:06 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:20:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935cac5b9a7726bf52f28e66e7790d4ac0eb9ee2a85bae0d647b9e75ae37ca92`  
		Last Modified: Wed, 24 Jun 2026 02:20:28 GMT  
		Size: 158.2 MB (158166945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593674bcf12e2328f015fb98693ab7fdbd4349e0f4d2b134cebd078557cc7b79`  
		Last Modified: Wed, 24 Jun 2026 02:20:25 GMT  
		Size: 20.1 MB (20107809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c610e7a0acfb02b6a478d182c51f8d6047c2332be3c898bb32c42eac2fdbd2b`  
		Last Modified: Wed, 24 Jun 2026 02:20:24 GMT  
		Size: 4.5 MB (4515218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5065dc9772eba756844db383949114fd48049a1603016820ddbb9589ee571024`  
		Last Modified: Wed, 24 Jun 2026 02:20:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4c98d8bab2e48fbb1bb71c7e81d81b4a0020080f358266fe462485e4f9e49760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab8434db60d498b2b4491338fe254b5c3239beb6e8f2d3c8d30bd6dfd829fc0`

```dockerfile
```

-	Layers:
	-	`sha256:41662801ea8a83e515a2974c18ee4367b534db0932a9177c7c1dc33aff887566`  
		Last Modified: Wed, 24 Jun 2026 02:20:24 GMT  
		Size: 4.3 MB (4286520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:364c7071f695a1025016845b1e9b5b34194ee280ef28daed9aef2dbda8e01ea0`  
		Last Modified: Wed, 24 Jun 2026 02:20:23 GMT  
		Size: 18.4 KB (18388 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4d98e0646acb425b6ea85a9f0b2ef850e51e9c5022057f25f294034ccedd240e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.3 MB (229306049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225c79dd8177f92e9ab89b910c54f15c778facbbc482d89aa7c62b779007e9de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:25:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:25:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:25:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:25:36 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:25:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:25:36 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:26:46 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:26:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:26:46 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:26:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:26:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:26:48 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:26:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927f316cc5ccc38d3b8ed1880c7c71adeb35d272173a0ba401499fc990b8101e`  
		Last Modified: Wed, 24 Jun 2026 02:27:10 GMT  
		Size: 156.5 MB (156461247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef3f3a1c228e8cf04e7ad9782d58f25964b0a22b1492bfa1f8693378b8fefc3`  
		Last Modified: Wed, 24 Jun 2026 02:27:07 GMT  
		Size: 19.9 MB (19939970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee8fb621d8f071a2ac7e1a780fbbbed0229d79ed28ca9190b3333e0112edc7e`  
		Last Modified: Wed, 24 Jun 2026 02:27:07 GMT  
		Size: 4.5 MB (4515204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909d6de1cfc6ebe8f410c71f0bca6e7fbd6a4e28c79dadae437ef5aafb5a050c`  
		Last Modified: Wed, 24 Jun 2026 02:27:06 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6dc4f4ac3d02d01a48d68833f4d007410d7129982d515cf498ca31d8cd266b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8375936577f03e0fd8c7c652c05878e943742dbae21e75441519e69ea74aef`

```dockerfile
```

-	Layers:
	-	`sha256:55494aabf15b46fcc7f6487ac9743e95e43663af03da72440ba804e82da18d3d`  
		Last Modified: Wed, 24 Jun 2026 02:27:06 GMT  
		Size: 4.3 MB (4286159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad35e4d8ff37e794b1cf3f37d74309996eb4cb4ad1ea5c461c628735e6559020`  
		Last Modified: Wed, 24 Jun 2026 02:27:06 GMT  
		Size: 18.5 KB (18533 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:acd67f13b3bba62f2597e226c4ba629c50043c95f26082121351da8cfad5bf4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235537949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa1df1ea0cc5a75bb803c4fefad37ee1709f773676c7104947f1aa954f7c5ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 08:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 08:11:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 08:11:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 08:11:43 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 08:11:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 08:11:43 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 08:14:14 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 08:14:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 08:14:14 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 08:14:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 08:14:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 08:14:18 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 08:14:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:55b0e891f4e8dc14bf4bc7e853254fcf1f3ba5a8e8e3c07c21e7dd5bd6d87882`  
		Last Modified: Wed, 24 Jun 2026 00:27:34 GMT  
		Size: 52.3 MB (52346847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b243922f32777162d6293cd958624c070d9e6bf6ae5dbe45719e167e86cde0`  
		Last Modified: Wed, 24 Jun 2026 08:14:59 GMT  
		Size: 158.3 MB (158343212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb60bc2698d06ddb2c29051df80bfc7b3ccd69381d2e8f58d3037af120b9b64`  
		Last Modified: Wed, 24 Jun 2026 08:14:56 GMT  
		Size: 20.3 MB (20332244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6905be502eaa749d7140e4d02da5a0e90ac29d4da73494a106a0c66c6ef976bb`  
		Last Modified: Wed, 24 Jun 2026 08:14:55 GMT  
		Size: 4.5 MB (4515218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b74651925144e690e36dff95d1fd4be063e497927a7d642c1437a09a2177857`  
		Last Modified: Wed, 24 Jun 2026 08:14:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f4b8a0354bc75d189b66a8d95a0e16915debc7436c47c28ebccccb12ffd35505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f067a4042a71ef005b400c895d5de71155c7c0e47d67abe13c0b50acaaf37c3`

```dockerfile
```

-	Layers:
	-	`sha256:cfee3b0652022bc4613daef5ba0049465112c3b29b325e740a210180d2d07e24`  
		Last Modified: Wed, 24 Jun 2026 08:14:55 GMT  
		Size: 4.3 MB (4288393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cd1c5f887596a2392193a804d88d2bdd76fa74297178896bf7fdcdacd50508a`  
		Last Modified: Wed, 24 Jun 2026 08:14:55 GMT  
		Size: 18.4 KB (18444 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:37c2c8aa1c241592b0cdbb23ef6a79bab9b4d762068f37004adb46676388d1a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218836124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc91538842d290f779dcd8e918412893bc9d8240831489f88bed2c65d1e581b7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:14:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:14:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:14:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:14:04 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 04:14:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 04:14:04 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:15:11 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 04:15:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 04:15:11 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 04:15:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 04:15:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:15:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:15:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bdd2e9d83d68023204331dd445067114dbd3500d2d496368624fa7ef81743d4a`  
		Last Modified: Wed, 24 Jun 2026 00:27:09 GMT  
		Size: 47.2 MB (47161675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee288d67ec7e9d3f16346468657d9b92cb88d075c672782c475a601fcdc7be0`  
		Last Modified: Wed, 24 Jun 2026 04:15:41 GMT  
		Size: 147.4 MB (147388408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987bde2f02351a31a40f204dc2c65eb963d09835871d2809a0bcbf85f03649fe`  
		Last Modified: Wed, 24 Jun 2026 04:15:38 GMT  
		Size: 19.8 MB (19770401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bdeaeec1d919952fdaf1275f8cd1f059c3c31a5ffdec7011cb35008ca5c9d8`  
		Last Modified: Wed, 24 Jun 2026 04:15:38 GMT  
		Size: 4.5 MB (4515211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54aa4816ebdc4576f7219d56fad505ee03ef6371fce3306eceae7791c0ac6a78`  
		Last Modified: Wed, 24 Jun 2026 04:15:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:63ede07cfad0e491a61bfc9312d0bef1c611cc1001bf02525761910e34e11da4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4296722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4223c3ee29e6cc01601bb9dda7bedfe5ee422490da7249af243ab84b5c1280c9`

```dockerfile
```

-	Layers:
	-	`sha256:b1953c8b9e212ab9b1a3f7e14e4c371f515d4fbbf6582c9397e60577589a90c3`  
		Last Modified: Wed, 24 Jun 2026 04:15:38 GMT  
		Size: 4.3 MB (4278334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fabb50f27ef4b065f9ec90ea595400c5c269f253f72115e51f02ce84c00785a`  
		Last Modified: Wed, 24 Jun 2026 04:15:38 GMT  
		Size: 18.4 KB (18388 bytes)  
		MIME: application/vnd.in-toto+json
