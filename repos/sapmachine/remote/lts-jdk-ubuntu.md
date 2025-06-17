## `sapmachine:lts-jdk-ubuntu`

```console
$ docker pull sapmachine@sha256:dadc5a5c8383840988460b17e53083674b398dcccaa758119432d14321ecf125
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:d5f207e361d87c282c1f72ce4fb5a1a9443d0dd03839c674fd8f0f62019c3334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244836056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50126a0861c4ce9891079856c6d1c697c2e87d270f0cf9f98e4d92f0019369f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561be86f29e7fcaf4b4181d6462c52fff294fe5a23fbe7accdbd859857134f64`  
		Last Modified: Tue, 03 Jun 2025 13:33:43 GMT  
		Size: 215.1 MB (215120719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1788fe014e95f51c0fc828a8fc6334713a5affa6da21ecb7e10df51c4ea14937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2511738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c67c5a0d5ef0461c000ad5858782289109c11f40ccf1cade69e9f9234b0f5f`

```dockerfile
```

-	Layers:
	-	`sha256:74ce0b56a9ecdd9c566310ac9d3bae6bfe747ba3184295b2186b93552029770e`  
		Last Modified: Tue, 17 Jun 2025 09:52:15 GMT  
		Size: 2.5 MB (2498419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:122db0ce9bc629bf01e51c2d96ac5795cd4d3f0de20c4c30a0e67fc2af2eecf0`  
		Last Modified: Tue, 17 Jun 2025 09:52:16 GMT  
		Size: 13.3 KB (13319 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:86bc90360fc643b0a0dd51df9545386e215505b1a4214524a371500af8fa80cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242238836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc92ba98e87a89ea57c3a2c6631fb0f48abce2f19c55e152bacd31371c0f4c64`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3615e74a277bf6ee87e30e40c7bcb0e2b9666d34c5c69d32de53ee13bbce7036`  
		Last Modified: Tue, 03 Jun 2025 19:36:20 GMT  
		Size: 213.4 MB (213386937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5561db3a97ef02c0963a7d758e6811137e9ca5d8accaad044b7d8202c7f27a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2512646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aac5e5e912cb4719f4d17562bf168ea81c1a4b4160b255781072ac2331d6046`

```dockerfile
```

-	Layers:
	-	`sha256:786e44422814afec73962ac08fcbaacfe692c957c17a3c6556e65b099c154b4d`  
		Last Modified: Tue, 03 Jun 2025 05:59:16 GMT  
		Size: 2.5 MB (2499055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fab5bf932fdf1fe4ae5c54cee562acfc9f49a3bca3ef0f967529daa20453474d`  
		Last Modified: Tue, 03 Jun 2025 05:59:16 GMT  
		Size: 13.6 KB (13591 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ef0ff94dbff02e221dc756b408e9c357ab52c740acdad9540d3780c990a32e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250856398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab5388ebb91af447d8936c185b47f1b3e899f3ac3852bfc96a119525a5e5e4b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c2f42758fd8b0e8e371753d0c0faf79b7ddf4b494c6651d3a7e8b6469f01c1`  
		Last Modified: Wed, 04 Jun 2025 01:04:31 GMT  
		Size: 216.5 MB (216531188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9b03ce49ab844ab0a0052f4fad8a83b83628a04541ef21833a70fe82e3297d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2514077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bbe2d07f8ac9d3427d1785c69487accd99ebf9eefcecd3742f54e449f3deb26`

```dockerfile
```

-	Layers:
	-	`sha256:0586ba0f24ce24f884999b3149dc2b2d8c74b101da3d2d1efcfa96324212c316`  
		Last Modified: Tue, 03 Jun 2025 05:57:42 GMT  
		Size: 2.5 MB (2500630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e34135f88826843ad930b5220985ba3c0f8b5f64508381da8f2dfee90c8b3e3`  
		Last Modified: Tue, 03 Jun 2025 05:57:41 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json
