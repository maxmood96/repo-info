## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:7dccc15250cc0ddcd39d66a1ebaa56cd500936f09f3c3de9cb3a8731a154c960
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:227fc947602e3e6c4acb6b039cc5f11ee8bfa632a7e7ce01b52b3403edefd525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152476796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6d54de45dcf267394b826d30a4d7c1a4410ecdd4453bbc21e602670a38501e`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ecd5cb5bf3bca9f126e23505885df38d47fd61690fee5521dec4414c49913d`  
		Last Modified: Tue, 10 Jun 2025 23:50:05 GMT  
		Size: 54.7 MB (54716158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23bd6c57b0f4d272b0ef631c138e10b323774505041d10b73a71a77c253c152`  
		Last Modified: Tue, 10 Jun 2025 23:50:07 GMT  
		Size: 69.5 MB (69529864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbb155f5589091c85d72a299ed2d51fa5ec2150e6144d4ccd981348129029a0`  
		Last Modified: Tue, 10 Jun 2025 23:50:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3b0e67622b6037900c8ef5a7980ea4738d2c4047a7f7fd698b65c26f6f089908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5245789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9e48f0c2ad2bd09b1f8ffbcceeb1ffe5c3baaf381311d2ccc12398740f6f38`

```dockerfile
```

-	Layers:
	-	`sha256:5be52accb2580e42778c3d939ef89e456ba1177b5a73b07ad47ede2379e5f507`  
		Last Modified: Wed, 11 Jun 2025 03:41:27 GMT  
		Size: 5.2 MB (5231498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03c667556662c4f8d7800246981794dde59c80fb9fa62b385845e93f4a04f005`  
		Last Modified: Wed, 11 Jun 2025 03:41:28 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9e91660dc282735529dd50bb12eda9a13a06e7ed1cf4aa9ea1013ccb9a2f0c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151300104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cccbf4f07b06cfe85f25f515a6002515b0cd130c64972ef43f44f214053de1e3`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad0563892583b6c6ec5d5fbed80818f17182d77b30b2494ba804acaebf04701`  
		Last Modified: Wed, 11 Jun 2025 08:05:34 GMT  
		Size: 53.8 MB (53830509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be00ede887e92938cdd854dc5eb9b4fd821c0f1e01c6644a06a249ae2042e60d`  
		Last Modified: Wed, 11 Jun 2025 08:09:31 GMT  
		Size: 69.4 MB (69391274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d78805309a277683f9cc1de60b7ec131232dc2c073e5d735af22649b0f149b`  
		Last Modified: Fri, 13 Jun 2025 01:36:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8c1f90c4dc3535e111e40cab9a27bb0de616d2d85c425d72a5cc7cbad45d0425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167d915276015a082952f026b253bc72a91f116006193c128264eea4092d76f6`

```dockerfile
```

-	Layers:
	-	`sha256:523965540ef182b75c7db092b82ff63534d07f197f6d78fbc5fb963e5b5d3a61`  
		Last Modified: Wed, 11 Jun 2025 09:42:46 GMT  
		Size: 5.2 MB (5237957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b7f215ae04180a976fb8e02694e2f0107f457b36bf4ce46ff580fe9d2479be2`  
		Last Modified: Wed, 11 Jun 2025 09:42:47 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:5133e9e7ef34e6ca684de36323a372bd3187cd388240c3d6321407fe6bdb6a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159587248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2603fc279cf67043205736a8661b5bdee2f89f81ff13cfe715e08f6cc8fccec7`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2b15ed600b7fe4d50b0cd7de41758257e340c3d61ffb406e8d0883d92caa23`  
		Last Modified: Wed, 11 Jun 2025 12:19:08 GMT  
		Size: 52.2 MB (52167960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189dd1689d2e69f730a23ee4c6491f2c2b0ecbc61ea2c46d7b8f139130c12a88`  
		Last Modified: Wed, 11 Jun 2025 08:09:10 GMT  
		Size: 75.3 MB (75345847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a34b8f020a83c0d960edbcbd6276171d8f128a30b655fb29f5f87a854bb74c6`  
		Last Modified: Wed, 11 Jun 2025 12:19:25 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:24df8377f4b678df889d9a3789e10f12ec8f2769a7e3f12425e2aff0fe1b0a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfeaf98bee5b207139d007a42d287e76fe9a1117777e03b2f3a89f1e3a3b8b6`

```dockerfile
```

-	Layers:
	-	`sha256:41968abd6a3eb998567d27ba791604b0cb9e7bef8e10493c1ed45fde14e96fcc`  
		Last Modified: Wed, 11 Jun 2025 09:42:54 GMT  
		Size: 5.2 MB (5237249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb9774a981fe962210e41bf6b10db6500a3bd8db20337a9e6a049fde2de7704f`  
		Last Modified: Wed, 11 Jun 2025 09:42:54 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
