## `clojure:temurin-23-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:06334dea0e3d0c99e2c0fa418859ccbfa1779627e407c79accabfebce5968b96
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
$ docker pull clojure@sha256:f58d6eb0c91e8ecc82fdb03f8f502f49497d118db79e1069779985e27932308e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286455660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aba2d4b5226671c7095b2ab155dd6093085523e72a6b8641a05d6e77c63ce538`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
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
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e3acd407382ba38be4751d630a7d727bf3b7c34f0761ee6972cc6a0d9947b0`  
		Last Modified: Thu, 17 Oct 2024 08:29:57 GMT  
		Size: 163.3 MB (163252799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb74ca72c72562f7df25601c768ceedb917c24fc75e71697f0be9c5fa72a1746`  
		Last Modified: Thu, 17 Oct 2024 08:34:14 GMT  
		Size: 69.5 MB (69466925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6f5cdb7ea85c7b78d28ed4315ca5d3de5b3f202146f830d75c3d4b4508a12d`  
		Last Modified: Thu, 17 Oct 2024 08:34:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8cc0b325b8497bd2ccce895b6000f96e8b8c7e95f6e67adbf877a1e9edb8c1`  
		Last Modified: Thu, 17 Oct 2024 08:34:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:dcca7000cfd69ca7dc83cf87428e23f5f66de9ef41a3de20623dd79742566767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7215151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f10c023d673954b1e0192fbe61b412bea6444bf50b8184c54c0a1f843f45f0`

```dockerfile
```

-	Layers:
	-	`sha256:6d1eb154b1594a10e5436cbf9c28d3018ea7d47b7de3e51e585c9ce35d6095d6`  
		Last Modified: Thu, 17 Oct 2024 08:34:12 GMT  
		Size: 7.2 MB (7199567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ceeb082f376fe692a0bdbd452d66e213ab8bce87ebc8101eeb95763d4a4066a`  
		Last Modified: Thu, 17 Oct 2024 08:34:11 GMT  
		Size: 15.6 KB (15584 bytes)  
		MIME: application/vnd.in-toto+json
