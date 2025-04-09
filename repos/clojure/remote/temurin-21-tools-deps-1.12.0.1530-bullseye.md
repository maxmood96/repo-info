## `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:dd6b519c6b1eccb1b31e0956cff1a30deb168f182b6f31fc47237d8ab1418140
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7c400398fbf3a603e7fcd0e9705ede0316ad61a3f130e24cbeb1ce92d6bbdb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280730428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57bd517184d7940b2ec9b5568a56c3807d861020b413f2a41ac9d612e5a1d0ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d2f360033006d4cb51169c1bf4275f208ff993f5983e6a1aade0947ff577fd`  
		Last Modified: Wed, 09 Apr 2025 02:19:18 GMT  
		Size: 157.6 MB (157585849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90996adfd7264a3585c3391d4e37d449ba3725516ce8298ebb751fe87821cc5`  
		Last Modified: Wed, 09 Apr 2025 02:19:17 GMT  
		Size: 69.4 MB (69395009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e43b69a77fceeab2b323596239daf072b1d375dcf8e966b79c2254c092b0a6`  
		Last Modified: Wed, 09 Apr 2025 02:19:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3965b2d9fe91eaecec3accc318aa3716191a872478d205d6e2742179d8e5ad`  
		Last Modified: Wed, 09 Apr 2025 02:19:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4386791363c96137c238de15253e1e9bbbf84c49ae476d34fc5e68eb36ba9cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7226776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645760d74b6affdc0158831fa7658622099a343444ad18dd211d2ba22ce21eb7`

```dockerfile
```

-	Layers:
	-	`sha256:4c113e418828e959b2688d1216ee7fcb613fefff9e950ed2dc5197863fb1744b`  
		Last Modified: Wed, 09 Apr 2025 02:19:15 GMT  
		Size: 7.2 MB (7210279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc57206aa55fbee1689af1d11e6f8f47886d9a7716fdd3d30237d1fcf101796d`  
		Last Modified: Wed, 09 Apr 2025 02:19:15 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6f40d650eccd13d3eb12562c12fef80d28c368e827ed38e5df0c87b95a857dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277644340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75663ab9ae40a6eb65fabcbfdcab9bace494037182aa31e3f44767657bf59671`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f215dedabd3f6571b951ada57aeede59411f781d2de563093560f3e7f1cfa37`  
		Last Modified: Wed, 09 Apr 2025 17:40:05 GMT  
		Size: 155.9 MB (155859314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5155a179ab5a9579a4f06ed2157c926741d4334c7c5c28c02bc70931381a7c16`  
		Last Modified: Wed, 09 Apr 2025 17:44:31 GMT  
		Size: 69.5 MB (69529764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e9609faac1da72a1b639845caf5a634a69332df6cce8a309729c2f58834627`  
		Last Modified: Wed, 09 Apr 2025 17:44:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bbe51577ecc890c7200356b52f405c1d9cc35c399bafab510bc01357fe1b44`  
		Last Modified: Wed, 09 Apr 2025 17:44:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3b932f5c014f7ddb3148092585a3a3816665363df848ce9132b942a065146815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7232041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cea6237d9672971c54c09443b81e9c48b1441e4b627071371ddb117c3b0230`

```dockerfile
```

-	Layers:
	-	`sha256:23d63adb3919a048b0b4861697c6e94e4e7100aebed5e08e45e53db3ee9ef2a4`  
		Last Modified: Wed, 09 Apr 2025 17:44:29 GMT  
		Size: 7.2 MB (7215402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19066828eda4291354eacd12a0eb231d55a1fd1e3a13a6d0f172a65b5355c74e`  
		Last Modified: Wed, 09 Apr 2025 17:44:29 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
