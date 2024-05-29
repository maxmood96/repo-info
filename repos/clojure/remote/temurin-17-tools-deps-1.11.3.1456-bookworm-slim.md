## `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm-slim`

```console
$ docker pull clojure@sha256:5315e50a20ae265c4cfa9ab23478e56c07963b917aaeb1212c8765d08ee3e9db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f0795f2b0310c7158df07334d4ecdfd764e059c54d3b77eaeeffe9808d84515a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243114585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f7d2353ca7423e992dc840365729c74a16430590441cc756513c5e03e1d08f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084cd2598fcf7a9e095da3754e9b2795b89caa5de0b755d30dc04395a6ded66d`  
		Last Modified: Wed, 29 May 2024 19:57:16 GMT  
		Size: 145.1 MB (145095011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd2dab6d1be25ed6dac9996bc7fc665b53b249facf5a5a9cc728209e03d6767`  
		Last Modified: Wed, 29 May 2024 19:57:14 GMT  
		Size: 68.9 MB (68868118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fceec9a83a01064f0e73e78ae5ac6f97009cc18da8f07a6e9731772a00d2fc2e`  
		Last Modified: Wed, 29 May 2024 19:57:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240afa2a991362756f073b6b4787cf67c2af3c7faec49d1eb992a5b70ee9f797`  
		Last Modified: Wed, 29 May 2024 19:57:13 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cb13ac023a07e39c1308fbba6ded7689746b6a4dc4af6be1415d9cea156a5906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4720402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8315bba1988885f239ae7ed08aa1cd0d27373bf7880c2d409a510298cf6224a9`

```dockerfile
```

-	Layers:
	-	`sha256:9340e563b72bf44dc97776d8421aa6df90bee55166ff1c32faf496012c52d213`  
		Last Modified: Wed, 29 May 2024 19:57:14 GMT  
		Size: 4.7 MB (4704939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78815be805a4cd3a0ea48ca8bee8b646041f0fe1451778df9e276e19f0aae4ba`  
		Last Modified: Wed, 29 May 2024 19:57:13 GMT  
		Size: 15.5 KB (15463 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b01098be2ae462e801902b59ad32724f21d8b4681aea5649229052ba4628af44
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241890676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143c1a9630904da6d7ae933dacc82e9873c0773ec2036b0a2ed01fe80e267d9f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:54:57 GMT
COPY dir:317487729b1812635c51c5f305bd9178bd957a141903eab756a1683874b5752b in /opt/java/openjdk 
# Tue, 28 May 2024 19:55:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 19:57:08 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 19:57:08 GMT
WORKDIR /tmp
# Tue, 28 May 2024 19:57:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 19:57:23 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 19:57:23 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 19:57:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 19:57:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72920bb393b41da798570e0a544fba4a0fc4aee2db82d333d8a4949661635df`  
		Last Modified: Tue, 28 May 2024 20:14:53 GMT  
		Size: 143.9 MB (143891839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b329ed1bf6490b2ec99df0756cffbfe08add1994636346fb4dd7f664d528815d`  
		Last Modified: Tue, 28 May 2024 20:16:35 GMT  
		Size: 68.8 MB (68818317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a18a35366468e0d3ad2c2ff5a887fcd16c09f5b25079e953734fe783795a4ae`  
		Last Modified: Tue, 28 May 2024 20:16:28 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f7de2aed3cb3683a10c33362cbf02afa3c87bfd146610a10e6d8f73ac52221`  
		Last Modified: Tue, 28 May 2024 20:16:28 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
