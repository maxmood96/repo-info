## `clojure:temurin-17-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:298249d2a7e6b6c52fe12f83ca707eb3bf99a032bb9d90933eee6217f7225180
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5f14c223aef67dfda4d90e08b5c80ba79ae9ae995b0d641f50b37fe986d50f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196311610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fc989f7655c247be1d8d5619c476e24319b9e686d102249c8abb3aeae2d7ba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:17:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:17:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:17:31 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:17:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:17:31 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:18:36 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:18:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:18:36 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:18:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:18:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:18:38 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:18:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0251c4232e4025b51352f0bb7119fd866d4a6a62861f09baea6fe5af4c6eee59`  
		Last Modified: Wed, 24 Jun 2026 00:28:14 GMT  
		Size: 30.3 MB (30259447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39231051b63614d1451a8ed6f665dc385dc96ac540d1438a042627df14c0a46`  
		Last Modified: Wed, 24 Jun 2026 02:18:58 GMT  
		Size: 145.9 MB (145905430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9eddebc9acd7df71d2e48cec0e27f08702e5092b97d9345ed960a56297c3bb6`  
		Last Modified: Wed, 24 Jun 2026 02:18:55 GMT  
		Size: 15.6 MB (15631072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ec25d719274db81e53239350654bc61a2818db0201efb8e3f8a9b899b44fc7`  
		Last Modified: Wed, 24 Jun 2026 02:18:55 GMT  
		Size: 4.5 MB (4515232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41560b8b996de7190f51ae8c1310f48cd9ead8f16d8be678cabfaf79e7d6481`  
		Last Modified: Wed, 24 Jun 2026 02:18:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:805eca2a6901949c9be456925b7ad9b455471d371a3708e824891bf02c78bfa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d54440a1fdf199bbc53d22f817bbd4060b49ae52583fa0f07fe29bddc436ac`

```dockerfile
```

-	Layers:
	-	`sha256:b930977096dad1e2ca6eb7945a7a204b2b095d675a70739aa81a9ef744c5d059`  
		Last Modified: Wed, 24 Jun 2026 02:18:54 GMT  
		Size: 3.0 MB (3037112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0ff31a24115938ea4884c288d0fd68c690389b5e442e117aae5edd3ed8f3631`  
		Last Modified: Wed, 24 Jun 2026 02:18:54 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:71c51f70fcbf113051bdcc0505c314e8aabf5539be8ab27307a6ed5b37551fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193606787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47b35a1447cd38bce626f3d76c5ea6c4529566b660f7a399b3e535e483bb3f6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:24:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:24:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:24:07 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:24:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:24:07 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:25:15 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:25:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:25:15 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:25:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:25:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:25:17 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:25:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:58009b48fe731a10341c4f5f98dfa280afd10fa34cc71961411d37e306120dd0`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 28.7 MB (28746926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512f431cce5178d6d196d9705cbff7f5d2a291b4b5c935132608e96be1170bdb`  
		Last Modified: Wed, 24 Jun 2026 02:25:37 GMT  
		Size: 144.7 MB (144724350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbbfd2717f7a08a92410ef01b40d756d8fd91cd8f06e01df169dd57b750fdc4`  
		Last Modified: Wed, 24 Jun 2026 02:25:34 GMT  
		Size: 15.6 MB (15619866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845f0df78e2e686c34a11be2bbf6507e22798b020724b4aa6ce2fd3eec64d48e`  
		Last Modified: Wed, 24 Jun 2026 02:25:34 GMT  
		Size: 4.5 MB (4515215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8315839fe1a9b52ec32ae0863f23feed3160687c71b92e2b47ee44de3b6de2e3`  
		Last Modified: Wed, 24 Jun 2026 02:25:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b25a9d38b46d126c62c918c7eb9a22bf650e65a1df7d9b43f476f5a72bea6b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9164f7b2d4fdb65a00c3a9276f55d1a4e87950661d01de5e4548187c4588b57a`

```dockerfile
```

-	Layers:
	-	`sha256:64f93e1c95c805696266c2519c98e551e38f9c475fd9405c97e210f04327e5a6`  
		Last Modified: Wed, 24 Jun 2026 02:25:33 GMT  
		Size: 3.0 MB (3036721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ba02e093d4cd5e41f9a45dbc6121f1bd46ad05987541c9620a13e2a9b6150d3`  
		Last Modified: Wed, 24 Jun 2026 02:25:33 GMT  
		Size: 17.9 KB (17894 bytes)  
		MIME: application/vnd.in-toto+json
