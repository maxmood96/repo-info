## `clojure:temurin-26-lein-2.13.0-bookworm-slim`

```console
$ docker pull clojure@sha256:745c13db103175144fff95d3ea64131c2ccf5d1af0f1190b784385055ddec6b7
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

### `clojure:temurin-26-lein-2.13.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:852e046082a6d7e994bc2584a8b5db7bec154ef427f3fa0fedeb8ce17387e8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145336785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b662a3e4e8a4319223c3b454c723a2e60a3a9893f3b1f94084f1e29388da57`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:22:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:22:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:22:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:22:22 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:22:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:22:22 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:23:30 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:23:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:23:30 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:23:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:23:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:23:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:23:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff27641e7af9ecac852f28c96a3c5826e128fa00b592547bfee72ac79c68ab41`  
		Last Modified: Wed, 24 Jun 2026 02:23:51 GMT  
		Size: 94.5 MB (94524390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879e739e5c39fad568ec34f53e6295bae4b566791b4638f35023127429d66661`  
		Last Modified: Wed, 24 Jun 2026 02:23:49 GMT  
		Size: 18.1 MB (18059113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece51423105868f7e96e637ccbb7bd830b02785d8358110607ecd2426855aa61`  
		Last Modified: Wed, 24 Jun 2026 02:23:49 GMT  
		Size: 4.5 MB (4515214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a13e86d8703cb4d7972bf8d85e3d7c28a0a1872c8d19cbae102ca22d9f82e91`  
		Last Modified: Wed, 24 Jun 2026 02:23:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b0b43a3814f2fd3524e0167543466972a990d807127b9f4cfe4fa641a748504c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2714994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d266fc22c09bb23cb95448bae4f41056ea85bd7b7045b183314a82065bf336`

```dockerfile
```

-	Layers:
	-	`sha256:53352c6dde1ebb21d38228d74f64f5fbf60e7deabf6ae7446cce8c8c267f9963`  
		Last Modified: Wed, 24 Jun 2026 02:23:49 GMT  
		Size: 2.7 MB (2697228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80d15bf875431c6492b7d183646b894a3ef45cfa9560856379b67e61af453967`  
		Last Modified: Wed, 24 Jun 2026 02:23:48 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4f73bb2ab8166614f4248886795453dfc7c56107e1a5059580e486703ec73e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144036712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa860475be61365d9d02149ab69ecf7a3fb00cbb0d7de9917efa9daf83e2ef3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:29:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:29:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:29:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:29:00 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:29:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:29:00 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:30:09 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:30:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:30:09 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:30:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:30:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:30:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:30:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988a8a1796bdca29adc7eecd883466c32adef1f4e92971123c44853c57c25cb5`  
		Last Modified: Wed, 24 Jun 2026 02:30:30 GMT  
		Size: 93.5 MB (93504324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39619b02eaef1527b22cd18e50bce82f042c22b40de4ce6c5c890d1ed67a4cd8`  
		Last Modified: Wed, 24 Jun 2026 02:30:28 GMT  
		Size: 17.9 MB (17894344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e810d21c4a383558092c98682ee4f318d89db7846076eccf3a8adc831b997b69`  
		Last Modified: Wed, 24 Jun 2026 02:30:28 GMT  
		Size: 4.5 MB (4515197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5c137051f5b22e796f7ad043c7fcbea4f0eb54973da4c5c53e7a1323db5bf4`  
		Last Modified: Wed, 24 Jun 2026 02:30:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8a32bf53e76b8537f9e8fb3747d54ef52c75304a93f7bcbd1a61151b6e3d073d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2714726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf5a16e798099a092196451cd5228ed676ea26c4a41a976c448bf480fcba4c1`

```dockerfile
```

-	Layers:
	-	`sha256:0725756c5e064110513296dddb16d869943f7b225282de5982a9153354c73dcc`  
		Last Modified: Wed, 24 Jun 2026 02:30:28 GMT  
		Size: 2.7 MB (2696840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a22a78ab65b3c2cc7e324c9a54df97558143b98d9e893cd025948ada0dc22fc`  
		Last Modified: Wed, 24 Jun 2026 02:30:28 GMT  
		Size: 17.9 KB (17886 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c309e748d6a28784a55a8e95b4b7cd0f06b339fcc502bc8fb569977eae872838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148762978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ec0f64b9479cfe505f8820410b55ef202feeb9f438a5db254c7aa1be625e11`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Wed, 17 Jun 2026 00:10:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:10:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:10:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:10:18 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 17 Jun 2026 00:10:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 17 Jun 2026 00:10:18 GMT
WORKDIR /tmp
# Wed, 17 Jun 2026 00:12:42 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 17 Jun 2026 00:12:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jun 2026 00:12:42 GMT
ENV LEIN_ROOT=1
# Wed, 17 Jun 2026 00:12:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 17 Jun 2026 00:12:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:12:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:12:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f29b00e9bc0b9af92e1b64e13edf9ecde1571af48c5d8d0fce068fb62ea3514`  
		Last Modified: Wed, 17 Jun 2026 00:13:19 GMT  
		Size: 93.9 MB (93902081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33648ce62c2e7cdbec7791b4a5963531c6c9da3b53bd57ffd24ff658ad445438`  
		Last Modified: Wed, 17 Jun 2026 00:13:17 GMT  
		Size: 18.3 MB (18263305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6745d66e8d3356f540699a80478b7c520e561c7dfb1d2688ebf23ca2fd13751`  
		Last Modified: Wed, 17 Jun 2026 00:13:17 GMT  
		Size: 4.5 MB (4515220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a7582c65a86f0c61d178db1cf4278471b35085c8a5a6f795025d4a420910df`  
		Last Modified: Wed, 17 Jun 2026 00:13:16 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:083f7c9c337e541cece8a1254513006c618617b2fbd47e54a8a05666f2fe62fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2700807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cdc3de8df0d15057ac261ec3775f3fe654c0d6b12e1d1ce05a8ae3b3a7c3055`

```dockerfile
```

-	Layers:
	-	`sha256:a758da015a4fe5dab05f606a226a79773e595c12b92833ba972b76cf15fad680`  
		Last Modified: Fri, 19 Jun 2026 02:58:37 GMT  
		Size: 2.7 MB (2682997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16c0f16a8542596fe98abc9a6bc33711f03df8cfa4d636236356e1bfefb779cc`  
		Last Modified: Fri, 19 Jun 2026 02:58:37 GMT  
		Size: 17.8 KB (17810 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:6723af90163a8b637fc516fd55cc3a82832a9d4819129c7d9701ac9e4650f333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139671257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f631b9334f27582fb7cb37f130a99fb3186477aa106cd2dfa4d0b74c8c0ebb5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:19:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:19:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:19:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:19:36 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 04:19:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 04:19:36 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:20:47 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 04:20:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 04:20:47 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 04:20:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 04:20:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:20:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:20:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34db396c791848b69e7c26c38ce79f42e22c2f325a414bab3309ac2f2c84ba38`  
		Last Modified: Wed, 24 Jun 2026 04:21:13 GMT  
		Size: 90.5 MB (90536980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7dd760556fe70203c10715c33df4c8d90ecdf28d4b9426342c396676ea8232f`  
		Last Modified: Wed, 24 Jun 2026 04:21:12 GMT  
		Size: 17.7 MB (17725058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea29f96e18536990bf3949b559a01725c0295d9b935c044f776a0e8a340061c`  
		Last Modified: Wed, 24 Jun 2026 04:21:12 GMT  
		Size: 4.5 MB (4515205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5e7065a2803368d54039954d1c8c52753e31d0522e07eb23e339d8d6086ea4`  
		Last Modified: Wed, 24 Jun 2026 04:21:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:41d4e9a49a88640a9c0669e59c1d20a163784ccab8b40cc9566049177b6bc39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f51a3276f7827b5d6e399d2c18fa93898987d1cb5359f7aa20b933749a1a173`

```dockerfile
```

-	Layers:
	-	`sha256:a62ccd3cbf8357d84a0b144aa9cabcd61bb7165e97e382fcb3cd35a5fcea2174`  
		Last Modified: Wed, 24 Jun 2026 04:21:11 GMT  
		Size: 2.7 MB (2674228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d655ca35ab694554fd1cb0854d63050ac8e28173659f385038f85a2da17031d`  
		Last Modified: Wed, 24 Jun 2026 04:21:11 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json
