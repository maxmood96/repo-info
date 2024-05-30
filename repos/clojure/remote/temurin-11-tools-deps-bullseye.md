## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:7f7b9acadcaaba73682af1a826c7c7a6a103a9cc03a17592750246d0b51ba314
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f1b63e827b574ac06f72bab50249930eefae5610b5c7ec266d63dd467fe23d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269421292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9f6e4c4dd2dbeb650ea06f8f9304aa605b25c78c16da4d25565a9ba5d99fd0`
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
	-	`sha256:19b36057bb4fe1b73e315df52d3becfa479c00dca1fb735459751fb10a1b7c55`  
		Last Modified: Wed, 29 May 2024 19:57:09 GMT  
		Size: 145.5 MB (145504827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf183e8c272679131f5d90146115164f329bd4cc3e1c0fc325552f336c814d3`  
		Last Modified: Wed, 29 May 2024 19:57:05 GMT  
		Size: 68.8 MB (68816417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f39fddff9ba16d1d6c1e6aa64363a6a2d6d80b044efa3e893b15d8f47902de`  
		Last Modified: Wed, 29 May 2024 19:57:05 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4d27560b2eeafbda02fe4a6455494c464c1546f128423306a9b5a90ae6eee1ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7013567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b567641afc1aca0b31fab6c840c33fe457dcdc6ecedd4ec78f98b72e71d0ae`

```dockerfile
```

-	Layers:
	-	`sha256:3a2525c8332bcd093fc0364412fcd6b4baddbb7fc7586406b5e82d8780c924b7`  
		Last Modified: Wed, 29 May 2024 19:57:05 GMT  
		Size: 7.0 MB (6999752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5216c45c6e9f93b3ce1fbd75ccce72fd97a5aac4d1a22a02772e7d4a2631d44`  
		Last Modified: Wed, 29 May 2024 19:57:05 GMT  
		Size: 13.8 KB (13815 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a172bf7af21885606a91b6f271831ce36338f3f9e89894349ed11ada135834ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (264973003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3e863f13f2b3f592bce0bc5d81851830760ca2e2bf50d1a4cfc1a5ee853547`
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
	-	`sha256:5180cdf83b9e6d688ff5d031db6a4009dc64691aa8d105945b1d8621f3656844`  
		Last Modified: Wed, 29 May 2024 20:37:28 GMT  
		Size: 142.3 MB (142304134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75fb8d721675133ccaf2a5d0585e96dc8ab1e791c1e57d8bdc0f96bf2892a78`  
		Last Modified: Wed, 29 May 2024 20:53:13 GMT  
		Size: 68.9 MB (68929233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0ade809f77e97da3a805209365676eeb43201d5b9c999e61ec519bab731f01`  
		Last Modified: Wed, 29 May 2024 20:53:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5ab36708e318c52a540ca83fc51dbd2dd0cf9d2c16ca1ed5143092f36a4a0be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8a26b4c3b328a144e970c7ce44de4d392e0a39952493c95f4c2d860dbb1d30`

```dockerfile
```

-	Layers:
	-	`sha256:6f89b19977252acab499482cbc36e809ed37909825eb87db397dea0e1c540fb7`  
		Last Modified: Wed, 29 May 2024 20:53:07 GMT  
		Size: 7.0 MB (7005474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a24723948cbf6994a3f31a81acb35e261583c9cff967c4854fa5f5a8b4fde8f9`  
		Last Modified: Wed, 29 May 2024 20:53:06 GMT  
		Size: 14.4 KB (14351 bytes)  
		MIME: application/vnd.in-toto+json
