## `clojure:temurin-22-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:7921b6dc9384cf129a907585a45ef55f980f26d76189e5b3c7079a374d5023f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-22-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:25a4744038ab3871134c7d768e4d855cf1c5462dd5fed051a3b864644a851fa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256096230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d22c0fcc4519080b47e3f37966f7760b1c8c0b470ab8158ccaa52391fb4b21`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 05:20:05 GMT
COPY dir:657bb663bfeaa42d669fabe632e75f73eae3c4aa2d4e78ab7b29311c6e01254d in /opt/java/openjdk 
# Wed, 24 Apr 2024 05:20:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 05:21:59 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 05:22:00 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 05:22:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 05:22:18 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 05:22:18 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 05:22:18 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 05:22:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885c6499b1f95f19d9dea6bd5e6a966cc93e1ccc522679f6864f64d1df9ecfba`  
		Last Modified: Wed, 24 Apr 2024 05:36:40 GMT  
		Size: 157.9 MB (157879823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df160719a93f5107b9d6f5fe1c65d83d63247ac35531f7fa0aa36e4d5d07378c`  
		Last Modified: Wed, 24 Apr 2024 05:38:05 GMT  
		Size: 69.1 MB (69064908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43128f455c415aa43a3752ad333b93f6ad9a1351ada2a00fad199f7dbd86f00f`  
		Last Modified: Wed, 24 Apr 2024 05:37:57 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4040c34417926e5d0248306393d84bc96bdbbbb8a35cab6a92a252fbf5bfc857`  
		Last Modified: Wed, 24 Apr 2024 05:37:57 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-22-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2602651f385ccb8981cb5a03a7d85ca7a3634ba4c540faf8a3cd2fe98955e96a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253861965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fedf5da6aa430ce4fd381b9826b3409f2e072fe818c532a8116495487753f065`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:43:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 10:55:23 GMT
COPY dir:804c07f15e876d329ef9551fe4e0597856a4396e905a8f833a1110ebfd35dfdc in /opt/java/openjdk 
# Wed, 24 Apr 2024 10:55:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 10:56:54 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 10:56:54 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 10:57:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 10:57:10 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 10:57:10 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 10:57:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 10:57:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdf550fffc52e29eb87dc8854c07bdcf13dac348ebcd70f281f24485f6ddef6`  
		Last Modified: Wed, 24 Apr 2024 11:09:50 GMT  
		Size: 155.9 MB (155861704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7970e677e443410ae0c2f95c47d8346af38251721cda500b3fd853a34cbd263`  
		Last Modified: Wed, 24 Apr 2024 11:11:06 GMT  
		Size: 68.8 MB (68819307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f000590ebc5c0c54e079a092702e38d9d04ab93fc26889ef8617f6a2509b58f5`  
		Last Modified: Wed, 24 Apr 2024 11:10:58 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0d314e147f9fa5b6e2d8f957c3c2ed945442973eac1f53a8ed71025a011a8b`  
		Last Modified: Wed, 24 Apr 2024 11:10:58 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
