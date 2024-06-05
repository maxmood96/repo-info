## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:76f278c82ab7b133ad9a826ea95b7cc1b0c787a7fd7cf2c9a80a45e3afe2fdc2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3b2be7257a33e929775d1d061253a09a4335ba536e2f4d63832e4d6b6df7f6dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193454417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a55fd2e0a651225cba2d468ead1aece892bac9355e9476cb61f87eceaddabf1`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e12b95760a35d4c76eb751b062abf0b3ccbf8b606b9738ddb8a69aac67628e`  
		Last Modified: Wed, 05 Jun 2024 06:10:07 GMT  
		Size: 103.6 MB (103600201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6309a6be53354ca4b8eb42a27e631016d7254cd6f3d632be508409e65ec2bd77`  
		Last Modified: Wed, 05 Jun 2024 06:10:07 GMT  
		Size: 58.4 MB (58419636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214b2aed85635ec0caeb291b113a0ef7d123faaa15ff57fd04e9f4566225b818`  
		Last Modified: Wed, 05 Jun 2024 06:10:06 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6c8c1c2053c3c755774a570002ee069c9fab439ed7b8e263c1f18db41fd5e850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4945591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5746e5dbcebfc0bb6b4edaccd054e53d2792cd9e40559aac67725ddd4dd8ec18`

```dockerfile
```

-	Layers:
	-	`sha256:765c51b7556e9c9c49855a9cf3faa1c92de9aa14df2ab4d2c0069e148d583791`  
		Last Modified: Wed, 05 Jun 2024 06:10:06 GMT  
		Size: 4.9 MB (4931721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec4c2d444c2326198af864d044dd619f1165ba2e65faf7e61b169d1143c4245b`  
		Last Modified: Wed, 05 Jun 2024 06:10:06 GMT  
		Size: 13.9 KB (13870 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0c1586e5bbd565e4acbcbde099919cbaae34e274598a95cf1f7d1572b33b14f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191328039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cae886fd160423780d569733292248d240e0436e06eee17e1d70eca59afc989`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e546727f5b9ded0de7ef1070d114e444458b69f242bb195ae7941bc15b2b68c`  
		Last Modified: Wed, 05 Jun 2024 13:34:05 GMT  
		Size: 102.7 MB (102700399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de437f87829a11d0d62921139efa95c07ac08585f125c8ae513d370bbc9065f6`  
		Last Modified: Wed, 05 Jun 2024 13:38:56 GMT  
		Size: 58.5 MB (58540084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7df307392bdfe6a76390c75ba779017f2c3f57e92fefdeeb558fa51b61e0dc`  
		Last Modified: Wed, 05 Jun 2024 13:38:54 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7c6bb02506f7e6948355b75117ef7b25a783bcba56ed80a23570711a82717156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4952488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57644879a7d279fae726661fee58728815a274612875c9e58734871ad57ac6f3`

```dockerfile
```

-	Layers:
	-	`sha256:19472621f077b6ea047d99b7860ceadcf370ae4a7f90beab3c5d45e958d51dfc`  
		Last Modified: Wed, 05 Jun 2024 13:38:55 GMT  
		Size: 4.9 MB (4938077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf28a6092e185517cd9efdd153f1da8ccfaf2eec890839e2c67a8b3f545fc92`  
		Last Modified: Wed, 05 Jun 2024 13:38:54 GMT  
		Size: 14.4 KB (14411 bytes)  
		MIME: application/vnd.in-toto+json
