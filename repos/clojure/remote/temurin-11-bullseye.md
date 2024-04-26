## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:50ca2177f40b60861c7173bb8cf5cdf133956dab566fc61e66b232416f6a05c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:49167f0bab19b0312e3b68b1af8e9cbc0ba7520ca2550b5095e89515446b8bdb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269627679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ad8eb73242f2387932b2fcc515d70075b7927ca097af9ba2339d5810d5e562`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Apr 2024 04:44:07 GMT
COPY dir:e23ce7557a2e7bee9271385ae1512d655314258ebf585995b794db69e6e3d8aa in /opt/java/openjdk 
# Fri, 26 Apr 2024 04:44:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 04:46:42 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Fri, 26 Apr 2024 04:46:42 GMT
WORKDIR /tmp
# Fri, 26 Apr 2024 04:47:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Fri, 26 Apr 2024 04:47:03 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 26 Apr 2024 04:47:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4427caf927495e62e89f897690044d4bf78001b43414f226c88d479c035c69a`  
		Last Modified: Fri, 26 Apr 2024 04:58:53 GMT  
		Size: 145.5 MB (145504625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd562b77cc8a43bf5c22032fa31bea22febc73468578ca5c07ed2b29164a51d4`  
		Last Modified: Fri, 26 Apr 2024 05:00:29 GMT  
		Size: 69.0 MB (69023564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21eb7fafa16a6df080f9663979445eb23af090aa65b37f970d37413facaec8d1`  
		Last Modified: Fri, 26 Apr 2024 05:00:22 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8c8751c397f949a2a890bad4e22b4667d4c25fe7841f945beb670a45a1d02a82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265188295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21664262c11713ae0ab0eb9b81ae0b3f9fe0299fd3fdcbc1279c7fec974b531`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Apr 2024 01:26:44 GMT
COPY dir:c78738cfcdd58dc875cb3f022a49b10c7fb9df08ee8a9995710ddf9cd16d96a3 in /opt/java/openjdk 
# Fri, 26 Apr 2024 01:26:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 01:28:55 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Fri, 26 Apr 2024 01:28:55 GMT
WORKDIR /tmp
# Fri, 26 Apr 2024 01:29:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Fri, 26 Apr 2024 01:29:13 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 26 Apr 2024 01:29:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2379b596d29c4a48c7ba2b4784c6d0898b32073be72fa219ab0f0f5637a4815b`  
		Last Modified: Fri, 26 Apr 2024 01:39:07 GMT  
		Size: 142.3 MB (142306371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d237890cfde8bee753a6832e333408aac0e1d1a4995e5fcfa3a67b54c65e58e`  
		Last Modified: Fri, 26 Apr 2024 01:40:39 GMT  
		Size: 69.1 MB (69141347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3c6599cd561ef5d5c3de3be1e1462f5526fff83f49d0c3a7cdba081bbc0283`  
		Last Modified: Fri, 26 Apr 2024 01:40:31 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
