## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:165aaf74d87d0716b5755f7c2b3bc1ba8d71c25ead95a4d4bf3231a746d91086
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dd16540f9f44b9da90d9e1b242331d7e389ebd934d6375ef3435a058890b1027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243126706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4008777eb23f491ee6a91ea987e86656a092cad6923f819cbe0c7a168b53b9`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1df056f7597fe0be8a080d930c01500600d25a2c551a9b1f7299d8615fad5f`  
		Last Modified: Tue, 24 Dec 2024 22:38:01 GMT  
		Size: 145.6 MB (145601503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157fbe74ba4dfb51e526009414b405f606993d922bac74b9dcb69b48d78ab3f0`  
		Size: 69.3 MB (69292977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd9ec7d2e14c3acd4819e954a35564c2de168dcca33cc792de382bfda20688a`  
		Last Modified: Tue, 24 Dec 2024 22:37:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0e71dc2dd3b878dbd439776258ee88b6ce686118cfe0f08296e78eba3a101d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4946956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db788a11ed11d205b6c2cdd084ebc7db15211ca91bc5bae8636c56f81546689f`

```dockerfile
```

-	Layers:
	-	`sha256:9dc55e1e8c446e664139879bd8ec60a1a2ca4a807849aa9db5f749e27e3d72f0`  
		Last Modified: Tue, 24 Dec 2024 22:37:58 GMT  
		Size: 4.9 MB (4932646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c149351972106576220fd31491e9a30e7fed9c9eb02cb8b411cfa4bc175e9307`  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:75356c64f3f47e0f141ee8fbb025b9f0f9796e28c70c1902f24934d60963fb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.6 MB (239589599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30368ebf0453a4b5d22ebbbf72fc5246d63340a4af5c4e79c44ab57ddb860429`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb81eefa71bd631b66935bc0c6a842daa9ef69a8d87d3547942afd439994d11`  
		Last Modified: Wed, 25 Dec 2024 07:19:01 GMT  
		Size: 142.4 MB (142388995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36bbd9abd1af0f63bee3bc8e77c2fe95d746904541aabf92be8e4ccc75acca6a`  
		Last Modified: Wed, 25 Dec 2024 07:22:18 GMT  
		Size: 69.1 MB (69141239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df8091fc8b20ed7e7fc98e37ab4c1b4cb46a0d8d4ef856b5348858f74fc5462`  
		Last Modified: Wed, 25 Dec 2024 07:22:16 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:00b4eae1276694233a389f97126077cbad1a97b6f9c90d7a3f2968aa56f12945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4953453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e65992d006a63f9134cd022080c84ca517c927fa22abbc70d8a004a745d22c`

```dockerfile
```

-	Layers:
	-	`sha256:367bf505841aa8cd88370f7d66f6ddc1b320f6470496d6bd681f66010939c323`  
		Last Modified: Wed, 25 Dec 2024 07:22:17 GMT  
		Size: 4.9 MB (4939025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45f8b9e8b013b6012259426cd78c25cff24b8a1bad1abd9c40f7cceb7b243fa3`  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
