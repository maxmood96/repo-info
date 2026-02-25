## `clojure:temurin-8-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:e69642394dbb8da3001b4f302be874a130c9faf4654d366ae4c4a21fe3b27097
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ae4e3c138c85c84bdf4c34adba48cc2e089d84485a78be5ce4fd0a164e743d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156943688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f97dff986e3c86d84c3bd84d2190e1a2c5de12a39a1d107b404d127186ae769`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:52:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:52:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:52:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:52:33 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:52:33 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:53:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:53:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:53:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8362d916c99f3bb6ea102c595ddc32c0a7078d13606452e9b735932635b03336`  
		Last Modified: Tue, 24 Feb 2026 19:53:04 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29dfe36fe7db5c430b5f01343060839548aa081a40aff5458a2877d0255a9081`  
		Last Modified: Tue, 24 Feb 2026 19:53:45 GMT  
		Size: 72.0 MB (71994353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27833084c3442a859d5e396bf4097d94c34e06205bdd050e83c37906b7d3703d`  
		Last Modified: Tue, 24 Feb 2026 19:53:43 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8ba5ec559335fa940d168f56b4400c043c906b9328b5685567b78a53b34646d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5392766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03991517924139c6ba014af0582592f6b7de1c993a83e2fa67f1eacd0210273f`

```dockerfile
```

-	Layers:
	-	`sha256:3b7bbe12129928a0641838618cdbfae5c322e1f5902cf193c9f15d9ce0321890`  
		Last Modified: Tue, 24 Feb 2026 19:53:43 GMT  
		Size: 5.4 MB (5378538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7231c411135ae657ff6807fdf8aa43978b793c6cfdbb3db8a6d7c7c0b6d38557`  
		Last Modified: Tue, 24 Feb 2026 19:53:43 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3829f4d1a04e256db5111dcb611d40bafded29118a9fdbda36e40c6b30d369c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156200179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64e303c0445bb808a1de1443e58fb2549f64013f0b6cf246e2da78a7e9b2674`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:04:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:04:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:04:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:04:10 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:04:10 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:04:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:04:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:04:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1778e3b75b22d1e590ba68beb45a4dedcc1893c547192fc892f6b9778a812f0`  
		Last Modified: Tue, 24 Feb 2026 20:04:47 GMT  
		Size: 54.3 MB (54251627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212d52cf5534a02c86a6d1643022ee371cb0e44648695353a996e097336ffd33`  
		Last Modified: Tue, 24 Feb 2026 20:04:47 GMT  
		Size: 71.8 MB (71807811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8af6e8d7f55dca1e4beb33e7a996218b87e173467bf6c21542cb8f99ca518d`  
		Last Modified: Tue, 24 Feb 2026 20:04:45 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d84599c30d3d3b6e234399ed2b527f0b0ba91aaf7d068100b1480d58d31f0b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7031d103fe5395e647f7dabb3834da2a63dc6f37cdc18c5390ee02b0ca8c8058`

```dockerfile
```

-	Layers:
	-	`sha256:7230459c2ba3a853adfc5a4679dac4d7f1b90bcbfa411b64352e2f793189bfd3`  
		Last Modified: Tue, 24 Feb 2026 20:04:45 GMT  
		Size: 5.4 MB (5385007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5eb65ae258bc982bdbae4257559d33adfdf8a754036b549db964e5f09a0b79`  
		Last Modified: Tue, 24 Feb 2026 20:04:45 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c107d85e5c90c4a69933cb47831bf782ee5b3d47f2896482ad57871c9d53c41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163658394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b185b1f7a04f9628cc223925cb299857740024ea1a2ba93e26359fdc2943fd46`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 01:44:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:44:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:44:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:44:01 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 25 Feb 2026 01:44:02 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:48:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 25 Feb 2026 01:48:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 25 Feb 2026 01:48:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1d2b34408ac8afec8ecb73eda9c9a8f5b90be5df6cc2f490984d24c34e7003`  
		Last Modified: Wed, 25 Feb 2026 01:45:24 GMT  
		Size: 52.7 MB (52650417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0431294aa648933c82a92c992c630eb95c5475c0c8d9b1d55a469a4b60a5995`  
		Last Modified: Wed, 25 Feb 2026 01:49:05 GMT  
		Size: 77.4 MB (77407114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1432d7867539a333040bd0beda5e76909b27321379cb77abc8e8e80db291ed`  
		Last Modified: Wed, 25 Feb 2026 01:49:02 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1978711e47930bbcd23357ea3afe73f946b4fba25b60955db3e66beb95b51a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b7c915ae55c735087fb816f1682a9369364cd3f65e744c14d0f6d4fb09dd0b`

```dockerfile
```

-	Layers:
	-	`sha256:7cda05a9cf4ce7d5ce50432cdb2a25e4381a2108d837a2cc387b4aa8c6cb6e9f`  
		Last Modified: Wed, 25 Feb 2026 01:49:03 GMT  
		Size: 5.4 MB (5383504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e5182528aa2cd88f67873ff1a63dd2bfd22609bdc19c8bee5069685649d61ad`  
		Last Modified: Wed, 25 Feb 2026 01:49:02 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json
