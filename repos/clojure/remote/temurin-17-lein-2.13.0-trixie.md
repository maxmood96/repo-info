## `clojure:temurin-17-lein-2.13.0-trixie`

```console
$ docker pull clojure@sha256:1819c84b6c397239f848181316554facc3dd2a5e2a95cc279f2a0f18e229768e
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

### `clojure:temurin-17-lein-2.13.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:8fdf68e31f873c52247734a8c8c4849d365bf8618b95e30fe5b40f985fe4a46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218618168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e539176c80d4d19e41731b3419f9c985cc1c92b0ab40dacf45ed7ab30727b5ec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:17:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:17:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:17:42 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:17:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:17:42 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:18:57 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:18:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:18:57 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:18:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:18:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:18:58 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:18:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc725b6497756557fbc8430e1fce0a2d5b2449fd2f8599a2301cf8822ca383bf`  
		Last Modified: Wed, 24 Jun 2026 02:19:20 GMT  
		Size: 145.9 MB (145905441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530266ea1ded44632de90dc0006be6204241456118db844f9f141fc53f13373e`  
		Last Modified: Wed, 24 Jun 2026 02:19:17 GMT  
		Size: 18.9 MB (18879869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35b303b9e9b25ef06125fa6862c35e0277c22b422bf2b6a2c765193da63e910`  
		Last Modified: Wed, 24 Jun 2026 02:19:16 GMT  
		Size: 4.5 MB (4515174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ccad1dae9c9a3eae613ad0222da2ddcd0fe1c038baabab86339fc93a626bae`  
		Last Modified: Wed, 24 Jun 2026 02:19:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fd0218aad0d9abf06ea8d2e12aaf36e29c6cf3fa6e3159ba040867e5a7895051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51e5a71e59b42c4da1ac714f197ee70d1836e405b9eddeb6a3ecf5794140667`

```dockerfile
```

-	Layers:
	-	`sha256:ab0d4767c01310e2d8ab796552ab8ab14b8159f50b7714f72a97c56fbf53e2f2`  
		Last Modified: Wed, 24 Jun 2026 02:19:16 GMT  
		Size: 3.8 MB (3817820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:912dd94c288a85612bd937f861cb29a69cc6022773a095830a1001bf3f7e9845`  
		Last Modified: Wed, 24 Jun 2026 02:19:16 GMT  
		Size: 17.7 KB (17718 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f97fc44bd721174b4e439c0fc9fcafd550e2e46f220e6c32193d0a64b978b9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217757795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8eea3b58dfbdeb5cf3710f3258ee404340b0025ed104da87afb8f81fadd1d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
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
# Wed, 24 Jun 2026 02:25:23 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:25:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:25:23 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:25:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:25:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:25:24 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:25:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512f431cce5178d6d196d9705cbff7f5d2a291b4b5c935132608e96be1170bdb`  
		Last Modified: Wed, 24 Jun 2026 02:25:37 GMT  
		Size: 144.7 MB (144724350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01848e92cae60a90ad8787529715d2d44ea171ff16bf0b25aa88f651aac1ac0`  
		Last Modified: Wed, 24 Jun 2026 02:25:56 GMT  
		Size: 18.8 MB (18839439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c8c89322ebbc0b6b3724bc0f5abf9077a277a6eda7a9d2dbcc022de26fb309`  
		Last Modified: Wed, 24 Jun 2026 02:25:53 GMT  
		Size: 4.5 MB (4515181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262e9003fe49c9709b73b5e93eb265fb3f9799181f171238e393ab26883037d4`  
		Last Modified: Wed, 24 Jun 2026 02:25:48 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d3327b04bb2844d8e7c29a54701c870e06c6aad6759b48dea6de2dad0b74ed93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac1480a010cfce90540293ff230c0fd9cc6c6ef83e9e1ad9386e14f02e1fcb8`

```dockerfile
```

-	Layers:
	-	`sha256:2aa6ae8befc30d1704cf24f6a548cecc1ee5e22b0ca4ef3aaa459afcf00957ae`  
		Last Modified: Wed, 24 Jun 2026 02:25:51 GMT  
		Size: 3.8 MB (3818060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca9fecc436992b17d08d90ea3b474706807032487fe83e789b8cd1e67396478a`  
		Last Modified: Wed, 24 Jun 2026 02:25:48 GMT  
		Size: 17.8 KB (17838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:df8e9dc40857c3f980459bf8e73b053da3ddd751afa8d715e35c4b5290c7017d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.4 MB (222356447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001ec24b104d058da3b41b786b5c830f3072dba17fb59a586a4c65654b1f0b71`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:40:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:40:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:40:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:40:48 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:40:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:40:48 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:44:06 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:44:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:44:06 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:44:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:44:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:44:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:44:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4c522651359f2b9382194c5170132137b32f6d0214c41d2c39ba3ec770a8cb`  
		Last Modified: Fri, 19 Jun 2026 02:44:52 GMT  
		Size: 145.8 MB (145766191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd274513b420e4bb3a0ecb58544c5242815ebed9ed6da61d5bfea5218b8f7db4`  
		Last Modified: Fri, 19 Jun 2026 02:44:48 GMT  
		Size: 18.9 MB (18936669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f329c88d6e76266b37eadf4693d273775fd1d92445c57e2df132c84e9061e6ce`  
		Last Modified: Fri, 19 Jun 2026 02:44:48 GMT  
		Size: 4.5 MB (4515218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e16c408a81fb540b5029c73f97c3042d48349864073f488b7eaddd8e535668`  
		Last Modified: Fri, 19 Jun 2026 02:44:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c392c3a400788c6eb6a81b8813948b7cee4e5a7a3512ce586b83d884aaacec90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba206f20a93d01872f287803c4a4bb4e6064cbb91d385477e860449debf292b`

```dockerfile
```

-	Layers:
	-	`sha256:0de40abeabe438a5fa8ef4946a361b0339580868efb3e2163873394bcab2386c`  
		Last Modified: Fri, 19 Jun 2026 02:44:48 GMT  
		Size: 3.8 MB (3818820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1361fd3fafae2440e8a9c044ffe7a0aa626d8fb3ceb36d3d2be7b09b48444746`  
		Last Modified: Fri, 19 Jun 2026 02:44:47 GMT  
		Size: 17.8 KB (17761 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:65887237e21c21c395d5fcc6b123313b96b40882cdbd30e982a24dd120a996d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 MB (208734231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5463d8cd4aeace8a1c55ee1076f84cac1eb4f4bfe672c8e4adf425c84d447e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 04:11:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:11:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:11:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:11:54 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 04:11:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 04:11:54 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:12:58 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 04:12:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 04:12:58 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 04:13:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 04:13:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:13:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:13:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4acbf08d84aa74ba1f41a222ae6a061c228f6ba4fc5d1d428650c7427ca1fbd3`  
		Last Modified: Wed, 24 Jun 2026 00:28:42 GMT  
		Size: 49.4 MB (49386060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f578fd1d3edc228a6dfcbdc9d47149a7226cc5f1ca354d1a0d7b0fcbb5c79263`  
		Last Modified: Wed, 24 Jun 2026 04:13:26 GMT  
		Size: 135.9 MB (135910382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa47f4242ef2fab0dcd3b11f6031c9fa9da44e75ecfcd374ee4d0ec2c883e2a`  
		Last Modified: Wed, 24 Jun 2026 04:13:24 GMT  
		Size: 18.9 MB (18922154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db4c9dc43f799e8c1330bf7d6dd61fcdb2aaeb99f8c241ebca3d06b80cb3028`  
		Last Modified: Wed, 24 Jun 2026 04:13:23 GMT  
		Size: 4.5 MB (4515205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04599a4d835f234957fed28ebd6268b91f2e8c2d46e39a996f82f937a2f99db1`  
		Last Modified: Wed, 24 Jun 2026 04:13:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3e13af0bb3e909c86c4a2be63b06876cfdb43cecd57e6526b7a9f74788762f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed7d6e008717a2c4ee5c7a02ac16c356c7a281e540e382e8f3140e02588f332`

```dockerfile
```

-	Layers:
	-	`sha256:06e9299a71d1f89557e558053b0bc38795b215629750905ae207214ba7215aff`  
		Last Modified: Wed, 24 Jun 2026 04:13:23 GMT  
		Size: 3.8 MB (3814247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a4c09864be0d540fa0733ef9f51b2ea91e84a59a312788ed484b681997f7b16`  
		Last Modified: Wed, 24 Jun 2026 04:13:23 GMT  
		Size: 17.7 KB (17718 bytes)  
		MIME: application/vnd.in-toto+json
