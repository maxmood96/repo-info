## `clojure:lein-2.13.0`

```console
$ docker pull clojure@sha256:7f9303bb1de8830590cd8ed0e2d6c90e51c7a566ae9d4b34fe87a88128606f76
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

### `clojure:lein-2.13.0` - linux; amd64

```console
$ docker pull clojure@sha256:f3126992990a0fdcc48feda8a7ee804f09f627659e6ec02a25bddfc3898292b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165700404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d296725e82c8753b1b71502530ec673d0790105818e29d423e8e57fec079202f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:43 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:20:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:20:43 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:21:53 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:21:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:21:53 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:21:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:21:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:21:54 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:21:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee2c0701b44194a96eb0a36e1e6b593d6b91da51bdfada17fe3ffee640f09b9`  
		Last Modified: Wed, 24 Jun 2026 02:22:15 GMT  
		Size: 92.6 MB (92574567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3da1d12fe1bd67b9a1cb64d59e338c0dc41a5c5ece92df2ec6682a1768d3edc`  
		Last Modified: Wed, 24 Jun 2026 02:22:13 GMT  
		Size: 20.1 MB (20108017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d98ea3c5f0c99bcb67677de959da2134251d13d41b02ea07cb739304c4ff1a4`  
		Last Modified: Wed, 24 Jun 2026 02:22:12 GMT  
		Size: 4.5 MB (4515181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d53b24d2dae47f8566dcf3b5cca8157e7129e77f7e81537f2ebf40c139b1594`  
		Last Modified: Wed, 24 Jun 2026 02:22:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.13.0` - unknown; unknown

```console
$ docker pull clojure@sha256:e32f63edd4ebabacee7f0e245475f70f0592a0550b7ea9afaac1e0b3830a9dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09350e5bf9a8ef749d8d4d456e85b2cd0652ae3b08591da84f6f2adcebe5344d`

```dockerfile
```

-	Layers:
	-	`sha256:8f417570b583a038668496634d644b0afa8c5f87ee9e51c502ec8312f4a7df26`  
		Last Modified: Wed, 24 Jun 2026 02:22:12 GMT  
		Size: 4.3 MB (4253310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec5d5eb3db4c7df8c4a94c5dbce4352268a0e842b79a740e005f83ca27ea20e9`  
		Last Modified: Wed, 24 Jun 2026 02:22:11 GMT  
		Size: 19.6 KB (19629 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.13.0` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ff42e79f1ab03c6fca0846693cda29e376f25f504f85ac8661e2842c0cc25695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164387202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e623a2d35b632db40e835c4356aa84d1a16c774d8e0d9bec81378ab286ef7b18`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:27:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:27:08 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:27:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:27:08 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:28:18 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:28:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:28:18 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:28:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:28:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:28:19 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:28:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db5afc03736b31104e588033cea3438f59c73d2780c15c98314a6028d9fada7`  
		Last Modified: Wed, 24 Jun 2026 02:28:39 GMT  
		Size: 91.5 MB (91542269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d75895775f3556ccd5acaab5e9f155b5ef4354a215e7148ee1bdcb6420977ff`  
		Last Modified: Wed, 24 Jun 2026 02:28:40 GMT  
		Size: 19.9 MB (19940122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09137afc3e1da52feed01bf5d98ec85fe4cf62ca5961bce3c3c15b91412bc3c6`  
		Last Modified: Wed, 24 Jun 2026 02:28:39 GMT  
		Size: 4.5 MB (4515181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7cc0c6b70fcb7108ad40bd79cc037d53e9963674bbc239cf6d0fe29dc449dc`  
		Last Modified: Wed, 24 Jun 2026 02:28:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.13.0` - unknown; unknown

```console
$ docker pull clojure@sha256:030b9c4a33161b2f31d9af277404b0510062b221fcdad5dfa7e4cd547d9ccd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878d47eb450563036bdca1867645311053d2d9384c2d4d4fb5d364dced40b272`

```dockerfile
```

-	Layers:
	-	`sha256:0bbf5598e1594ffe87b4fdd7e785fff3ef488908d7e586a6ca1c9e47175a2eb1`  
		Last Modified: Wed, 24 Jun 2026 02:28:39 GMT  
		Size: 4.3 MB (4252994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:363e217c77ffd15bd37660098b709a3b70760d87db182b7b73f86f24bd4e7093`  
		Last Modified: Wed, 24 Jun 2026 02:28:39 GMT  
		Size: 19.8 KB (19821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.13.0` - linux; ppc64le

```console
$ docker pull clojure@sha256:f179e58df2450e746ddbdae5f18eca4312365a9247d0830d85d58c0aec72f210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169108168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0946dc73b9cec62a85ec1814ad55485ea17f60420920f3824e70b66d7cc323f9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:30:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:30:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:30:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:30:21 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:30:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:30:22 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:33:52 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:33:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:33:52 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:33:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 17 Jun 2026 00:02:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:02:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:02:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af2d7bc5e0f6f23b949f449ec38352dcc13ff43d0d262dab584e4f344eec386`  
		Last Modified: Tue, 16 Jun 2026 23:35:12 GMT  
		Size: 91.9 MB (91914009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68947c24a5e1c48feb5dfc5d4e28fe4f56550fcd7d0ffdaf1322d3ddb36f090a`  
		Last Modified: Tue, 16 Jun 2026 23:35:09 GMT  
		Size: 20.3 MB (20331869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7f1d5b8d6bc4ae48b7364827721c152758155257cfff4b80279cd72f3d6bf1`  
		Last Modified: Tue, 16 Jun 2026 23:35:08 GMT  
		Size: 4.5 MB (4515191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf89a28de7a2761db3b1d45bf3c00b21c7ab706a0db5122da20022d327e92acf`  
		Last Modified: Wed, 17 Jun 2026 00:03:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.13.0` - unknown; unknown

```console
$ docker pull clojure@sha256:2cadce95d8e923b6153bd02c9f9dcce3f6787e1419d4e0d885a5c92a7d268afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4258228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95253a85c927dae803396fff97931566b21def29e53435e55c9f705145327753`

```dockerfile
```

-	Layers:
	-	`sha256:c01440eecd04d82a4e45f97594bb7a0f49f23f1333d4b3ea97ffc3dc2bf1f775`  
		Last Modified: Fri, 19 Jun 2026 02:54:17 GMT  
		Size: 4.2 MB (4238519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2561dd60319cd3da789732cdeac71965020c1b35cfd067ecd01e79569ff7829`  
		Last Modified: Fri, 19 Jun 2026 02:54:17 GMT  
		Size: 19.7 KB (19709 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.13.0` - linux; s390x

```console
$ docker pull clojure@sha256:080bdd76c1776a635e819d21924dd62eabe9ce4e43258590e5478ae70aa88d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159868315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a3cbdc6c06e7d0e2264fc7ecddb1b6d93b6b1ba9927a7bbac0071fc0238851`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:07:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:07:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:07:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:07:44 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 04:07:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 04:07:44 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:09:00 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 04:09:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 04:09:00 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 04:09:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 04:16:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:16:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:16:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bdd2e9d83d68023204331dd445067114dbd3500d2d496368624fa7ef81743d4a`  
		Last Modified: Wed, 24 Jun 2026 00:27:09 GMT  
		Size: 47.2 MB (47161675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42b02c985ff427f09da77745bd5599ec265500d0ffe9217e4629e6e410d74c2`  
		Last Modified: Wed, 24 Jun 2026 04:09:44 GMT  
		Size: 88.4 MB (88420330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5807e04f5849dd283ff540b02d07b6683180964ed3837e17d4bb24c987c5b6`  
		Last Modified: Wed, 24 Jun 2026 04:09:43 GMT  
		Size: 19.8 MB (19770663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1030fac02fc7fb6c91fdb9664b2131408274d0bb6c4fd223c0b7b0635b4163`  
		Last Modified: Wed, 24 Jun 2026 04:09:42 GMT  
		Size: 4.5 MB (4515219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb5d83e368def47b9f1afb2895d4d3623800d7955077984eb7050dd1f5a205a`  
		Last Modified: Wed, 24 Jun 2026 04:17:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.13.0` - unknown; unknown

```console
$ docker pull clojure@sha256:8c4c415b66996c3614e5347cdc4ef134cb86e1cc956464ae6d8096ba3de9c17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d4ac3ec8453944e11f4ab01447fac0a96d5bc4dff75158340a524e4c67f38c`

```dockerfile
```

-	Layers:
	-	`sha256:ebb8c08eee2230518ab867ed3ef9f2c0304481056cc5f8cda5924d8f766e1dbe`  
		Last Modified: Wed, 24 Jun 2026 04:17:08 GMT  
		Size: 4.2 MB (4229686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6c6a5ef93ec355003f53afc56b79658f729a3526cd874bfbd9b927c8b00884`  
		Last Modified: Wed, 24 Jun 2026 04:17:08 GMT  
		Size: 18.7 KB (18676 bytes)  
		MIME: application/vnd.in-toto+json
