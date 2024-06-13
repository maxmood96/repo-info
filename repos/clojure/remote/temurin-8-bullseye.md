## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:bd217be05688e95144bde28df7ffb01b9c850e40eaff616a1e069bb491d285b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f5a8dad64a17e9a35ec0ad457da7dc84d646b540e2f89441b8c41d63e25b3dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227516041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f7efebe1bcef52c8ec3973c24253338db767478fc16eb211889db3d51d8195`
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
	-	`sha256:f013f6a0c5ec47134ce0155c8d45534deaf1023ba7c58358e3e7e39b245056dc`  
		Last Modified: Wed, 05 Jun 2024 06:10:13 GMT  
		Size: 103.6 MB (103600201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e800ebe45a6b7c734a16bb3bf90c47557a756f57f5aaa6ed02259252e709cdf`  
		Last Modified: Wed, 05 Jun 2024 06:10:12 GMT  
		Size: 68.8 MB (68815792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182e23e77733d2115c97fd9ccf1629a8b01ea21ded0933f21e21d9cfb0cce0f1`  
		Last Modified: Wed, 05 Jun 2024 06:10:10 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0c083cea0f09d145adcf879d282e407e84cbd8a71e074d497b98c72a1d98666b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7036041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b276e1dd6f57934f0b80675ca23e0ad8c5f7403eb9fff0ab1110a3a7a94dd45`

```dockerfile
```

-	Layers:
	-	`sha256:ae8eeeb4d9087ab830a98fb5bfed2a5255b3eeaf9b7732dcadf3e9c8389b1d3f`  
		Last Modified: Wed, 05 Jun 2024 06:10:11 GMT  
		Size: 7.0 MB (7022239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85569d455b7e3af13e9ea2e06ad5350a1be22fbc185886a95a502c4af04c0ed3`  
		Last Modified: Wed, 05 Jun 2024 06:10:10 GMT  
		Size: 13.8 KB (13802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cfcfb23a8d728d89449201d5d9ce1a34e7e6b8261e94f9cb14955a93c7787335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.4 MB (225369819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea7a8f2e5bf04b38e9206733c6e6b216fea06db1dfb8025bb1f7dc75476e527`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Tue, 28 May 2024 15:17:11 GMT
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
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63aa4caacc3a1e1326d77d86134d7ff7c6a2d2448547ed3ea79282943e9bf562`  
		Last Modified: Thu, 13 Jun 2024 11:22:13 GMT  
		Size: 102.7 MB (102700428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4eeb2b4efcec690c350c7e3bee6d51b3ace6fb6ac81b1a3de4be97994e738c`  
		Last Modified: Thu, 13 Jun 2024 11:26:40 GMT  
		Size: 68.9 MB (68929162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa32573f55e5178cfcd6f2c73ff2be5511a2413be9839f25f2f1056fd10737a0`  
		Last Modified: Thu, 13 Jun 2024 11:26:38 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:dad028556975055dd46cb41b1551937adbe71269717eb9a8af2d09fa4bce6785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7042347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8c201b335c88868996eb33189f778502c3f420a016f08c354b83290b22bad5`

```dockerfile
```

-	Layers:
	-	`sha256:6f6e0cde1525227b4bdf5c94a5fdeb9f79ad3914684ec33497ca5ed3e5ecb157`  
		Last Modified: Thu, 13 Jun 2024 11:26:38 GMT  
		Size: 7.0 MB (7027961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d17b0fe84b37e49ea32b1156e0b5d6a3099223b2d18a4c08d4d1460d41ed3d2f`  
		Last Modified: Thu, 13 Jun 2024 11:26:38 GMT  
		Size: 14.4 KB (14386 bytes)  
		MIME: application/vnd.in-toto+json
