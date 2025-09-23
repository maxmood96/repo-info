## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:6e0ce651e1141b0d5bdce8b4ab3cab6eebfe8cc92d3048aa6d1ce50234861078
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:50fbea95caca48405631f686787f3addeb097a87e42e0142e4f5f0a1706e516a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247215476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48899d2a0cd6638fe2513d2b6b72e86d3427308ba5e200204b3ea218bd7bfc6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ca34e513b1941dda52263423ad815985f3080330c9c0ac90a8ac6c53a9d2b3`  
		Last Modified: Tue, 23 Sep 2025 01:47:54 GMT  
		Size: 157.8 MB (157804741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfa4cdff2acc6f219efce80910ded6743bfd574d7e6d2739291f1be97ae3f9f`  
		Last Modified: Mon, 22 Sep 2025 23:46:28 GMT  
		Size: 59.2 MB (59153624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00901312528f32e0171d01749e426ebf341399d1c548e981eedfb293adab349f`  
		Last Modified: Mon, 22 Sep 2025 23:46:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdc9b7c56987e5e9928fdf7266a3ea9460e8155c9240dd87264111141a00db5`  
		Last Modified: Mon, 22 Sep 2025 23:46:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8b1fdf67d674bb14591288cd773b3e904fed374798c48313a0644ebe3271e940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5328440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048fec74e0345962612abc3e6fd44ba0564e005efa8e739be6e30c7e0aebf6d3`

```dockerfile
```

-	Layers:
	-	`sha256:cb8b208202f322860d5868049fd8b8e199f2907d10c853dd921955decc00feb1`  
		Last Modified: Tue, 23 Sep 2025 00:41:24 GMT  
		Size: 5.3 MB (5311865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18e4c9d06d02089e3a709069bd2af1fd6aefad9b18dc7d2ae4cf2fa6a99564c6`  
		Last Modified: Tue, 23 Sep 2025 00:41:25 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d21d55ae27d4724936b45b3a79f0f6b49d6a51d1529a04e5d05ffe694e166838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244119941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf99966d6d29459e8248d77c9a3304512b37c387c7242bb798252769a0a7103`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df05e6303dcf72e66439ed7e7ce33fe693063f77991319a9da129c5a6c6047fc`  
		Last Modified: Tue, 23 Sep 2025 13:20:27 GMT  
		Size: 156.1 MB (156081196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2532f7b18b822ec2ddfead86db0b46d70fc90e17919a46dca70a9ec8475afa5`  
		Last Modified: Mon, 22 Sep 2025 22:20:15 GMT  
		Size: 59.3 MB (59287244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764825db062e90a7f711871d8c5c762ed9ec8e8b8398ff944d98fbc09ce0dcc9`  
		Last Modified: Mon, 22 Sep 2025 22:20:02 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a193667c2153f62d7b8a7771c774e97f5659a8e048ad37b6927deae952adb`  
		Last Modified: Mon, 22 Sep 2025 22:20:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e9ea3962478059e1ab61954a621d200ab1e014f87342f2c0df954454efe215bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5334336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c998fb441eb84a62888a7b49f3f3ee819047fc1059066294295baa11d2963423`

```dockerfile
```

-	Layers:
	-	`sha256:30cd707d566c5cb73421b39897c9c6f99dce6ab51a217273f5c6dd3bdccc390a`  
		Last Modified: Tue, 23 Sep 2025 00:41:29 GMT  
		Size: 5.3 MB (5317621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b847f6bd1c22a10d43ad61138e278b86e3274c0f81f543dcbdda2dcc69620193`  
		Last Modified: Tue, 23 Sep 2025 00:41:30 GMT  
		Size: 16.7 KB (16715 bytes)  
		MIME: application/vnd.in-toto+json
