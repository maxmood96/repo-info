## `clojure:lein-2.13.0-bookworm`

```console
$ docker pull clojure@sha256:2eb79b4655f0bbfd748ebe8a0f17ef31b3a1614588715be0e217c795ef2738ae
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

### `clojure:lein-2.13.0-bookworm` - linux; amd64

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

### `clojure:lein-2.13.0-bookworm` - unknown; unknown

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

### `clojure:lein-2.13.0-bookworm` - linux; arm64 variant v8

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

### `clojure:lein-2.13.0-bookworm` - unknown; unknown

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

### `clojure:lein-2.13.0-bookworm` - linux; ppc64le

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

### `clojure:lein-2.13.0-bookworm` - unknown; unknown

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

### `clojure:lein-2.13.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:4cfcadd0572b5b444e9799569faa3e136dfe4a4e297cf010dbf3a8d6ffe85c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159867763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a87b10344ab2fedf822731fbb050f9dd174f5625565366c8e21a366e47f5854`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:30:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:30:16 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:30:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:30:16 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:31:32 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:31:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:31:32 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:31:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:20:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:53 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14907b0f682b8ecfba5edca7e3ae44505f908a9f5163eb33cb4b2d568ad948ea`  
		Last Modified: Tue, 16 Jun 2026 23:32:19 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e7043565b34b7284c7fa5d693843e5ece45dbcaec9986711d409c32de70cec`  
		Last Modified: Tue, 16 Jun 2026 23:32:17 GMT  
		Size: 19.8 MB (19770336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987739cc204bb874386b889d6cc4fae0c385eb47a370889b6f322604802cc162`  
		Last Modified: Tue, 16 Jun 2026 23:32:16 GMT  
		Size: 4.5 MB (4515179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4aaa912ff704d061d44d23769c8be07901fe41f606472834ea209de6b20d73e`  
		Last Modified: Fri, 19 Jun 2026 02:21:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f5068281eb06bbdfea22c7b322d7be432eeee3f9c10404cd1c88dd0748b8462d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27786433f82ddfeef171bc59fd2f17d00e1c80f284cb4ac561c26186eb46330`

```dockerfile
```

-	Layers:
	-	`sha256:ee98f5f42ece53f4711549f487ad2a4086af1382044b6054b6d3c987fc2574e7`  
		Last Modified: Fri, 19 Jun 2026 02:21:04 GMT  
		Size: 4.2 MB (4229686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80bf930ce76771bd72b8f2feaf0c88d0776e651c0deaeb7f818d36e4f1812595`  
		Last Modified: Fri, 19 Jun 2026 02:21:04 GMT  
		Size: 19.6 KB (19629 bytes)  
		MIME: application/vnd.in-toto+json
