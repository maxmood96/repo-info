## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:d2393334a708f263a24b3cf7a4d848928ddc929bd5cae72254508994b0b76cf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1035d17567e74f87028e45393d809bf420dfb5730a0205a35365cb5a27846eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (275018936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a4ebc8884be27ab608667ca84d10b3f8b9b005eb9a23a878240cb3602acff6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e1272909ee26099c8fdcdfd3f6114ac100926b37a4928b79cb72bbef898181`  
		Last Modified: Thu, 24 Oct 2024 02:00:18 GMT  
		Size: 144.5 MB (144534819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679b1152c167162ec1d82048469ad4bec068930fb7f1a44134c19a9210cd9f61`  
		Last Modified: Thu, 24 Oct 2024 02:00:17 GMT  
		Size: 80.9 MB (80928051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1534373ed7c64bddb6ee53d5f9e35f036a1b77cf0b35cd99ad0badaf0eb8b978`  
		Last Modified: Thu, 24 Oct 2024 02:00:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864da9def97ed1c6cae9fe2d7cd2c26de4a7c39c6e6f4177a35999cb93fa737f`  
		Last Modified: Thu, 24 Oct 2024 02:00:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:87bd504063a88e203bd4c2b41f3d57fa04cb383c845ee7a8c4870b6d64ce143e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7198033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b465e687ac788a54b1446f5e5f0dbcbd6045b0539a93ef7f7761a6bf4f51fb29`

```dockerfile
```

-	Layers:
	-	`sha256:58a854794df2a8d95353c419a1cba020b617ea27bb7f6dad86b8d1abd8881787`  
		Last Modified: Thu, 24 Oct 2024 02:00:16 GMT  
		Size: 7.2 MB (7182387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3bfde37fe3521e8ebe122865a8724150d7b8d9ed715ba656f9b0c03a145e615`  
		Last Modified: Thu, 24 Oct 2024 02:00:16 GMT  
		Size: 15.6 KB (15646 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dfe23b482395c88b2b2eb5ca76edd11b2ddd122ef8170f946862a7f2aa3fedf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274335776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bc7c4315bd97bfab60de7aa210fb5a6b69e2ff05a99b1d548666f6158c27d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237653f214e6df6277c7b47d5a245880430d05230855ce95f46023867b57c6a8`  
		Last Modified: Sat, 19 Oct 2024 12:00:15 GMT  
		Size: 144.0 MB (143959441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055062ba45f591db1d3e3c43ac3f6e853fa2bbcd837e7bccdf575a2c8de5edd6`  
		Last Modified: Sat, 19 Oct 2024 12:06:07 GMT  
		Size: 80.8 MB (80790316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b82ae0d3a52f4f4588e6ec2cd6867dce6f8015031368a7deefc3e8bce4d450`  
		Last Modified: Sat, 19 Oct 2024 12:06:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76a73437d6d89e691c58d742519591415ab884ed32124247d617325a3e827d6`  
		Last Modified: Sat, 19 Oct 2024 12:06:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b64633c06bad5aec7d3c86e7e80262233a39baa78dbb039e76349fa70625b917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7203277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a471219ba18623fc37ba4b007518cb0ea94e181ad46b29d091ee0b12eb169bff`

```dockerfile
```

-	Layers:
	-	`sha256:d62938ec6ef1ee16a047d51e89df78d3a49c03dd21f257559ecf7d574f73fc05`  
		Last Modified: Sat, 19 Oct 2024 12:06:06 GMT  
		Size: 7.2 MB (7187519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6adc214802212035ccb7662a80f8eb62661c5fa9d5c1c4373801c9f44df26b7a`  
		Last Modified: Sat, 19 Oct 2024 12:06:05 GMT  
		Size: 15.8 KB (15758 bytes)  
		MIME: application/vnd.in-toto+json
