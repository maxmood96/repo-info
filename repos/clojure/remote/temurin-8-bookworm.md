## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:31fc6ca7205b13008087f283a821dd841eedad043c905735f6c6d1412a19b018
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:862d206b6373d1540d07e3deb9f44ffe19418956216c51a8f718e70251204069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184907717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca73871a3154f8a1016c6d0725dc194fe44f3d040dad95bebb7a0f02f308d0e4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:55:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:55:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:55:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:55:32 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:55:32 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:56:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:56:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:56:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3648f3291a4d25e2bb51f0f1669282bedc7fcae8d94b6e98cdf3b987afa8012c`  
		Last Modified: Tue, 19 May 2026 23:56:02 GMT  
		Size: 55.2 MB (55198702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759c1861373ef3f2ac1a12b2476b9dda6db3e90c73408d03415d257b9170c62a`  
		Last Modified: Tue, 19 May 2026 23:56:41 GMT  
		Size: 81.2 MB (81212938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3353dbb4df9fe78d6e5f7030462b78471c234b1002fd6b6f415f261d5b7963ed`  
		Last Modified: Tue, 19 May 2026 23:56:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:30c860006a9d9b46e709160a19feb54bf94d739c57a6a23bce73f4047f46b0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7512703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31bbf4bda9b67faa79ef864d3aa01e6aa817a46d19d315677ed402e8d543e765`

```dockerfile
```

-	Layers:
	-	`sha256:c8ea6f6625270044bc4dc69fd9c1ef4bc3bc2e8a63e8571bcf2f50dea088b8c0`  
		Last Modified: Tue, 19 May 2026 23:56:39 GMT  
		Size: 7.5 MB (7499309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:363e5080fa75e149b209c10066708715055efdc2fdeceb0f0c8b2de0d0837ff7`  
		Last Modified: Tue, 19 May 2026 23:56:39 GMT  
		Size: 13.4 KB (13394 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:307d7be8f6230f878efb6388bfdbedab40a073f8e8edef5abf29f63d64b676f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183866476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c221061b57cfd7807ffbb08f72cc67bf222fc6420f53af01bdb6c41bec024e7c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:03:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:03:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:03:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:03:26 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:03:26 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:03:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:03:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:03:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269db274a15c3c2bcdd6fb03fcf5c6e2a1ef870be8c072283fffa6a2773f6bf5`  
		Last Modified: Wed, 20 May 2026 00:03:59 GMT  
		Size: 54.3 MB (54272904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4539fc16c85202909d5e3223914cf95826e64eb9ed8b55d79ab1dd6839d17da1`  
		Last Modified: Wed, 20 May 2026 00:04:00 GMT  
		Size: 81.2 MB (81213496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6514924ed5f41ae8016cf7690ea15fca57d2cfe62e136d91e40fc0b430e8cce1`  
		Last Modified: Wed, 20 May 2026 00:03:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1cc0f79bfdb4d13dad7cbab52b0046a7a7a876b5b600da293d7c61f5ca135960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7520238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd953d8cbedd700504a2fdb231433769d566d5c3ca35c0c280a864a0a3439dea`

```dockerfile
```

-	Layers:
	-	`sha256:c9b5ad8df944a0efa21241f60c49a6b028e947bd479041d74c2f09512313610a`  
		Last Modified: Wed, 20 May 2026 00:03:57 GMT  
		Size: 7.5 MB (7505772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99e31f5d13d161e917d51c4e48947c8f29e45c2f69aa1b31fa7743edb3b3e2d8`  
		Last Modified: Wed, 20 May 2026 00:03:57 GMT  
		Size: 14.5 KB (14466 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:3e985898bc1d76b2d013e49f564ee85929d8ff9ce79af94669b02a915433b1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192056683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6379561f8ffe9220113d4e8d6e130f857b14b4f676dcecc0fcaf616d71bd1d4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 05:41:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:41:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:41:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:41:57 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 05:41:57 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:45:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 05:45:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 05:45:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b865ce015782198efd3fb681f99e5929fef916aa774999d18b087fba22a996`  
		Last Modified: Wed, 20 May 2026 05:43:04 GMT  
		Size: 52.7 MB (52669123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d8b4f429ffe45b4310483af5794f7951ea8a635092cfc12348c5ed77f57ff1`  
		Last Modified: Wed, 20 May 2026 05:46:25 GMT  
		Size: 87.0 MB (87046716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e3aba79218146336fcefb2126e2fcc28d2109896b61399569858c6c9c87c49`  
		Last Modified: Wed, 20 May 2026 05:46:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0d8f133d253df359e394b32a59665bcf70cf3ac54d056bb1e86dd6ac614ba726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7519516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f1b9085057ee67bb6dda9ae0f081139a620bb93bfd1ebd4a75113afca7a1fa`

```dockerfile
```

-	Layers:
	-	`sha256:9325b15c48157623d931913185b17823bd176081324f6c3b2a67759c8a7987c3`  
		Last Modified: Wed, 20 May 2026 05:46:23 GMT  
		Size: 7.5 MB (7505120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d576c1ed9cfd5009d77c344b047a03a6b16d0337681231d64431fa3663591be`  
		Last Modified: Wed, 20 May 2026 05:46:22 GMT  
		Size: 14.4 KB (14396 bytes)  
		MIME: application/vnd.in-toto+json
