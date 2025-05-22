## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:703effb8ab73f8575997301934c7249b768d5e4c2db37cbffdcb36438a55ecb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2d6812b31cd7ee66fface65f98cdb44ecef8f0a4dbdc02e8be6d36442fb983d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233886022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043461d731d62d038ea9916c585dc9b2de9d153848f547cef9b62bddb561aa20`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad752d778bea653e830200e896b46c5b8e9e344c11ec9571ef3e28d39700df46`  
		Last Modified: Wed, 21 May 2025 23:33:09 GMT  
		Size: 144.6 MB (144634958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc74d9e963c0f7d2e04769e6484efebe4ff1c5d20132086a528f80ebf40d572`  
		Last Modified: Wed, 21 May 2025 23:33:10 GMT  
		Size: 59.0 MB (58994084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684ff8e4e7ffb255129f39a0e044a882e2810e05ae80de784e599f1cbbb81e67`  
		Last Modified: Wed, 21 May 2025 23:33:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3191b92dcd9b4812b08cbfc89c5ce4fa26e0f50b288073d29a8b8914504914`  
		Last Modified: Wed, 21 May 2025 23:33:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eb66b9d1f030d6d0462e8018011413c5f94514ef8048e20925f77f02c632fe07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5182869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5e16c9740919e9a6a4d7229a5e685d65fbe39fd77844680ff4364512c42940`

```dockerfile
```

-	Layers:
	-	`sha256:f76fe00bfedeaf92ff87013d0ec4da8392b59b74c76b4b67d3005b32200b9384`  
		Last Modified: Wed, 21 May 2025 23:33:06 GMT  
		Size: 5.2 MB (5166990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba45d3f97e92298e62d895cf7a6da6cac69206ae7733a8a00c8abc5889475cb7`  
		Last Modified: Wed, 21 May 2025 23:33:06 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a29cacc65b363d77c12828e7bf41d5e8cec2e9f8743e3ad55b55157cf7c1379d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231388893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32593512a5af9366d9b21a8e40ff73b4973268118cb043da9620d0e5d305541a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Wed, 21 May 2025 22:28:28 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8312cdb9051efb69c102039d6eddfca07c90fb35536c0a89ddf1296555f86542`  
		Last Modified: Thu, 22 May 2025 03:15:08 GMT  
		Size: 143.5 MB (143512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0349280929762625e2ab627884dcf475e83a6b8e9cb885ce0dbf83f86596f46f`  
		Last Modified: Thu, 22 May 2025 08:27:06 GMT  
		Size: 59.1 MB (59128962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8791fecd373a236a98f4e8490efee8dc69d3e16c1d0fb6608811087fbd6855`  
		Last Modified: Thu, 22 May 2025 08:27:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a6b19db3e3e69fe4144a4d3eb1a4c420e2371ae4e3c55ca1fb47f283edb1c0`  
		Last Modified: Thu, 22 May 2025 08:27:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bffd0f5ba9ece8aedc64cbc3c1e959e0cf87527f837a2668ad7475ba269e266d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5188719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128863a6e9714c1d4b032f2f42553931c2cdfb810b47af8ccbea95abf6fc587b`

```dockerfile
```

-	Layers:
	-	`sha256:b7a60150e1c0e8fa54959205a9fa76897e00fd3048aa481def78217b28c6367d`  
		Last Modified: Thu, 22 May 2025 08:27:05 GMT  
		Size: 5.2 MB (5172722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22b902a0817f113805d5d8150a862d788922fb38f5ff0a1a383fa8f4a8961bc8`  
		Last Modified: Thu, 22 May 2025 08:27:04 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
