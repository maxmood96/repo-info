## `clojure:temurin-21-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:c2c9c91490011c24682b00d2b86cacb15e51304f4c2f14ace75a7b2c405a0fdc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:661351a2a6db633ec57e00d9b7cd00d3154f108c1216728c68813beac2c89485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289065450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b210411e02b18a66fb53365098a503aeca2a532958b90935c979ea7affb7ce5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5d1b112766dce8be8fea91336d5de0fd6f1f9c5873e936e712cd27863dd684`  
		Last Modified: Tue, 17 Sep 2024 01:57:09 GMT  
		Size: 158.6 MB (158579294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49562f0a8084f94eb33c51919cfad673e9bf3828fb663461a0fe53e1d9375a0`  
		Last Modified: Tue, 17 Sep 2024 01:57:07 GMT  
		Size: 80.9 MB (80928408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76f48827fd5b6c365a16ceddae6521bb01ccf5eb5351b3a13786be68daab4a5`  
		Last Modified: Tue, 17 Sep 2024 01:57:05 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abbeca2ab0f7e0dff3f64bafdd1e664cd25e5a170d053264948ff751bdf11ec`  
		Last Modified: Tue, 17 Sep 2024 01:57:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f6c29166bfec1c1e3af20cfb8a118ff0a400ca214dc7029fbcb74ebd2961ddbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7026436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576c5fc734795bc12a28012fa258dcbe73b474302f68c2e1395088eb6a18a670`

```dockerfile
```

-	Layers:
	-	`sha256:5c7213a33817c4f0423543bbd44c8ab392705328aedff45b0287a9d1d82c0a90`  
		Last Modified: Tue, 17 Sep 2024 01:57:05 GMT  
		Size: 7.0 MB (7008997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70a3037cf2b67b8b41ea0e482c94ebb8b6b1357d2fd51c1b9752e303b463067f`  
		Last Modified: Tue, 17 Sep 2024 01:57:05 GMT  
		Size: 17.4 KB (17439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

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
