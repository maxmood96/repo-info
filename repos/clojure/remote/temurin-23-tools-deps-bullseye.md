## `clojure:temurin-23-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:afacaa31704cd26abe42736d7b89b4515bdf8d5c98e05c55f0bf78c121df1b34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:fdcbb179fa2da59e1f1ec660bf64ca66ee3e670b6ab4c3aeae7cc1dc4da2f38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289683006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968755819bc3837f6086ee5cbb79835eb1f6e7bde048afe0b6bbb7fcd6d5b7c7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
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
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bb4210724a31037da3bd0c038a3cbf334515c0d34be8f9b9fa37447de3afe9`  
		Last Modified: Thu, 17 Oct 2024 01:13:43 GMT  
		Size: 165.3 MB (165267658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff98e7d9abd06db1d3b0de32ee7d24513cb19b96b0c0ce72b2ccef25bdec5006`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 69.3 MB (69333702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5090cabe37594cf06f3723cd425beb7f8f07a1116c9e67167b23638d1547b00`  
		Last Modified: Thu, 17 Oct 2024 01:13:43 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fbf2d313d31f7a8ac90c3d2072a530ee4001ec393796e6ca1b26cde4e29194`  
		Last Modified: Thu, 17 Oct 2024 01:13:43 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:fc093e89bc50cad9f32c1de6bab66fd2d211ab393ed8216a73fc2676b044cc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7210564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae4d1b3b90529269b6a6ceed785acc4f29a92c85227ad7a32e17672f6d02844`

```dockerfile
```

-	Layers:
	-	`sha256:ed88b1058a428e99140e11f7d7c3a2af8ac45fb8956e4ca595de68cb5eca2d4f`  
		Last Modified: Thu, 17 Oct 2024 01:13:43 GMT  
		Size: 7.2 MB (7195086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:534469e47def185f95d9a37d27d646beba9dde75ad2c1c46d0d03403649805e3`  
		Last Modified: Thu, 17 Oct 2024 01:13:43 GMT  
		Size: 15.5 KB (15478 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:44fa2a5560594350dea6aa49b892c67e4f984801c0db6f5165d9fe211c332db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286454678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c015bef07e7c0f6800471883f00ae0f0edaa189c0c1d908f9fc7227d6d46e409`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
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
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc66007fccb5edf87947252ad7999f9ecb41dd40a0be6c9a5a53e8254e22ab5`  
		Last Modified: Sat, 12 Oct 2024 01:34:11 GMT  
		Size: 163.3 MB (163252784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a64410d4c70f17c0fab562c0f3d469d9c446a88f58d889a79236c57a59fbc06`  
		Last Modified: Sat, 12 Oct 2024 01:38:37 GMT  
		Size: 69.5 MB (69466990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9723970ea76d7fc5e590154b5f5a815fcb39237b563a151e23e9ceadf0c8e6db`  
		Last Modified: Sat, 12 Oct 2024 01:38:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f203dbded6fd1ebbc7e5f9006e7d2ac468aebda7640c5af1a118a2936cdeb606`  
		Last Modified: Sat, 12 Oct 2024 01:38:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8714cdcbd5dbb5f8167ee73b8d6d6c429b9f769d197914b755b5dc20c5b2b09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7215061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1bc8b191d54d7d48c231402c00d6c2735699a41d83aef5ec3644d509eee528`

```dockerfile
```

-	Layers:
	-	`sha256:66ba01554a4205ad48145bddbfe9815b55dc8b59094398e2f43642510030a534`  
		Last Modified: Wed, 16 Oct 2024 02:42:47 GMT  
		Size: 7.2 MB (7199477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d994215eb3fd3c70b46cca065844af5187b1b227bfe35f8bf65968bbdab3949e`  
		Last Modified: Wed, 16 Oct 2024 02:42:47 GMT  
		Size: 15.6 KB (15584 bytes)  
		MIME: application/vnd.in-toto+json
