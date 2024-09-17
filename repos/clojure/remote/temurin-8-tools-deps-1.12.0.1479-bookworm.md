## `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm`

```console
$ docker pull clojure@sha256:5cce9dcfe298351cf804175ad375f9eba569a07932ae4db0611ca1a88313c52a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:aa52d06f5e0db888cff10b23b981e630d13d4c2277ebb928c651b921475eb6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234097851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa5cef0f0f66d62c11a74cb601e3af960bc2c372fda3d26897cd565b48789bc`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
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
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90df4a4e4a06bfd7c8d25e966dbe9f812aef03e096228f459a4dd84c94fce26f`  
		Last Modified: Tue, 17 Sep 2024 01:56:32 GMT  
		Size: 103.6 MB (103611919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba172b6f79e6087fd588ececeedb18a6cc94f170173c15d3a419eaf4081b67a`  
		Last Modified: Tue, 17 Sep 2024 01:56:32 GMT  
		Size: 80.9 MB (80928583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5956ff4bdb7859eab9c0d8903c464d6e18d904b876323ecfe34251fb1d9d87c`  
		Last Modified: Tue, 17 Sep 2024 01:56:31 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:261c8a920e614b2829254300dc6e39534b858ea1f9a8f9f5cf48e7c524ece111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7046330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9791a850fb9f28a2cf1b497dee6af405f357f4338aedeb29e258558b93e388f`

```dockerfile
```

-	Layers:
	-	`sha256:170d8245377e4b30b64c2f91f0cb2927a78ea116171e398f23c4d0c35181fbe1`  
		Last Modified: Tue, 17 Sep 2024 01:56:31 GMT  
		Size: 7.0 MB (7032478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:372069eb3a288d2d7452d89b63423721653613da4f9a3bb8a0ca5778e99d05c5`  
		Last Modified: Tue, 17 Sep 2024 01:56:31 GMT  
		Size: 13.9 KB (13852 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eec4a8c368e7ff3b9239cf80f1505fbbff1ced47465960885489d21a97f6f73a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233105291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3bc542e175ea9cca71e9a78c9deefef6fa1d005fc3f7a5a68fdf786a50c258`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
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
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22506feca16d1399f16de0c102b0b2250234c9f2d1ddfb76fc7c96b7f82fb0d2`  
		Last Modified: Tue, 17 Sep 2024 04:07:49 GMT  
		Size: 102.7 MB (102729254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d595ffd0d9e524356e1953b0d7c59adcce257a561dc3ba29825f17fb2e4871a7`  
		Last Modified: Tue, 17 Sep 2024 04:13:22 GMT  
		Size: 80.8 MB (80789766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764603c660e4b90df6155863b64c2a4ebe6f3adca4f199e0b5ad172bd689b0c7`  
		Last Modified: Tue, 17 Sep 2024 04:13:19 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:67086288f3fad7afd042a30b2a858afd02272bf059ab127450c364c2031ed182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7053252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a27bdcc16fcdcee992db42638f6792ac472ca52d25e37f554b312d84941b92d`

```dockerfile
```

-	Layers:
	-	`sha256:e913b0eb6cd8827dde362b78c4aa62f3cfea9f87491539b106960ffad9be85c0`  
		Last Modified: Tue, 17 Sep 2024 04:13:20 GMT  
		Size: 7.0 MB (7038865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:753a3eb9a4eb5520050f6de2336be6d20c0fd570bed4e1373e42180843ae6150`  
		Last Modified: Tue, 17 Sep 2024 04:13:19 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json
