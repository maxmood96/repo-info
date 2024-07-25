## `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm`

```console
$ docker pull clojure@sha256:cfbe5e789ac997282f3498ff4348afb1be1036a0220c322f634de1589a861ae0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ac8b1be659b5085773a9f57ce2b2044cd7a27570520efef1c298508e3655a90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233680432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93444039d657412c41a598bee85790147c3da68770ad7ec8409908980b941151`
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
	-	`sha256:41fce9840073454d081dc02ef265d1a7f6908bb895b890034ebdfb5c528abd6e`  
		Last Modified: Thu, 25 Jul 2024 19:01:56 GMT  
		Size: 103.6 MB (103611901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887694b36813de837e5f3fca070812d154dbd8da5d7ce63d65e0a2db37192a4d`  
		Last Modified: Thu, 25 Jul 2024 19:01:57 GMT  
		Size: 80.5 MB (80513810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11be01d47336cbeef04230d57429b554b6b9235e278e63a0212a9340c123032f`  
		Last Modified: Thu, 25 Jul 2024 19:01:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7cafade29f87e5e33b0fd59c202afd0289fb3af23b7ebb4bef28eae1c904297f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7039429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc646c9c0618b3e3efdad0e0e8f4af30226cc5fbdb6fbdbebdfa40d2f4db2161`

```dockerfile
```

-	Layers:
	-	`sha256:1d0aa4cfa7f2b69785ed6390b9190d53138e38078e5fb18c0d5e356efd40123f`  
		Last Modified: Thu, 25 Jul 2024 19:01:56 GMT  
		Size: 7.0 MB (7025577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0f4374cbfbf2f10d2148b1febe09f3f8fc722c45d6a6ebbf1a75384b2e96316`  
		Last Modified: Thu, 25 Jul 2024 19:01:56 GMT  
		Size: 13.9 KB (13852 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:02354ca0448f5867ea1bdacb91463b6eea141fabef98e4d9df513888c65476f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232578217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f5d3ba6ef7a79116bdf8dce0115eb0392f589eb591dcb51785621b0fc04607`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
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
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1a56e08878ad85411f0e218bd104699f02c4529a70c0284bb23803e4bf6a92`  
		Last Modified: Thu, 25 Jul 2024 19:07:52 GMT  
		Size: 102.7 MB (102729199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e830dc170bc6647de6d8bae7861a9cd25be293184888d31f0ed658bf823c0c`  
		Last Modified: Thu, 25 Jul 2024 19:14:12 GMT  
		Size: 80.3 MB (80259932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a2cf295e70cbc883dce4da9d595d607811df53afb43d5497e68affb88f6292`  
		Last Modified: Thu, 25 Jul 2024 19:14:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:44f2bf227fdfa1b38092b860829a008edd2072f32c2868dbe914c99ba2baf12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7046351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd8bc67e6bccd8845d14c89a63b113ca4f11d531f5ae6a27eee6f0ad93a7d53`

```dockerfile
```

-	Layers:
	-	`sha256:92cd0d574b552a8658506183332d78cd5ebd65102569b52b124d5c83cae226d5`  
		Last Modified: Thu, 25 Jul 2024 19:14:09 GMT  
		Size: 7.0 MB (7031964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7195b13467e2071c23990bc40dd951fac08c898606bc1ce6da1ad6cf916b26ed`  
		Last Modified: Thu, 25 Jul 2024 19:14:09 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json
