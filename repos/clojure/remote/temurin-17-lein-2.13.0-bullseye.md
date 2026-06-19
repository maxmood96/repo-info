## `clojure:temurin-17-lein-2.13.0-bullseye`

```console
$ docker pull clojure@sha256:38c12fe158c0be12abfce542239e5d6989a76f8eb689fe33ca9e8da717efb924
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.13.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ed3d760cbdc1bc46a025245e3e9595192280e0fbc2bfaec1ea77ddcd5c16d820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221121533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0cbf28b2d23b2cdad89394e0be19778bc7fc5320f38f869139033cc8a1ea36`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:16:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:16:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:16:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:16:57 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:16:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:16:57 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:18:00 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:18:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:18:00 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:18:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:18:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a59815f07d195238fbc5411c5f60523304f0417ce5c51ede29a900843da00b6`  
		Last Modified: Fri, 19 Jun 2026 02:18:22 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5945b72451b685105d794cd8f7b789b7eb6bc95daeac95766de2ecfbd1e631a7`  
		Last Modified: Fri, 19 Jun 2026 02:18:19 GMT  
		Size: 16.9 MB (16928652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f15892e904bf03367cb62d566bfa612efb0e02a176e23886d0c3b60184d824d`  
		Last Modified: Fri, 19 Jun 2026 02:18:18 GMT  
		Size: 4.5 MB (4515229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76ab50d478fad84083d12d9b99a5c750eb41dd47e0b910b9cb52ff732b15d50`  
		Last Modified: Fri, 19 Jun 2026 02:18:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f476c979400b1424fe2a9dc650df4207952658ca286af2167ede0454a211bc76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a777b87b04e55317084c064ac06c9d0d3881d239da732d09028a432d57fad9d`

```dockerfile
```

-	Layers:
	-	`sha256:5f129d6f82d75d07b6a2899fb8386bb10ebc2f08e1666c06cc06c1e3e9debc8a`  
		Last Modified: Fri, 19 Jun 2026 02:18:18 GMT  
		Size: 4.5 MB (4502651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9619a1c52dbd102e9a7dc47a34fd015f727d1bc3a7f9689cd24b1f0b69f0757d`  
		Last Modified: Fri, 19 Jun 2026 02:18:18 GMT  
		Size: 17.7 KB (17738 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:76eb2ffc588d3673ac8510491e091490c793ee2129014873b2ca189f11e44560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218421806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a6c97979cfa29a9c4cd801c269bbd1fedd6fdfe56a897859059742fd052495`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:17:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:07 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:17:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:17:07 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:18:12 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:18:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:18:12 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:18:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:18:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:14 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d0dd045dc33d640d2ed82c9f22695f3a2c3b3778384a270c4fe0c8d1060672`  
		Last Modified: Fri, 19 Jun 2026 02:18:34 GMT  
		Size: 144.7 MB (144724298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5bc168cc01ba8ad98ca3530fe18361ad1185c5d3dd713837eb4cff4bada119`  
		Last Modified: Fri, 19 Jun 2026 02:18:32 GMT  
		Size: 16.9 MB (16917731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1f4c1dbf7e3db452c324740c6ac9854ee4988cfa471ee0735353a3c3ff0249`  
		Last Modified: Fri, 19 Jun 2026 02:18:31 GMT  
		Size: 4.5 MB (4515233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fab5f01eecf96a7ab3a6efdeb308738fb609713e0af77ad53f23d3099a831fb`  
		Last Modified: Fri, 19 Jun 2026 02:18:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9cd734608da21fb7672a9db7b40195749d070c74a219958136b25758c88b6ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4519483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb1cb8aabfc11a720331706d8775b1c4b039303aadbf147dd21cddb9199fcb2`

```dockerfile
```

-	Layers:
	-	`sha256:45b1c6dcf853e6a7f01e6e9c14e4f39c1de8389ff0b6c0c1c1fa0930a255bd60`  
		Last Modified: Fri, 19 Jun 2026 02:18:31 GMT  
		Size: 4.5 MB (4501625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:529d26942d73524279da7b09a3608e74a114760b2fbd6535a8d9ce8a2a4c483f`  
		Last Modified: Fri, 19 Jun 2026 02:18:31 GMT  
		Size: 17.9 KB (17858 bytes)  
		MIME: application/vnd.in-toto+json
