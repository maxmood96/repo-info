## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:4f3dfb2136be5c4b93f91af71b5ddfd4edf3b757d3d0377b894190ff8a28668a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9af583cdab63913cac69504a94dd89fca419998e58dbe7cba6763bc93964910d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233817792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cb9107b689036fc84189589b15352da13bca42cb19b319828bdcad831b95c1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0238cdd747238aa54036a3e440a7f27a7d74dcd00708f33eafecb324cd0ea92c`  
		Last Modified: Wed, 09 Apr 2025 02:20:03 GMT  
		Size: 144.6 MB (144566536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cbf2ae43aed20391a9ae77fc72b3a19aed0a581c6d23aec7c3020d34bd394c`  
		Last Modified: Wed, 09 Apr 2025 02:20:01 GMT  
		Size: 59.0 MB (58992793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b16ba2fe3f7968998fe3851d1bb6e760914d82efd73c925d188bef51e54458c`  
		Last Modified: Wed, 09 Apr 2025 02:19:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d8bb15013f461bb80f18fe41ed3d9603f3e7e4064cab133d60c1f02886f3b7`  
		Last Modified: Wed, 09 Apr 2025 02:19:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bd6daf7f32f989321f717b79fc01add3235e9a667ea907d8ee623f447b429eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25728a1e8a51a701686effad4a8f14979aea86bfd1c6df67158e9193e7b9c499`

```dockerfile
```

-	Layers:
	-	`sha256:67e2948e657afb19cf34c5dd5183a15c08785029bd1e31e4d6da87bac904b255`  
		Last Modified: Wed, 09 Apr 2025 02:20:00 GMT  
		Size: 5.1 MB (5119013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c0302bf71e66e2a4ea47b638a56f1fa36f4db7422d8105060ce6bb3acb44d5`  
		Last Modified: Wed, 09 Apr 2025 02:20:00 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e7746e81210a7f81a7c4e21956e5a106a0426973bd3a2e286f5a997a67c373be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231332554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869607fbe52fe32472408b852aec707d768a5fb8be04fe23a9b5f1148df2507b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971d0a5f174ee83e8d1d2ce1d43c957f29dd748519dcec96fd7d75e73d64da4e`  
		Last Modified: Tue, 08 Apr 2025 06:31:18 GMT  
		Size: 143.5 MB (143454703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad6f7eeb0382285ea5534828fe2932a1dd58cb1c826999c73ec41393e409e8b`  
		Last Modified: Tue, 08 Apr 2025 11:31:04 GMT  
		Size: 59.1 MB (59127311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0848dcec648310405ddbf690471ac8ff6c44fc6b31be4a32f04a5292dfa4836f`  
		Last Modified: Tue, 08 Apr 2025 11:31:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13567466b1c2d59659b21ed5796fa78f0348e03150d09db3efc2c0cd2dc44b9`  
		Last Modified: Tue, 08 Apr 2025 11:31:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a744ce0febc2a4c5dde2a4c655541cc8cd1e5e6985ceb2bf302c95e00f6433f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435cfe9f68c197bf1066eea8751635502e231560497c8ff0451418284906b24b`

```dockerfile
```

-	Layers:
	-	`sha256:4e37dd09232186a1bc869dde3def62ea3f49741f4255eab767a556fa4bcd8ecf`  
		Last Modified: Tue, 08 Apr 2025 11:31:03 GMT  
		Size: 5.1 MB (5124745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2308d92586aed11550bf34e3db2bc4781d0adea1db4738a2f0fc4e4e36f39f2`  
		Last Modified: Tue, 08 Apr 2025 11:31:02 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
