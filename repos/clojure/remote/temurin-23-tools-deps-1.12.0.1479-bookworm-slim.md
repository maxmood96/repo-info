## `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:a4303bb66dac5043d5b97e4ca939c4c779921a2d3f69831e481e334557db1213
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c3611f8e4cfec184b4e5bf809c88847065547dc09a8324e3a4c7d126e1a9cd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263911391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3293fb89a0b2b9af7062cf35596ef3eae1fb17795290c4e88ca24d200ec282da`
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
	-	`sha256:0dc58329d931d82e09f83e2f9a4bfd305408f1f761ebfe2f1b0dadc050e0d3ba`  
		Last Modified: Sat, 16 Nov 2024 03:51:52 GMT  
		Size: 165.3 MB (165295087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881974135cd9230da9f4207e96f3e0e0821a7a4c6e1d65d84ba9ded63b900c4d`  
		Last Modified: Sat, 16 Nov 2024 03:51:53 GMT  
		Size: 69.5 MB (69487269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8500218364e162823f74446d3166916e246f94e278f9105ffee2b512a6be4d`  
		Last Modified: Sat, 16 Nov 2024 03:51:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c29120b1a5d75dd00bf6ba6f35b0a5df81f679a6861c278ed1880b470430ae6`  
		Last Modified: Sat, 16 Nov 2024 03:51:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a8785937f20bcffbd632d405e3b37fed4a7187fa411ee5e9b20d71f5a64bc4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4941519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:020524f39898172554a521e15f1e0c8d73bd8c194c405bcb9e9239eaf3474f35`

```dockerfile
```

-	Layers:
	-	`sha256:9ce082e0148ddfd7a012339bddad5ebe8b5afcc6f08be635e5d353f2c276a81e`  
		Last Modified: Sat, 16 Nov 2024 03:51:51 GMT  
		Size: 4.9 MB (4925641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9f58b843e22350b8844b95cca5a03dfb1219ef31ff7000ccb424f2b46a3d124`  
		Last Modified: Sat, 16 Nov 2024 03:51:51 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0f15b80c1cb7a14aa080a15f7959af84434b35ec34e7983729acc388201162b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261774881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63a7d529e8d42e2fe86e53fb759352233bdf1363164582ebd87fa9a78c6c778`
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
	-	`sha256:7e8d146b306dcdab2d600e1d2bf7fb965e385834e6c85bc62b45ef12055a0a4a`  
		Last Modified: Sat, 16 Nov 2024 05:47:39 GMT  
		Size: 163.3 MB (163281818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f128602e54bd4c6a6a199bbfc2436c8df0c0bd2778b5e2aed66a930f47c8b0`  
		Last Modified: Sat, 16 Nov 2024 05:52:31 GMT  
		Size: 69.3 MB (69334665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d43d03368f862722e0a35df5cc1bf3cf3212a01eecce76956ec57261c5b6dc2`  
		Last Modified: Sat, 16 Nov 2024 05:52:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5420ad31490430f22828af4177cba2ad26b527276d02aba00988300f716f3aa4`  
		Last Modified: Sat, 16 Nov 2024 05:52:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2f7680dd9341a1cc17c9a79d3315cf49adcfb476ff79cb4db60e46b2f234ae63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4946781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7dd65f2742dbfce54ea8b6714771ec0d1f4a17ac7898f4b864bd7bce174341`

```dockerfile
```

-	Layers:
	-	`sha256:52eadcd1a2d837ac63a1e2cb442311faa840c1f4320c33894ef09a5c1b2e83de`  
		Last Modified: Sat, 16 Nov 2024 05:52:29 GMT  
		Size: 4.9 MB (4930785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea424eaa91858d3d567e383aa0f537ded5e01eeb799f825f06e34103945b26c`  
		Last Modified: Sat, 16 Nov 2024 05:52:29 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
