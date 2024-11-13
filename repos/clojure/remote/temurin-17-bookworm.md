## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:7975745b13bb2c3f21591f7045892b4654515286525054a9e0d817200bd081a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:30cc9042cf30bf0f338f5a11eb20f9d5788b04b9d00260fcdf7a710db0ad1647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (275049801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054e9646d267b2333d0dca11defe2e0f0a1e5a2b05f2d5474b68131cd2399282`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61a889d840f7bfb98e4ea4c7cf62a1896212502c6fe93f75580d40c3ed6b4b6`  
		Last Modified: Tue, 12 Nov 2024 02:24:14 GMT  
		Size: 144.5 MB (144534744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f30d37bd605978f8d583b610d5b80a9b9738d5de6e77b28530d9d20110ab6e5`  
		Last Modified: Tue, 12 Nov 2024 02:24:12 GMT  
		Size: 80.9 MB (80938325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dcdefbd4708efa19aeffa0083e8941e69ab0fc2898db57535271974a1e67ea`  
		Last Modified: Tue, 12 Nov 2024 02:24:10 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4e4f8322cd0829a881c336faa3290a66c541a7100bef94ca6ba44bcef11e0a`  
		Last Modified: Tue, 12 Nov 2024 02:24:10 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:49ecc6d8c85b61582fe866239df6f81f694b08ed6ec43a4a09e8dac9506b7efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7198243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a4aacbf92a9134b67a7903d25a77556a28d717be500a73812b3667193db244`

```dockerfile
```

-	Layers:
	-	`sha256:f638bc63f3e9958789142d4c14d432650b42c0ff7308e799024d7fe7be3bcb2d`  
		Last Modified: Tue, 12 Nov 2024 02:24:10 GMT  
		Size: 7.2 MB (7182423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d57c28ddbeeedd3728c7b737dbb5521c48011cff587968257dc7c64ecb4c066c`  
		Last Modified: Tue, 12 Nov 2024 02:24:10 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8eca09a5ab620b67b2db3c2d4aa8c463de5d96a0da6dddda4c2053c5c128a674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.7 MB (273747227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb87d9b43e95c4b6655a9da0db75e287888cca5458b176c60fb9eddf52d438de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1816c3db93a74e6521bb886432625b8422c73bc5fb6f01e58c6137bc5e733bdc`  
		Last Modified: Wed, 13 Nov 2024 01:17:29 GMT  
		Size: 143.4 MB (143361035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd033e39ff74fd2bbabc9a7290a01c7cb1bf5c636d1accd89c58b0f120e898b6`  
		Last Modified: Wed, 13 Nov 2024 01:21:44 GMT  
		Size: 80.8 MB (80797950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc18575ad497b30836a17a849b00c6f16423af73680e28a5fed0cb426ce523f`  
		Last Modified: Wed, 13 Nov 2024 01:21:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8839070e953882b700bbc6105deaf5e6a31cadcca26fb9a011e4dd03ac008fc`  
		Last Modified: Wed, 13 Nov 2024 01:21:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e83d24f64e0f2f383a4bc6fbcf6b749c2633e7f43dada5d9e2b7f4216833ac5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2279725a4fa10bf765555cf24b6b6f013acc6303e4d3b4f07a44b26a4b03840`

```dockerfile
```

-	Layers:
	-	`sha256:64085c80be3064f293c43265b34070fac495534ab248d30854ea1d08b66477cf`  
		Last Modified: Wed, 13 Nov 2024 01:21:42 GMT  
		Size: 7.2 MB (7188191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfa3e54cb4eccc25a3c69607ec800ec6379222079b6546a65413cc2a2fc898c4`  
		Last Modified: Wed, 13 Nov 2024 01:21:42 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
