## `clojure:temurin-25-lein-2.13.0-bullseye-slim`

```console
$ docker pull clojure@sha256:21796af20f59d2b9cc944768d6cc3c1733dba714e31d2272134acc3d6e694b07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-2.13.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1003b8247fc2af394e4eb7e5be08e66e0bd98b2e1a9424beb01fde283e4b1bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (142980859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ed70f21737514db6295df1f55c0bb9be1f2e1e887cf522a4202678527d270c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:20:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:44 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:20:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:20:44 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:21:54 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:21:54 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:21:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:21:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:21:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:21:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0251c4232e4025b51352f0bb7119fd866d4a6a62861f09baea6fe5af4c6eee59`  
		Last Modified: Wed, 24 Jun 2026 00:28:14 GMT  
		Size: 30.3 MB (30259447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be058dafa1f71c274107a9c222441eeace74d3c28cb7968128a224b88eaa396e`  
		Last Modified: Wed, 24 Jun 2026 02:22:15 GMT  
		Size: 92.6 MB (92574577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f07dea5adbc3cb1fcc95049acdc02bd79385412e41b749f4183a87c260cba7`  
		Last Modified: Wed, 24 Jun 2026 02:22:13 GMT  
		Size: 15.6 MB (15631226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52bccb5d74344217d6bd148432a6a2f8b0361ba5f0d03f1ca7a4d09acc0a004`  
		Last Modified: Wed, 24 Jun 2026 02:22:12 GMT  
		Size: 4.5 MB (4515179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728b30fd41d00359032c9bc0a0b8c9ac76569a5b0d02505a0786b56d42cc68b5`  
		Last Modified: Wed, 24 Jun 2026 02:22:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.13.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e3602621ed9ba774ec3ac1ee162506cc9aa02e06ba82ec388c10ac0a0dcf79a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3023596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f89d67a862575d5081d71ed76379c129f028065c848ca16ea4449933d75bfb`

```dockerfile
```

-	Layers:
	-	`sha256:e36140804f56493edb3612dddeaf8c4da3df1736c3fcc42e7bafe9e3e5fb99bd`  
		Last Modified: Wed, 24 Jun 2026 02:22:12 GMT  
		Size: 3.0 MB (3005168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa1a1198afbc2c0029d100cb0644d1f020827440f243eb0bda03b263b0ce6a63`  
		Last Modified: Wed, 24 Jun 2026 02:22:12 GMT  
		Size: 18.4 KB (18428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.13.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f4df5d02b7c7a9e72b6ce28b50015934ce9533798922b261c3c996d9dbeeabe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140424511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce0de4a92a4ef7d00e2971a8df3a1008e1334fd4a621ce0907a2b1a991bb868`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:27:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:27:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:27:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:27:31 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:27:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:27:31 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:28:37 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:28:37 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:28:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:28:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:28:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:28:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:58009b48fe731a10341c4f5f98dfa280afd10fa34cc71961411d37e306120dd0`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 28.7 MB (28746926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a90c4f6de630e67514fd2652e9e03ed96e1011bac0a114646606c2292bec1e0`  
		Last Modified: Wed, 24 Jun 2026 02:28:58 GMT  
		Size: 91.5 MB (91542238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578e68ac83231eb1c9c274247ce9bfd40e1017b9a1495717aa4df008a9bda926`  
		Last Modified: Wed, 24 Jun 2026 02:28:56 GMT  
		Size: 15.6 MB (15619713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ed471847a9933e3bc2cc9007268930b2fdaba60c1d8bd59c1dbb73fd4e70ac`  
		Last Modified: Wed, 24 Jun 2026 02:28:56 GMT  
		Size: 4.5 MB (4515204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1da6b9d8efd877ba22f8222c96770f55a78660d6ff46308c815857f3daa263`  
		Last Modified: Wed, 24 Jun 2026 02:28:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.13.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5c0e8ebabb0587e817ce79740a91b0773151f5b1735c32ad4f395b7ade0e310a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3023371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60518a291590c1eb48796ed45c7d868ddd42865e54024776a6526a53d835781`

```dockerfile
```

-	Layers:
	-	`sha256:1c7a9ddbfd9cef3813e866d3e7c43d49ce455190d694e2126a44b3efbba2ef37`  
		Last Modified: Wed, 24 Jun 2026 02:28:56 GMT  
		Size: 3.0 MB (3004798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75b86cf356f79139e3a2765ce925ba5824d441eb76399d275dd990bdd9fa776`  
		Last Modified: Wed, 24 Jun 2026 02:28:55 GMT  
		Size: 18.6 KB (18573 bytes)  
		MIME: application/vnd.in-toto+json
