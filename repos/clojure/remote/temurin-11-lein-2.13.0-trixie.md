## `clojure:temurin-11-lein-2.13.0-trixie`

```console
$ docker pull clojure@sha256:5d6ab3bcba6f67334a4b3c85872f66b0352448c0adc7da003b1c6445692d977d
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

### `clojure:temurin-11-lein-2.13.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:abd766e5268f1d8e4e77a9c828dbfb2a321c22368a750c296ee6a703f25478d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218598574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574c670c6b1ca8bae15119a2cc5c8090d7af4085c5c21b9549342302574e8a81`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:15:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:15:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:15:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:15:58 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:15:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:15:58 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:17:11 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:17:11 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:17:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:17:12 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e100bf5ce2aa48b7d7a0e58257a07816727ee4ce8e87384879ce371be7203264`  
		Last Modified: Wed, 24 Jun 2026 02:17:33 GMT  
		Size: 145.9 MB (145886166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb30becc39fa69062a511dd3475aadf86faa639b02d2e6045799487321427bb`  
		Last Modified: Wed, 24 Jun 2026 02:17:30 GMT  
		Size: 18.9 MB (18879952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5717738d1328935c37a95e311a25f2d7abd6aeea00dc3d0c371259af0025282e`  
		Last Modified: Wed, 24 Jun 2026 02:17:30 GMT  
		Size: 4.5 MB (4515169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:21ddc347f4e4e58b9e16099d2088b03db7b9aeb697c8e6869317ae7cf87cf17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79448879ad0c0452c32ded826abee5d63826237ec147f1bfdad1560dff6ac9b`

```dockerfile
```

-	Layers:
	-	`sha256:6a9773cafb56a8dfc4decf1f8a6abe3f5664b7d4dbb450e32f4eb494d0ef7774`  
		Last Modified: Wed, 24 Jun 2026 02:17:30 GMT  
		Size: 3.8 MB (3837336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46cb1daf775c061d881e12e065f277b983a52571958105f16aaff02b275bbe06`  
		Last Modified: Wed, 24 Jun 2026 02:17:29 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.13.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:79e93951ac76deaf695515bdf4051b2fb284cf437fd4352057f1b57f6889f116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215615478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea486d9e637341dfcd04e9aac6b103e134ca77c3166def02e9923ffae659dd4`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:22:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:22:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:22:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:22:33 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:22:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:22:33 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:23:56 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:23:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:23:56 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:23:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:23:58 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4b3dabfebe32e2a0dcbe4b31eee5e7f1c200a07b7d8f48787ba312af138e84`  
		Last Modified: Wed, 24 Jun 2026 02:24:19 GMT  
		Size: 142.6 MB (142582159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eb459091c7351bbebb74988247c0abd5053eb62beedfe9addf1fb6ad583d60`  
		Last Modified: Wed, 24 Jun 2026 02:24:16 GMT  
		Size: 18.8 MB (18839679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c1a3f48004b9389944cb5e350547d501f7cc5ab5339d3cd22f8a1037ed701`  
		Last Modified: Wed, 24 Jun 2026 02:24:15 GMT  
		Size: 4.5 MB (4515213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4fd2394161d6bee24b8116f2a6e407f2540618cd5de6892d39f60da601d2b148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3854048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304a4ddce3910db5309e665d55368a5bb0e724b1b987167427627ad6386c9dc7`

```dockerfile
```

-	Layers:
	-	`sha256:e3be9e5c412e1bc19268171ff1a9585a2238a0d07c72ef87ac068ff8df21ca03`  
		Last Modified: Wed, 24 Jun 2026 02:24:16 GMT  
		Size: 3.8 MB (3838194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecb2d43a87d7c9110a600c076043e66550574eaa035f58664433d5a2f9722d8a`  
		Last Modified: Wed, 24 Jun 2026 02:24:15 GMT  
		Size: 15.9 KB (15854 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.13.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:296fc97ceb29a73c8c3e0f5c0acfd0b658045ed3aa1576c3b907c95fb23bf005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209700181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0cf6605387afd92c734944f1f7efa819cb79341e576bb2debc5e9110a6d29ac`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:28:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:28:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:28:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:28:46 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:28:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:28:47 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:32:01 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:32:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:32:01 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:32:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:32:05 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c757e25eae7c582cfef76c30181fc527b42e7b29239bda1a4edb72b6b1ee22ff`  
		Last Modified: Fri, 19 Jun 2026 02:32:44 GMT  
		Size: 133.1 MB (133110616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705138ea13377438f3eb070b2fae51c0dd70212ec3066aa3293c3499cd87534c`  
		Last Modified: Fri, 19 Jun 2026 02:32:40 GMT  
		Size: 18.9 MB (18936379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79dfcbafe8f03f8d9a2c90d261fb14d29dffe52de4f921cd6c9ba8617ab63019`  
		Last Modified: Fri, 19 Jun 2026 02:32:40 GMT  
		Size: 4.5 MB (4515215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:dc5520ac888f7da2f69f00c5403e5e97bc0cd7490b6222d342d99a507cf68210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e539417113b6f688c6b18f54439aa2cd316f236dea2faf0db1b5c9f20b2c1497`

```dockerfile
```

-	Layers:
	-	`sha256:c64da1b2afdb8ac383a9f04114ce7d0ac6bb49ef2f31e1388159d84f32098d1c`  
		Last Modified: Fri, 19 Jun 2026 02:32:40 GMT  
		Size: 3.8 MB (3837721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49614cbe7baf3af07c853e56adf559b8a27de824b7b06e6ffdfb9f8dabd15ca2`  
		Last Modified: Fri, 19 Jun 2026 02:32:39 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.13.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:579832fe215dedba14b93227d44656bb0d85e7e04c8900fbad1b8e150ddfb1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.5 MB (199475717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b6f06f0c3f70fcf778b8b08660275d0ee13c709b5e1f91b59d0cd6afed58c3`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 04:08:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:08:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:08:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:08:55 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 04:08:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 04:08:55 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:10:15 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 04:10:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 04:10:15 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 04:10:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 04:10:16 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4acbf08d84aa74ba1f41a222ae6a061c228f6ba4fc5d1d428650c7427ca1fbd3`  
		Last Modified: Wed, 24 Jun 2026 00:28:42 GMT  
		Size: 49.4 MB (49386060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a047bdebac385e4e1223b3d3369c2bc758010ba299a5e191f34627a8d29c4026`  
		Last Modified: Wed, 24 Jun 2026 04:10:42 GMT  
		Size: 126.7 MB (126652580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bd9477a84acc009ae75fd54d08191c4d56c98942f2e178ea2d7ce636756cfd`  
		Last Modified: Wed, 24 Jun 2026 04:10:40 GMT  
		Size: 18.9 MB (18921858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0d95dc5bc1847d02fabd314d70ac936e49ef73c59639be2a10ca2391202b9e`  
		Last Modified: Wed, 24 Jun 2026 04:10:40 GMT  
		Size: 4.5 MB (4515187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:96dafd753c79c1e1d930fbd6ab0d761709fc0a1e7855388faad606de7643211b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf2be7fc8ba32e5dfb40d2b7796fd150854d1d59ce28d33b99dc785f04b9083`

```dockerfile
```

-	Layers:
	-	`sha256:006e25020d839c0110db584c4bf5bcaaa5ed3b5299e64bc8defc0a1960182dd9`  
		Last Modified: Wed, 24 Jun 2026 04:10:40 GMT  
		Size: 3.8 MB (3833767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:984c017335ce506150db79de35fe5b542305e539c30caa03162e61634ac0676c`  
		Last Modified: Wed, 24 Jun 2026 04:10:39 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json
