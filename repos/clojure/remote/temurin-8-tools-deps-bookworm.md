## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:f20d41a54cde5548438222c542da906721583446608f73d5b4b820b73b6d0610
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:e340fbddfbb2fa77a9a9e8ccd9bf452e1f13b6ae4bc4ae2ed2a66180a390c8e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184192556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd6e546f79dc835656c96ee9501f637d464963052c5e462512bb5b14a13b291`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5715cf08eed2ec48fe1d1370fad6eb658563c0528f64dbeef58255e980314331`  
		Last Modified: Tue, 25 Feb 2025 02:15:15 GMT  
		Size: 54.7 MB (54721234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34387be61223da3ddb28bbaf4ff43f1da3e0953ab55419e1b07c432a2274d61c`  
		Last Modified: Tue, 25 Feb 2025 02:15:15 GMT  
		Size: 81.0 MB (80994576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a1100aaa94a5c4e887e384224f89e8e36d9acfc6f8bc0344ae27a2039d3702`  
		Last Modified: Tue, 25 Feb 2025 02:15:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:322c5a6079f762cb148db918e6725d269a2720406a601851a8865b5633ef0aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7306942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db975616bda169999c0cc9e99dddc0e55d76b1f76e15a0031a8ed10257da3831`

```dockerfile
```

-	Layers:
	-	`sha256:83699ad9f2e2eaaa092b70070521c2281c8223dd87397c76df91b1d5a7db5158`  
		Last Modified: Tue, 25 Feb 2025 02:15:14 GMT  
		Size: 7.3 MB (7292706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b3f77eff6b030cec00bced06afd60542accb7e7385d30b5131833bc263e0033`  
		Last Modified: Tue, 25 Feb 2025 02:15:13 GMT  
		Size: 14.2 KB (14236 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:24f5f48ba439511c00102504aa0edd312cb3521e507dc322d6a50bdb65932527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182973944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24288190d93fa54dbf709a867d39266c3b3189bfdf8e60d7f1bab7ea2e45e16`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73158f818927f3d5d74c42ecfa65f28017e7d8107b6335006d95965106742209`  
		Last Modified: Tue, 04 Feb 2025 23:24:17 GMT  
		Size: 53.8 MB (53822777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd95378984ff69528a6e4cfbb8b3f4cdca757403a9afd7dffbd7b5f435e6c08e`  
		Last Modified: Thu, 20 Feb 2025 03:38:40 GMT  
		Size: 80.8 MB (80843969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b879f84f423546016ed12b8565657d26f72bbf4c69579a9a55d274d506b7a9`  
		Last Modified: Thu, 20 Feb 2025 03:38:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b3c7ad65e9f35bb3fa6eb7ec100727918281ca241e98fc89ffd527c8be1c8783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7313504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28cd2f17a9e399629b70bcb7f4d63a6f9bfdba0f54dcfc5ce25cfc26317c62d`

```dockerfile
```

-	Layers:
	-	`sha256:7a886df520cd185bc00b0e52533ae9f6dda8fe713da3416819cd0f0b1e08d7ce`  
		Last Modified: Thu, 20 Feb 2025 03:38:38 GMT  
		Size: 7.3 MB (7299149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5586d4893a3c98b230d700394d9ff7ea03f3fe244118173ecc23f449aeae11d1`  
		Last Modified: Thu, 20 Feb 2025 03:38:38 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
