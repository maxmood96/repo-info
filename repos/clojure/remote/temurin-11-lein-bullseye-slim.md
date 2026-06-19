## `clojure:temurin-11-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:4d3dc27b0e1485c3b8c08ff6e9536f3737d056ef962ba83ccee6b3b0b7c4f1d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2865c37a2f4d4ec189ac19a4ab8666c9a7fc8558f951f73ced8f5fa3c1641b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196292593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0e9a28254eaf11f34827d123ba567caa57d0b24a3dc3632bff1d1e0c0a46c1`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:13:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:13:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:13:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:13:34 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:13:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:15:18 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:23 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:16:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:16:23 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:16:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:16:24 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db656f3b87d09a96a6f5af282a203ad3d787588e0867d88cfd9d704858d8d860`  
		Last Modified: Fri, 19 Jun 2026 02:14:28 GMT  
		Size: 145.9 MB (145886162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7e5df9ecc618521b829cf6c223290098cbe7054a550b72dcfdc2c3973ec2dc`  
		Last Modified: Fri, 19 Jun 2026 02:16:32 GMT  
		Size: 15.6 MB (15630961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c32be956bd3b6bb624a0fc023f92ad5bd6f7aa12ddf5e68dd14196b687c4c4`  
		Last Modified: Fri, 19 Jun 2026 02:16:32 GMT  
		Size: 4.5 MB (4515183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:494d9c360cd864d93e39152864098922179aebb0f1e8b02426776b11be906bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3074030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0239efce17f810601781234f392e87bd79636c1310711594463b20e4e3f1a6e`

```dockerfile
```

-	Layers:
	-	`sha256:c93f801b3263544f154ceb15f53469c16be16a6f84dabb6285a1a76b1bcc2d7a`  
		Last Modified: Fri, 19 Jun 2026 02:16:32 GMT  
		Size: 3.1 MB (3058252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7f60d7bb26398b46618e9ace317ff70a3d13b5652c58b8c7f588098afee93f`  
		Last Modified: Fri, 19 Jun 2026 02:16:31 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:103f4fe5e29c9cd7b8ee354446a010e82275b1615ca6738c13465aa0a27107cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191463007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0514fcb711c863ac079cfcc0a1cec9d424e8a93271a131902d4bf500a320ff4c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:15:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:31 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:15:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:15:32 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:40 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:16:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:16:40 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:16:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:16:41 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfbd14a6151c57e76c1876d5b161d779a48ba556957b37f2f3b7052c44dbfa2`  
		Last Modified: Fri, 19 Jun 2026 02:17:00 GMT  
		Size: 142.6 MB (142582161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffb37413fbd7ff87cf5980a320032a57e0bf7908cc8304dbe5efe28a6576a4c`  
		Last Modified: Fri, 19 Jun 2026 02:16:57 GMT  
		Size: 15.6 MB (15619477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46e4290aa6294526df7d438a7bb9a5e79baf8fad50f97b4506ea316e279452a`  
		Last Modified: Fri, 19 Jun 2026 02:16:57 GMT  
		Size: 4.5 MB (4515183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ae3b283f6175a19221beb55f47f215f821b902c2cc7ae2cdc1912046168312db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3074378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc7af57add31e737d710bb179a2f5dcc0ebd998cd60ef8d4330e8c8aaafad64`

```dockerfile
```

-	Layers:
	-	`sha256:007c0e18ebc9d64fc9aa6a1309802bdd215c1fda80e34aeae06e317b01d29673`  
		Last Modified: Fri, 19 Jun 2026 02:16:57 GMT  
		Size: 3.1 MB (3058479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba418acea9d8d379c6c2c58fc38f90073ae50dd0b38411579fc9fc6b308d6697`  
		Last Modified: Fri, 19 Jun 2026 02:16:57 GMT  
		Size: 15.9 KB (15899 bytes)  
		MIME: application/vnd.in-toto+json
