## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:1fb9c4de2a944bc23d144b98e62f7f6996583eeb7f37020066a10cd4bf1a06d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f56e9f2ad810adf0e56b636526e1e2c43f45fe15328fd1bd2b1bd9053c68faf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275175627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24d82f83746e6bd200002a4489da0cb0b260f573c4a1385645de8733cd51fb0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827a724696149bf469ce9e35dc582aa6e95cdb7aa639ba213f8beff5ec877672`  
		Last Modified: Tue, 13 Aug 2024 01:11:32 GMT  
		Size: 145.2 MB (145166552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7f0122cdd945b17237e83d2b15254a2b27ae4191af03ce34e7b3743be2539d`  
		Last Modified: Tue, 13 Aug 2024 01:11:31 GMT  
		Size: 80.5 MB (80453955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0138111b0a1e8e9bddf974104eacaea721921df4ef6aaa47b637142bbe3ba8c6`  
		Last Modified: Tue, 13 Aug 2024 01:11:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df2cc016f3db50cfbc4c665cade69eea9438e2c6a616f2348aa747f9b5774dc`  
		Last Modified: Tue, 13 Aug 2024 01:11:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:99b9021f2060617f02ffa2dfb022120d7e2ca18c52787f9119e1e5629db16c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7015526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31c34cfb7efc6b38b34ff5ab38afce5ffd5b71904e698f28cfc33869224b77a`

```dockerfile
```

-	Layers:
	-	`sha256:c935e3281b11941b2687c99fa6c0c25e6087aee4619f269b2af4f1ea27d1440e`  
		Last Modified: Tue, 13 Aug 2024 01:11:30 GMT  
		Size: 7.0 MB (7000086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be0877e95d58b2d21abc3aa9464a2eb9ebfab322ac278af4d56c9225e2f8a76a`  
		Last Modified: Tue, 13 Aug 2024 01:11:30 GMT  
		Size: 15.4 KB (15440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:102ab4ac8037f9faae4c14f1be4f25048acd574d5e937b66c24d2a9886c4369f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.7 MB (273747383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc89edb7a7c6bc8de7769c9700d34eeaf6d2d65d890410e94a3f0f8cd222506`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:40 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Tue, 23 Jul 2024 04:17:40 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e6dc0d1ac0a27933e4c618ce199a96734abbfb43e28d24de43f2e5a448b936`  
		Last Modified: Thu, 25 Jul 2024 19:29:36 GMT  
		Size: 144.0 MB (143959482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410849b4ae4ace9ebf3c0a60a8cbdcb47afab9fed364951746322a07ac98d5e9`  
		Last Modified: Wed, 07 Aug 2024 20:07:12 GMT  
		Size: 80.2 MB (80198418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a82a7e2251b14390c799bc52328aa15a7b9236453b8561e9b22448c6a56806`  
		Last Modified: Wed, 07 Aug 2024 20:07:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22722fa9cc96859ee505ff9ba456d81d22e22b2010d562dc47e182fb5ec64a59`  
		Last Modified: Wed, 07 Aug 2024 20:07:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1d0db14127c8ab45fb2edaba3bd4316da61bfff66a7e0b1f9b947afcf099e111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7022449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e40d7b11b95ee458f10b16c1b13f8dd4ac40ecc58a6b1fa5d41762530f124ca`

```dockerfile
```

-	Layers:
	-	`sha256:a39098580424c5642debd2d88c8f53d64d2a07b238ba95caea5312c941c458d1`  
		Last Modified: Wed, 07 Aug 2024 20:07:10 GMT  
		Size: 7.0 MB (7006473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68c55e2328729e350fdf9adeda319927af52be99ae59c3ff234c27110fe84939`  
		Last Modified: Wed, 07 Aug 2024 20:07:10 GMT  
		Size: 16.0 KB (15976 bytes)  
		MIME: application/vnd.in-toto+json
