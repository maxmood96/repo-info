## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:dfb458096e04034c4cbd5c16fca9d12c5a22195b22f116b5fa2850842b8e82a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:66960315c867caa63b30d7b8eeae5d3f3d8486c140487e44fed14dc8256f1df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177860024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbec13db5857bff1e1821a0da6cc04ffaa5632531afd27bc9321555970da1e6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ae857c483d9db15f355917316c91aceae5e787cac978212c74ba565a9dc1cc`  
		Last Modified: Mon, 28 Apr 2025 22:05:51 GMT  
		Size: 54.7 MB (54716178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17cb4befc0064a1c0f379061d3f9cca407f6a30ab999c63d7dbbbdddb3fd65b`  
		Last Modified: Mon, 28 Apr 2025 22:05:52 GMT  
		Size: 69.4 MB (69395462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290a85fcb4408343e9dcf0fc793035b7d4994ef55681fc97426c4b9445b39780`  
		Last Modified: Mon, 28 Apr 2025 22:05:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:02b4adcf0ff59e7a73d89b81dd16d4189a10af61f3135f4af7df860795b93b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e801c47565888529bcb76185126f76646bd08371c9257f8d45b196c42ce3f28`

```dockerfile
```

-	Layers:
	-	`sha256:39966fff111b6f2c003491a78b9ac11442b0b87fa8b92601d99c9f07127b04a0`  
		Last Modified: Mon, 28 Apr 2025 22:05:51 GMT  
		Size: 7.3 MB (7328165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1716e0add8cccb335cdc0bb545d6c3edcda20caba532a1e4a6d66c65a07cb951`  
		Last Modified: Mon, 28 Apr 2025 22:05:51 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a0a0b3f0d920c04eb40c2211def3192acc0fc0bdd688f41b628e4daac693a7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175607362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba696ac061cb0c91b23a69043ec0c35d65a535ad2969342ccc201f8fa4baa82`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ed3c3095e037dcd3f9d0412720b3f9d97adc708c3eb9bcf47590225cb6ba6f`  
		Last Modified: Wed, 09 Apr 2025 17:13:13 GMT  
		Size: 53.8 MB (53822769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34092dc2461bcb3831495c1ba70141f831b66ce92bf1d133f861ba63d4785356`  
		Last Modified: Wed, 09 Apr 2025 17:17:46 GMT  
		Size: 69.5 MB (69529724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11454e28439357d483139c45b2fc48c70bac65250d2a33ef8900f2b30b5d3ed8`  
		Last Modified: Wed, 09 Apr 2025 17:17:44 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bf760e6e7186454907e9f5e00a860acce6fcbb04af91658122b96650127bcae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7348263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402e7c52358bbf566064de5bb027e1235f49749d3e5978693d512a4ecf446989`

```dockerfile
```

-	Layers:
	-	`sha256:7fd6a18d8a41bed3032aac74256024e4a36ea2d44129795cf734e9d3d4f5d61d`  
		Last Modified: Wed, 09 Apr 2025 17:17:44 GMT  
		Size: 7.3 MB (7333908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cabb721a4cab1ba300182e4dfa0afd89f00e12e03753e0b7a7b9d6980820018`  
		Last Modified: Wed, 09 Apr 2025 17:17:44 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
