## `clojure:temurin-8-tools-deps-1.11.3.1456-bullseye`

```console
$ docker pull clojure@sha256:04bb3fd2d219f37b94d228ef2bcaf8ecdc54a6bd52437ed15a7f2a50feea2810
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.11.3.1456-bullseye` - linux; amd64

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

### `clojure:temurin-8-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

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

### `clojure:temurin-8-tools-deps-1.11.3.1456-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e9c2cf1b2a14ddc8fbe412e3ae03145826fbd9338175223f8b494e19fafc4a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.4 MB (225369516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3447ca7241d84f1866983976fe4f37283171b1e4f689015a97a239ca30c2923f`
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
	-	`sha256:7dcc37bae6a1dc6c0c9626d3bfd2d90ee8c71cdd46d65f0e9956b0b109b2f6f6`  
		Last Modified: Wed, 05 Jun 2024 13:33:15 GMT  
		Size: 102.7 MB (102700399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43322799f5e265527e2d7f79345ffe6e7eeec776b9537af66837176031c299e`  
		Last Modified: Wed, 05 Jun 2024 13:38:12 GMT  
		Size: 68.9 MB (68929478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6f4af0301ff135461d725b1dbbc3840927b9ab41e30141051aa18cc9b8f77e`  
		Last Modified: Wed, 05 Jun 2024 13:38:10 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ba8442a999ae8e86d48cf5593454c5cf07a1575aff489610109f64685a630915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7042298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f89ab23ef55969957f644cbd900721ecb61251203a9a9c9328315cce83c075`

```dockerfile
```

-	Layers:
	-	`sha256:eabcc91c0f3c9d8dbe537628dcddb6533fa087afa0a8ad540cf8b242176996ea`  
		Last Modified: Wed, 05 Jun 2024 13:38:10 GMT  
		Size: 7.0 MB (7027961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7570fb03d3491870d3a96179596baec008574d65421384c754129cbd2692d4`  
		Last Modified: Wed, 05 Jun 2024 13:38:10 GMT  
		Size: 14.3 KB (14337 bytes)  
		MIME: application/vnd.in-toto+json
