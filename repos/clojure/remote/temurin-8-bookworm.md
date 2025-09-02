## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:f81a200c4c88ce66137dce87b473b825d393c69cda492c0d1d76323c733fd287
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:de2444b769a0c8c00fdd55882ecf9cc89666d3fbc986b9bc2a93c3b9a0fdb02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184364795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc669b5ddbe2f34c20bb8f41999d23769ef78fe1b4029125daa0230c179e32f5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d1c110aa8bd0ff975bbb69f58c0d3b1fdba7bbfabaaca571b5c9c6872bfaf`  
		Last Modified: Tue, 02 Sep 2025 00:17:03 GMT  
		Size: 54.7 MB (54731307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbfbc9611b29202930b8f496d6ea0b82cb413a4ce95c33f2fc3262643377129`  
		Last Modified: Tue, 02 Sep 2025 00:17:03 GMT  
		Size: 81.1 MB (81138333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da5b7cf3e21926edb9b7e6efb9e298e8cf0ebef4d1d43ad94b0f4ddaa8c929e`  
		Last Modified: Tue, 02 Sep 2025 01:00:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:296e5686c774f06e12dc7216e14a2132a4a1ebb55fab49a0bb0b6491927f4fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a047cd0e50645dcd6f41afffcc180cd91476c4e8ff09cd73185a3c2c2878253d`

```dockerfile
```

-	Layers:
	-	`sha256:f93185666a1f90150cfeedb00e5f5270644cfbbd669fc4cd82fecd314ea1e91d`  
		Last Modified: Tue, 02 Sep 2025 03:45:16 GMT  
		Size: 7.5 MB (7489907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952032ce622d1b07aec33fbddffb08a0022bb7c16454e89bde7772fd24061c33`  
		Last Modified: Tue, 02 Sep 2025 03:45:18 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4c58db2214c3276191b9c8c521f140d95d937f4926469445e4b9bcb2b872cca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183188104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f40ceb73033d105cf8daa73d6cb05fc2fb94f9eb3e99ab6a78e13acb17c4c5e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab8e03733fa4cd230f3c654cf2c9de160d54ba2f0b7af6f920b3c8ffe594231`  
		Last Modified: Mon, 18 Aug 2025 16:52:49 GMT  
		Size: 53.8 MB (53835608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abadc1236379723ba9f788497752f33352451f41715ee2b271f81d9794efd199`  
		Last Modified: Tue, 26 Aug 2025 17:28:11 GMT  
		Size: 81.0 MB (81009399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac1b35762c7b9b5d068ed016ff3d80968368b68f919f10d0964759651618af5`  
		Last Modified: Tue, 26 Aug 2025 17:28:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b8bd53ef3d4f28cd1c8bd04f43ab6ef5ebe3458ad708012e9f79ee13e1cefbe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5836083437c36ba440b11adec1239fd18e4338101ac26cd7e3bdf7b3f2fca86a`

```dockerfile
```

-	Layers:
	-	`sha256:47056a4f6b3abed98615415b4c92568e5227e477c2209c8e65c835764f677c62`  
		Last Modified: Tue, 26 Aug 2025 18:44:52 GMT  
		Size: 7.5 MB (7496368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a147991461f593fc9f05898b878bbfa5a14865ecd235761ae4049ca7f360dade`  
		Last Modified: Tue, 26 Aug 2025 18:44:53 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:c016aaec93b05cb82f6bc699865b56cb051f0866d9418b15c078231ca16a25e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191476813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ee32566e761f216223d056c867254bb4e58dabfc68d0ace4b367d65bee3b8f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47051cd5c75ec10709ec504d89b39f72c1348ec4054ca49be83a8093cd36b3e5`  
		Last Modified: Mon, 18 Aug 2025 16:58:10 GMT  
		Size: 52.2 MB (52165394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7680678465b4587df92250daf849f4b5686df684d75eecd6d9e39528d6b9dc5`  
		Last Modified: Tue, 26 Aug 2025 17:30:31 GMT  
		Size: 87.0 MB (86972695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c71b2780d0e7d4c66c185c57c432293866f55fa6356d664398d949cf9b3154`  
		Last Modified: Tue, 26 Aug 2025 17:30:23 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:88b39871024d63f82056ed76aabfd0f2e63675237baf97f6cd52921f45a7db87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed8de86c131cc606e5dcf4e770780f45ae178b3a7dcd3af3ff2f24b36309cb0`

```dockerfile
```

-	Layers:
	-	`sha256:eb4b7dff2e2d6d781dcae88a57cce2524b06b5ecc542ba6caa8850055c8f3527`  
		Last Modified: Tue, 26 Aug 2025 18:45:00 GMT  
		Size: 7.5 MB (7495704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dbebdfe73740f5c0e3361fb576eeaadfdc18ec2f5a68284a1d8ef4a7dda755e`  
		Last Modified: Tue, 26 Aug 2025 18:45:01 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
