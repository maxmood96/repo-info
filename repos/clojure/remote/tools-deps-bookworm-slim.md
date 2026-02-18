## `clojure:tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:6cb61fbbbeb4150fab0842ab35f6befaa6231e9d3d8465afcd0f33482b3a080b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b0d24c14b4500445e52349d3fffe42d943cc2da1f0223ff3c687206590cb4196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190163340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16b2e69b2fff1f31e9b8d4df3b10b8cbcded8b5c2efa1cc649d8ca4dc627511`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:45:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:45:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:45:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:45:59 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:45:59 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:46:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:46:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:46:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:46:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:46:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77437f05fcd5e08c58d99e1215b19a627c3f59f929740a78b912fee96bfd70b2`  
		Last Modified: Tue, 17 Feb 2026 21:46:31 GMT  
		Size: 92.3 MB (92256289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c9d736179f3e1ce1d562c3c21293059ac6fa80effd20fabdb95ae6612e9705`  
		Last Modified: Tue, 17 Feb 2026 21:46:33 GMT  
		Size: 69.7 MB (69677522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c56d06b81a4745d728a06dab5e0d1ec219a4a68cfb43ca3da85588ef839e191`  
		Last Modified: Tue, 17 Feb 2026 21:46:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724e5508ec99a79b529d512c1244931a59e8ed68f357ebb7ca268f251b8022e5`  
		Last Modified: Tue, 17 Feb 2026 21:46:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:382e8b1fc91a7822949d1bbf5a46a796e699068f7e2da5af37f1e91bae8c7082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5099273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d007b826ff076a201888d86106a401ff75e69ed6a84835d169d08b1f2ec8474f`

```dockerfile
```

-	Layers:
	-	`sha256:819ce5e29239982d9a610a80fb3d1f8d4728a0ef95e3fd393c76bc7a5e3e7de9`  
		Last Modified: Tue, 17 Feb 2026 21:46:31 GMT  
		Size: 5.1 MB (5082748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cadbe806933f104c224e5b84bbf342812b5f1b87a7f9abb0b12fe0bc3e0677c7`  
		Last Modified: Tue, 17 Feb 2026 21:46:30 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:31c6fc2d635ce71814dcfaf521e2815984c6b5e5c7f4ffbcca256a12ba8cc567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189069807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d06270ca5d65feed6b39d3d30d0f0fbe9598c7cdc29e12cce9c776b24a6ffe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:45:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:45:39 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:45:39 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:45:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:45:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:45:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:45:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:45:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4fb92781f5977c953da0ca8bf3803d22f9b891f2250f1fe412965248d48b55`  
		Last Modified: Tue, 17 Feb 2026 21:46:18 GMT  
		Size: 91.3 MB (91288273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9a8c7ba53d7fb90d177cc883d9ce45c99b773e358d6c10020804fe3ea9bc88`  
		Last Modified: Tue, 17 Feb 2026 21:46:18 GMT  
		Size: 69.7 MB (69672667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95b85146fe8ef105e3e741c5841c460595321565a8e87866fe9a0d51f2e7b99`  
		Last Modified: Tue, 17 Feb 2026 21:46:15 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4eb8037a1c31018a7296e8afaa3a02645f885c846ab7c768f14eb8cd6879deb`  
		Last Modified: Tue, 17 Feb 2026 21:46:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:13cdb75b8606ba59094da0ed7ceb4f2f655a97afc8b2e8a8b31f8ba39e705715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5105197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98111f294406daaee3a4ba254a70783b1a571e7a6fe107a0e0fcd189851e345a`

```dockerfile
```

-	Layers:
	-	`sha256:f2182701e91d70fe112b4c99c794d284fa5bb728afa0b1b143a101cc318fe23b`  
		Last Modified: Tue, 17 Feb 2026 21:46:15 GMT  
		Size: 5.1 MB (5088530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceda88d4e71ebb99e88bfeabc454dc31920aeb8b9b9c29449e0fa0346e7b8968`  
		Last Modified: Tue, 17 Feb 2026 21:46:14 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ba21ec4963ea21d4e0ae3efad26dfb2cc580d885f5a7f5fb4d413bf967f1cbc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199216822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fc958b58d01acd7176e51f6ab2352e48f6ee5282ac77174baff581b6619cf7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Fri, 06 Feb 2026 00:46:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:46:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:46:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:46:09 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:46:10 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:51:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:51:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:51:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:51:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:51:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91cb234547828975d01511eb3f1e2f07f4c3226976323dbaf0a3fe8832f8431`  
		Last Modified: Fri, 06 Feb 2026 00:47:43 GMT  
		Size: 91.6 MB (91632917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7d1bff7a7aa17d12bfad8d52d8030be45d899e876e5cf39f0f2c8d9fcfde89`  
		Last Modified: Fri, 06 Feb 2026 00:51:59 GMT  
		Size: 75.5 MB (75514150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feea98bb1e6e49d6287c83e30989b16ea90787b12d2ccf31792e8ce47337c41f`  
		Last Modified: Fri, 06 Feb 2026 00:51:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f3e6a206e0bf371d7ecce2d701cc3627bcb799a2f65be0b2b875a0a201c6cd`  
		Last Modified: Fri, 06 Feb 2026 00:51:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:14aaaf781f8439cdfdfd1c7b600c3afedeb03eb30c8af74c773d6cfd880379c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c90e9260012b338bb83095fa85b6e97cc9cd83c0a2b298f773ece7b14dfe71`

```dockerfile
```

-	Layers:
	-	`sha256:b14b64cc28c2b0c4a6b418ce8ef20746a12c684dba6be2ec8dba519a0697db23`  
		Last Modified: Wed, 18 Feb 2026 00:05:49 GMT  
		Size: 5.1 MB (5071230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a7855f8cd12557371e34e9d9ca4b864806a49d2709466af8bb837159ea0a48d`  
		Last Modified: Wed, 18 Feb 2026 00:05:49 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:54ca839f270a8981f4f94b595fd76bda843c0ed27a3e71a925501d076ae05272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183609736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad414b62689ed4a2a3a171fae02077cf778ccdf5eec3c6bbb165262ec167fe8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 22:18:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:18:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:18:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:18:37 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:18:38 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:19:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:19:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:19:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:19:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:19:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4636a94cb236173f2946325ca125ab41014db7d1266b07c990630f0108714938`  
		Last Modified: Tue, 17 Feb 2026 22:20:02 GMT  
		Size: 88.2 MB (88233848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c97c45197cc0e279cd8c3f369b2656351c10fa5ae8b60fbaf106e1a10ad7e1`  
		Last Modified: Tue, 17 Feb 2026 22:20:02 GMT  
		Size: 68.5 MB (68490462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc1943add3341b425e7e354cdbb4b9c7a12dc20d1a9bd073fd0a6c02777b07f`  
		Last Modified: Tue, 17 Feb 2026 22:20:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5319830448305c9fb934be3699c4c723781e069c0e94f77e96bd17d6dff8d0`  
		Last Modified: Tue, 17 Feb 2026 22:20:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d9a131a57b8e920f33836d66f7bca87ae9ecdffdb32aefc35e948966f9e5e9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5075156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af3bcf39b3521153f8790199c9b368da700eb6d34027aaf870e1bccfec92cfd`

```dockerfile
```

-	Layers:
	-	`sha256:3330dbc2d44a7ab6bc4eb6b7461ebe3111f48d0a43792613ef7cf3cec7cdd4e1`  
		Last Modified: Tue, 17 Feb 2026 22:20:00 GMT  
		Size: 5.1 MB (5058631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c19a37954aada8ba76121c51e498d115d8db40f769d42f6b5891a2c2b2aacdfb`  
		Last Modified: Tue, 17 Feb 2026 22:20:00 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json
