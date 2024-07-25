## `clojure:temurin-21-tools-deps-1.11.3.1456`

```console
$ docker pull clojure@sha256:e1dc2b54faf4bd60721687009f28f56b9e6c43efe833359f660a5ccec20bd378
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.11.3.1456` - linux; amd64

```console
$ docker pull clojure@sha256:65bb16068a5e18926344c57a6b066edf237c5ee6ce4e317850f2f879695f7530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288648402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc1ae24af777d969e314d45f0a9235247d0785f4be21dbcd5083797970d97b9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4300b0c064bbd3979bd0192d82aed7173fca8c3ba024244c8ae2dc4583e339fc`  
		Last Modified: Thu, 25 Jul 2024 19:05:38 GMT  
		Size: 158.6 MB (158579315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4130da8f16926bc174a089a745b070f9ff7d2c61093eedb36040642d13a52dd`  
		Last Modified: Thu, 25 Jul 2024 19:05:37 GMT  
		Size: 80.5 MB (80513971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e404b1e24f0a0d06b6ffc0fe88e6ad53eba3967d9f06987c2356a7e2b87f559c`  
		Last Modified: Thu, 25 Jul 2024 19:05:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85345993cec52850a5273d480ebbd7e76ced73c7f39fe9b171bff0cffa138958`  
		Last Modified: Thu, 25 Jul 2024 19:05:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456` - unknown; unknown

```console
$ docker pull clojure@sha256:75ec7f3778bd9f2d431da2d45d97986bd83a5d2221ea14d91090900b8053d14d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29390095c2086e3427be35afb906e156bb0016c95ac1d8566b0d647092b5b2b`

```dockerfile
```

-	Layers:
	-	`sha256:5b44baacc63de5564dad6778c9491fb7ba555f114535679c95ca2cb9b226e157`  
		Last Modified: Thu, 25 Jul 2024 19:05:35 GMT  
		Size: 7.0 MB (7002096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0647518e687238e92f84d6e908f66a75e4a0eb8cb4dcc5580f8cf89c124ee90a`  
		Last Modified: Thu, 25 Jul 2024 19:05:34 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.11.3.1456` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:de250669be86fb9b5e3e04dce5182561e3f2d5b43a50f9cf649598cadb0c88e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286594877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5e756ecfc1e183f668c57ec0b907a8d08844297b475b6f03737a3d7e17f679`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa02fe68cb544c51a1303e36a18cf608c75bc1de3f7949ee859b2dd1faee5a7`  
		Last Modified: Tue, 23 Jul 2024 12:02:51 GMT  
		Size: 156.7 MB (156746178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee00dd69dd8f60bafbe46c0fffb40efe640234119ca127c08eab03eb2f1bd90b`  
		Last Modified: Tue, 23 Jul 2024 12:48:33 GMT  
		Size: 80.3 MB (80259220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e7a3c2e3a4651aeb042bd36557c34d12acc69280d0caf229389b2e3a45c5f9`  
		Last Modified: Tue, 23 Jul 2024 12:48:31 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffa309cb00a389e909fd58ef5971a5efca018aaffc01c9104822adc1b4ca980`  
		Last Modified: Tue, 23 Jul 2024 12:48:31 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456` - unknown; unknown

```console
$ docker pull clojure@sha256:a6177a555ea4c92b8424faa74ca230211b42eba16e69d28117b3570113f725ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7025772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4228824ee1c5b7865ca80cce613a00c5ea2002960b0f958a6156f47c103b40fe`

```dockerfile
```

-	Layers:
	-	`sha256:b172b9c63b5388f2cac325a6b57015f5c864d99252e3face89a01653d994c2b4`  
		Last Modified: Tue, 23 Jul 2024 12:48:32 GMT  
		Size: 7.0 MB (7008555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96e8695b8c21cab3bebd2c4630b9ec53cec8a2810c895b5d45c4d7ef7c7c992d`  
		Last Modified: Tue, 23 Jul 2024 12:48:31 GMT  
		Size: 17.2 KB (17217 bytes)  
		MIME: application/vnd.in-toto+json
