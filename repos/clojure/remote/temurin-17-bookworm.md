## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:e5bdf34fd67b84d222e6954cb614acb643e89ce6a1f7adb0b97a79a7b266161a
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
$ docker pull clojure@sha256:179116dc994ce3f4e53d75881b28be0f672379c573e41e2c537da0396244da1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.7 MB (273737235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca1862f4eb94ee6eafaf05a4a8661afbe9946e3a43e54f4c85a75773037d560`
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
	-	`sha256:d6be9297fdd1b50f05a57283e6dbe8e4455d2728758fd4fc2d4c702510853b21`  
		Last Modified: Thu, 24 Oct 2024 09:14:04 GMT  
		Size: 143.4 MB (143360984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efb70d7a7e67334cb84b12216d4f00e5696b9aac03323bdf7c880a388713d6a`  
		Last Modified: Thu, 24 Oct 2024 09:19:44 GMT  
		Size: 80.8 MB (80790236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e8f96afa40605a1611566f93c08a4d399d4183aa106ee907336099c871d437`  
		Last Modified: Thu, 24 Oct 2024 09:19:42 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cacdd3a836a48026b6be8904c6908681f7a1f2f6f051db4aa23380a20daa0f0`  
		Last Modified: Thu, 24 Oct 2024 09:19:42 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:37e1c0f3555c2c7c257db8882bd4250043491f6ee90be14c2bdf2b8447306095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7203913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8ac1c1995e2321d4bb64e2bafc967b9d5f34f1cb195d900735d3cbc72c2d78`

```dockerfile
```

-	Layers:
	-	`sha256:28df1518aac66858fc0f1908b9c92d3f8f644f7455098c8788c91ff2c1fe84d6`  
		Last Modified: Thu, 24 Oct 2024 09:19:42 GMT  
		Size: 7.2 MB (7188155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:988bb27f34148dcad858a86eb3ff097d3ac04ad9ca2937132bc3a8605afea474`  
		Last Modified: Thu, 24 Oct 2024 09:19:42 GMT  
		Size: 15.8 KB (15758 bytes)  
		MIME: application/vnd.in-toto+json
