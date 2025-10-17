## `clojure:temurin-17-tools-deps-trixie`

```console
$ docker pull clojure@sha256:2cb080f6fe31586f66b0b8a9d70d4a5a0bebf7417bf7d59608fffae33214e5a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:3f24695e2a3e0fa7022b44d15a741d602b0e0fc6b446ebd02e406b4d787c9a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.5 MB (282477192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94634f7964a870feb1556e479a6e845888462d6324db1baa1fee8fe58f286170`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e2daa85dbf261e0e6bcf9a7a85e81ea0c72879690928287af5647f4327d0ca`  
		Last Modified: Fri, 10 Oct 2025 08:10:52 GMT  
		Size: 144.7 MB (144693289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3578cbbba666f8c6acb1cf127040f21047e24f599073cb7dd0198788ce4c325e`  
		Last Modified: Thu, 09 Oct 2025 22:29:08 GMT  
		Size: 88.5 MB (88498236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2f039e0dde49dcbf56780ac436b77ca99d8d3659c2bc601f51ba07edc28a9a`  
		Last Modified: Thu, 09 Oct 2025 22:29:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8284ba52813be3283bb43e4acb5f30e3c1aa26544c85138ad676c80239f619`  
		Last Modified: Thu, 09 Oct 2025 22:29:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:eed9e2924dce18ab45a10fe8a04dabf458b40898e428c332905489ab312b1269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372bf5f3d75b605a124dc1b7761a31565f74f9bdedbc900d5df7cb340f9112a3`

```dockerfile
```

-	Layers:
	-	`sha256:8c2663dd2c04a649ad8faf07e4ec37385cc86261a9831c27f6b57d61fb3e76ad`  
		Last Modified: Fri, 10 Oct 2025 06:42:33 GMT  
		Size: 7.5 MB (7466899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:980b6f803e9b29c165e0c0c9244155d7cac0784ad78d16e505dd49263bc94fda`  
		Last Modified: Fri, 10 Oct 2025 06:42:34 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6ec7d4042c4fa8d128a5b7517a4e65e11f71c0afba1219bd90d085e86503e7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.9 MB (281882306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd68d733105ee724ff656805d4b8cbae031c790891155ba2d1c81c481221b7b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184277e53d72b468f6bee45e16599cae1d5cdc14be1d2883827d1da07e0549aa`  
		Last Modified: Sat, 11 Oct 2025 03:29:05 GMT  
		Size: 143.5 MB (143542159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9e7d8a58da53a7d0a19c557991551a113bcadb2068d0db6c7c320010cbe0b6`  
		Last Modified: Sat, 11 Oct 2025 03:28:49 GMT  
		Size: 88.7 MB (88690407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3d908128a1da8ef0feb9a2482456900642de12deb31f63077c302a8d419c9d`  
		Last Modified: Thu, 09 Oct 2025 23:11:51 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da03d9f27c9f157ddffc4b0b19c9491d5253eebf9b4448bde661b256b7fb0889`  
		Last Modified: Thu, 09 Oct 2025 23:11:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a12b3a033e1daf2ef217cab9c934df03b464c3d133b01ed3563d009e9f1c1c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172cce81213085c651ccea4490e8d12baf5b93ab0e62c8f7cf18d56dfe707a8c`

```dockerfile
```

-	Layers:
	-	`sha256:f533e371e32d505ec71472f6c9622d7b2399db379a938074e01e7a072e7d2095`  
		Last Modified: Fri, 10 Oct 2025 06:42:39 GMT  
		Size: 7.5 MB (7473929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2955bee249b1f53586728011b2ceccf3649ae4e42ffbd0df8f279dc568996bca`  
		Last Modified: Fri, 10 Oct 2025 06:42:40 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:03be69dfa448add7ee751f3590064464f8a74d588c8c2a338b82b4926134228e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.6 MB (291634842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339f8a52c2a102c6b32b9133a2c83d60802cafbceab6ab0fe1047751f5970efa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec14b4c204116b4d7facf8cbc27f3b315966b70cabcf7b1b2004e1e01f519c40`  
		Last Modified: Fri, 10 Oct 2025 05:20:45 GMT  
		Size: 144.4 MB (144372884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd881904ec06420a711ab36bb8c0e5a5bf012f8d1ae7412e6d48cad38efcee74`  
		Last Modified: Fri, 10 Oct 2025 05:30:18 GMT  
		Size: 94.2 MB (94151699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4204c0d7e43692326d48d0a00ebb3d1d76163a98d00efbbb095a9998e850d5f7`  
		Last Modified: Fri, 10 Oct 2025 05:30:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e127b7bdedda38a6a1452946ebfa5b6f37e1dce3903bccb4b6f176fb7f5dbd`  
		Last Modified: Fri, 10 Oct 2025 05:30:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9fe902387b3ec674c8e0fec13e7de05776af156b10c3fdf2af6e677edfa2c95f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8747c412dbbb5dab72208222d8c1ee7ea78034a8fcd0d2c42ed23e4ed21825`

```dockerfile
```

-	Layers:
	-	`sha256:c2bcf7b2e95b95246f5d2ffdc4bafc009a3bf7a130972c17f6ed40142f14c7b4`  
		Last Modified: Fri, 10 Oct 2025 06:42:45 GMT  
		Size: 7.5 MB (7471318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8bde1c99f65241f8a0a3fdc8a7919377cd9082c4f9bc3937315617a2424c3d6`  
		Last Modified: Fri, 10 Oct 2025 06:42:45 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:77ab78a9618b94a09e4169577c98125104d3fcd23d1e04dbb9cd86e1249e3c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273395712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02b0d10b736c4d9b2e7db508a9f536815464119434fe6f89bec56447f325261`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:913254a25f5e448a50a1e74fa50f037e22f85cfe4d6a3c626f4b7405299b7c1b`  
		Last Modified: Tue, 30 Sep 2025 01:03:38 GMT  
		Size: 47.8 MB (47770009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da301767faf0be7c97a51d690dc02316655fe29df49b482bab04b89ae5a92b0`  
		Last Modified: Thu, 16 Oct 2025 21:34:47 GMT  
		Size: 138.6 MB (138575658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cba5c09ac28f4727f35f1e5a2c38ff6c8a48d3e152a9fdde51787a103cc65b0`  
		Last Modified: Thu, 16 Oct 2025 08:09:51 GMT  
		Size: 87.0 MB (87049001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9879e636406efcfad7103c554b0d0e0a769f48b40893f0cbc7f19dbf04a38d8`  
		Last Modified: Thu, 16 Oct 2025 08:09:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1603119e72cd7b55096006f1781edcac19dc66a54e52d7dcf8fb676f83a6babb`  
		Last Modified: Thu, 16 Oct 2025 08:09:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:329f2f15823bea64d57700d2e66d47670fa59c460558600fac467227381f9870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7468738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77eee61fb048ced494868f4a8bfac123c6c3e58efa12d46925a7ad7e5703ac35`

```dockerfile
```

-	Layers:
	-	`sha256:586e4d76d0aa68df31480210268c908bc7c004387ac0f174db1e1e065d2d9270`  
		Last Modified: Thu, 16 Oct 2025 09:37:06 GMT  
		Size: 7.5 MB (7452893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c80954e4cbcc9f956a832195b3f4fccee98bd4d551b3af580a7943c73089c795`  
		Last Modified: Thu, 16 Oct 2025 09:37:07 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:71f62cd18412f439017f7e23fabee2912b9edb75f7ef42bb1f66286828406604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.2 MB (273201263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615c89c55b9eb172b0439a1ed3154172d0b8f286e1ef8585197a7365ae5a0e38`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:024d6c344f0b9dbb2baf07e95dfd2abbfadc5c8262ca381f39f6489670cbaff5`  
		Last Modified: Mon, 29 Sep 2025 23:41:06 GMT  
		Size: 49.4 MB (49351442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24133c4045572f740b0ece90f7f2179652d7d347c8e44d8243dbb266de1bf45b`  
		Last Modified: Thu, 16 Oct 2025 21:34:30 GMT  
		Size: 134.7 MB (134723625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0fcd734d423d6a711f30db3c859cabe618ad72b123ddf9b26259968d78660b`  
		Last Modified: Thu, 09 Oct 2025 23:17:34 GMT  
		Size: 89.1 MB (89125157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6c5947ee46730726d8fd35f9b0c999dbd96a4bbc9db0bab5186d7e435e7206`  
		Last Modified: Thu, 09 Oct 2025 23:17:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2192f67e181dc3693825a04b68ebb01ca45d515f0f4a4d53b34a4b95b9f0fa`  
		Last Modified: Thu, 09 Oct 2025 23:17:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9adf03a728bb79b225cb78cbf6555d5d532ce419c3c0d8bc2982548305a12a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9312a4cfa24e09ea74844c8c965d94427501d283f5e7c96370275abdfa990553`

```dockerfile
```

-	Layers:
	-	`sha256:b2e680a1bf9ed272929a489dd19af71abfa42e7e1f4f886c8fc958c8a6065e5e`  
		Last Modified: Fri, 10 Oct 2025 00:39:05 GMT  
		Size: 7.5 MB (7462821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de8d850fbbfb292a94b8390563be3d584f801e49a6dc6c74301233ef1f9e5d0a`  
		Last Modified: Fri, 10 Oct 2025 00:39:06 GMT  
		Size: 15.8 KB (15796 bytes)  
		MIME: application/vnd.in-toto+json
