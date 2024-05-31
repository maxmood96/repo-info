## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:552cc357330299af31f4423cdc16d62134af38224b45e9a23539433679c4f16c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:22f4e94698ff19cca859654c30bfdbc5c6aef2889b596fcce3bfd5e463655020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6490391a89e51eb7d46952bc649b6a3ab18926e30ea9f459f376d4b90c48ef0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d4c3c94e5e10ed15503bda7e145a3652ee935c0b2e9de9b5c98df7ec0a0cd925`  
		Last Modified: Sat, 27 Apr 2024 14:54:51 GMT  
		Size: 27.5 MB (27511657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d5c32b56a7bb4f3bc718412ea8bd648edb0660f1231f7f8e7454518b7b9cc6`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 5.4 MB (5360241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64b1e5dcb5bc5ea11cc316a30022dd544be08e7ff35bff0c49b019a293e7c7f`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ca3b8c895950389becd9bd41f45bc1692e32ad08257b9dc050e454019fe9b8`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f62fa24fc1f5ece4b6afd0dda81f7d6677cacd6f8c2289c7688b0e7daea1c70`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 105.2 KB (105234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f63c65c3b418ae41a5635f8be194cfdf4c957c0b26ea2e8b1e7d2716748fe4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1991312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9469e71351bdf024ae1eedc2f364e1c30d8289b20b89a56d6945145683efae9`

```dockerfile
```

-	Layers:
	-	`sha256:24273410e30ea80c582c3b6b7d44dd6d61822ef648ec3684096e1624714774d8`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 2.0 MB (1977956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7713f1a8595ad80b05b7290f60a0f2811f96a292da47fe498dd6cefbc445ec9`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 13.4 KB (13356 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:12d87894dcf40f73f1dc0981a999188ec9339d9647de3f5f467680b92b3d5562
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32923360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d72f1bf58338578515814f40c9b1763b3d773724e54030661b42de5e43da7a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:51:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:51:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 02 May 2024 03:51:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 02 May 2024 03:51:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:83049506c6eb6b11ef1a8774b3486a01a1804f7d13bd230b44788bc63248282d`  
		Last Modified: Mon, 29 Apr 2024 19:12:05 GMT  
		Size: 27.2 MB (27206145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4fdca9bff7469fb7f91efc5d4f1ee7651f285906bf8e776665d68a49b7e5af`  
		Last Modified: Thu, 02 May 2024 03:53:02 GMT  
		Size: 5.5 MB (5475090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ed250aa69514898898f0c3da8f72239ddb8fa82d8bd4f34c01eb9e3f4e43e7`  
		Last Modified: Thu, 02 May 2024 03:53:01 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a252a424d41765180fb5016b6a8c8e15e54a40f5f4f6c9f19da63ee8e0ff06df`  
		Last Modified: Thu, 02 May 2024 03:53:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56680e3134396295ee20c1269290ebc4f52c7f1e111adcedc031e51f2db6f86f`  
		Last Modified: Thu, 02 May 2024 03:53:02 GMT  
		Size: 240.1 KB (240111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
