## `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm-slim`

```console
$ docker pull clojure@sha256:e17181d083cafc713c3ee59b521c55f76db925a12413520a796f9f9dab1a934b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:038355c73e0ee165f1ad1d3821a091a5d89af379434fac1026e4b5076af4c7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.7 MB (245693540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e917226ef2660922a978838ae7046e2c6cee3f6986b2e31d896d8109b788a5`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2f0a3dbb399c143baa0a34e10639774fe4f0509b0ea46c13d1547b2ccdb8e2`  
		Last Modified: Wed, 23 Apr 2025 17:15:33 GMT  
		Size: 145.6 MB (145635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c93f22f087a68502ced1fd18b663b171aa9b16deff2e1d5728271517c94916`  
		Last Modified: Wed, 23 Apr 2025 17:15:32 GMT  
		Size: 71.8 MB (71829804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b14256264f9a5af0720d5330d12cffe83097fda1191ce7513c439e6afdd808c`  
		Last Modified: Wed, 23 Apr 2025 17:15:30 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:55f72d2cb8448336ae5d3cb8b71b6329323eb3ced0f103e03c1ad21a6eee38ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4948416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75468947487ee0d057cea476313c51acb91a8021b516879dc6b2cafd1b01a90d`

```dockerfile
```

-	Layers:
	-	`sha256:2ded650dabe05c94544b58a7c7b96b8d990d7496496b07152269965b0b17a7df`  
		Last Modified: Wed, 23 Apr 2025 17:15:30 GMT  
		Size: 4.9 MB (4934106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03e416df35be0f8df1e5efaf06343078ffc854d8f60d3a6d3e020a7ec7e2d486`  
		Last Modified: Wed, 23 Apr 2025 17:15:30 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1c8a14699ba6d180f48013232de92c7f3f6647a0efe4e4d5716e0ef52adbe472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242138461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b786c3a290ea25f24cb14584741f767da2079db038d588475b97e7cd8f28cd0c`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428a83b2f0dc282759e31456238c765c06fd3c54f3eaf46c5235474d47999590`  
		Last Modified: Wed, 23 Apr 2025 19:36:54 GMT  
		Size: 142.4 MB (142422063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d729e6d1a723788e84208d814a16f23da8db4590f8f0a16fcb3dc32190af5a`  
		Last Modified: Wed, 23 Apr 2025 19:41:51 GMT  
		Size: 71.6 MB (71649430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c496add761fe5df8310952e69de3dd926a6f8c9c69d62f3cad866c0de900b8b`  
		Last Modified: Wed, 23 Apr 2025 19:41:49 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:deaa5cf7bc7065ecaf46904126c7773923db0de8233e704cb2b0e11ca31f691c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4954913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b0c3009321dcbb88997ee8666cd6d1822d5ea01e4399d33b6725c47ef928d6`

```dockerfile
```

-	Layers:
	-	`sha256:5eca4f73a2be01162f9fa173b567a6dae52ffe462afe94515cf43097bbe4f4b7`  
		Last Modified: Wed, 23 Apr 2025 19:41:49 GMT  
		Size: 4.9 MB (4940485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f30121124735f2aa0101a859a0443a90bc6c58fd2c0c489aabcf6a10387186c`  
		Last Modified: Wed, 23 Apr 2025 19:41:48 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
