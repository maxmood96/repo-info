## `golang:alpine3.22`

```console
$ docker pull golang@sha256:768675ef6a9ff4f4344c9798ea3a02b5dba30929a6035b82ec1c79f048e1a9a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:alpine3.22` - linux; amd64

```console
$ docker pull golang@sha256:d38977262c1b461c57d4458bf93b110dd6bfc9dc56a41f26b69360384084bd30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71318299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a24d5386f650274857accaa40b080113c51aff01b38ae5fa2daadc7b86a54f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:25:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 17 Apr 2026 00:25:11 GMT
ENV GOLANG_VERSION=1.26.2
# Fri, 17 Apr 2026 00:25:11 GMT
ENV GOTOOLCHAIN=local
# Fri, 17 Apr 2026 00:25:11 GMT
ENV GOPATH=/go
# Fri, 17 Apr 2026 00:25:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:25:11 GMT
COPY /target/ / # buildkit
# Fri, 17 Apr 2026 00:25:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 17 Apr 2026 00:25:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56732981ad05c998c7bcf712b0ad8b8d906d502183b11cd7409ce67313656c3`  
		Last Modified: Fri, 17 Apr 2026 00:25:26 GMT  
		Size: 289.5 KB (289451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55da06e3b41084804b2e5dbba71d35d26478b19ba8055d07a393cae22e9935f`  
		Last Modified: Tue, 07 Apr 2026 21:13:57 GMT  
		Size: 67.2 MB (67220501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f467c362a884ae4bf70c4c3d971e5ac7d27bcaef75385218543ac6d630e37ae`  
		Last Modified: Fri, 17 Apr 2026 00:25:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:8f40b6ef4f619476db619308a4239e0da8f11326ca95b82e1e8ca2371920ca46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 KB (219934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50f512b0341893f417d63ff671c337f8469246898cf2d5ede2e1024f0249233`

```dockerfile
```

-	Layers:
	-	`sha256:0947888a1d590418a69e8810690eb26f0981fe3a367bb1474d1f496827e3bae1`  
		Last Modified: Fri, 17 Apr 2026 00:25:26 GMT  
		Size: 195.1 KB (195127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d2fcae71e29848861fd58daf6212ecb5b09f559cad7f66d75378b20fb0c57c2`  
		Last Modified: Fri, 17 Apr 2026 00:25:26 GMT  
		Size: 24.8 KB (24807 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:5d317ad75e0a9a5b0c6029d555e721cd5bc221685dc5df03a92991cadc224a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69548897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2254b321402a6879eb4fb36fa6965b24611575eea6be9eaaf5ce28d5c5a636bc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:28:22 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 17 Apr 2026 00:28:31 GMT
ENV GOLANG_VERSION=1.26.2
# Fri, 17 Apr 2026 00:28:31 GMT
ENV GOTOOLCHAIN=local
# Fri, 17 Apr 2026 00:28:31 GMT
ENV GOPATH=/go
# Fri, 17 Apr 2026 00:28:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:28:31 GMT
COPY /target/ / # buildkit
# Fri, 17 Apr 2026 00:28:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 17 Apr 2026 00:28:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb73082823697f16e5bf1efbdcb42da033e6d29911be4568035c38c603dfce53`  
		Last Modified: Fri, 17 Apr 2026 00:28:44 GMT  
		Size: 290.3 KB (290334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e327e2b14e32d059b1daa22f82c1fb7fa98060bc20d47dd6686da42229cba8b`  
		Last Modified: Tue, 07 Apr 2026 21:13:32 GMT  
		Size: 65.8 MB (65751024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61855757aa4412305001c6bf7dec44ea31d21c155011ce1b4712a4866d3a4e5`  
		Last Modified: Fri, 17 Apr 2026 00:28:44 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:3b1bac524a841c20dfc06fee004cc36c3bf5271923fa8c384b2aa5e35b0f74fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935f02714aaab10ba36970bd096b9d51b4bf9d6de44b25579569a499abfda7d4`

```dockerfile
```

-	Layers:
	-	`sha256:2cc58ada87498c190c8505ca0479ce8cde971db619383b01c1c6afa0b1184b1a`  
		Last Modified: Fri, 17 Apr 2026 00:28:45 GMT  
		Size: 24.7 KB (24698 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:c34d76f7ce9f6c6813f926e89cbca56a66d7474daf9c1a64f7ed062ebb01377b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69266474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235291fd2c7bd13acd994daff283dfdbbc6ef4c3792237d47b3d7561c60ad688`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:28:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 17 Apr 2026 00:28:58 GMT
ENV GOLANG_VERSION=1.26.2
# Fri, 17 Apr 2026 00:28:58 GMT
ENV GOTOOLCHAIN=local
# Fri, 17 Apr 2026 00:28:58 GMT
ENV GOPATH=/go
# Fri, 17 Apr 2026 00:28:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:28:58 GMT
COPY /target/ / # buildkit
# Fri, 17 Apr 2026 00:29:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 17 Apr 2026 00:29:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389aa30d40d2cbe01ad2b410e91e2b2e19f63b148025e6b7f637119ec3a1dc15`  
		Last Modified: Fri, 17 Apr 2026 00:29:14 GMT  
		Size: 289.5 KB (289509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3c0c93980268a0e43ceabcbfa19841d8859d03f3623b4521a7ead3d6e1badd`  
		Last Modified: Tue, 07 Apr 2026 21:13:54 GMT  
		Size: 65.8 MB (65750977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9632d635ea79d4ed0f20337172c2216e2c1af529629b39d67cddabc7b953f74c`  
		Last Modified: Fri, 17 Apr 2026 00:29:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:6bcfc31564d703d04d9ba8d8d804d67dc922098fb6d0b1df84464bea09397e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77625a1d19ec6207cf39c9e352ead529f9784b1ea046bf8004557f9d04d094d`

```dockerfile
```

-	Layers:
	-	`sha256:a6f0bf965c87f4d1bed6dbdc35767ecac76a8137fe0b88af08a8380fede4d928`  
		Last Modified: Fri, 17 Apr 2026 00:29:15 GMT  
		Size: 195.1 KB (195147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f1fad8443220a748fe2c2769ac5eb596b74c5ecac4db1ecfc6a84f1b70eb31`  
		Last Modified: Fri, 17 Apr 2026 00:29:14 GMT  
		Size: 24.9 KB (24913 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:7b3c9bfcf98c50ec5c5c45ae24145fc2cfa801b3327830d52a006d3913e394ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68542708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173795d68de4dd28ced1e7c103dfb6a8ccbaae687fb8356362dc5f3b8c5d68f3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:26:43 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 17 Apr 2026 00:26:51 GMT
ENV GOLANG_VERSION=1.26.2
# Fri, 17 Apr 2026 00:26:51 GMT
ENV GOTOOLCHAIN=local
# Fri, 17 Apr 2026 00:26:51 GMT
ENV GOPATH=/go
# Fri, 17 Apr 2026 00:26:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:26:51 GMT
COPY /target/ / # buildkit
# Fri, 17 Apr 2026 00:26:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 17 Apr 2026 00:26:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527bee0f073751f66f273363b2cc8a94a04b321edb76fa53995078c17cd216a3`  
		Last Modified: Fri, 17 Apr 2026 00:27:07 GMT  
		Size: 291.9 KB (291898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e89efc4b5ec39fa30d639b12ad2c7fd994a11ffa608e77427a882d73768d76`  
		Last Modified: Tue, 07 Apr 2026 21:13:44 GMT  
		Size: 64.1 MB (64108758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d63976fe65d4b982eac540ded960317b6669121d7737d2545bfd522de84a3d6`  
		Last Modified: Fri, 17 Apr 2026 00:27:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:bed0b9eecedbf8dc54892f895e3a6060bf57f0a02b168f6298c524e22fd8cbcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f833b1dcbf191eef06283a8bcb1c7f9e447351c01d8c23841b3bfbedcb82395`

```dockerfile
```

-	Layers:
	-	`sha256:97692731fd40a6d1efdf9b95793ad1a8a00caa1343ff6767163f37a7edeac268`  
		Last Modified: Fri, 17 Apr 2026 00:27:07 GMT  
		Size: 195.2 KB (195183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b93b3bf15ddc923ec45a70907a45e4737d250bbc79295513cc37d06212001670`  
		Last Modified: Fri, 17 Apr 2026 00:27:07 GMT  
		Size: 24.9 KB (24941 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:f4129399655961ddde0f0b9bfeb259cb4e39866746fd917b4150d6907f6d17ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69454272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf879ebb117863934a6b9f49ac514ec3c1b97d04ffc0ae30e5dc6ffd49fae02`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:14:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:14:30 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:14:30 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:14:30 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:14:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:14:30 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:14:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:14:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532811068730c9b22d3bd442e4fca2d64a5642e86a062043ff60e4658c9c6823`  
		Last Modified: Tue, 07 Apr 2026 21:14:46 GMT  
		Size: 291.6 KB (291617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8469b29d109e367ac43f3e67c104c046d01b1c6cca80443b728b2d38a262b476`  
		Last Modified: Tue, 07 Apr 2026 21:14:00 GMT  
		Size: 65.5 MB (65541767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142816441af8199349bbf2a6b237808713d0b8d0d3e28fd8981d432494f83a2c`  
		Last Modified: Tue, 07 Apr 2026 21:14:45 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:6b2ca3c69b760c25d4d6aecf4baf6a465a11208a91b989deb9f36a43808dbf24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 KB (220544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e9f3bd51ac1ecf7b1dce1dc0f5133a9a215a3db20bfc895bdc1d48533bb703`

```dockerfile
```

-	Layers:
	-	`sha256:eca93653b5a4dcde2871b12026293529aaa3cc9b90f1e737c247535519c79abd`  
		Last Modified: Tue, 07 Apr 2026 21:14:45 GMT  
		Size: 195.8 KB (195773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c753e1f24403a8563a8113918f82438552e028b2c67aac8a31133544c6cb0a1b`  
		Last Modified: Tue, 07 Apr 2026 21:14:45 GMT  
		Size: 24.8 KB (24771 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:471963d2d4c7070d93c3176f19c69692fe22d5a8557d3bc3e7f4acab8238f16a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68787021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b34c4e7ecbcd37956c8eb7aea41296a5475dac1a20feae7bb94b2f3f727b18`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:17:06 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:27:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:27:19 GMT
COPY /target/ / # buildkit
# Fri, 17 Apr 2026 01:17:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 17 Apr 2026 01:17:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573996c1704299f203b95192cb9a61f40867e3dd7bfdbb9d3428c371304bd492`  
		Last Modified: Fri, 17 Apr 2026 01:17:54 GMT  
		Size: 292.4 KB (292441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fa701b604ea6f9fea3ed6559e2106d2a891e54c2977fbb8bdbf9d75d69aa40`  
		Last Modified: Tue, 07 Apr 2026 21:28:13 GMT  
		Size: 64.8 MB (64757766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c891dd4ae046679c1687589c197d8153faf17642addb2be03543f6897f0019`  
		Last Modified: Fri, 17 Apr 2026 01:17:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:f4c65bd2a336d5e5858c2d1088c9e9c654f67fc6b824d958c5aea300d93b771d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 KB (218080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7282342035a2b7346ae9968b89d6f562bfe725213a4ea476161bc2a1324fe18a`

```dockerfile
```

-	Layers:
	-	`sha256:3b3206d3c733f8b0ace02999b3ad197c685cae19eb77058ccca687a7bf7a9e0b`  
		Last Modified: Fri, 17 Apr 2026 01:17:54 GMT  
		Size: 193.2 KB (193226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3966b96090b2fedbb42b40bfdd9cc87a2d8b16c8411e8435de5d467a2d36b49a`  
		Last Modified: Fri, 17 Apr 2026 01:17:54 GMT  
		Size: 24.9 KB (24854 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:2ccb9e2aee77b4f734d09e3d8726e59a7e7ab1b00514c09cb049b46b5ed65763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68902949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f0bbdd3f4bdb09e7aeaf4fea4735953c6d54164574c39aa3359607514f8322`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 09:33:17 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:31:22 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:31:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:31:22 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:31:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:31:22 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:36:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:36:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ffd6ced4c894ab06d11bb63b601a98fc1d0536c2ff8bedffe653c521058ea`  
		Last Modified: Tue, 24 Mar 2026 09:34:58 GMT  
		Size: 291.5 KB (291515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7d1d0582748c5d1e12dadbe34ea1c9ef1815ea945fc3f044f96549146c6e58`  
		Last Modified: Tue, 07 Apr 2026 21:34:28 GMT  
		Size: 65.1 MB (65093854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36db47b53633837a8f42a2b2cb282f4046d841119ec0e31f1eb89250ef763987`  
		Last Modified: Tue, 07 Apr 2026 21:37:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:f07a7ec0621f611abf54217eb1fcfd0bd503b0aacc34a70d364fcc721db6df90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8ad2573bc79855adb9dd6f037ecf2ab2bdb88a0d3d8c6e029c18a2ab315475`

```dockerfile
```

-	Layers:
	-	`sha256:7fe0fed988e12f765e2e17bd377ea0e54dadb63897c8c9095de9acce5eaa7b2e`  
		Last Modified: Tue, 07 Apr 2026 21:37:22 GMT  
		Size: 193.9 KB (193909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4be754fb7b17607d24edd412b181ef8d59df714b51007e2cb7e17d15225b8f3c`  
		Last Modified: Tue, 07 Apr 2026 21:37:22 GMT  
		Size: 24.9 KB (24855 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:b7cc538906ba1e5be4a26cddbd867925294ac3571ea673cd0fe9e07988848450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70376691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf116fd7083c245ba50e042bc5ab31fa1b4b89ce419634b54534ead8583df0f2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:41:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:13:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:13:11 GMT
COPY /target/ / # buildkit
# Fri, 17 Apr 2026 00:42:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 17 Apr 2026 00:42:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0222edc5317b2dc2298df74fb4a61c9a344e0cd003e6bcd18f12349c6aee5d`  
		Last Modified: Fri, 17 Apr 2026 00:42:21 GMT  
		Size: 290.5 KB (290476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80b37d7575305ba979d392f19380204aa402def17a0f42736f2c66c815c079e`  
		Last Modified: Tue, 07 Apr 2026 21:15:15 GMT  
		Size: 66.4 MB (66432184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c49503a4e2d600d9a611a3613d8d717f74ee138b363f7bcc9d431274f2b87a`  
		Last Modified: Fri, 17 Apr 2026 00:42:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:88cecf735a27193e508b3333e602364e620756ed60e389fbb5b9a78f5b357d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.0 KB (217983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2102e4ab039df5e49dd30332464eef541512d295dd407f71179209d083e6b5fa`

```dockerfile
```

-	Layers:
	-	`sha256:0cdf32c3702136c3fb67d73f730c053cf3936f9b276b1824933f64bc9904f398`  
		Last Modified: Fri, 17 Apr 2026 00:42:21 GMT  
		Size: 193.2 KB (193176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5bc5366622bcfa383e05a60cd08803d5423fa475a7900ec00c427fd330f3343`  
		Last Modified: Fri, 17 Apr 2026 00:42:21 GMT  
		Size: 24.8 KB (24807 bytes)  
		MIME: application/vnd.in-toto+json
