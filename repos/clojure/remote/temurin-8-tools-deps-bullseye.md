## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:38b6b334102f34f5ee7fd03cafe4294ebf2c0cf5a69f11ae76ed5a0079a984e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2ac9358f728541dcc9edaa685220e23019e51f990670c2232096bbf0bc581de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178047701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0b55d3e2587ebd8d24296940757b634ef0be3455a6d1311b6a3acb94590451`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81023bb0945c6ef23e6bebcdb19fd4205554aed80612ecb6a07c64d2f04cca0`  
		Last Modified: Mon, 22 Sep 2025 23:44:06 GMT  
		Size: 54.7 MB (54731284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ba37b8e2547e8d6a97463ae1402b211664fe02f6239fb479e05beb1500b256`  
		Last Modified: Mon, 22 Sep 2025 23:44:16 GMT  
		Size: 69.6 MB (69560374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b512359862a9ebb94b4ce0a30d0381858bd0a24f027da392697b9c723b7c79`  
		Last Modified: Mon, 22 Sep 2025 23:44:01 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d213c1174318d8590d0aa9e890728521225a6c7a1619913e54cb4efc88cc7a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51d241fccc9f384578c01fc7e00e663c5551516353177d5460d03a1841da914`

```dockerfile
```

-	Layers:
	-	`sha256:023a1cdbdb11c68750ee98cee8532f92fa3c29202fa2c05bdc2cc7c4c43cfa7d`  
		Last Modified: Tue, 23 Sep 2025 00:46:39 GMT  
		Size: 7.5 MB (7517277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:558520c5d7ba93683c31db6697ddb353967897ac292fea771e09f4a3819670b1`  
		Last Modified: Tue, 23 Sep 2025 00:46:40 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fd660ddfca77beaa8ac3a7d167df80bdef1010cda3af3885321d25b2631348f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175772301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f8b7a39f0b16474fa03dad07d3f589cbb5c964b82c076e0f484afd9891697b`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7349adf63dbe70c58e7182c66fd22616e449d71f15e9692623abe16bec9e689`  
		Last Modified: Mon, 22 Sep 2025 22:16:15 GMT  
		Size: 53.8 MB (53835607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e4c9dd122e21f9c38f670ad7e72bd368abddf826bf508b52f00cca5b5cf14d`  
		Last Modified: Mon, 22 Sep 2025 22:16:18 GMT  
		Size: 69.7 MB (69687678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c262ec4ad4ea9664cfd2d8a65049e870de671780cea98da688ee1fd060c679d6`  
		Last Modified: Mon, 22 Sep 2025 22:16:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:90f85320e1b92a37df27b3ce0052e8ac6c7790a609a09a15b5243b244edcbe38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274ea6fd6e902bf19b07b0f6e724ab715c0c8c860a0184904fa3bd440f84cd87`

```dockerfile
```

-	Layers:
	-	`sha256:2191948931542764e54b52446b963fe8f7c46c7eeb1c3f76e94573e5b48672c6`  
		Last Modified: Tue, 23 Sep 2025 00:46:46 GMT  
		Size: 7.5 MB (7523074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc08d086bf513411e603dc1d80f7d7e740c26b4191daa8336abd94216d0d5999`  
		Last Modified: Tue, 23 Sep 2025 00:46:47 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
