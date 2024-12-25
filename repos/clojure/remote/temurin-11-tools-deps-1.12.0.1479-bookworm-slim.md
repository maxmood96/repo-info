## `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:478a04cfcf64f48a95e110781bfc44dfd0a45af33d21478b9f371e57895c53ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

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
		Last Modified: Tue, 24 Dec 2024 22:38:00 GMT  
		Size: 69.3 MB (69292977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd9ec7d2e14c3acd4819e954a35564c2de168dcca33cc792de382bfda20688a`  
		Last Modified: Tue, 24 Dec 2024 22:37:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

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
		Last Modified: Tue, 24 Dec 2024 22:37:58 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9e60cbcabf282e5f3bb2bc308c66e29a7f2cdbdadac908fb3e39f92af771d777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.6 MB (239589349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf2122188fb511668480afab037af29249bb2db7c97a8490e8185d0ce807974`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee73b740bf0c91d6533d7223a2201ab13c32a02ba20c93d7ea7ea16f74d4af4`  
		Last Modified: Tue, 03 Dec 2024 15:10:14 GMT  
		Size: 142.4 MB (142389034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42019f3dbe82ed62652b9dfd4ebacea7dd161f679b5c3f71bf492ec7201def0`  
		Last Modified: Tue, 03 Dec 2024 15:14:24 GMT  
		Size: 69.1 MB (69140861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2721b8553131d2687fa412a2c1299514a6be6f18fa54b2485a45848c3959e6f2`  
		Last Modified: Tue, 03 Dec 2024 15:14:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d5fd67c5c79e594d8ba59ee1807c6a3f79df2f4ee0b2a30ad8ea4e901c6a5347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4960364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:999abf1abdafc5168237db6f2894986ac53575f435d86777c42640990b2a2e94`

```dockerfile
```

-	Layers:
	-	`sha256:7f28bfb239a2a7116fdcc0f4f4c96f4a1f310c394f6515b3f7c9206f4444e8f1`  
		Last Modified: Tue, 03 Dec 2024 15:14:22 GMT  
		Size: 4.9 MB (4945936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:272016f4de68c85e44628cc9ae25a4bf1a50ae700f1c15f2125f8a6d912e010c`  
		Last Modified: Tue, 03 Dec 2024 15:14:21 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
