## `clojure:temurin-22-bullseye-slim`

```console
$ docker pull clojure@sha256:f1fe99e951f5a3f35556787f5347f4e931dd6a06b52d91dbd0816537cacc3625
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:68a516d66317d7294a1a8842dcbc2ed537a0578e3eb8f66ce19495ecaf06ece2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246535169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508e444de10280d0131b57ca40dc877b582b5857899db67e5c082785f752aaac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec36eb3032d0fc48ab966398bcb29784830a89b620e50e63231f0efe66f84aa7`  
		Last Modified: Thu, 25 Jul 2024 19:05:49 GMT  
		Size: 156.5 MB (156481593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c03a5a3249d16f06b870405555bee1466f7b5d00cb92870f1d0a993ba521ca8`  
		Last Modified: Thu, 25 Jul 2024 19:05:48 GMT  
		Size: 58.6 MB (58624202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322e81228af6278df617419424ab4c28f265b75001ff18b82049ae439df9852f`  
		Last Modified: Thu, 25 Jul 2024 19:05:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa30c30b8ec18d004365842b6388c67f78469a0c76017fb352f3cb4dd631b362`  
		Last Modified: Thu, 25 Jul 2024 19:05:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:654a477d07bcd8c86ed86c13e9eb177842b3043e6378f6af2bf45a1b63ec0f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4965333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8725442c5ddf03ed274bf90392f36e35911def7cf1a7f4e1e4c3dadd3599154c`

```dockerfile
```

-	Layers:
	-	`sha256:8bdd084c5052079641f8e40a506488063b032442cd882b9a6a3b34ac6e867fe4`  
		Last Modified: Thu, 25 Jul 2024 19:05:47 GMT  
		Size: 4.9 MB (4949820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e9615c1c8cd4bae70ddd922f626e176b1606324abde598dc7e92a26386b0da9`  
		Last Modified: Thu, 25 Jul 2024 19:05:47 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1af719c073d33578e5bfff327a05bc629bb1d1570b12939a28927ea808b79706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243324743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b997205035d92d7170d8b883c97c98c8e73df9a71405d4094e4a192cb4416b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17f7259615f2b4da0ef3be88a82b06bb1d532b4794f2546bb169903c80c5c0d`  
		Last Modified: Wed, 24 Jul 2024 11:39:07 GMT  
		Size: 154.5 MB (154503703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f58381209588be05ed54bb47ac21e70843a295b40f6fca0891771780527fb5e`  
		Last Modified: Wed, 24 Jul 2024 11:43:16 GMT  
		Size: 58.7 MB (58743914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dced6eab9c22d3c4cf96b53686cc07c1e35e16c23f89709199db87f25d3f110`  
		Last Modified: Wed, 24 Jul 2024 11:43:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c58e1b78928d2f8764dea254146caf19d7aad25e15c40a3c05d02ad4dbfd42`  
		Last Modified: Wed, 24 Jul 2024 11:43:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:34b1b07c2c7223ded1805cb1d6ed542d59ed62221ce44425fa57084f215c0220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4971399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa70ca2d3299e85063f369ac62c517222db8a8a96d1b01becb1081e02edff2a`

```dockerfile
```

-	Layers:
	-	`sha256:9e13a19057b4570ccc23535c76fb69dd5dfd774db1944bd4554501052db3a402`  
		Last Modified: Wed, 24 Jul 2024 11:43:13 GMT  
		Size: 5.0 MB (4956176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2990721d8c0ba9ec7560c4e2ede0729e818cc6cfdce829b7f621a88fb0f73656`  
		Last Modified: Wed, 24 Jul 2024 11:43:12 GMT  
		Size: 15.2 KB (15223 bytes)  
		MIME: application/vnd.in-toto+json
