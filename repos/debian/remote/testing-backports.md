## `debian:testing-backports`

```console
$ docker pull debian@sha256:c2584559d13d805ce2950da2004e3fc3977d4a0fe573deb8d699ad6f8e8b4f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:cd33e6682453818500afb3fc04ea7fe53742b2b8568b372138b35a48e18e7bf2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55578213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1641ad42e596beb5e31f1e99252b1999117efb89625e4252a62dde6702a2716`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:45 GMT
ADD file:b6d9d03d246917cd8a499e26b7dafcdd42ca61c3cbb6e60b78c888a349814210 in / 
# Tue, 17 Nov 2020 20:24:45 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:24:50 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a919358b170f991da872d2c4a5b2210ce45783166a93d65c90ee3cad6b86dbc8`  
		Last Modified: Tue, 17 Nov 2020 20:30:58 GMT  
		Size: 55.6 MB (55577988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c23c0cbec8cb56e79f68689adb24f09c38c8e3c7cc61cb759ee3ba2b325040`  
		Last Modified: Tue, 17 Nov 2020 20:31:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:62627ad98ab22a1ecbbf1a377255f25ea96a787dce403e8b11e03ac2ebf21831
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53174619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fba079cb37d66043a08861130fec87e4f4e363f149ecf91929b52c29177fe8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:26:49 GMT
ADD file:389a03ab4ddf6818faf0639b3a082c7b983f84e1d9314134442750182fcfcf29 in / 
# Tue, 17 Nov 2020 20:26:50 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:27:04 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:814eea095dfcbe1041c39cdf2ddd37b3ff85b14da1c3bdf9c5c8c9e60383f75c`  
		Last Modified: Tue, 17 Nov 2020 20:35:18 GMT  
		Size: 53.2 MB (53174394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87add481e9cf75e2e9dbf578d61e78c389e782a1fd33b3e56c4c2100810c10f`  
		Last Modified: Tue, 17 Nov 2020 20:35:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b6492f2a5475399f672ec360b6a121a891f9c5e05c512c8b4dc8e2c7e6a065fb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50757207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a0abc6a5ce7f8168bc43285b79bfab97f72bab373ae77faa662470592778d10`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:27:49 GMT
ADD file:6c63336c5c49a2dfed43416129b0e045999b900d218fbec7cf6830ae0dbd5bf3 in / 
# Tue, 17 Nov 2020 20:27:51 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:28:01 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e6490248107e3a403308ab6ccbc31b76e7ea8d3d48c8184f6501d809d1f8a606`  
		Last Modified: Tue, 17 Nov 2020 20:36:10 GMT  
		Size: 50.8 MB (50756981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2a16c3b7d5a1f1683060438325763e115fee96df369c7de75e88d78c513612`  
		Last Modified: Tue, 17 Nov 2020 20:36:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:568128087a4186ada2a63d29119bdbe6da59b5283627f8b257940c6edd844bdf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54323739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1f1c46a9b1786aa755a3d9b8b433d5348f429156d27577121f055bd4b290d0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:28:30 GMT
ADD file:d37369ae30ab48a0f2543398c3654e86c4974a89273a04c2eba7fa459d0bc05b in / 
# Tue, 17 Nov 2020 20:28:35 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:28:51 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:43bafc6092e82ecdff33419c83556ff270d573c7d3e94e242c50046b2cde340e`  
		Last Modified: Tue, 17 Nov 2020 20:34:59 GMT  
		Size: 54.3 MB (54323514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7fe6b62c1783e2c7b00e2aa7d85c19d2fce9f61d9382f1a36ecf0f8fd4376d`  
		Last Modified: Tue, 17 Nov 2020 20:35:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:013dd96cd2fa1ad18e4036abeb481c97d006d167dbc4e504320bb85cb86967f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56729041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80ccabc6474ea9c78132a7aff2affa40413e33ffb060a83b886af8904a82ff8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:44 GMT
ADD file:5d7125b48de3a64cd62eacba76795e462d306f38c7dece65208998e9e95ed52d in / 
# Tue, 17 Nov 2020 20:23:44 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:23:50 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f0742afdbddd96eeeb7ea72c2c3c446463155eb85ae05dc81f7d08c09a0d6315`  
		Last Modified: Tue, 17 Nov 2020 20:30:43 GMT  
		Size: 56.7 MB (56728818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e1ad62a7333ca0bdac338fd2554987bc583f96d95b552b8c32856ac00064ec`  
		Last Modified: Tue, 17 Nov 2020 20:30:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:b295398b4d859a5e337133c555be8e197fd33b4a5eb97a5c22dcb5c7c41d23d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53861836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35395d5f7210ee1632546fd1444e721d38fc46f9de1bb524010036ada9d19c0b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:41 GMT
ADD file:a754a6582929c3c72e89122948fe0dbc5d4032ea1b3ec3c3ffcb27b8d942196b in / 
# Tue, 17 Nov 2020 20:21:42 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:21:48 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dafe7e883a4098dcc8a47b53af85af92c19540a34948e979dc5a05940ad07c16`  
		Last Modified: Tue, 17 Nov 2020 20:30:05 GMT  
		Size: 53.9 MB (53861611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f9885a77ecbbb43f6d2b82cba303d8096b22e22b3b65df5423de7ed037a77f`  
		Last Modified: Tue, 17 Nov 2020 20:30:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:6fdbc6b954f72b01dd7beab2f94efbed76125f2172861f7461d69c32a663861c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59761661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf24b624151efb5a25c2f2a943e00868af702359b4a336f6c9b2dfe604ddab2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 23:25:16 GMT
ADD file:74e3f9199d8973f4d6859f7dfad98ea11e79e7829d5756710a16351f8c033596 in / 
# Tue, 17 Nov 2020 23:25:24 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 23:25:42 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ac668230de37b88984090c102d2d7b0848c85b72d33b9fe4aff709b7ef0074ed`  
		Last Modified: Tue, 17 Nov 2020 23:38:25 GMT  
		Size: 59.8 MB (59761435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff443da6ef37ef9c6f8f07cc7934240463f2f5ba6e21edc058b780c84ff850b`  
		Last Modified: Tue, 17 Nov 2020 23:38:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:3e613496ebffe1383299dc95f26c2e87edcb97af40ff2fb66cefc695d7a9a0f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53806427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e675b073b029ac696f39d735bbb4f2e4963266c5e20f5b0eb2b002382e12c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:29 GMT
ADD file:3a821b81168a1d7aad1e864fb90de7cf1092adb1399951e8f329675f23dfbd81 in / 
# Tue, 17 Nov 2020 20:20:40 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 20:20:47 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6af7e4bd3fcc2f09f363af50d2fc21a7fa6269e916e94ab50557691b40a4d931`  
		Last Modified: Tue, 17 Nov 2020 20:25:01 GMT  
		Size: 53.8 MB (53806203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d799e31fa4564944897b094d625a45b5f53dfb4ed4a01fd26453a05141df9`  
		Last Modified: Tue, 17 Nov 2020 20:25:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
