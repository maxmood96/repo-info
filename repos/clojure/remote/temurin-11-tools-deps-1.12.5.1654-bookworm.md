## `clojure:temurin-11-tools-deps-1.12.5.1654-bookworm`

```console
$ docker pull clojure@sha256:5dedf95e7d5babce8be14300cc79e1f3f5c38ff7401d90173aa7e25f6fc88ab7
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

### `clojure:temurin-11-tools-deps-1.12.5.1654-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d87c42565c5dca6833dac6ddec626354e6825430f023d45f76af299c9d0f1013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272513724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20269c227150e3dec3ea75f743242ccc10978075ff8b4939957e31e2591b98a9`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:15:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:58 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:15:58 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:16:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:16:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b139be38763e67841b4b9784d2215b175e4c76c9b570463f69323d4a35ae91`  
		Last Modified: Fri, 19 Jun 2026 02:16:30 GMT  
		Size: 145.9 MB (145886130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edec4ed1ee96bbec7c1cf696fa5d2cf639f6712b188b29d9afd87203b396c764`  
		Last Modified: Fri, 19 Jun 2026 02:16:35 GMT  
		Size: 78.1 MB (78124908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8161c6ada6d072df31ea618cf20b5964d09e044232534481a41f0ab7dac4da73`  
		Last Modified: Fri, 19 Jun 2026 02:16:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:edd56fb0800713ac6c618e7d86a18c5e592bb625a0415748bebab2ee148e2151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7410013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:079c29fc3d35d04ef16b19c37d346eb7d6e1880c3046b8bd03c50fda3b1d8251`

```dockerfile
```

-	Layers:
	-	`sha256:d73d0254b9d1e8c232118010214ddcf6aa8a4e6818504fddb9ee4a74b77990ba`  
		Last Modified: Fri, 19 Jun 2026 02:16:33 GMT  
		Size: 7.4 MB (7395650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afaf6b6b935f0abc4eff431b07614410a0027792557126422d1dd1d21f4e1dae`  
		Last Modified: Fri, 19 Jun 2026 02:16:33 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1654-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2b9de3a7f70e05a510316de8d521637eaa0e97b67046072ffd6178eceb5ba034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269101195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e113657205d75fd78dd6aa3d9efa8f7fb68abbc079ecdd29198a87469f1ba958`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:15:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:52 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:15:52 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:16:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:16:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8b76aaab1e87ab47f1275b0bc7769c7561073f2123c9db7ef3f81b0159ac3f`  
		Last Modified: Fri, 19 Jun 2026 02:16:31 GMT  
		Size: 142.6 MB (142582158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a400d138f18992b0146c3556a73d8445c031f5cd6048cbe353e1b696e3e0d69`  
		Last Modified: Fri, 19 Jun 2026 02:16:29 GMT  
		Size: 78.1 MB (78129377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b77cd72f029f173b635fda1c43e6ee26bd0ad7f1b78f0fa2b63628faf71eb43`  
		Last Modified: Fri, 19 Jun 2026 02:16:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:56e0c80ba4b03618960cbc91f95fb2dd9ec858e329f75191d80ac1f7445699dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a8cb8e6de5dac146d25be0bffb4a55c6e5efed96d3757b32f1010c1ff89cae`

```dockerfile
```

-	Layers:
	-	`sha256:9f620cf4dbac89d2c61561d1a4683f1d1c36c5261dd42ea120d7b87ad51a85c4`  
		Last Modified: Fri, 19 Jun 2026 02:16:27 GMT  
		Size: 7.4 MB (7402031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1e8197d66c7b7cdbb87596220b22636d8984c42e80f5f3f13e7e44d2f745f2`  
		Last Modified: Fri, 19 Jun 2026 02:16:26 GMT  
		Size: 14.5 KB (14481 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1654-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:b69da280c237832b698133c5792256c974d46ab8dcae1e1bb7f8ea283d1d47ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269416843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28333adf5a78534935ef5402cc2a1eb969cd7710d9d05364880bb4821ebcc81f`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:24:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:24:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:24:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:24:25 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:24:25 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:33:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:33:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:33:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fc64daf9c9f118fbcba656767bc8dbba78b223045b626eb61d82cdc3a433d8`  
		Last Modified: Fri, 19 Jun 2026 02:28:29 GMT  
		Size: 133.1 MB (133110739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967b429242342850ada761a4f0823256e32b5fa5b6262eb64318972a318ea0d3`  
		Last Modified: Fri, 19 Jun 2026 02:34:32 GMT  
		Size: 84.0 MB (83958791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b4d1319770b51b178efa11c827cfc78d09df64b44ae1af21a6fec8529010a1`  
		Last Modified: Fri, 19 Jun 2026 02:34:30 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:206e3c15fb55dcadba2c13029bb227e080973ea83d9bc5d6e6c0c4ecae85d7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7414662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad44115fbf2eb94734936bfb945246c52d39db3809f25f2b7168184feed0fc4`

```dockerfile
```

-	Layers:
	-	`sha256:724d946195c41da9d661b8911b11084a814ccc7daeeeabad6213e1f876dee354`  
		Last Modified: Fri, 19 Jun 2026 02:34:31 GMT  
		Size: 7.4 MB (7400251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14358d5ae19713c86fe4418e1425c02948d8a37ee792beeb604f330f3f82c612`  
		Last Modified: Fri, 19 Jun 2026 02:34:30 GMT  
		Size: 14.4 KB (14411 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1654-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:48558c0bed57ef1e5195714ff0eb1dfa371d5245d7a5d2e3d77fde3539211cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.7 MB (250744428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc95a610ca922aa162e5e80c601fe6dd2e896a6217fb6c892289c1000e6f6fd`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:13:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:13:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:13:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:13:19 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:13:19 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:15:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:15:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:15:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec01773c1e8ae5aa1b17b3f9ed96fe3b2db5b42fdb8cb8ff5e6dac16b5f5027`  
		Last Modified: Fri, 19 Jun 2026 02:15:08 GMT  
		Size: 126.7 MB (126652584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995157b38c8044df61cb85fe2cf54ec098defe646d527d97c5b6c9aaa7325297`  
		Last Modified: Fri, 19 Jun 2026 02:16:05 GMT  
		Size: 76.9 MB (76929698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa75593ae28c39f5238cb18d599ff5ec68894f7bfc8fbb5d03705d17d40ce75`  
		Last Modified: Fri, 19 Jun 2026 02:16:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c5a958a0fb4df7b8ec31e5863f5543f9553391e4ad4256f917a95ffaff238c44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e20a662b77d73b009b315e2223b4c65778541a8c8666a160a14d24defd62fd44`

```dockerfile
```

-	Layers:
	-	`sha256:f2b246a7a851b038f332ec288616187f0d62dd9449828379f3f86258359c9c36`  
		Last Modified: Fri, 19 Jun 2026 02:16:04 GMT  
		Size: 7.4 MB (7386973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12348cd59cff5edac03607452aaa0043d73130e225d9e37d8084fd50c80f03f0`  
		Last Modified: Fri, 19 Jun 2026 02:16:04 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json
