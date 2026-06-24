## `clojure:temurin-17-lein-2.13.0-bookworm-slim`

```console
$ docker pull clojure@sha256:8ffcb7f91fdda1a388dfc74fe60b5e6797caf8459f49e8e4a872fb056805d295
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
$ docker pull clojure@sha256:436d971adf4e46ed014469c41b77f63b64e7e640269f55d7e5f5c1cc95af2da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.6 MB (200627087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5602caae5348275740718c4eea5564dab08d0bc2c43bf3c6d9615ba1afb699`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 08:01:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 08:01:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 08:01:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 08:01:52 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 08:01:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 08:01:53 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 08:04:30 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 08:04:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 08:04:30 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 08:04:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 08:04:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 08:04:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 08:04:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0887e2dadb1bfb5e02baab4d6c0be869a68f477e138f696ef3347af998103de1`  
		Last Modified: Wed, 24 Jun 2026 08:05:10 GMT  
		Size: 145.8 MB (145766157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc9bcc36610e1c22792e3438f85cba15ed2588a59b884d95beb50f60f1d9c01`  
		Last Modified: Wed, 24 Jun 2026 08:05:07 GMT  
		Size: 18.3 MB (18263306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eac87fc13c94e0e920f4dd5c557755d8162dc826a311249b56d49f12927f096`  
		Last Modified: Wed, 24 Jun 2026 08:05:06 GMT  
		Size: 4.5 MB (4515216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c126320c22e3d77d8f05af6dc1bddf12c263862e1b79d67e09d38ab64f0b7a`  
		Last Modified: Wed, 24 Jun 2026 08:05:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:17434c071ce0f0d6c5ad5166d1dda25a5dff3b4943e52c78bb6a343a5b0d7170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1d3b4430a90e9ac60ba629b7b885a2abe2560034c80f741b06866b8ceebd24`

```dockerfile
```

-	Layers:
	-	`sha256:e4a742592e0f7505968a0514dd6baf06a83d744adbe31294ee140289aa69818c`  
		Last Modified: Wed, 24 Jun 2026 08:05:06 GMT  
		Size: 2.7 MB (2734170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7afd4122735de198828eeff2f36b6b4d78c92b97a0993ddbccd4f43c841856e`  
		Last Modified: Wed, 24 Jun 2026 08:05:06 GMT  
		Size: 17.8 KB (17816 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:86576f30c477a36930f26e8aa35735caf1f11d1d9311a8a6974231dcaa4b5384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185044389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1ca239f94bab12146092ea759003c0c4505e1d85f6b12f0e6c668a940ba5ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:11:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:11:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:11:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:11:51 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 04:11:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 04:11:51 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:12:48 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 04:12:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 04:12:48 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 04:12:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 04:12:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:12:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:12:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb29b7db06616258b2d15f77b8d57ad53977da53f7b57a048a06f610786cd7e1`  
		Last Modified: Wed, 24 Jun 2026 04:13:16 GMT  
		Size: 135.9 MB (135910426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88940829989e69f33641341040a4fb0a2ffc345e1a992b46b0a0d86b4386f150`  
		Last Modified: Wed, 24 Jun 2026 04:13:13 GMT  
		Size: 17.7 MB (17724771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c69abea9d4edebdb0539a2cd6cc6a6cf9af763c016690c41ac2cce4ecc2205`  
		Last Modified: Wed, 24 Jun 2026 04:13:13 GMT  
		Size: 4.5 MB (4515179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a363df15fcb750bfca8dd30c1d17927c86ede5e110a2003c519e2dcff4a08fa`  
		Last Modified: Wed, 24 Jun 2026 04:13:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:509317a56032f5601be30a80ab54445b281ddeb1043d1e2337b8ff38ccddf25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2741924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a838ad3277d5f66df874c8f1a5b7a1b388fd359bffad75992bc2761c700bae83`

```dockerfile
```

-	Layers:
	-	`sha256:7b0bdef7fe6114d106b40c772cd8806b56c853c57415ec894bec61e485b6863b`  
		Last Modified: Wed, 24 Jun 2026 04:13:13 GMT  
		Size: 2.7 MB (2724151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:248101ce0772e4caee519c03b0cabb88a1c27045d0d4d881c65a31402a313620`  
		Last Modified: Wed, 24 Jun 2026 04:13:13 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json
