## `clojure:temurin-17-lein-2.13.0-bullseye`

```console
$ docker pull clojure@sha256:a38475b0715aa8d9bbae4335c585300db800bbec15171fdfb82bef05ffd2c688
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.13.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:368f98390e8d1acc8fa6b5629f2bbe7b7c6e094331414bf723f8d2fd1bc8a063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221122762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be149a5e4263e6631f40ae892a990f1400b700ec9b96b2a8eaa90287dae004f`
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
# Wed, 24 Jun 2026 02:18:44 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:18:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:18:44 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:18:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:18:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:18:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:18:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c67cddb4b9fcdeefaf829aa012f0ccaefcfa862a558064326104b95b8849cd81`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 53.8 MB (53773009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1879f1d4cd54f020da48200eb2f76e11a3ecbd0847d257569b2e1f536b5b09af`  
		Last Modified: Wed, 24 Jun 2026 02:19:08 GMT  
		Size: 145.9 MB (145905430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd19f6b363670cdc28e89cfeda5849a3b60ca4de5da33f325cb32f36e27bf92b`  
		Last Modified: Wed, 24 Jun 2026 02:19:04 GMT  
		Size: 16.9 MB (16928671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d9f6c6e45d29ec2ad3b6b2532e673157edb89090265ba7e97d6c4f8f1afa92`  
		Last Modified: Wed, 24 Jun 2026 02:19:04 GMT  
		Size: 4.5 MB (4515223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea99db76324af43d39e29687f0180be5dec88331a52fb07185d6aa628095fff5`  
		Last Modified: Wed, 24 Jun 2026 02:19:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a2b45651f706591f75bb236c0170ade15fbe68b4cb02730d408439512ae4b582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4518765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b06a9b8ca70a5231c366ee8ffcb34a72895ad0df2e4762628a2e5e89ab1376`

```dockerfile
```

-	Layers:
	-	`sha256:cf061bb60153681b8de3755d6b189ad7ae55207a008d2d4a03c25a4b74f1999e`  
		Last Modified: Wed, 24 Jun 2026 02:19:04 GMT  
		Size: 4.5 MB (4501027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50ad1a3c579cef387437638abef16de4ddf137d25d664011126a85daf2e4d0af`  
		Last Modified: Wed, 24 Jun 2026 02:19:04 GMT  
		Size: 17.7 KB (17738 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:807f918054bf9aed786542e4054aa582d73e38684e4744bd7945b718dc6dab1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218414536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f2b4391dfb0ed9ec31ebeff56b7daef6b75afe76537c66ea638a10e0a93078`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:24:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:24:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:24:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:24:04 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:24:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:24:04 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:25:14 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:25:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:25:14 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:25:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:25:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:25:15 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:25:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:35157acdff35db21da73141f382d0dca0f6bc6d183c3a816d283fe39f471e539`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 52.3 MB (52257219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cfc830c71fff73f1a366acf3969641f26b93a077e099a9e67fa3ce58f88159`  
		Last Modified: Wed, 24 Jun 2026 02:25:37 GMT  
		Size: 144.7 MB (144724351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b77dfbe3e01a3baa6c2125caea25fe0ede12ab13e32219fdcb22f41728d5e3`  
		Last Modified: Wed, 24 Jun 2026 02:25:34 GMT  
		Size: 16.9 MB (16917362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190cd0dc38943a93a6de31e8a1798e17a70643cebc8d47111b0ca4410f0192e2`  
		Last Modified: Wed, 24 Jun 2026 02:25:33 GMT  
		Size: 4.5 MB (4515174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1839cb7178741825d157b4828f61c1bb832887a1e21aff77eda6018acec4c5f3`  
		Last Modified: Wed, 24 Jun 2026 02:25:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9557d8d3c46edb4a2d0f18ec591494db3c88bcce66c12f797331f96a38392c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc111138a792dacdb938036fa2507d86111e48dad380319c648989f3c70efa92`

```dockerfile
```

-	Layers:
	-	`sha256:7f2babc11cfad87519bd3c0089427f0616e3930972c1d8f4412f76f9d2880ee8`  
		Last Modified: Wed, 24 Jun 2026 02:25:33 GMT  
		Size: 4.5 MB (4500001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d631e9d5b9cebf9c6cd881c26822dd47a1661abbe120ac2a6510bbc24c40ef92`  
		Last Modified: Wed, 24 Jun 2026 02:25:33 GMT  
		Size: 17.9 KB (17859 bytes)  
		MIME: application/vnd.in-toto+json
