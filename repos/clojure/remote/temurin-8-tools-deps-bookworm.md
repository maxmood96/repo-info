## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:e3edf60248663353f8814ac59f73bcf16b64d86adb9484fb46f638c6515d6304
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:c8610dff2d2c67efb2757ef7ff0f9ec2edcd768eee405b9845f821295f856758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233666108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b029720469f8a86f847c122484051ca784bc5740a23f91cac818a1b33bb89c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
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
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4866ba19e9c11f2424962795d506073e117a5c2ed6ead2512222b850b13b12`  
		Last Modified: Tue, 02 Jul 2024 07:06:52 GMT  
		Size: 103.6 MB (103600229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cb0929bf09eefb15319051e5b3e4c5f424c5d948341ae6ae6971e13ae15b99`  
		Last Modified: Tue, 02 Jul 2024 07:06:51 GMT  
		Size: 80.5 MB (80511171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d4d41db000299d23c3a0dc031cb7ea60cf584c3786bf408b879fb9fe95c27f`  
		Last Modified: Tue, 02 Jul 2024 07:06:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b099c7533554d3c527d222e37663767f66be36572143d186cdb7d703de5bcfcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6996300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8cf2a6400b74e20221b611d046f1f53c9337036f5bef2502f4b60b254b6e81d`

```dockerfile
```

-	Layers:
	-	`sha256:f74eb1c2bb32ff90d16d933c2b22515f5b60bca1a5442a4ed3b02ca013ace366`  
		Last Modified: Tue, 02 Jul 2024 07:06:50 GMT  
		Size: 7.0 MB (6982449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c4c1ed4a759f224fa87e89323983334f7b470181786de31af23d18e2e4cb526`  
		Last Modified: Tue, 02 Jul 2024 07:06:50 GMT  
		Size: 13.9 KB (13851 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

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
