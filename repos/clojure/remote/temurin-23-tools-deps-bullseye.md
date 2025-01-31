## `clojure:temurin-23-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:b24efdf3d984f6d5d00e0df08b1c438975abae43c917dad5150ffb754b2e21eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2dc098b73a2d1a6a6f1424bb72e8bfd07917c7a93e5b51a7bfa3f933709ac379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288225738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd1716500af784732bdd99cf00d63e271cbd06d7b42b532481f4eee8451bfb1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e318e3d642b90f9a492c60197763b7504708d74368893791b183e44e1d3389b`  
		Last Modified: Wed, 29 Jan 2025 20:27:44 GMT  
		Size: 165.3 MB (165295053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9927c7fd0a9b73dec1978b16d5f958233485cc36db15e5a808ccc750f68a79cc`  
		Last Modified: Wed, 29 Jan 2025 20:27:43 GMT  
		Size: 69.2 MB (69190481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8f9bc322021afdafab81ee96ce5fcaab06df56d85a1268035ba94e1625dc17`  
		Last Modified: Wed, 29 Jan 2025 20:27:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc711fe89f9b24b9e570810673fbfb5df42df6f632e7b1eb440efdd99526f31`  
		Last Modified: Wed, 29 Jan 2025 20:27:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d4ade7a66ebe6e86ce01cd79832c4e6c3793202388dd8cc518a425fe03c26160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9ce5a087d063246d268120ebc48cd15d5baa737a57eae94a2a138a940d4d9f`

```dockerfile
```

-	Layers:
	-	`sha256:867906f272f1c95acbe1d190e3ce29ddf1310ee9b6e9014368b01c79b1557445`  
		Last Modified: Wed, 29 Jan 2025 20:27:42 GMT  
		Size: 7.2 MB (7209562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72f8c79f8c2590a6208b654d49e11d31cf90ae2d5a5ca007d8c0fbe65a87babe`  
		Last Modified: Wed, 29 Jan 2025 20:27:42 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3e6b5ac66115783e67ed041431b9c980968ecd88ec12d89455b7078ca11d4eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284840339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f6c09c828c66ce67dd3f177c19f97bdb108dde8d0d95bf1e844850f93dd65b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ca543c77f30c2f45d64e12050b7d093e1c0ddaf3c74b92fda20bba862b0f7d`  
		Last Modified: Thu, 23 Jan 2025 03:55:52 GMT  
		Size: 163.3 MB (163281769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30181f9b9171237018058a8a8ae6d33794791b431bce8990cbbee8ba001a32a7`  
		Last Modified: Wed, 29 Jan 2025 20:59:20 GMT  
		Size: 69.3 MB (69311468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7ffc29c2a72a870830bd2aa3796a3460d59569456337a1c517659dd94f40eb`  
		Last Modified: Wed, 29 Jan 2025 20:59:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf93e6ae0d3745994323c0e49ef0bf96c5571215f51d76c9583aa1a0f6d18c0`  
		Last Modified: Wed, 29 Jan 2025 20:59:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3e8d3f008e543d0d86739b92b29b8d5f1b644e36556a5be85dd5eb4c8b964a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7229978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3516e794c1060985d09ad494ebaf9e0012d83320e5bfc9f7a3538f6f412ea113`

```dockerfile
```

-	Layers:
	-	`sha256:b54ee27a1b52d865f2d920f57522d9e4661866b42a5f9471f8ff0d6e9775bb2d`  
		Last Modified: Wed, 29 Jan 2025 20:59:18 GMT  
		Size: 7.2 MB (7214040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a86214c01192b32f300b0c66c3a40a1ca11f8e292eea74cb8eaf7c416fc991d`  
		Last Modified: Wed, 29 Jan 2025 20:59:17 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
