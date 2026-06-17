## `clojure:temurin-11-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:5ca5858cd2d61f9b180aee1aa43229ef00d0f722569e9ec575eb2e97004a46c2
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

### `clojure:temurin-11-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a99a1bca5460d2b11a99b19542aad99b6419958311f1ac05f65e308d9f7ab194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196698285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f9d35a7151b6b86666928d817360bf05edd8384a1d2fb0304b285078b260cf`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:33:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:33:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:33:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:33:04 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:33:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:33:04 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:34:12 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:34:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:34:12 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:34:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:34:13 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158cc4fe0244d95723aefee1700292a1d7a3fcf74a1c4f9f77f2b07c9419f777`  
		Last Modified: Tue, 16 Jun 2026 23:34:31 GMT  
		Size: 145.9 MB (145886263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad592978333d5357a609205d0da803f5359d1c6a93bce20527cac5ed88b9b331`  
		Last Modified: Tue, 16 Jun 2026 23:34:29 GMT  
		Size: 18.1 MB (18059185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7d877c3c92bbc9f2164c759c8db8e6d4199909bc4e4e3f028a10dfd2052afa`  
		Last Modified: Tue, 16 Jun 2026 23:34:28 GMT  
		Size: 4.5 MB (4515181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:56f638e1f5dbfb88680587cee85694273a461bd9a85f575fbccef193e8980827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2767631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503f2f773d1c32fba07991ef3d6932593a546839d5098d5b23fef069ccb39816`

```dockerfile
```

-	Layers:
	-	`sha256:22f5f574321e4135aa8761786d05a3b986afcbc92b1fb2f854c8f6627e4da6f5`  
		Last Modified: Tue, 16 Jun 2026 23:34:28 GMT  
		Size: 2.8 MB (2751853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa88f09f8ebf271a887dc8337ee87f09c14f37c4c93755bccd43fa1d7412b40f`  
		Last Modified: Tue, 16 Jun 2026 23:34:28 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c884937df1e17c60c2f9635aefc765aa9485e40bcfc14427066da8650bf10ac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193113946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f544f85411b29de22f7479cc73036e9e881a454dfdca0a8c6b55053b7e01eebd`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:32:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:45 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:32:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:32:45 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:33:56 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:33:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:33:56 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:33:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:33:57 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf665a19feee8920f992dccb9c0e8af5919ee5105230b0b64bdfe6ad6c9667b1`  
		Last Modified: Tue, 16 Jun 2026 23:34:19 GMT  
		Size: 142.6 MB (142582245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2579923e65ccc6ccdfaa01de57960a87726a7149479344006b36e7d8a6fa8a43`  
		Last Modified: Tue, 16 Jun 2026 23:34:14 GMT  
		Size: 17.9 MB (17894190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de34c0b84b5fca3dca9771748738e53a81eac90e8a63966dcd424758e16c8f4`  
		Last Modified: Tue, 16 Jun 2026 23:34:14 GMT  
		Size: 4.5 MB (4515172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2c032ec16e2459addc338d8439a64a1a1eaa236405d7f6f48165b141dd15fa50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2767984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96179f6d5e934982d2649d8f2fa0d38b7211e9c1636be841f68fc44856edf283`

```dockerfile
```

-	Layers:
	-	`sha256:2319ed3a1ac2d3ee207ef8855bac8aeaca7bcd93898086c29e654203df0b9f1a`  
		Last Modified: Tue, 16 Jun 2026 23:34:14 GMT  
		Size: 2.8 MB (2752086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:746dc7fd4ee222bb821c394e04c945a6e9d51252be1e6cf4ef5e207f52391707`  
		Last Modified: Tue, 16 Jun 2026 23:34:13 GMT  
		Size: 15.9 KB (15898 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2e3ec9037b05ebf41885e32db11daf7d1edc0a5ce9e111037b159a674c401421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187970681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8de1be50575f1b915969064ae92b4ba043cf89855d7875dfb42133047aeefbd`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:34:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:34:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:34:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:34:46 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:34:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:34:46 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:37:12 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:37:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:37:12 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:37:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:37:16 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7161800d380a8452dc2e8dea3ec57d37eaa21b39c174f1db5e09fbe749e0575`  
		Last Modified: Tue, 16 Jun 2026 23:37:51 GMT  
		Size: 133.1 MB (133110132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8034eab7da763fe9f0e97ee9a1ad385c7e22e659aa924e63e43f7464a63399`  
		Last Modified: Tue, 16 Jun 2026 23:37:48 GMT  
		Size: 18.3 MB (18263364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bc63fc2df9a496833a9a6e7230438aab640b6fe779fe1956dcc4c549bf3ac6`  
		Last Modified: Tue, 16 Jun 2026 23:37:48 GMT  
		Size: 4.5 MB (4515212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9cc820bd6791e560e0f3604efac207d776143f9fe664b8f7161ae2f784e9a24b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2768893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64543316ffbf54fa3a1ea11297ab0d3bd6e2db688257355a72f3919f98dff24b`

```dockerfile
```

-	Layers:
	-	`sha256:c76fa975423534cc67151fe3d1b88b6868a98c06840582adc2ea8bd54228c293`  
		Last Modified: Tue, 16 Jun 2026 23:37:47 GMT  
		Size: 2.8 MB (2753071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4ab5e0c21e340b282444c256193cd82b1996231e9f8f26444d0e3b894003572`  
		Last Modified: Tue, 16 Jun 2026 23:37:47 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d67fd7356187057a25d1dd78cbbfef4a47d3f04b4a04cc70a958d2a94b57fb85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175784869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4228046ddf9bca5acc398ade348ca838ad8bac8b3ccbe79dbe9c94f7bea845`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:30:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:30:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:30:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:30:17 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:30:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:30:17 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:31:43 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:31:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:31:43 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:31:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:31:45 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faac26a16c3512d100392fa084d87083a807fb6ccdcbaeac23013af9a52a1d55`  
		Last Modified: Tue, 16 Jun 2026 23:32:10 GMT  
		Size: 126.7 MB (126651720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ff0fbf3a68498dadeb7047580c0be56a102066ee10aab6784d6e9612cbc6e7`  
		Last Modified: Tue, 16 Jun 2026 23:32:09 GMT  
		Size: 17.7 MB (17724393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2129df300fb9ad772c6ff26da956f73600aa7f4d52785f12e005aaf50c2f99`  
		Last Modified: Tue, 16 Jun 2026 23:32:08 GMT  
		Size: 4.5 MB (4515216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec7c32efb93392c3d3e974b9c8e704ffb4e158fbdde2c95dca246e145940d989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2759449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ef65e5faf3f474cfd2b7c34ef7a3847d6e79c789073972e143f0f3ad003c5e`

```dockerfile
```

-	Layers:
	-	`sha256:9a12e7cb9345be21c32f410fc462696b58fa85b46d2338fbedc3e57c81383e05`  
		Last Modified: Tue, 16 Jun 2026 23:32:08 GMT  
		Size: 2.7 MB (2743671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07eb00c299352f75561b1e362508eb287db1a943a8d366b81c2a3b06e5d7d102`  
		Last Modified: Tue, 16 Jun 2026 23:32:07 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
