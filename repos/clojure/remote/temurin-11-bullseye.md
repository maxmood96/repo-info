## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:17e47ace895f3e60e3ab2aca0e870666da5c118013dd23582802efd4f7adda2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7c701b476d68adb6ec7588b7affcd5ecc80355f2aecf74d98d5bb63633bda849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269252284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8b62a763bba2d72c58434c2e87476a32bedb1cb54eb52655c7ba5615ffaf64`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:13:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:13:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:13:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:13:53 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:13:53 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:14:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:14:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:14:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715698428c4bcd49f1b2be3786f6fad7fa42a9057450ea36b86d790c4a4a4c17`  
		Last Modified: Fri, 15 May 2026 20:14:29 GMT  
		Size: 145.9 MB (145886202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3b815df26aeadcdac3cd769ac811339b29061309ab85d34f4b84b46306a78d`  
		Last Modified: Fri, 15 May 2026 20:14:28 GMT  
		Size: 69.6 MB (69602093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0d4f90d9238b6b5e5f79803a545f99b150392b226c7bdbb75f0b2b4dfb528a`  
		Last Modified: Fri, 15 May 2026 20:14:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:646e3b0a97983bff3667c16d099e1f184cf74c719a5736f9b97a124b02c54fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a360fb03f2972862bf5ee1b4516ef9d66b1aff6d7a69d54c87eba4826bc8d67`

```dockerfile
```

-	Layers:
	-	`sha256:23595f446010f96b31539665c34d3d988edfd5a28f1e5ae1b7089114e79dfaf9`  
		Last Modified: Fri, 15 May 2026 20:14:24 GMT  
		Size: 7.4 MB (7427794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:156a5f7ac9fa611fd6c14dad9aceeb17b8ce9f15030e7935fde450960248ac3e`  
		Last Modified: Fri, 15 May 2026 20:14:24 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1677fefc58dfb5df920428be453e7384c6388a620c54f9e63fa0c658d5c7dd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.6 MB (264607100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d5023602f8b835c15ab4406eda79942dd6f65556d74de153b9b09f3e679cd6`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:13:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:13:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:13:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:13:46 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:13:46 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:14:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:14:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:14:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fe468a35275c9f353d82db36fd260d7810732bc0ef141a9dba8b46eb3cc4db`  
		Last Modified: Fri, 15 May 2026 20:14:53 GMT  
		Size: 142.6 MB (142582228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5456e310ef078460012d01cd16956de95e2a915f7d53f5fbed218f9f02e51d31`  
		Last Modified: Fri, 15 May 2026 20:14:51 GMT  
		Size: 69.8 MB (69771015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa76b4e92f87697bbde2b3471a5b82e42e9638507b41cb52b8e8aa88b661c9be`  
		Last Modified: Fri, 15 May 2026 20:14:48 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b09b65b6b355919489bafd37c5a5eeb8967c6761a9c3bc68b774043b5900a2d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7447992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb9526592cb63eb075665d7dce2134a6af71f03c609d6b7ebd2bb373f8cd156`

```dockerfile
```

-	Layers:
	-	`sha256:7562ef7aec9783f00cda0902db92f04b787b93b17355a979fb5ff09a6f4ad852`  
		Last Modified: Fri, 15 May 2026 20:14:48 GMT  
		Size: 7.4 MB (7433511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4749b84cd3387ac4b360862d25ae52e6d457f2de3e316aa3d1345d6bf50742d0`  
		Last Modified: Fri, 15 May 2026 20:14:47 GMT  
		Size: 14.5 KB (14481 bytes)  
		MIME: application/vnd.in-toto+json
