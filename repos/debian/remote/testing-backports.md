## `debian:testing-backports`

```console
$ docker pull debian@sha256:50aad0c9e75483f1d62751d633575fe18c1cf0ac7d1cd86b33801adc015bbe3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
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
$ docker pull debian@sha256:24bb20bb42cad52f14a12562ce44f9f42d1b4e020e58c1c8ddc0448f6665178a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55754427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701d57836f2b76712c5a5c2aea825ab252fd13adc995918b020234ae545703c2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:06:58 GMT
ADD file:b73203ff651eb3f27ab9c4a7c28a6755505d1cf75a460d3d0a00e1d77e6efc0e in / 
# Thu, 17 Mar 2022 04:06:59 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 04:07:03 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:be551d0f976eb440c1b93a9408e36752142151abf4d1a1c0972a21f347227b74`  
		Last Modified: Thu, 17 Mar 2022 04:14:26 GMT  
		Size: 55.8 MB (55754204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f93d2b6ac71c7deb3a8d3f2f818b442133707f35cd24e1ea461c8c7d493acb`  
		Last Modified: Thu, 17 Mar 2022 04:14:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:6266254c9bb4a10acd32de42f1af642a33de1d4cd08f14617645b4d3596f43c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53139297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5179d1869d2964ccd89838f1d285ca14b6e0ac2c209d8c4de6fd1649675a2a5a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 05:25:46 GMT
ADD file:dc5b93b1740a9ef205260e1e4c01e82ed4a3548089d6d6f5055c92f14d2cd223 in / 
# Thu, 17 Mar 2022 05:25:46 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 05:25:59 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e0e0ad2f286495a2f826121d61f5f1eb200ee6ac209a8ab2a7528044e6253e17`  
		Last Modified: Thu, 17 Mar 2022 05:43:34 GMT  
		Size: 53.1 MB (53139073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167b742fba3e570b943b781ad88f8e1dbedf289add509983e6db5c24358fb485`  
		Last Modified: Thu, 17 Mar 2022 05:43:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:4eae2988746d07856d2e191bc9437596abc6b49ebee22ff7649b41411710cc37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50761964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7d1e59be91978ec86d4ec104628e18228a1654eaecebff109f66835d5472a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:37:30 GMT
ADD file:e48122605a6ad12bf999cb26f6fe881ad2ec1939ab5474e408297deab0a70fca in / 
# Thu, 17 Mar 2022 09:37:31 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 09:37:43 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:eea842a9758d1e19604d8dd7a26043f0985dda6ccc4f9a5cb2d561c013878adb`  
		Last Modified: Thu, 17 Mar 2022 09:54:18 GMT  
		Size: 50.8 MB (50761740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b1701277c0f2adbad1edb07aeb91874fc79c9a17b01120cd71384e921d85f2`  
		Last Modified: Thu, 17 Mar 2022 09:54:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:14d5fe03d40a7f219199a03fe20b3919d4547f51b02391ebd827ba0a69e228d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54668221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81584b770d524007ec60d6c17da01835bd3a8fb205d265d0287ac034b8d7753d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:24:27 GMT
ADD file:80ce6b59df4a0234aef0fab1a3d5dce8227ac2503bf797cce72cd3991380b16f in / 
# Thu, 17 Mar 2022 03:24:29 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 03:24:34 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a5f8037aec3dd841314901f25fb22b57dab74f5428d97a5eb6b6c1c3f5c189ba`  
		Last Modified: Thu, 17 Mar 2022 03:33:23 GMT  
		Size: 54.7 MB (54667996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d0f3244b30ac740815c28c3783daa2bca9b3ae828322df64ad2ec30a5a16e5`  
		Last Modified: Thu, 17 Mar 2022 03:33:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:cf905862bc758ea8b033384550e4fae1fdd6db303a77ffacd9e8a808896248ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56786344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd31b06297df4fc0dbf5d00f31ad499c5404a263e9b91dc1a3eeddc5e7f1c6c1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:19:03 GMT
ADD file:f07cda6f1f339bd120e4bf36822d73f6ac1613acb202af6dc3b3d4af673aaea7 in / 
# Thu, 17 Mar 2022 08:19:04 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:19:09 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:41f7caf1bbf6875c1fd4b1ffa0ff0fbaf06cdefefc340ae6c143560a557eaa86`  
		Last Modified: Thu, 17 Mar 2022 08:29:22 GMT  
		Size: 56.8 MB (56786120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d2a87e2c20f5c4b3c3445a1e6f2e8c57d464a1bb72d4e289bf09c94f260ac4`  
		Last Modified: Thu, 17 Mar 2022 08:29:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:d0f67eda44af99b7596d6d996c43fbe2d26407026c79344c7e3cc228e81cb6e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54412607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2483d8799fb193db1c05acfd09f065281723839b69cb7738b3afb2ec7b19e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:07:23 GMT
ADD file:2ff6130674858ade10e1446423b258c28dbc756b9edc3bb0c1604f7e97162e82 in / 
# Tue, 01 Mar 2022 02:07:25 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:07:31 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c74f313d79a92468c004a2e62c5e8be074866491cabf1d87df92d2f3e5d6e615`  
		Last Modified: Tue, 01 Mar 2022 02:17:59 GMT  
		Size: 54.4 MB (54412382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c235fc2acd6d8139c9cd26792c60451ab12640eed5893909d8dbb9a24b81b10a`  
		Last Modified: Tue, 01 Mar 2022 02:18:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:a389d897fd17aa8644c560e184d31d7c3464c250515da14408556a4dc30084eb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60166509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7566a47475a2b7fe4fcf458e361212fd5d2f9ec45544165d0b332d8aca3d094`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:09:22 GMT
ADD file:ecbae239a294b05483b5400d24edacdf29c149c700631f2b5532a4a4abb2b6ae in / 
# Tue, 01 Mar 2022 02:09:28 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:09:40 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:91cc91972e5f07c31b49a5a17e3b7279431ecfbd12c3ad333e61d0c4e87d015b`  
		Last Modified: Tue, 01 Mar 2022 02:19:12 GMT  
		Size: 60.2 MB (60166284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e470b04d4fb0283fa910bbdba2e46ddaaffa9d83cf9851a5b81d4e2c6a60d77a`  
		Last Modified: Tue, 01 Mar 2022 02:19:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:40c55f2bd8e38a5d16379d810d2bd24b855dcd1ba956621efcdc9f23a9c5c240
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54000925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984f640543c74b45204a20e33f116624a4e69c1d3d31e319e28418e485f65667`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:09:05 GMT
ADD file:6eb397f5eedde7035cdb2bf9111259ff2e90682463e5019a0378e8a1f429ffee in / 
# Thu, 17 Mar 2022 03:09:09 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 03:09:16 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:373c0d1a4ca5b7de38c634b77e4e81cc2544d5d8d1dc697e268a5329abbb6fbe`  
		Last Modified: Thu, 17 Mar 2022 03:14:49 GMT  
		Size: 54.0 MB (54000700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b119aa47295b8fe45e4d690d9e8293fca545bd054c91240385b4e41dbd7bc4d9`  
		Last Modified: Thu, 17 Mar 2022 03:14:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
