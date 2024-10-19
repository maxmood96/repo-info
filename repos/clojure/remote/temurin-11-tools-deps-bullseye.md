## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:f75423c1664079c958fc87267b0e58903a1b6cf2493f64b7e0347e9ac3b923e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:da2489de04a95e16df9e8657bf0965fd469a9693049c92e8adc20666706bbc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 MB (269964627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5144b1ac36cbebbcd18c1d9ae5efb781444de04f58c44ee19e194e43e6877f24`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
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
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ec098c0abd6ba8fe997ec07c2583b1b32befd694235ebd9975bea01056bd90`  
		Last Modified: Sat, 19 Oct 2024 02:55:36 GMT  
		Size: 145.5 MB (145549948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80fbed3f626dfcc0d034871464e57566a652714f319687a3ed9a6af79e9f674`  
		Last Modified: Sat, 19 Oct 2024 02:55:35 GMT  
		Size: 69.3 MB (69333424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd915b496ee64d36d7358fc407a3019aad14abc5925862af877ec8479a597c78`  
		Last Modified: Sat, 19 Oct 2024 02:55:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b26b2e0df63ff73085c83f4a7bd6f5a0456b76cfcdd3d945d10e3b83bd04cdd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7250076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07fa0aed9fc5a5f1bd4b8ca47491f74cad32bb514c7a47044772968eb44794b`

```dockerfile
```

-	Layers:
	-	`sha256:db3861d29843e8308edd2fa8ec31c8e4eac26d6e2428d04d01bd812396ed08ca`  
		Last Modified: Sat, 19 Oct 2024 02:55:34 GMT  
		Size: 7.2 MB (7236005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6ac0b4ab8aae3307740cf758d64074ee8f3ff205e9727fbf87308ecaf45a544`  
		Last Modified: Sat, 19 Oct 2024 02:55:34 GMT  
		Size: 14.1 KB (14071 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f26aa53d764d2aa57dfa85c5410dd158ad5155b257c5ad397ada570cc94ca628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265558958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6c6e1cff43e0652992b4b19f980e4e8107fd1f80c4d6a3e60f2d4a218d4d0f`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
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
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bda293784e347b2519c90ccae374d1fef0769a110f0539ea381e5d0173cef5f`  
		Last Modified: Thu, 17 Oct 2024 08:05:45 GMT  
		Size: 142.4 MB (142356620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c05e41003ac86805de7b845a5875e74c40c76671bd8a5c23512babc22e02d5`  
		Last Modified: Thu, 17 Oct 2024 08:09:35 GMT  
		Size: 69.5 MB (69466801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4846c262d2b2b6d62709604ec56bc778b2aceb4a43e1d283e664537b3b30fadc`  
		Last Modified: Thu, 17 Oct 2024 08:09:33 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2874ce29bd18fcc414421f9cc02d5360b934d62cbef9b10655d033694e2c23ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7229991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1366e5b9bcf46c796d5a68459a00f82d831abe1e32b346903ccc275b6bbcc357`

```dockerfile
```

-	Layers:
	-	`sha256:a182b0efb885c7e9a9e7a990388086598e2a29d300cefdf521a2cf9af04d068b`  
		Last Modified: Thu, 17 Oct 2024 08:09:34 GMT  
		Size: 7.2 MB (7215982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfb3a8772bfc585c9d03e29cdd36f1268bfdb00d6eebda0d404b1d70b8940374`  
		Last Modified: Thu, 17 Oct 2024 08:09:33 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json
