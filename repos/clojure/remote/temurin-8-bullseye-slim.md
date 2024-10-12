## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:01ed138d52daadef72c5df237439f860d57ffed45c273bcab0560563f8a88605
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3a8bc93bd61f4ac98411ed4d77ff82367ae7435f2009c2e029200c2650287977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (193981209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e728d314beffd8155c0e98eea462c8a72131e7a8f08eb614c04651447706fb`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
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
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d650bf5f4959e0ff71b6b064903fd82c5f1cd1b92b2b79c11d156a5403baa054`  
		Last Modified: Sat, 12 Oct 2024 00:53:32 GMT  
		Size: 103.6 MB (103611902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1de105bd7ad2a20276586613c08dfcfb030aeedfe3667da2fc5c114fe41e92c`  
		Last Modified: Sat, 12 Oct 2024 00:53:32 GMT  
		Size: 58.9 MB (58940064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bde9e060c4ba6951da578ed2fcab7ee30789eb061d3371a438f441dfc46170`  
		Last Modified: Sat, 12 Oct 2024 00:53:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5dcfb7c9399ade1a5faf4fcca929b59bbef2e01de40cc143ddcfb2633a5fffdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5235610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7862a56345d4b06fa3b7c1c2643001038322037ba48ad7488232a4e2179b768d`

```dockerfile
```

-	Layers:
	-	`sha256:6805a7fb76ab4b2dafa1c00eb90ada3cf77e10691afc9d0b8b8c28df43b406b3`  
		Last Modified: Sat, 12 Oct 2024 00:53:31 GMT  
		Size: 5.2 MB (5221651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1f077d82ec877d58122523ff6b7cab4720e4d7bb5c662a28a1b8638ff3fa703`  
		Last Modified: Sat, 12 Oct 2024 00:53:31 GMT  
		Size: 14.0 KB (13959 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:50532f2ca10ef5d9dcb0bf24d94850745cec10568b1bc3ab97be89fdec0b7d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191877899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91349f1f4eeb1bf7381f11b97c110e7d9b0f74e0a834b3dffa1bab610afd0800`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb75fe23968e35e453b89cc8dd158cce9129a4418492f492ec116f1b8ed71cf0`  
		Last Modified: Sat, 12 Oct 2024 00:58:35 GMT  
		Size: 102.7 MB (102729198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5d3b3c1b95f64d8468a23913509bc6d83f742ff63e7437013d66e40fed8d70`  
		Last Modified: Sat, 12 Oct 2024 01:02:57 GMT  
		Size: 59.1 MB (59072897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fec10c386b5f4dd0b4a042c5a353d324b11008b6c2703c35abb55709b8dac5`  
		Last Modified: Sat, 12 Oct 2024 01:02:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3489899cfeaf3ae81c5c841521ee36c8f75aa7515aba3e0ae853c43d04c3091f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5242152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39fd07554fb471666eaa056900e220a4c6325da1fd0489608fa78ce4c8fd8f5a`

```dockerfile
```

-	Layers:
	-	`sha256:f4d8f91fffe9c61f1f14ef7285aab50e0bd84acc0659c7b8847a737a2427e22e`  
		Last Modified: Sat, 12 Oct 2024 01:02:56 GMT  
		Size: 5.2 MB (5228087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dcd9287c8732bd3d30129fc62f5fe068b6d16d6c9a91256f9143c48e0f58876`  
		Last Modified: Sat, 12 Oct 2024 01:02:56 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json
