## `clojure:temurin-17-lein-2.13.0-bookworm-slim`

```console
$ docker pull clojure@sha256:c46725e6570451dce14b4a8cc48b1b8420165849deb072985b43e088c0c50589
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

### `clojure:temurin-17-lein-2.13.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fb074d09766734b8a92a99bfec39f08fb8233f20a349fd2f3b8e0889aebe7aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196718012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a2b03a34c21cb0aa293566f997fefcd7223c180e9887bd731ff958d06664371`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:17:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:17:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:17:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:17:07 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:17:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:17:07 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:18:08 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:18:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:18:08 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:18:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:18:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:18:10 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:18:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c170ab4bdbc1b802a20a004f93ddf957fac4bddb6313fcacaff6df67baf59d95`  
		Last Modified: Wed, 24 Jun 2026 02:18:30 GMT  
		Size: 145.9 MB (145905427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fab852c521fa0ededeafe3695404f518ecd2ba02a6377c42777b84ddda26e9`  
		Last Modified: Wed, 24 Jun 2026 02:18:27 GMT  
		Size: 18.1 MB (18059298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6666dee327d71e5b0a6270d462d1773d3cb9cfd58f7c82e99b2b14ae720f873c`  
		Last Modified: Wed, 24 Jun 2026 02:18:27 GMT  
		Size: 4.5 MB (4515219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda1abb9114597b35ec05eca9ef78a2f229d6fd74cc51f46576ee6e5e6fe9a13`  
		Last Modified: Wed, 24 Jun 2026 02:18:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:34a927e3dd9ba8872fcdc21bf528b2cfe380a9c2449ec719d29d7d278144b677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2906634fc467c7b16f3f51fd80cf6ea41e325f31c8946c52ac9d36bfab592fea`

```dockerfile
```

-	Layers:
	-	`sha256:1fdfb70eb563e5fed724098b4165dc89813bfc7fbb670f2df5f9a82d2f166a89`  
		Last Modified: Wed, 24 Jun 2026 02:18:27 GMT  
		Size: 2.7 MB (2732337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2c7fff79f572159450c37bf25231bf060f0c5d3a6c05f7b658216114522e15d`  
		Last Modified: Wed, 24 Jun 2026 02:18:26 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2f914a2cbd0e4a4c49eaf2168ec41a84ef765d218e601fd00fb202adcaa68187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195256678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f9934a0ee11ca4525ac0adb2bacf7580446323d79c9e3da8c04cb849549b3e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:24:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:24:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:24:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:24:00 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:24:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:24:00 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:25:05 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:25:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:25:05 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:25:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:25:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:25:06 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:25:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd373a3b1852ebe34292d79564064f5ce6f464544f20c9e5bc1a00f14ec408ce`  
		Last Modified: Wed, 24 Jun 2026 02:25:26 GMT  
		Size: 144.7 MB (144724352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170a2fb75ec8e1b9ff92fdaf65690477aa0d3bb77eb258d9565c336407f02499`  
		Last Modified: Wed, 24 Jun 2026 02:25:23 GMT  
		Size: 17.9 MB (17894310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d58dc4ca26eebf6e30651373c7617008baa11dcf64f186522cf9e3125add17`  
		Last Modified: Wed, 24 Jun 2026 02:25:23 GMT  
		Size: 4.5 MB (4515167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b81ed04f6bf421c959d6045cdaffe8fc066903a902f98d04341603ae44f9272`  
		Last Modified: Wed, 24 Jun 2026 02:25:23 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7e8f33a6e3794e30e414130b9f34820136bd5e9ecf1a4056b68c7c33b44668e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2749846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43e52835c3fe18e3b20bf94fc179184ef4443be329a2890715756ddebccf5f8`

```dockerfile
```

-	Layers:
	-	`sha256:3ab3bf1d55befc974daf0b7ab647ee2745b0509ec8daed9600fe6d35eedd62e5`  
		Last Modified: Wed, 24 Jun 2026 02:25:23 GMT  
		Size: 2.7 MB (2731952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12acfdf18742b652b0c71f1c230fdab3b15738693d7636fe789025de53bad620`  
		Last Modified: Wed, 24 Jun 2026 02:25:23 GMT  
		Size: 17.9 KB (17894 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:93a727013f1fd2704f8b6b6a6def79f27cbc8e499d486544a370bdd241748eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.6 MB (200628124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5c3ef3d3d1710b2472a47813f5aedb8430980ceffa30fc1b299c4f44084de0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:36:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:36:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:36:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:36:44 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:36:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:36:44 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:39:43 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:39:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:39:43 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:39:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:39:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:39:48 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:39:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011a8b1fe08cbca6cfbf84dcf1035227586f8c0a013a520d08ca8f1bb6f1baa7`  
		Last Modified: Fri, 19 Jun 2026 02:40:33 GMT  
		Size: 145.8 MB (145766212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b9429faf06a6a931fcef324548560e9d32258e57b641ee3dbb734991114222`  
		Last Modified: Fri, 19 Jun 2026 02:40:30 GMT  
		Size: 18.3 MB (18264317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d3ff347e392f913353f35894537b62ca405c4cee7b9a8b913d564c9ff68e65`  
		Last Modified: Fri, 19 Jun 2026 02:40:29 GMT  
		Size: 4.5 MB (4515224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137905a61e4f8bcfce485cff77745059e0d5b7ca2614d760c9d7b63109355888`  
		Last Modified: Fri, 19 Jun 2026 02:40:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9c3aa451abe9502b11d992728d892494dc6e384e8753dc519393f5d94b265d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5fa7b593547aa559e15e1de8a5b11eec97250e72a921e0c27448f325e91cc99`

```dockerfile
```

-	Layers:
	-	`sha256:fec91cab972426c6d095c5e54ff99efce334cdfbd91a1c9a4966d447164b00e9`  
		Last Modified: Fri, 19 Jun 2026 02:40:29 GMT  
		Size: 2.7 MB (2734170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e1ee7abccd29301ed079d7c2c1387605ac5cbba877f9d0be673f6779c199541`  
		Last Modified: Fri, 19 Jun 2026 02:40:29 GMT  
		Size: 17.8 KB (17817 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c292c355fac241b3757881fe77ae2ebfc6782d471def6e2ba3b3c3629ce73246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185044183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02ffda4154db64e0869acd7948684d0ae557ae5d1e5a596e2f67c2602c9d6a2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:16:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:16:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:16:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:16:40 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:16:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:16:40 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:17:37 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:17:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:17:37 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:17:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:17:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:17:39 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:17:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12de02280ae8885a4001fbd484dbfc1d6554fb904cc661889a6e6ecda0108b20`  
		Last Modified: Fri, 19 Jun 2026 02:18:03 GMT  
		Size: 135.9 MB (135910426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca2bcd94048a86c6e0e0c7ece80a89ff5d7f968530f75ef3a2e3e78f4297e5a`  
		Last Modified: Fri, 19 Jun 2026 02:18:01 GMT  
		Size: 17.7 MB (17724608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26c701fadb65fc96941cc6b306bfb5ddda9340e3a7e5de08c2a208bb8e8aef9`  
		Last Modified: Fri, 19 Jun 2026 02:18:00 GMT  
		Size: 4.5 MB (4515211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fb507f01a3cf7ade72ac7b4af46d7ec2a3830e45b177f8326448bccafc00b0`  
		Last Modified: Fri, 19 Jun 2026 02:18:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2de1aad371661a6f870b0a0a17c197d664046a925330f9b2d2c8cb3b67ef0978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2741924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1949e1ca33eb9564eff5671d555d79e2b15fcd217f9db8a92a9dc403c7ad82ab`

```dockerfile
```

-	Layers:
	-	`sha256:b672d88b15d83ee63f4cd77ed81658ec243517122778bf6b3f890c18ba90b32b`  
		Last Modified: Fri, 19 Jun 2026 02:18:00 GMT  
		Size: 2.7 MB (2724151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1637a6d31fb8f391e8021968174cfdf4889bc381f8d644780cc324335a785eed`  
		Last Modified: Fri, 19 Jun 2026 02:18:00 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json
