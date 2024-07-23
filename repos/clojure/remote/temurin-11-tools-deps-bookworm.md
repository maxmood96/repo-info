## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:8ecd58d3ca1ef4c0521a405945cb645b1281941c047766ecf662e8817175ab32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7133e5515bf6a03534b9effade90cf514767a657b0e2f61873efd639edf2b6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275573518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6b213f31f2868a94aba0d8c8baf3a3799e7c03a10fd46a3273a278cc279260`
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
	-	`sha256:8d84056db697da37a3615b25ce1fbfd9907eed4795489c07225cfa03a6c76bf3`  
		Last Modified: Tue, 23 Jul 2024 07:13:54 GMT  
		Size: 145.5 MB (145504811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e17724f744f4cb6158d3f5ff4f8540aaace120a8b38a72c5057545c6bc46e5f`  
		Last Modified: Tue, 23 Jul 2024 07:13:53 GMT  
		Size: 80.5 MB (80513987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c764a58e5efaf9be35ee9170a22a178bbe71fbae66c9239ba2126a48380b3b2`  
		Last Modified: Tue, 23 Jul 2024 07:13:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c6190a54c5f295bbec42b2012260fe16f40cdd87a17d5c547c9c36ef9f3bbea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7013950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665301e45142fd0d02784e13eee6631939f35e33ec2e91c814d3871d770c34f9`

```dockerfile
```

-	Layers:
	-	`sha256:36594dbb83b6a3be9d1becb51929d6a188adf0a93fcf950d277dc8556cf6db2b`  
		Last Modified: Tue, 23 Jul 2024 07:13:52 GMT  
		Size: 7.0 MB (7000086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bf6da4b27f07f9195ed70122c49ffe8191edb24fbba8c4f2edd9d960981ece5`  
		Last Modified: Tue, 23 Jul 2024 07:13:52 GMT  
		Size: 13.9 KB (13864 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:901c9b64f92a5e261f1b84aed139b4f05ed350cab02e53c8b1ebceddd447a00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272152117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca319a47123aa3cce081ff749b456782387776c963fe11178694a4c8b21f82c`
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
	-	`sha256:8dffb1f75978ef43d292c0cb041c95f5715e5fc129376ba058729c266e853fdb`  
		Last Modified: Tue, 23 Jul 2024 12:16:01 GMT  
		Size: 142.3 MB (142304069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ad31fd32b70e29ad72b8f423941fc710b40326be64be22ba3470c939eb3960`  
		Last Modified: Tue, 23 Jul 2024 12:21:16 GMT  
		Size: 80.3 MB (80258963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f01391a071da5a0977dd1fff45b635e47ca72aa5c68a134c43c5c7c682be50e`  
		Last Modified: Tue, 23 Jul 2024 12:21:13 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:202ccf343677a1e3aea5ca3901161757c2953d78ac9fb8c340bc445068b29d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7020872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bb0924fe4ccd6d9ca66fc3c35252723c6f274178d2cdcbf2f08d05192f6eb1`

```dockerfile
```

-	Layers:
	-	`sha256:d9e0313995ea128962f16c47d0d61dcc5ea085b9d6691eaf0b95fdc0c0272d5f`  
		Last Modified: Tue, 23 Jul 2024 12:21:14 GMT  
		Size: 7.0 MB (7006473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0f19783953cf6e58f12b3563fa79adc1736aed95b3ba293d3349d1f4ef372c8`  
		Last Modified: Tue, 23 Jul 2024 12:21:13 GMT  
		Size: 14.4 KB (14399 bytes)  
		MIME: application/vnd.in-toto+json
