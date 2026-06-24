## `clojure:temurin-11-lein-2.13.0-bullseye`

```console
$ docker pull clojure@sha256:200317883b6fe1b861a542ab9d20a446ec280a31e1f8d4e856d3d565f0f77dad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-2.13.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:732cc7aa6a3544b4b51d3f7f981a3984f19f585ce45e7c61e7f6797488082ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221103186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ee3c7c1bfcd0edab06c39cd67fcfe1b9a87a24030e0a2b7577445dc97dabba`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:15:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:15:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:15:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:15:29 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:15:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:15:29 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:16:43 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:16:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:16:43 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:16:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:16:44 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c67cddb4b9fcdeefaf829aa012f0ccaefcfa862a558064326104b95b8849cd81`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 53.8 MB (53773009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a1dc46c3ce8219db875fe6086ba97712b8cb6090c0b0b825a29c5ddf2fa1a2`  
		Last Modified: Wed, 24 Jun 2026 02:17:07 GMT  
		Size: 145.9 MB (145886164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9347dd16ae7e4c8ee2b83f63886188b659994c01287cb72fcfc85fd80b2f3274`  
		Last Modified: Wed, 24 Jun 2026 02:17:02 GMT  
		Size: 16.9 MB (16928795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f7a0a7047078434cbd42493c9d838f1b6ba13028384fa21010f40550738666`  
		Last Modified: Wed, 24 Jun 2026 02:17:02 GMT  
		Size: 4.5 MB (4515186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:71cbeac21c37022ee476c066cc91cadee8ed137a98309b83134c7e601c82177c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4536291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a63ed5292533a4fd392c369615a877fff579700d8c6a068c7b85876fd2d125`

```dockerfile
```

-	Layers:
	-	`sha256:ded281ac957ce48470ce70927112f9d49bc8dfa165091b290125013b3bcd1564`  
		Last Modified: Wed, 24 Jun 2026 02:17:02 GMT  
		Size: 4.5 MB (4520543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53e82b14e5582dc0cf56212273d48df26ba2b4fe8df242db59c0ac98fdb09776`  
		Last Modified: Wed, 24 Jun 2026 02:17:02 GMT  
		Size: 15.7 KB (15748 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.13.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ca1da7b08eb741ed2bc6bbe49ade814aacb5b04235dc6413b3e31869067b8ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216272240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c98608660b4bd0b5197350a56b26b771ac8d1b171821b338f04423a4d53106`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:22:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:22:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:22:05 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:22:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:22:05 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:23:16 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:23:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:23:16 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:23:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:23:18 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:35157acdff35db21da73141f382d0dca0f6bc6d183c3a816d283fe39f471e539`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 52.3 MB (52257219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d82e13ada5141b7524ac17017dcfbb1f0d163adbdc1598ed841888cf451f7e`  
		Last Modified: Wed, 24 Jun 2026 02:23:38 GMT  
		Size: 142.6 MB (142582140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17bf0ac8dcf759320c78309a9ba34051dbd464c953725a8cd21dbc33acd9f5b`  
		Last Modified: Wed, 24 Jun 2026 02:23:36 GMT  
		Size: 16.9 MB (16917631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8728da35e523733a2d5cd868e3938b4cef6a4f0c7589d7c7bbef6581f181fd2`  
		Last Modified: Wed, 24 Jun 2026 02:23:35 GMT  
		Size: 4.5 MB (4515218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1c497ae264e57aedd3fad6b8c726911d6b658b3df73b67aaddc21f27d28c2b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4536004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55013f70d23578a12ae0240412aac33b4fb7ef3d3a6c99b7e84d31a43c0fefa0`

```dockerfile
```

-	Layers:
	-	`sha256:3f7dc685204bdf5ff1ea4b472d4560291a8ca2bffddd21ec82afa3e6ed2e40bc`  
		Last Modified: Wed, 24 Jun 2026 02:23:35 GMT  
		Size: 4.5 MB (4520135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81038b074e18a2bb53ddb49a034d0a21a101a604412b36ede1a4a738fa6ae2ea`  
		Last Modified: Wed, 24 Jun 2026 02:23:35 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json
