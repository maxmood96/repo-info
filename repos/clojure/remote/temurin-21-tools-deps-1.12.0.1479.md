## `clojure:temurin-21-tools-deps-1.12.0.1479`

```console
$ docker pull clojure@sha256:b094ebd70bf433ea82419a52cfc429e068f140b7dddc64bae4a5b948bbb3d2e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1479` - linux; amd64

```console
$ docker pull clojure@sha256:208e131a5317b7f5a02b88463cd4709a96c8955a8ddbd75818a8cc0607e42b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289063366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52cdfb1002da92599a1ab6b1c055aa11b6e8702e86ea99bec7d1ff40d6be0aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5bf511d386afafc6fea17dddf462d830c9957bb2229c2beca4baf7ce0fca0f4`  
		Last Modified: Fri, 27 Sep 2024 06:01:34 GMT  
		Size: 158.6 MB (158579257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb58b06016f40ab4e9624f1c1c0eb49948285a3e25b0159484a443e153e66e8a`  
		Last Modified: Fri, 27 Sep 2024 06:01:32 GMT  
		Size: 80.9 MB (80928020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319a4b361ced04f6f180d615dc4dbcdbff74aa2f503aae82402888b675b4cead`  
		Last Modified: Fri, 27 Sep 2024 06:01:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48aca2c271eb7fdb00d553b0e091de5c77b7d2129915c0bd8e63e1c70fafe0a`  
		Last Modified: Fri, 27 Sep 2024 06:01:29 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479` - unknown; unknown

```console
$ docker pull clojure@sha256:48d4f3826769b55e7d33497fcfb148d3769c3464ffd4b49ae1385adf8cd82935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7179187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41db52d5909e6be548d295d4054bb9141b237f7c550e2fccf9e5bd141f2f6e7`

```dockerfile
```

-	Layers:
	-	`sha256:825a417d87ae3b4c5536c6fdfd7304beed26bd5882e8374794b3f1e10a0bf79e`  
		Last Modified: Fri, 27 Sep 2024 06:01:30 GMT  
		Size: 7.2 MB (7161747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8c947abf7202dbda8cd6fbc8f1c261990a8326559a4de20baf6e2a741a253eb`  
		Last Modified: Fri, 27 Sep 2024 06:01:29 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1479` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:78594f859e82d1467b2d3bf9084be8f667d6758e480e0113d0bffc787a98a116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287122790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4943853f2e1a3d654da9496d080661af70a57f293a7fd2352d087861997ff9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd9444cc64ba812cb54dca0942a0244c0f9189074a2d336c3c083dfe9807dd3`  
		Last Modified: Tue, 17 Sep 2024 04:06:44 GMT  
		Size: 156.7 MB (156746196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5ca50fcb28b529baae287ac023c6bda09bb55d0bced16735cf47fb864f69a7`  
		Last Modified: Tue, 17 Sep 2024 04:47:00 GMT  
		Size: 80.8 MB (80789927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c109965bcc2585b7502311bfc5b9d154a07aafdb2a753f0483d45759e8d3152`  
		Last Modified: Tue, 17 Sep 2024 04:46:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2022caabf71a95f677505e630e4441340c84632ed86bbc0bb5b0187b8951d8b9`  
		Last Modified: Tue, 17 Sep 2024 04:46:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479` - unknown; unknown

```console
$ docker pull clojure@sha256:09dbd4b2b965be3045cce35118dfe0aab9ae31f6e64968e9d1b48d57be88fd63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7033504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f6b720739a5c278e84b52c1a562c2a72f079c33e9bfc1640265fce6eff7b9e`

```dockerfile
```

-	Layers:
	-	`sha256:78517b276bea992581a2508ea055792fbb84593e40c7ec559280892b91eb18ba`  
		Last Modified: Tue, 17 Sep 2024 04:46:58 GMT  
		Size: 7.0 MB (7015456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a64610d9e1f61afcc54a38fdcb72cfa27f5488884917460d6e70601bdcb27fa`  
		Last Modified: Tue, 17 Sep 2024 04:46:57 GMT  
		Size: 18.0 KB (18048 bytes)  
		MIME: application/vnd.in-toto+json
