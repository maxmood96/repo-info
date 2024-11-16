## `clojure:tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:344e66c2c353b9115445233f6ae67c6f9973d2c34d438b75a49b5b4b68142183
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:61fba031af6a68457b20f571396028cb7b540a800aaa068f7f5c5dc608a4fd40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256185038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b052e8218e20fd02bab6bd8815e60695b875576a3cd5736c1c004b8bcbd1f483`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e536f4f8f9ff43ea94cd2cfc25271a4a262c9cdbcd3cc917b3f0fd120f215c`  
		Last Modified: Sat, 16 Nov 2024 03:51:54 GMT  
		Size: 157.6 MB (157568674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a939d90649728cde2c6a90067b538cb5882496853bd7e4e73d18aac1245110`  
		Last Modified: Sat, 16 Nov 2024 03:51:52 GMT  
		Size: 69.5 MB (69487330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f09bc96129759fd9126fa2077f671b60178220aab24ada2b1058e04ed03b07`  
		Last Modified: Sat, 16 Nov 2024 03:51:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e64565c2f79956077eee8c1277c3ff339bdb8aabc26f1dde1a77e170add9bc2`  
		Last Modified: Sat, 16 Nov 2024 03:51:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:345ef9333264623fb93814292d667022b0b88738cfc9b663126327937236fd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4941006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd9f3a8970d32b904540382fdb61c4a9c6a2e0247d9d71e4348ab929d5dd906`

```dockerfile
```

-	Layers:
	-	`sha256:4ef6a1a925eae5a10f51f04bac9941f2fc2040132f8bec96f3c27a4913955f32`  
		Last Modified: Sat, 16 Nov 2024 03:51:50 GMT  
		Size: 4.9 MB (4924431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fa8b87f264cb34e688cc691d17c0dae6c8fd18d72c702e831e799a943005b97`  
		Last Modified: Sat, 16 Nov 2024 03:51:50 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ee7ef07d6c2ab36fd9f3c2bf31a6b03fa14e7ab421b6e7cf4dea40059755c28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254286240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6916ab1d65fc87ae289b2a38350d9749faa9a008d8f56f617d170f81ddc96363`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f7539dee24a48611ac02187ae2256212e947bf77784c765e04b2e40e3962bf`  
		Last Modified: Sat, 16 Nov 2024 05:38:25 GMT  
		Size: 155.8 MB (155793074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8211ebfccbf5d7099e43767466885fd641a6ec3476c6569e5d2c9a1fc142c2`  
		Last Modified: Sat, 16 Nov 2024 05:43:06 GMT  
		Size: 69.3 MB (69334769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239bf7c2b78b8bdad07f1ccf3e22a122452cbe25452605c5aa120117c0c627b9`  
		Last Modified: Sat, 16 Nov 2024 05:43:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e39f70758610f0057aabe665649561acdee392357b1ec9f7159c826e19fcd5`  
		Last Modified: Sat, 16 Nov 2024 05:43:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4d845007f43574942541bec38094a5379418fe83375fd70f77b687694cd3de5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4946938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77058c63467c623b37eb124fdafb372142a142041f0f6b4a6a8d3533a0616c0c`

```dockerfile
```

-	Layers:
	-	`sha256:13bc6ccda15d73c037910d94a55e1a20024c8a828bbe47ee21b5b414c3bad01f`  
		Last Modified: Sat, 16 Nov 2024 05:43:05 GMT  
		Size: 4.9 MB (4930221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ee748580c99c627f3111a727e5ee2168a2dd48353acd7dd2dda47d428886e6c`  
		Last Modified: Sat, 16 Nov 2024 05:43:04 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
