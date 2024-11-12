## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:a14a4481066e88721cfa12c852efc94799cc302b04a84293f6542598e6ec209f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ff60f5f5fc11bb6a3a02108ead5652c35748f89c748c10fdcc87c35363716b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193826347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35d10e944afbfe16b4098c032788cbf790634519938b9e1a0c458cd32c49504`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431ca0e90c0313dc6bffe0393dd5d7dcf7f141c9ea48f075560d1ffbcf1f5d75`  
		Last Modified: Tue, 12 Nov 2024 02:23:02 GMT  
		Size: 103.6 MB (103633935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2692235f4903bf3f9ef690319dd8534fc464b55e4471852f958a5ee975995fe4`  
		Last Modified: Tue, 12 Nov 2024 02:23:01 GMT  
		Size: 58.7 MB (58740207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f102d4f3dece76a981be22cc4efa814ed7ef680fb9bad9e4a6ea1478fe64d76`  
		Last Modified: Tue, 12 Nov 2024 02:23:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:34a16eef4d7b729ea3b742a93f34221a9739a2dbd1f69e8a6c0aae611214f291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5261818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1baadd3c20f952e55593062f07f9d3230d2c2330a3e035059140ecaa3a30d6`

```dockerfile
```

-	Layers:
	-	`sha256:5eaa3e64d6caf8e0e4c88df957d7dc3d2054acc2906ceab1fc4532eb32976ee2`  
		Last Modified: Tue, 12 Nov 2024 02:23:00 GMT  
		Size: 5.2 MB (5247522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99eb0e7ba12e845969584bd65e92e5bd90d87cab09066a6731db344d49181d9c`  
		Last Modified: Tue, 12 Nov 2024 02:23:00 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e5fbf4c6edcf3af554d924d121476e0ca3f8f14dd7d20e1277ced0db4ade119f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 MB (194121044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7554677f6fdafdde64d2d9f16ffebe79fb3b6c8f415b637510cd2cdec3708f6`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd56617999195b0ffb1dc67e741ecec316ed3d649a5eef28e4cd2edf9608af76`  
		Last Modified: Thu, 24 Oct 2024 08:54:34 GMT  
		Size: 102.7 MB (102747708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c435960262df43cf05e7f7a69e91a688f8b5f7a4c94b39453521af8247958018`  
		Last Modified: Thu, 24 Oct 2024 09:00:26 GMT  
		Size: 61.3 MB (61296936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa1ce581441f5c970efa30e4bd66e268aa8cd290b1420d4b6a561acce712db3`  
		Last Modified: Thu, 24 Oct 2024 09:00:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e1c15858e069959a8f4ed55620bf08fca2988197e2a318df3281129019be6c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5268164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93768c7959a3e4d0f30cb00eaa7d9490f8fb0d004f1ff7b970b0fa9010f74c9`

```dockerfile
```

-	Layers:
	-	`sha256:f6b30e4f632f24d5af5836df7619c075e3d0a21513a772c802f03e47131b2b5d`  
		Last Modified: Thu, 24 Oct 2024 09:00:25 GMT  
		Size: 5.3 MB (5253922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48099febf26c23e3f0605a85613e9ce1f2ace2d4064f1beef38354f3e1523a1`  
		Last Modified: Thu, 24 Oct 2024 09:00:24 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
