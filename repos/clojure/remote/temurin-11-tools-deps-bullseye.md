## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:ab8d321367a9f9911ceacf9add811b5b73d50409449957cedc9bdbec89739b0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:28d8884f708e0705ab599002bb7587c16093202a6432b5a8a9c5b292dc9568e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269420834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0580d282effe40fd7b685b1ff724258ef1265f6eb7b83588603bb3426d3eecdd`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0bc80bdef4c94e792ecd12931c5f998377d0365ad287e2c5840339e296fe9`  
		Last Modified: Wed, 05 Jun 2024 06:10:20 GMT  
		Size: 145.5 MB (145505192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba9256b5c4ade5e89233ce0ecb43b250b2eeca54262786046644684bb28a5ce`  
		Last Modified: Wed, 05 Jun 2024 06:10:19 GMT  
		Size: 68.8 MB (68815595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6995c214fa2e0bdbd05181db42b4edd43d8760cc95ee834867d4d11717f08a6a`  
		Last Modified: Wed, 05 Jun 2024 06:10:16 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:74e239081714a895c3929f5ecae44c190aa297f5666a9532b78ccf3d8b992033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7013566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e56addaf5c45111e5300a5e48b38bc48778ad856f58a1e40c2f3c8c04b8b05`

```dockerfile
```

-	Layers:
	-	`sha256:ff668ce713da11ddf8680928485a202d0a10c6f5fc0a501d739cebdec7956023`  
		Last Modified: Wed, 05 Jun 2024 06:10:17 GMT  
		Size: 7.0 MB (6999751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cf5b841526eccc6e3bd375df6af6ccd13cb2c4abebae2bf8b4c37424533de62`  
		Last Modified: Wed, 05 Jun 2024 06:10:16 GMT  
		Size: 13.8 KB (13815 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8f96c5f157db5a3ee67ab8a725bea7ddb0c8c16192018678c4c7f55f9d7ee82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (264973222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f311e3f8acaf74ce41fa4973dc50506aa6a99716a673d2425e04addff4a50ef5`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 00:39:47 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 14 May 2024 00:39:48 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26d124c437ecd9132308b68716da2e3359df4123193511a5af508c35a87f883`  
		Last Modified: Wed, 05 Jun 2024 13:54:53 GMT  
		Size: 142.3 MB (142304052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c84926d184cbea10c3432ff790619dab5a0461cc50d0c86cfe5850545622eaf`  
		Last Modified: Wed, 05 Jun 2024 13:59:30 GMT  
		Size: 68.9 MB (68929531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0e295fa86540fcebe42ec626aa727c3e621fc637282fd8d431172b7bd25b0b`  
		Last Modified: Wed, 05 Jun 2024 13:59:28 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c648c9d8f0bd4d938d4e277fcf52d019b4d5e66471b3900386a610bd80a421ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee08c7f3beeacdf44e17f0367f5535ea7eccebd5cdb408c65816a1ac744c6e41`

```dockerfile
```

-	Layers:
	-	`sha256:38d58ce5754bae82955b4082a3197f0785c0fcd7ec2e374ce0786651da880ccf`  
		Last Modified: Wed, 05 Jun 2024 13:59:29 GMT  
		Size: 7.0 MB (7005473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79e740f8531c826183c511d25ee013fe2f83ba51b79a59669efb80e1ef7b8299`  
		Last Modified: Wed, 05 Jun 2024 13:59:28 GMT  
		Size: 14.4 KB (14351 bytes)  
		MIME: application/vnd.in-toto+json
