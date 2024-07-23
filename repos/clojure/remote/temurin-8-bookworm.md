## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:17159e8a604b67b9fd0db108ce3e7e91a12b61be992ce2119f473544cafd60d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:6f526f80e4326ec9bee4761701f996ae744b05aaeff63651f8a9bf89c99e1624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233668936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a097580cd4372bb08872931b387c1b32764b352c825546ce17327a244090d40`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e232bbb243b670c69a521bf9ac6863cd531830bd42eaa97a11f021f6fb8c70`  
		Last Modified: Tue, 23 Jul 2024 07:14:21 GMT  
		Size: 103.6 MB (103600191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4781f19c24d6069379d82779db3568084949a97e1543d27e91e44852deb2ca`  
		Last Modified: Tue, 23 Jul 2024 07:14:21 GMT  
		Size: 80.5 MB (80514026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e183bbc5b0336d7499454187f0c22f56596095838922989469ecc0860a8c18`  
		Last Modified: Tue, 23 Jul 2024 07:14:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4b27dabbbac956963394d8eda3c604e9ac8220e024069c8b44ebaa5116832aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7039427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01dbbe36484cad44d6733fb800a7982925fb5917e26a1fdf644e941eb442d13`

```dockerfile
```

-	Layers:
	-	`sha256:76a8f5b5fe223eaab262d684f39f039b63ebc1f62fc1db267d144174b66f50fb`  
		Last Modified: Tue, 23 Jul 2024 07:14:18 GMT  
		Size: 7.0 MB (7025577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e04132557678664e3b57fa17fedb84bc41809ba34e7c202ec5a9edfbec4d970`  
		Last Modified: Tue, 23 Jul 2024 07:14:18 GMT  
		Size: 13.8 KB (13850 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:df56d84a557d69f1a36884881eee88bdf0e819e5941f4312c1e4c1db7a585254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232551564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35774b0a1ac6a674de269e1b070221961dd99c1c1730436582163d8bc7fe4076`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
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
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014b70c67983f97bfa73aa56a5bfb6b7a6e0d5e40844a9d2eb5f3d69651352d7`  
		Last Modified: Tue, 02 Jul 2024 09:11:04 GMT  
		Size: 102.7 MB (102700441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69a555b8b3c5ad784d94701ed5669fe20f4c744deda4a86c9827069d55d6a50`  
		Last Modified: Tue, 02 Jul 2024 09:15:07 GMT  
		Size: 80.3 MB (80262031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e22ce5273cf9cfa9d3c1c71929093c23ee446070d35e862049389e1a2b3618e`  
		Last Modified: Tue, 02 Jul 2024 09:15:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b23673cd924348b822a97241d3cf99ebbd6d9d0b32aa40bc1a1aec2ca8d98043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7003222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3523a260ecadcdd858b753571d9fc1730acfb70a02b0be15ab7ec089f9e712`

```dockerfile
```

-	Layers:
	-	`sha256:5f36a9e05147d43eefa101cdd3f3d9dbe54f61347c37c14fae76578b1953aa77`  
		Last Modified: Tue, 02 Jul 2024 09:15:05 GMT  
		Size: 7.0 MB (6988836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a81de52a2ae50218858be933f48707f03afef506b1bfc2d5301b88d0b23b54`  
		Last Modified: Tue, 02 Jul 2024 09:15:04 GMT  
		Size: 14.4 KB (14386 bytes)  
		MIME: application/vnd.in-toto+json
