## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:a2f3903796e259a0addad1c2e284d5986c48d776c5ba6b2d73fd3cbd325a7dba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:3d0de8ba4d64ce01db4ab645731ff76c6ab61a378f792ea29fa639ed8d41d6a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234095806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf0bfc4ea2046dab43b4b3e6fc5c00a02910231d03593c62e87916d84d2bfe0`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05b0f09e06b18cacd6ac15996c06091d7b742fc19f5c5e57fbc8d530a73d879`  
		Last Modified: Wed, 02 Oct 2024 03:56:24 GMT  
		Size: 103.6 MB (103611891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b723a5bd3b5dc01495e03ce09fd6841b820469f8ea13d368d885a22b8cb4efd0`  
		Last Modified: Wed, 02 Oct 2024 03:56:24 GMT  
		Size: 80.9 MB (80928220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e320366c0efce3307230abe279fcd0c0b752d892aab6082fd5b71f55c9ff6053`  
		Last Modified: Wed, 02 Oct 2024 03:56:23 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bb2db835271f53522fd571a33c408c54eb7039bc48599ecbf7b892d4d464c9e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7292668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8481c367c3db1ddccb46135fed58673942ae280c6457cb5124828bf3dd7cd14b`

```dockerfile
```

-	Layers:
	-	`sha256:cd5ea2822e40dee5e5e9e4ce8dafeae8213f42b8933f5c16d726102474226a20`  
		Last Modified: Wed, 02 Oct 2024 03:56:23 GMT  
		Size: 7.3 MB (7278812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2aa209ca6b3eac23bd684b4b7bf5a8869a4de21a728e247bf542fd1a1251ebc`  
		Last Modified: Wed, 02 Oct 2024 03:56:23 GMT  
		Size: 13.9 KB (13856 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cca6bb9c82b39ef274bc8456ab5d58810f482eb50f3eb966dd2730e71c63be04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233105119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1202cdbabf722ecf62c7123b2155ffe24733e0e3d87d92bfe1cef142a0ca2ab6`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cee2314f77650d7cb93045ab06a8beaf14aa8ff29be5cac8dd0a8b64aa77e7d`  
		Last Modified: Wed, 02 Oct 2024 05:24:27 GMT  
		Size: 102.7 MB (102729196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ac2bea371180a804309f8071a3cf363f201ae432e72eb28db88b9760e55630`  
		Last Modified: Wed, 02 Oct 2024 05:30:22 GMT  
		Size: 80.8 MB (80790394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a3b0dce862e25942015fba6f73978dc272cd80493073b68956afea4449d1cc`  
		Last Modified: Wed, 02 Oct 2024 05:30:20 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ffd2b4ac28a86f30166ca9f8f583bea8ac2a39d8c813a6f45edcb5dbf1ca8753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7299241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8658e2f10237f3edd374f60dc1ee98bf792c5dd6ea3c19868e36eb202c32c4ee`

```dockerfile
```

-	Layers:
	-	`sha256:f36c7878bff19822c97c17ff8db5015ecce8854023f7ba239eff1f4a99ba315b`  
		Last Modified: Wed, 02 Oct 2024 05:30:20 GMT  
		Size: 7.3 MB (7285279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4fa51f35bfc61c8b52e5370f654a8432d16e9d4ad2c899f0af2516f65a4c473`  
		Last Modified: Wed, 02 Oct 2024 05:30:20 GMT  
		Size: 14.0 KB (13962 bytes)  
		MIME: application/vnd.in-toto+json
