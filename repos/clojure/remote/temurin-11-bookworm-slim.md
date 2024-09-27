## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:c611f67d19d3283c78ff5846762c6100ac168222f41f07fcea1aecbdb020669f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:668a0eb305d0c78d6ae7a4fc345185413593dfb075f0a5632fd73b34c70eb7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244159763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3085178db92e259fc80d1bea4fd14cb0e917972f83dfc1d2f308507d2b8ff2`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ea3c03a361190cad8afabfce789c9ed7dec24b40916f7b769f492e580527fa`  
		Last Modified: Fri, 27 Sep 2024 06:01:18 GMT  
		Size: 145.6 MB (145550044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6ec35c9684274e38ad1f0e85c41e02133f18252842e183a425688a01950184`  
		Last Modified: Fri, 27 Sep 2024 06:01:20 GMT  
		Size: 69.5 MB (69482800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec5df26352c0c895906099236b2315b779c93abb8461dbf51fc921bd7b68ceb`  
		Last Modified: Fri, 27 Sep 2024 06:01:16 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aae3266662718d2d9a07e81cb5af895a532ae5f1f47e57375e06cfee86ac3c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ec850dbff4ee8677656f33375323063b77d32d582740f80e369a7e46917b54`

```dockerfile
```

-	Layers:
	-	`sha256:9db7fdc9140d27c39df65a59c76b7f255f9b987581549953be2b80407c82c7d9`  
		Last Modified: Fri, 27 Sep 2024 06:01:16 GMT  
		Size: 4.9 MB (4915018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e289df303cd038ea293f0351c98ccfc484c62a5eaa615d8dff9e26531c38f9ff`  
		Last Modified: Fri, 27 Sep 2024 06:01:16 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:083b1088fa73a4ce2fc05c3be01e69dc2167953813bd6cda7331278f10dfa4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240856487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbba409660391f7a73a2db42752c9c4464a44e19086520b3c05b5439760b8b1`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d47b458c8c18ce1896657ea931977961501bbeab7113170bac391a26a27601d`  
		Last Modified: Tue, 17 Sep 2024 04:19:29 GMT  
		Size: 142.4 MB (142354737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577ca71316865c0263595f246a34ba89ae1455690e4db4f8c395cc2b7fe749b5`  
		Last Modified: Tue, 17 Sep 2024 04:25:56 GMT  
		Size: 69.3 MB (69344558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e845307c82ae4464505e613a290432e766664b8f9d438432226b8ec95b1eb16`  
		Last Modified: Tue, 17 Sep 2024 04:25:54 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fb60611510ac9878be4cdfe69fde221829ce6c0036a9c75f15411589cf4c6a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4766056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48844d5feb3aab4927a01701c580c338d23458e80f05070ead23783c5bf548e8`

```dockerfile
```

-	Layers:
	-	`sha256:0174b5923c88c045eb2475ddc8310a925e86ebf3dcc372c1b6851554e1df2866`  
		Last Modified: Tue, 17 Sep 2024 04:25:54 GMT  
		Size: 4.8 MB (4751577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d5deae37847c5b6d9b4e1dcbad079dff90dd163078adc2b71d69362e34ddea`  
		Last Modified: Tue, 17 Sep 2024 04:25:54 GMT  
		Size: 14.5 KB (14479 bytes)  
		MIME: application/vnd.in-toto+json
