## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:d8616de6a17b2106a9e219e2b0ed695f00a96f01986bd832b553968618e596ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

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

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3e5518cad36ca8df4ee9a238000bf302d52a409cb80e8dc24eeab11169f51207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240857183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f115d9ce6020317bb01d699895da5d1d1cde4b9c664582b9f0c756b8349ec072`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d7e1497c246ec7127254becce8d04dfbba749f3d26c14f0ae781b051e9b846`  
		Last Modified: Wed, 02 Oct 2024 02:10:35 GMT  
		Size: 142.4 MB (142354841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467e5929d47f09ddafb5e415f85c60ecd6f8302370d2e91623ee248d1f8651b1`  
		Last Modified: Wed, 02 Oct 2024 02:15:15 GMT  
		Size: 69.3 MB (69345327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70dc6ec6ce9be035b8b3ed33a15496408fe8bced48d61a6d0129d072e0a716fb`  
		Last Modified: Wed, 02 Oct 2024 02:15:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:037570f3e59ea397bfaeea869ec259eff791cf1db017ab182c16695dcc2fddd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4935452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2f1d19ae222b2b4e5ad50c9a90d8b745bee39b062ab5a6645c3dde2d7081f6`

```dockerfile
```

-	Layers:
	-	`sha256:a3cfdfc83b4f579b8dc44286f967756f1629f195e57d0fc50df00ec2fd93376c`  
		Last Modified: Wed, 02 Oct 2024 02:15:13 GMT  
		Size: 4.9 MB (4921403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a5525b08d25d8e87d5c9b73d630b6d5115655e2fd4b0f3fdee303e6dc22b032`  
		Last Modified: Wed, 02 Oct 2024 02:15:13 GMT  
		Size: 14.0 KB (14049 bytes)  
		MIME: application/vnd.in-toto+json
