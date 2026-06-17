## `clojure:temurin-11-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:17a6936ce89f88b2b0cf50dae19819adb3266d9df79d4d46b93d95fe76d9a362
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:685ec006b1600bbf6588d865ded93d97860ff04b436eae12867b457b90164879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196292945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0504fbe616b5d8cf462b7c99502ab3bd6ea6a4693fc4e3417b3c5af608083301`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Tue, 16 Jun 2026 23:33:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:33:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:33:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:33:06 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:33:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:33:06 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:34:20 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:34:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:34:20 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:34:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:34:22 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b91b7c529e1aebd9404bad6534bc72f5d27487d85c4e5d9a6d7f947e21c638f`  
		Last Modified: Tue, 16 Jun 2026 23:34:42 GMT  
		Size: 145.9 MB (145886244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7074590d6b9352692db184fea49c8d588ebd95a3a3104fb8d9176952459c1b`  
		Last Modified: Tue, 16 Jun 2026 23:34:39 GMT  
		Size: 15.6 MB (15631187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec7db6c00cba4f33c60996c91105e06a647a401aa99eadac23f87e18e69f7da`  
		Last Modified: Tue, 16 Jun 2026 23:34:38 GMT  
		Size: 4.5 MB (4515227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c9e1982105c8f64880c44c9928b64bcc7b65e20ec020dc9dfe8f2f01ab650f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3074029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b66e52bf9f740ded8b49bd6d971ec38bf922c84f0b92092e4a2087ba25b83d`

```dockerfile
```

-	Layers:
	-	`sha256:3a744e05d45eb4198af2e1980865f0acf067dd8515ac4befb8bbd638a259ddc5`  
		Last Modified: Tue, 16 Jun 2026 23:34:38 GMT  
		Size: 3.1 MB (3058252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f95f03cbfbd066101a013ee6f059e54ad3d83bf3fa28513518b10823601b5cd`  
		Last Modified: Tue, 16 Jun 2026 23:34:38 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2edaf51bd059a0edf20b905b31a8be88a8ec95ace4cca82328157c2905e21834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191463229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4581f3a6e23e613c3735a3875628c8fd57a47e904e5960d298b267b444bed0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Tue, 16 Jun 2026 23:32:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:32:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:32:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:56 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:32:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:32:56 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:34:12 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:34:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:34:12 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:34:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:34:14 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dd05340f855b8885573381f3a58df0cca5bd565a58eb26747ce115f8361789`  
		Last Modified: Tue, 16 Jun 2026 23:34:34 GMT  
		Size: 142.6 MB (142582247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8233ab70d8cc0ac543c92631184a9b6928efa575863ca851ff21a3ef9870e8c`  
		Last Modified: Tue, 16 Jun 2026 23:34:31 GMT  
		Size: 15.6 MB (15619578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716aeb2a9216c7539d30f4eb12a38ceb20b1ea7ca1bd84bde948144ebbe585a9`  
		Last Modified: Tue, 16 Jun 2026 23:34:31 GMT  
		Size: 4.5 MB (4515218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:45b64b2af6ab78f93555a4fc1a03f82b9cc81ff1d1c27dc01b2ed231edb5a5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3074378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd6f276091a6702e692645b71b2fd436c20a560015a1ee03cbd840b3961c1de`

```dockerfile
```

-	Layers:
	-	`sha256:a653727f688ffd627c789af636242605f9e61ecde5949e4b198e2f84adba69f3`  
		Last Modified: Tue, 16 Jun 2026 23:34:30 GMT  
		Size: 3.1 MB (3058479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edb1fd2132220f04191127012976657fb6548fd493bf217ac67138b1ccdb940b`  
		Last Modified: Tue, 16 Jun 2026 23:34:30 GMT  
		Size: 15.9 KB (15899 bytes)  
		MIME: application/vnd.in-toto+json
