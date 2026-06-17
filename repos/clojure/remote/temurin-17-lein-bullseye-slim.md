## `clojure:temurin-17-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:9fc34cef41228cf390bece6a4110127eff28d4b4a18c587496fe8ee4a757e6d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e7426119cdc48f486f1f9de39d6051e5cefe5d56f45d07aa2799e143cd7e1124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196312126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b0aeed4fc4f089a0d82de56f6908ce7f8fed6f203430a5eae8c9fae9f85c19`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Tue, 16 Jun 2026 23:34:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:34:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:34:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:34:43 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:34:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:34:43 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:35:54 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:35:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:35:54 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:35:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:35:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:35:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:35:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8aae4a686965ba6e8db899be580bc2dbb80e93fece461cf09c0398a5e36eed`  
		Last Modified: Tue, 16 Jun 2026 23:36:16 GMT  
		Size: 145.9 MB (145905476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb898b1bb24bfc5ef76618664dcaadb2c7bd9bfe3ad52775ac2c778b343d95b3`  
		Last Modified: Tue, 16 Jun 2026 23:36:13 GMT  
		Size: 15.6 MB (15630787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f5248725806b5c72b539892b9898050a8c94e24f57a5db8ea4da4098f005f0`  
		Last Modified: Tue, 16 Jun 2026 23:36:12 GMT  
		Size: 4.5 MB (4515178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a500e6e3f753f24d7b13e508c04337307bf699dbd7b509052ebcea80aedbaa5d`  
		Last Modified: Tue, 16 Jun 2026 23:36:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dee8b1a3c601f1680a993ca3c701117e7d06901d37b6749cfeb94e33f90ebd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76b46d15a1f1a629a3de367884ef220db8c337f882118581b8bd467dd48bee1`

```dockerfile
```

-	Layers:
	-	`sha256:7cf36a8279d0ffcf1dd62fe5c817daf4eb71f3179f1672502ceda8b913ee517d`  
		Last Modified: Tue, 16 Jun 2026 23:36:12 GMT  
		Size: 3.0 MB (3038736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe82d04247c654aa78d66aead0606c94a9df51cba84f58ee392d7bc4fd7bf81`  
		Last Modified: Tue, 16 Jun 2026 23:36:12 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:97d7202910258ab276ad94e5f17306f1bdc4ba1eeef49233ec9e867b1e8043d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193605900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01dd4742f5ec772bec5a8ebb08baa63df2b96f4869fcd14dd857d8822b730a0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Tue, 16 Jun 2026 23:34:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:34:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:34:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:34:30 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:34:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:34:30 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:35:36 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:35:36 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:35:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:35:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:35:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:35:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368d2418fc9179713a9a0cfba8906d5931f99e1f58612e8977610762b9d1aedf`  
		Last Modified: Tue, 16 Jun 2026 23:35:58 GMT  
		Size: 144.7 MB (144724360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62ecf05fd06a7656dc2e3c78bdb0cea33402130ef29ad432acb5326558661b9`  
		Last Modified: Tue, 16 Jun 2026 23:35:55 GMT  
		Size: 15.6 MB (15619781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512c4815a048a486a2b06b8089e85b5adef3ec3076906e9bc8141b8a1222dc1d`  
		Last Modified: Tue, 16 Jun 2026 23:35:54 GMT  
		Size: 4.5 MB (4515175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46b4ea96c077dc50d9c719f3c12a4ecfc702dc0e037294621964933adcf350f`  
		Last Modified: Tue, 16 Jun 2026 23:35:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dfa86db672439c3149a54d57e014483b15246e95244c942c8cfedcb4c6c16981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e97249aee4a13a0327473cb254805a4549291a86708c43f28eeb105fa6729b`

```dockerfile
```

-	Layers:
	-	`sha256:e76de6ad20159396ac50c14c481f8a5fcb7549df6864af0d82dccee26d4b438d`  
		Last Modified: Tue, 16 Jun 2026 23:35:54 GMT  
		Size: 3.0 MB (3038345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:684ac3ed6a0af8c6ef4ff0edc237c0446f6a63fefa1e2d1787c1756b2bdd1148`  
		Last Modified: Tue, 16 Jun 2026 23:35:54 GMT  
		Size: 17.9 KB (17894 bytes)  
		MIME: application/vnd.in-toto+json
