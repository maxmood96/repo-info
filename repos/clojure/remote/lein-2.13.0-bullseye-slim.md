## `clojure:lein-2.13.0-bullseye-slim`

```console
$ docker pull clojure@sha256:160a245154d49e38f01ab3495672d559fb3c038afabb47a184373a41407623c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-2.13.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e5e397c840a9803af4393320e94452e94e20782b309128e3c9ea3408086e6ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (142981631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4284635b58ad8735454438417c96dd416b6aff7e55d049926a97623b2ade13ec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:20:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:20:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:20:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:20:03 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:20:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:20:03 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:21:12 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:21:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:21:12 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:21:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:21:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:21:14 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:21:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3fbb85ed69daea718ada1595b934b72277c0a30b053b783d24ea405a211dc0`  
		Last Modified: Fri, 19 Jun 2026 02:21:32 GMT  
		Size: 92.6 MB (92574574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0226a429a16a256c0c7b14d3135bfae1829ffd33ee414e2a75e79279c2a247`  
		Last Modified: Fri, 19 Jun 2026 02:21:30 GMT  
		Size: 15.6 MB (15631145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5791680e265c28ff620382682dbcbedf2b91b85afbbcf5562eec7affd6da2af`  
		Last Modified: Fri, 19 Jun 2026 02:21:30 GMT  
		Size: 4.5 MB (4515227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9855c54939cae53abe3f7d2dd7cae7107763cfbf9c7a83c27f1f918a8d5ed3e5`  
		Last Modified: Fri, 19 Jun 2026 02:21:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.13.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:41267e458d3273068f2943e1aeb629ea5799928d3ac1e09d624437cf47880af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3025220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b13fccaf283b9b1f155532f022cc549ea7c9fe1746c99ceec8d2143f1952ae`

```dockerfile
```

-	Layers:
	-	`sha256:9876dbc20b414d43bff425834a79f244f9a5914202c9173c45a951a7348d9d18`  
		Last Modified: Fri, 19 Jun 2026 02:21:30 GMT  
		Size: 3.0 MB (3006792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef88301ab020b2821d73116745e5ee968c83fcbc68fbdc6af8a1bf77431ca981`  
		Last Modified: Fri, 19 Jun 2026 02:21:30 GMT  
		Size: 18.4 KB (18428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.13.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:27ed4ac0d0829dcdb22fd24678cea59e8032f6f304c1f015e6f5d7f40ccf7102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140423794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c378df868bc1225979336c4c1499edf303acd14ef5a43e2cf6d0a5a1771431`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:20:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:20:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:20:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:20:04 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:20:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:20:04 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:21:13 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:21:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:21:13 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:21:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:21:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:21:15 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:21:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee3ff71742d4a68256bda0c72af24d4d7262496bacc2e018492e09598a3a054`  
		Last Modified: Fri, 19 Jun 2026 02:21:33 GMT  
		Size: 91.5 MB (91542237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fbe849f17aab0ba7f8ac6e0aaee133b7c61f45f3c9917637a15a7247633eb4`  
		Last Modified: Fri, 19 Jun 2026 02:21:31 GMT  
		Size: 15.6 MB (15619788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ad1c1c2bebf928707e93be7f4b1a09dd561948716f24a15de99eac847f03ec`  
		Last Modified: Fri, 19 Jun 2026 02:21:31 GMT  
		Size: 4.5 MB (4515185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb27f78654cff738649e54020e584f4777040a9ae41d2dc33a1e5d18c0dd557d`  
		Last Modified: Fri, 19 Jun 2026 02:21:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.13.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cfb775452c32df9ff26c1269298d4e3af326ccf3ab0f47ff4d5fd2ae1390c397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3024994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105e6b7eff347ad282e76c90067a4410b763b54a359ebce42850d6690ede9336`

```dockerfile
```

-	Layers:
	-	`sha256:0ca223d9957d5bbeb502a5352b4932328060e3bae32c0b091455bfdb959db7ad`  
		Last Modified: Fri, 19 Jun 2026 02:21:31 GMT  
		Size: 3.0 MB (3006422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd67715fd27b84f5139931f5293629d0e7b650034c5b46b7c0a1ee498abb9ba4`  
		Last Modified: Fri, 19 Jun 2026 02:21:30 GMT  
		Size: 18.6 KB (18572 bytes)  
		MIME: application/vnd.in-toto+json
