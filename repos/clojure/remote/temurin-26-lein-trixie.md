## `clojure:temurin-26-lein-trixie`

```console
$ docker pull clojure@sha256:f862e0d31ef2c30c3f6489c7e328a26e753c2622cd2e79c99b1c5cf7310f0fd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-26-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:de61f4641b73a2d256b530e003e21b7fd7fd56e43378be99bf9613fcfe1d6667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167237554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3b720a38b63fe441e61b7de23ca760dc006ef1b3eb53395ed2d08ae2b1c075`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:22:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:22:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:22:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:22:37 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:22:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:22:37 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:23:55 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:23:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:23:55 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:23:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:23:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:23:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:23:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8724f3f192c3330b13c572c4038b7bfbd6a8fcf1af119df9b7d87c776c1d4754`  
		Last Modified: Wed, 24 Jun 2026 02:24:17 GMT  
		Size: 94.5 MB (94524353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c2f5797f561439ae6e5d6541b088e3ae6ceb447e67723650fbf49673a9098d`  
		Last Modified: Wed, 24 Jun 2026 02:24:15 GMT  
		Size: 18.9 MB (18880306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d732c5560c0ade6d3d26d1baf9a4325e8682daba4a2ea2721caa8b0a42eaa6a3`  
		Last Modified: Wed, 24 Jun 2026 02:24:15 GMT  
		Size: 4.5 MB (4515211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64f22c2a156e31bf808ac2cf1d1b8416cfd3129dfb6818d1445c26bea8da25f`  
		Last Modified: Wed, 24 Jun 2026 02:24:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:aa6d6a470ea2e4329de835a3cb7d3900cf0f1a5ca76080c4819fb7945a4de86f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82822d4f63e58ade12e85ba980fde99fa1553b95cfe631cd0a62b65a7b361e39`

```dockerfile
```

-	Layers:
	-	`sha256:5806a08803f677d0dc43be79993ee39f6f402312c731256df06377c4b5c4a7f2`  
		Last Modified: Wed, 24 Jun 2026 02:24:15 GMT  
		Size: 3.8 MB (3782711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49626060496852b7ddfe49c2190f756ddd49310c43126b8126f384eea8243e76`  
		Last Modified: Wed, 24 Jun 2026 02:24:14 GMT  
		Size: 17.7 KB (17711 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fc146c2af776039453e143de15dc5f92c21a58c58191560e71b7e14ad7ae344f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166538155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1abb35534783f4516ebb511e64350c0f0dee74273c1d2d75e4acdb439b377df`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:29:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:29:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:29:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:29:21 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:29:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:29:21 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:30:35 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:30:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:30:35 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:30:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:30:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:30:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:30:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c435a64730b025afbb536b6d4234f517c2eed84566aa66af6d3c5d63409965c2`  
		Last Modified: Wed, 24 Jun 2026 02:30:58 GMT  
		Size: 93.5 MB (93504335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9ded00a238301ea2bb9a22b5e58074e1c4d56d4257152689efc316ed722124`  
		Last Modified: Wed, 24 Jun 2026 02:30:55 GMT  
		Size: 18.8 MB (18839798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c89ce1ce9e05ea1f3abec047975d1a2a8323c09e2ef962f3fb7ce46bfd6be54`  
		Last Modified: Wed, 24 Jun 2026 02:30:55 GMT  
		Size: 4.5 MB (4515198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5a4bde19c5af6ddf10cd36cdb58fc48b60ed012d3f86e2b5de80796d07fc19`  
		Last Modified: Wed, 24 Jun 2026 02:30:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5bcb929d2fabeeabe299c5c8ed4b42ca1a8c28b9ecf8b083c2c04d55b5aa06c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf98251e4e806c291b4bf5d07dd3e9ace6e9f5ec469485f0668298dc8e4b69d`

```dockerfile
```

-	Layers:
	-	`sha256:29e90369d1f14106f85e06974091b06cb0f81b606ece5b7c43bfcec02a9451c3`  
		Last Modified: Wed, 24 Jun 2026 02:30:54 GMT  
		Size: 3.8 MB (3782948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb2b0c35ce0a972878b661e972d6908168e872506e0626b2145aeb1c6deedef8`  
		Last Modified: Wed, 24 Jun 2026 02:30:54 GMT  
		Size: 17.8 KB (17832 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:1b978d8dd72d7f0e1dc1a9d106c66e1463ef4d3158b88da812a330b89032a675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170492189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe753831d2d92fa2e0118289052b55ab1d46d5692426a52569845a11f8c63da`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 08:34:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 08:34:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 08:34:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 08:34:39 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 08:34:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 08:34:41 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 08:37:30 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 08:37:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 08:37:30 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 08:37:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 08:37:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 08:37:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 08:37:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:99b7058514c1f9221ac3b0625d731341802c32d464fd604a099ae71d3765bbfd`  
		Last Modified: Wed, 24 Jun 2026 00:30:31 GMT  
		Size: 53.1 MB (53138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb8abfa12b6427363309b1547420d955191530c07a3fd257bfff14f6647ed36`  
		Last Modified: Wed, 24 Jun 2026 08:38:02 GMT  
		Size: 93.9 MB (93902053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e04753e42f93f7aef43fc55a11a604732b7c6a973c308dcd8fef6b77ca1e5b1`  
		Last Modified: Wed, 24 Jun 2026 08:38:05 GMT  
		Size: 18.9 MB (18936451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3bf55a84d7a76fde623723d2393dc23d70ed84d4c9dd63692be0c7ee1e2c84`  
		Last Modified: Wed, 24 Jun 2026 08:38:05 GMT  
		Size: 4.5 MB (4515187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51dc046439c577e4815a322c8dd27a18105e64fa9dde739d1c3a28f0c114757`  
		Last Modified: Wed, 24 Jun 2026 08:38:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4edb5a0eb619f737459d4c7f9997525d65ca717dc0195c48bea16c935786c3f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6691497225d9d9eaba31b983f40450e4bb9d23cc948f37b83813c2e7a4095e5e`

```dockerfile
```

-	Layers:
	-	`sha256:c65f7468bc977e831ac396b3998166ea993d576fbff0ed139a57a8504d6b0dd9`  
		Last Modified: Wed, 24 Jun 2026 08:38:05 GMT  
		Size: 3.8 MB (3767647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1fd6fcc675279d7d3f44defc58b064c76aa6cba4759f35e2dc36ac578d909d6`  
		Last Modified: Wed, 24 Jun 2026 08:38:04 GMT  
		Size: 17.8 KB (17755 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:b88d7a54cf302e72d6892be8208b819d2cb0660f84d3f38aec666625540827c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163360398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5255106701cbd74f1ecd0d169c643664d9ce7ee47a871d6f41eb139ba78e2fce`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 04:20:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:20:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:20:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:20:23 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 04:20:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 04:20:23 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:21:34 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 04:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 04:21:34 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 04:21:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 04:21:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:21:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:21:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4acbf08d84aa74ba1f41a222ae6a061c228f6ba4fc5d1d428650c7427ca1fbd3`  
		Last Modified: Wed, 24 Jun 2026 00:28:42 GMT  
		Size: 49.4 MB (49386060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f068187139e0bf91acf14c4ce90f28dbb05c05fb7a927bc3ba5c989c66e2291`  
		Last Modified: Wed, 24 Jun 2026 04:22:01 GMT  
		Size: 90.5 MB (90536980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e69daecbe5e880168c59001aa5ab1050228df06473ae61de227d5b33ce4b6dc`  
		Last Modified: Wed, 24 Jun 2026 04:22:00 GMT  
		Size: 18.9 MB (18921746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5edc6b5cf8248933ed4914ba3554a0ac63ca022737933bd468b3494eb7e74d1`  
		Last Modified: Wed, 24 Jun 2026 04:21:59 GMT  
		Size: 4.5 MB (4515184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c853f84bde58bd34bee5aaa79a12043f02df10b985079e5099ebd71f2f30320c`  
		Last Modified: Wed, 24 Jun 2026 04:21:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:05787575cb4bd97b5fefa584e0b3024b5536444c8f2bafbb648887e17129223f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3782034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef22afe47d5df84900fd043c7249e6e2679fdce4562325039b56c5cb749c10a`

```dockerfile
```

-	Layers:
	-	`sha256:4bd09df252de616bf1be2efa1148b33da9e0ae57bfdbc69b77a749c854a92566`  
		Last Modified: Wed, 24 Jun 2026 04:21:59 GMT  
		Size: 3.8 MB (3764324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56fd69815c1847890abbaa2d736fd6b6945b9e2e94f6b43ffd72ae244036ef01`  
		Last Modified: Wed, 24 Jun 2026 04:21:59 GMT  
		Size: 17.7 KB (17710 bytes)  
		MIME: application/vnd.in-toto+json
