## `clojure:temurin-17-lein-2.13.0-bullseye`

```console
$ docker pull clojure@sha256:98ff87ead011b1985795fc849449f2d467b8eecf42418cce3b074ee8610bc584
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.13.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4ef278de81802eb0fc79f881d49004ad441c25cd1ea47911fb3e0aa3655b9a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221121542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01afbf83624129627edd3144ca739854fce33081441c540e0657f5debba282a9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Tue, 16 Jun 2026 23:34:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:34:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:34:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:34:41 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:34:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:34:41 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:35:49 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:35:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:35:49 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:35:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:35:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:35:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:35:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a16c629b98060f1863731b3c6088b9f0d2e0f17f892b39dbf067ca09116e669`  
		Last Modified: Tue, 16 Jun 2026 23:36:11 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f982bd0733d5edff63cd63675acdaf2e4011a0d75dc720a4e14447a3c0931cc`  
		Last Modified: Tue, 16 Jun 2026 23:36:09 GMT  
		Size: 16.9 MB (16928667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55cedc8cecbf84de6584077b7fb1adca05d4b166e1ce904a5237b7bea2526dd`  
		Last Modified: Tue, 16 Jun 2026 23:36:08 GMT  
		Size: 4.5 MB (4515222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83563fe704f1f1d84faefd7393ad1189571a176501686015fb9178aae663d2dc`  
		Last Modified: Tue, 16 Jun 2026 23:36:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:403e48ee4468fac2cb5a47d733e1921fc91ddcda8dc11063a94dbf5a1bbd2c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30aeedc971f1d98dbfd92451a69aa0d576d1adca8e0590e4436f53e887d62dfd`

```dockerfile
```

-	Layers:
	-	`sha256:d9fd92a7f8b58879d95ed4a9c73cd5145ae1e8800823cfa1992985eb8f32ea5d`  
		Last Modified: Tue, 16 Jun 2026 23:36:08 GMT  
		Size: 4.5 MB (4502651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c539d46378301e146c274805c35dbfee46154315a9226525917462e35b3dfcc`  
		Last Modified: Tue, 16 Jun 2026 23:36:08 GMT  
		Size: 17.7 KB (17738 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:988a3f41cc6ca538e5fead947dd24e105aad1164c595086367c6ae0d71b6123e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218421682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d2396b3a12338b1473ad6ab883ca0fa13c1584e807d647c99572ed62ff9ede`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Tue, 16 Jun 2026 23:34:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:34:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:34:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:34:31 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:34:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:34:31 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:35:40 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:35:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:35:40 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:35:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:35:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:35:41 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:35:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab695f0574edba9011165216e164f5c6cda8ff8f2bfe48149e3fc78ce12dba38`  
		Last Modified: Tue, 16 Jun 2026 23:36:02 GMT  
		Size: 144.7 MB (144724327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8202fefd9a1289c67cfbe613904472d23f1c0f6c09f01940630f0fbe6f076c`  
		Last Modified: Tue, 16 Jun 2026 23:35:59 GMT  
		Size: 16.9 MB (16917632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefc0ad6c9f6b54e3f71ba1a05f50a9e0afd34a644fcd0bf6887b8a02edfc31e`  
		Last Modified: Tue, 16 Jun 2026 23:35:59 GMT  
		Size: 4.5 MB (4515180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f625098f0a83cf845e4ed86b048fb3906d8228574ccad6ee3631170490e3a800`  
		Last Modified: Tue, 16 Jun 2026 23:35:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bfbad0c7f1a0824903142c8569316eb3ba9fd368c56949ddc3a4a24570a69960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4519484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e327ed935079a3b8129d9d069bec576e6646b7170ad792d082544494ae7039c`

```dockerfile
```

-	Layers:
	-	`sha256:4c57a8eda89f8d2f9533205d87d199b8460a1461db550b98ce33c01b079637ab`  
		Last Modified: Tue, 16 Jun 2026 23:35:59 GMT  
		Size: 4.5 MB (4501625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:023b47b653b8923626ddc7230a43621b66861b5ba576f735c659ee94958dd026`  
		Last Modified: Tue, 16 Jun 2026 23:35:58 GMT  
		Size: 17.9 KB (17859 bytes)  
		MIME: application/vnd.in-toto+json
