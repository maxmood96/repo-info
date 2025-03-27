## `clojure:temurin-24-bookworm`

```console
$ docker pull clojure@sha256:81aa238120775a0a8601943eba3bcba54909480e06273f9a07100a0af70762e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:bebaf73bf601795d2178626b36b7893e5c268ac44889cdb094ff8d4a83fff473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219411711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7db9b36bf55f5783b78940ad3201dae8af8e6f3e76db3c8a797a8e5f27ee07`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d08d875573b35585a8a861fc2f477488a6d70a5ff24dc610e86658050c479e`  
		Last Modified: Thu, 27 Mar 2025 17:53:48 GMT  
		Size: 89.9 MB (89949034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402ef65397866a41b2e025e2495986ddda2efdd59eaf1f41fb60ea1af508ac2b`  
		Last Modified: Thu, 27 Mar 2025 17:53:47 GMT  
		Size: 81.0 MB (80993797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8983b8d13a61a1e347913e3aaddf4cad2e2cdae1eb25fca5d078b7c7ffdb8e17`  
		Last Modified: Thu, 27 Mar 2025 17:53:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99322f26de42acca1ff50cd5266a1d3a6b57cd2e0c9eb1aeb97e7e3858d41959`  
		Last Modified: Thu, 27 Mar 2025 17:53:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:25d79d9f521f4184c673bb1f7167fe0d381c66afa9e395f2d8ea2497762047e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7138920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d4d56ec14e5663ab7010d2c266b7265beb3ead1e7439179c64f80048a7a8b7`

```dockerfile
```

-	Layers:
	-	`sha256:d69aabeb5695307d007e7a2911e7b68cf864c2caf3d388d14623d57ccb5d252b`  
		Last Modified: Thu, 27 Mar 2025 17:53:46 GMT  
		Size: 7.1 MB (7122424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6253fcc29f096f55318c41cba37813a00ab0b2820e9e504399e5df81cf8fdf2`  
		Last Modified: Thu, 27 Mar 2025 17:53:45 GMT  
		Size: 16.5 KB (16496 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3638c6f30dafcab15f2ecc2f44eb928191e06cc4c73cf1b318295fbf48b205bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218241251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516532cbe635038e7646092592631a56f7fb7843d0e36d0b726593549bd70e2f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32f1d4584a0aa49d6c0f2a0d382f28e60f4fc57ebb8548010197c1a8c2e0418`  
		Last Modified: Thu, 27 Mar 2025 17:53:16 GMT  
		Size: 89.1 MB (89092702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbcbb2220cc29c57d15cf53ff89f0c4fb19dce9011fb91600590e71c0e0ddf2`  
		Last Modified: Thu, 27 Mar 2025 17:58:37 GMT  
		Size: 80.8 MB (80842652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa23cce58189077096bb9b63d2973bbd76034a26eb8cb037c3a0bf229e1abad8`  
		Last Modified: Thu, 27 Mar 2025 17:58:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d93a2f2f94595101b26c7c9a0f9d8afec2b5000969982883fe4ec1eb597e1d`  
		Last Modified: Thu, 27 Mar 2025 17:58:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:37bdd291ac808128e41c31b8b8b4e8419d9e0d07371ae3c3e22575fb5848ce9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7144847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62fb81c059c87cc55e90bf896e5451cf40bba79815cfa833f5ac04940203840`

```dockerfile
```

-	Layers:
	-	`sha256:1c8153facf09c14d567ae289aa45aa8b9c8612d4f54d6f7755aa37e23d5a0f1a`  
		Last Modified: Thu, 27 Mar 2025 17:58:35 GMT  
		Size: 7.1 MB (7128208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efaefebea300d26c674f7394eee2698e687f1bd1e451ff62a1b0ba8aba7e7e8a`  
		Last Modified: Thu, 27 Mar 2025 17:58:35 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
