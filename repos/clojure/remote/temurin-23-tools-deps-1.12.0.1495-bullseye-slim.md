## `clojure:temurin-23-tools-deps-1.12.0.1495-bullseye-slim`

```console
$ docker pull clojure@sha256:6ed08fae13afffb23e9a2c7209ef39d9ea4ad333cd773d120479cd829a49b9b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1495-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2dc6642348b64a27accec66d6fff41a41907237aea2e1e147cfdfa76da851544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254329596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60533e4bc6085e2178ab3961afc365ffc3d246c8137958050d06920457588f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 20:33:08 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7740923aa31c7a87f3318b897684df83e03e82c6b0e153d68b98a1808330951`  
		Last Modified: Tue, 14 Jan 2025 02:45:33 GMT  
		Size: 165.3 MB (165295114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9fd444573c89316950ac245110232334422402100559865f6f3872685d8aad`  
		Last Modified: Tue, 14 Jan 2025 02:45:32 GMT  
		Size: 58.8 MB (58780775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb567dc3ba4cc3a767935318ea446c62498fb9ad1d21adbb0effd58fda6d689f`  
		Last Modified: Tue, 14 Jan 2025 02:45:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64830349e211dde761879244558d2442aa829886e5e4ff43ba83438f4f002131`  
		Last Modified: Tue, 14 Jan 2025 02:45:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1495-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4b616b94d4ecc1fe1ca99ebdceda2c9c792007818a302864e831044070e38c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00fd9ea415cb82e55a60d61f5dcc0e74e46002571374c5d4d07199e98b75ba4d`

```dockerfile
```

-	Layers:
	-	`sha256:7cdd0cc27536f83dd3ff25f7dd0fcb1879b77cd485b1c766d8a385589ae9a830`  
		Last Modified: Tue, 14 Jan 2025 02:45:30 GMT  
		Size: 5.1 MB (5122074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9a39753c62d95b52e692b85225e4cc5293789f8f91dd6fdf8cf1846b058e08`  
		Last Modified: Tue, 14 Jan 2025 02:45:30 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1495-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:731759b5b30bd45315f58170318a97a086f23186b5d3125ec72f13212720c008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250932982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b0beb1ce3a398b5efd469032694282ac7db4537d6920d40408fec499726fc2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 20:33:33 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e206b6fd86d16b339586be06a284d97aa652cd2602791ae8ae2346212f045696`  
		Last Modified: Tue, 14 Jan 2025 12:41:46 GMT  
		Size: 163.3 MB (163281785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dd3db52a5eb193e40d2804bf5efd0f0f5917dbfdf358ad43fb05f226948137`  
		Last Modified: Tue, 14 Jan 2025 12:44:46 GMT  
		Size: 58.9 MB (58905242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd095e36253f4200eae061e4bf02168d7f3d145bc5f0b92a63271103a938770e`  
		Last Modified: Tue, 14 Jan 2025 12:44:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca357b42c840cafc1cff963374c6ea2e8745a8eec8abb735d0a24761973e3c29`  
		Last Modified: Tue, 14 Jan 2025 12:44:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1495-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:02fd003945ec473877e1a3ef8f5e17aae8e115193e83b650cbaebc509b7fc18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5142381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9236aaafc5ffe79e98ffa5aed5f9f821477d8e53053936b560afa7e3ec3130`

```dockerfile
```

-	Layers:
	-	`sha256:097dc8d212c6796264cda1a08a22c6f94bd72feed2def0972d97a1e6326663d9`  
		Last Modified: Tue, 14 Jan 2025 12:44:45 GMT  
		Size: 5.1 MB (5127185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d410d0c61190ef4e0f203ad4baa6b4d025cb7b4dd904d256ba10014b9d0f6698`  
		Last Modified: Tue, 14 Jan 2025 12:44:45 GMT  
		Size: 15.2 KB (15196 bytes)  
		MIME: application/vnd.in-toto+json
