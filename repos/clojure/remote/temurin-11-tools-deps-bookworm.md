## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:cc2c145989f3aca755afa02b92025d9310efa9da337bdb0a7cea0d059f90339d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:2544e1f29d1fc6b7041380bc6cfc6ea3bd3f8b2956bfc9fbb532c101993d7fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.0 MB (276033670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3464858e438981db96b44e2542065d76bcfff55734acb09c3d89e14ca6cabc2d`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33de332e00db79111aa999e46daf2676e5051eea6b3b563d0ebe87b03d7c6499`  
		Last Modified: Sat, 12 Oct 2024 00:53:46 GMT  
		Size: 145.5 MB (145549901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a54b14775caeb5f4f557926a51530445ed0c0df61ca26121e80f55dfd139b2`  
		Last Modified: Sat, 12 Oct 2024 00:53:45 GMT  
		Size: 80.9 MB (80928072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad440539d3c31ff21151a4689f1e7fdd7d0df0d2885f5c5e75208e1e8fc9673`  
		Last Modified: Sat, 12 Oct 2024 00:53:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:127fd8d5e8c814a39ed9b1dfeeb10da3f02c0a9b52d4120eb505d66317403b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7190716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:309c535a55b62dce07e11acbb7d4933e92471c3941b4578e503a7c1049e1eaea`

```dockerfile
```

-	Layers:
	-	`sha256:5b3d606fb8b5032f1f0d8d453453439bb98836580fd36cc3aab4ec464f926378`  
		Last Modified: Sat, 12 Oct 2024 00:53:44 GMT  
		Size: 7.2 MB (7176813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05bb5aff714afd8ae0001239ad9078648ed1d5f9137468df5115a6172baf92fe`  
		Last Modified: Sat, 12 Oct 2024 00:53:44 GMT  
		Size: 13.9 KB (13903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:04b1ca53c59ab1b8ef6592b42c4a21c21833cb011ea93d2d250cb0b3d0bd034d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272730957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176226c50a226c0c24a0d8b17a593a9bbad5dbbe80ea2c3123bbe5c4c95320e8`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d3571e8e8b3365e3661280c35c39d9d5732c8993112a36c1d6295c234a2718`  
		Last Modified: Sat, 12 Oct 2024 01:04:52 GMT  
		Size: 142.4 MB (142355044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c47002692074d312c3579e180960b22aa2d0c5d62061f714f79ef2aaeace43d`  
		Last Modified: Sat, 12 Oct 2024 01:09:30 GMT  
		Size: 80.8 MB (80790380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a840bbd33fc01958e839328aa42c0434afa9c4669ba781fe40a037899f4676ba`  
		Last Modified: Sat, 12 Oct 2024 01:09:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:19a46469df21c3b2814342f0290d42ae8c0e45c74700fe5ff6d1acbd98508c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7197208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15fd2570d3d7cd8a09d51f239398c815f1f732f9c41ef2efba726e4f7083ee04`

```dockerfile
```

-	Layers:
	-	`sha256:4ec709bcb35f06afafedbfdcab260d991be314ecb8a0bd0d1af8a8496837baa7`  
		Last Modified: Sat, 12 Oct 2024 01:09:28 GMT  
		Size: 7.2 MB (7183200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:442dd04030c776cd6346070db256cac3caf87c48033c0d68defdc52262d962a4`  
		Last Modified: Sat, 12 Oct 2024 01:09:27 GMT  
		Size: 14.0 KB (14008 bytes)  
		MIME: application/vnd.in-toto+json
