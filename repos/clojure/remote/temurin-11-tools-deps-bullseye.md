## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:c6d9275ee533c3c3d0368f3dfbe3ffa36a6b223d4447472020ba0f138f08a089
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6c80eaf02f83374ba8b953d2daf8fd6f2b0d74106c2f00c1e087381092bd5c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.7 MB (269656824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38298412c6b7ebf8186c834e62987a2876b474ca607d659b951e92703f00830b`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
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
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a903a3015649e8f9405e6cc4b08bbe3d472ca979bee2c788217254690aa898d`  
		Last Modified: Wed, 24 Jul 2024 03:04:27 GMT  
		Size: 145.6 MB (145550361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac23098323c259f308d6ac814ab6304124da5b9675e1f9b9fd9b15f15950c15`  
		Last Modified: Wed, 24 Jul 2024 03:04:26 GMT  
		Size: 69.0 MB (69021240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b886664ce35cadc7b4a3b955d01401c996bbdc3ad75cfaa156b206fe29b0343`  
		Last Modified: Wed, 24 Jul 2024 03:04:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:10239c1fb0343782b713b6aec3e4a9b351429bd1a880baf0e5f01461a4eaa28c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7054209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8c8e7bb35ef5187eb22e92a6ae6d2547d5f2cf6572711841008cee0619a0fe`

```dockerfile
```

-	Layers:
	-	`sha256:7447f0cec6f1555aa60dea3f5649f611b7c8b41434c04bed73b092a202deb877`  
		Last Modified: Wed, 24 Jul 2024 03:04:25 GMT  
		Size: 7.0 MB (7040344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca432292488cb68722e4e2d3c1a945637d27d476a14edaa4b287aee920d3745a`  
		Last Modified: Wed, 24 Jul 2024 03:04:25 GMT  
		Size: 13.9 KB (13865 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fefc01b1c8259f176be71a93db6d9eed4f882cf413f1582705b0080b29247d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265160293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c9c09ad5923d9b0a1a719f4a5f69ab1686ab4df2217347d702cbe084e75d71`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
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
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee87c36e87bb3bdbfe082f567adba704b3a12faa5430ffe9012e55d9f8698f90`  
		Last Modified: Tue, 02 Jul 2024 09:20:56 GMT  
		Size: 142.3 MB (142304047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f743b735815ca7e3de5a15fbabaaecacc8e2969f3af01b29476b634d9771a7`  
		Last Modified: Tue, 02 Jul 2024 09:25:42 GMT  
		Size: 69.1 MB (69133947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05e9bee2a519da0d5f2d4768491b2101a53ba5b804a1c8fa388f4fa2a0b88eb`  
		Last Modified: Tue, 02 Jul 2024 09:25:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5a0e5c5d93fcdef5342a1a5bc5e2b2987db5040f7f89bd10a9292781402c226b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90ea7396d21ac2ea2d6b2b82b6842c7cffa2e147e233480aaa4cf610c705591`

```dockerfile
```

-	Layers:
	-	`sha256:007984f80de6f1173b7e3cf35d399a1e6c0c6c01b26cf5a418c7612e9596c672`  
		Last Modified: Tue, 02 Jul 2024 09:25:41 GMT  
		Size: 7.0 MB (7005512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3197f1397e7b58206d417bf1858ea5de5902cf188cbb1ae4709a9ab56cdf773`  
		Last Modified: Tue, 02 Jul 2024 09:25:40 GMT  
		Size: 14.4 KB (14400 bytes)  
		MIME: application/vnd.in-toto+json
