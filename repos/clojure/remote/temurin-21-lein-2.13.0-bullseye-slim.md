## `clojure:temurin-21-lein-2.13.0-bullseye-slim`

```console
$ docker pull clojure@sha256:1f613488140ab7e62182f79f3b296bfe8d350bbebf2a174127938f361bf6a97a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.13.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7531b4771b7f9c420eee680f26bd35960058cd4dc8892e1e9d17ed046c080c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208572909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6393c18309a581477ec8b5fb79619d7450c0a8a90af5e8cd1ff523ad9c41bf63`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:18:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:18:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:18:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:18:51 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:18:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:18:51 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:19:56 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:19:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:19:56 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:19:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:19:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:19:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:19:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0251c4232e4025b51352f0bb7119fd866d4a6a62861f09baea6fe5af4c6eee59`  
		Last Modified: Wed, 24 Jun 2026 00:28:14 GMT  
		Size: 30.3 MB (30259447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d5e8235b3f79d86b37bf70f671640a49116677e2d025800905339e674caa7e`  
		Last Modified: Wed, 24 Jun 2026 02:20:19 GMT  
		Size: 158.2 MB (158166901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23298846c9d9687b87ec3b7e1eac99501ebc68bc27be1b0c70e247c8b38d9d2`  
		Last Modified: Wed, 24 Jun 2026 02:20:16 GMT  
		Size: 15.6 MB (15630953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8d39a252b98750d00a7c9d914da7bac616219094f9b3fcef14d0af21fba66d`  
		Last Modified: Wed, 24 Jun 2026 02:20:15 GMT  
		Size: 4.5 MB (4515178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab386fb8c589cfe3a04509028ca4f77593ca4d599668f9c104d9b101671d6b4`  
		Last Modified: Wed, 24 Jun 2026 02:20:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:86e04e00daee9e8f736818d1727f9eaa922f9b1ddda6ac28e0661357a608d39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef630a14f5c5b520ba33b93f781a020d3df97ecfb4e835b9c35312f7e4a4294`

```dockerfile
```

-	Layers:
	-	`sha256:00fa542aecd6a60677b3b571c0009b8f1db104e182e7a29c2a8d1552a87cfee9`  
		Last Modified: Wed, 24 Jun 2026 02:20:15 GMT  
		Size: 3.0 MB (3038964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01e2d38bd179b7afd3488dc77213939bdfa49ec8824b941db168c766fd6edec`  
		Last Modified: Wed, 24 Jun 2026 02:20:15 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:067de2a51a3182bd12ec99332d416b39c55ea54a2e6818eeff7bc45e2713ed71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205343385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28f184cc90f83b30f95013551845ae57d60ed775fac0bfb7a4a2c43fc9ceb67`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:25:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:25:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:25:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:25:40 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:25:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:25:40 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:26:47 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:26:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:26:47 GMT
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
	-	`sha256:58009b48fe731a10341c4f5f98dfa280afd10fa34cc71961411d37e306120dd0`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 28.7 MB (28746926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cb17ae08dcf2ec3b580971d8eca83799d587d6ba43491a5622ea57f983be5f`  
		Last Modified: Wed, 24 Jun 2026 02:27:10 GMT  
		Size: 156.5 MB (156461252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadb34f264f21191cb9dd28062dfb330776c59f5d103026ca1fabe95e05b0328`  
		Last Modified: Wed, 24 Jun 2026 02:27:06 GMT  
		Size: 15.6 MB (15619601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1763568a6968792a0e3c3612503d5838ddf05e7327e496c0535b05fd3dd8938`  
		Last Modified: Wed, 24 Jun 2026 02:27:06 GMT  
		Size: 4.5 MB (4515177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aca1f9c1af4282dc1508f6073a99b30104e5294a1f46b18c62f0e3c38fb549a`  
		Last Modified: Wed, 24 Jun 2026 02:27:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6e8d335fab2f11729b142c99ee601cf1c364b45d96b2c21c33f9d02444e1289b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b466110b084a75c95e5c4e2c7a2143882d08010f3ec99ed365421dc9a478ad22`

```dockerfile
```

-	Layers:
	-	`sha256:18533cbba99467af0bc6e7719c344133da0b10d65a23e251a46f6d9632e326ae`  
		Last Modified: Wed, 24 Jun 2026 02:27:06 GMT  
		Size: 3.0 MB (3038573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2003d7f283456c7f0c7fe71d4e5821acc163b4dfa1ea8dab740d586908e1f4c`  
		Last Modified: Wed, 24 Jun 2026 02:27:06 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json
