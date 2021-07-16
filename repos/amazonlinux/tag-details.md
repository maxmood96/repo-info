<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazonlinux`

-	[`amazonlinux:1`](#amazonlinux1)
-	[`amazonlinux:1-with-sources`](#amazonlinux1-with-sources)
-	[`amazonlinux:2`](#amazonlinux2)
-	[`amazonlinux:2-with-sources`](#amazonlinux2-with-sources)
-	[`amazonlinux:2.0.20210701.0`](#amazonlinux20202107010)
-	[`amazonlinux:2.0.20210701.0-with-sources`](#amazonlinux20202107010-with-sources)
-	[`amazonlinux:2018.03`](#amazonlinux201803)
-	[`amazonlinux:2018.03-with-sources`](#amazonlinux201803-with-sources)
-	[`amazonlinux:2018.03.0.20210521.1`](#amazonlinux2018030202105211)
-	[`amazonlinux:2018.03.0.20210521.1-with-sources`](#amazonlinux2018030202105211-with-sources)
-	[`amazonlinux:latest`](#amazonlinuxlatest)
-	[`amazonlinux:with-sources`](#amazonlinuxwith-sources)

## `amazonlinux:1`

```console
$ docker pull amazonlinux@sha256:d8db8960d84895fb10e491080d4069ac542aa06205a9ccf3af202a927d561bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7326b7afba891588bce0cb6a6244f9bb205bbbb7ad7b6a719e356ad8e878102b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62233767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07431b5cc2148664c7fd5c2f4e6c47bc7386eca1abd67ccc506240521e2a6dc4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 23:47:34 GMT
ADD file:d54600120dd0df387f02c9986b95553c7be4690d3226e5693a0621e1bbba9c79 in / 
# Thu, 03 Jun 2021 23:47:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8aa1c9f768e700368fba92ab67c462b5757d5e5d801b2309ce0ac018cc7a13e9`  
		Last Modified: Thu, 03 Jun 2021 23:48:24 GMT  
		Size: 62.2 MB (62233767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:1-with-sources`

```console
$ docker pull amazonlinux@sha256:bd7aca583738a44ccabf6582caa32ea1b3dbd5ffff26e0606c0f1a6a0515d8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:80878ae39f9fe1a9a950ff72ea175f41144032442c3e84f3635a135f7de32f57
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.1 MB (449096717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce78d0c69b908a315c3a8930d9e6bccef3317b485528e31c72acff0cb546755a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 23:47:34 GMT
ADD file:d54600120dd0df387f02c9986b95553c7be4690d3226e5693a0621e1bbba9c79 in / 
# Thu, 03 Jun 2021 23:47:35 GMT
CMD ["/bin/bash"]
# Thu, 03 Jun 2021 23:47:54 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-dc5d92c927a9f79aab7658e5c05df877dd40282d7bf9b4b11a5eb11b225cb7ad.tar.gz"  && echo "03509f1ca8f0593cf761a9fda3dc71baf0f45752a0d8908a04ccd9937bd1ddfc  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:8aa1c9f768e700368fba92ab67c462b5757d5e5d801b2309ce0ac018cc7a13e9`  
		Last Modified: Thu, 03 Jun 2021 23:48:24 GMT  
		Size: 62.2 MB (62233767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732b4f3ad9bb7c123e4d3b3582e82bff05e5f83438191ad98a2d271e235ff1c2`  
		Last Modified: Thu, 03 Jun 2021 23:48:58 GMT  
		Size: 386.9 MB (386862950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2`

```console
$ docker pull amazonlinux@sha256:3c3e9bb7dd5a41f171c8537a4493c707ce4ef3299d8e872ba2a9e765c3948d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2` - linux; amd64

```console
$ docker pull amazonlinux@sha256:8d6b5629641d79da29897c315e7905f8848e7dc26024c6d18e3136269728d1ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61966006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add9612f9214d711fe7587b00bbcfef289e0b28b28c76acf6e880b61aac123e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jul 2021 23:38:14 GMT
ADD file:87c0c8c13a50d18c9b35e048d635d04fcd6fc06e9416c68a5c3024c83b166177 in / 
# Thu, 15 Jul 2021 23:38:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:430235fb155c55a4e5a8c494a918c1d1bf2473e93cc35c4242ae089785dc1a42`  
		Last Modified: Fri, 09 Jul 2021 13:29:48 GMT  
		Size: 62.0 MB (61966006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:498f90fe9367d8434d69b4fdc2a26db4d86fb7172391b07739563ad3b693813e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63567892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee31c9549c007652c5924c734ee77f0a075148cdf5d85a5d6eaf5cafd9818117`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Jul 2021 00:09:26 GMT
ADD file:555fe2ebaf4a5e69a533b39ac234d3f7c6d7de6333e2882558b1b92f1320c8a9 in / 
# Fri, 16 Jul 2021 00:09:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6bc2b81b61fecbd717658fab4af4ed0a6b9e5a2e28323439c47d57a34db1908f`  
		Last Modified: Fri, 16 Jul 2021 00:10:24 GMT  
		Size: 63.6 MB (63567892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:45f8f3ddda7d66e494f8ae7e43a56cef0b31c423504b9acd90e84e1bb4ba328a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:11acf20c469405ac7d36fe6f1146981e2f086e58cfd197e645e4304adc5602b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.9 MB (542932383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a3aa430390cc3551dbadb7ceb4b7e9119c300349628add2429007752297b84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jul 2021 23:38:14 GMT
ADD file:87c0c8c13a50d18c9b35e048d635d04fcd6fc06e9416c68a5c3024c83b166177 in / 
# Thu, 15 Jul 2021 23:38:15 GMT
CMD ["/bin/bash"]
# Thu, 15 Jul 2021 23:38:40 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-0b02afd67a4ca356cddc2458f97e9d05c0057c8be3ea2fd746f2cb8f8117ce4f.tar.gz"  && echo "3ff5c45e8ab1cc7d959cec030bfe3c669cf7a22bab24ec55aaf5a76aab1b67ed  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:430235fb155c55a4e5a8c494a918c1d1bf2473e93cc35c4242ae089785dc1a42`  
		Last Modified: Fri, 09 Jul 2021 13:29:48 GMT  
		Size: 62.0 MB (61966006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072db9cf814d1bef3d48502777d5d881376a7a36685281fd7723509e9871a13a`  
		Last Modified: Thu, 15 Jul 2021 23:40:01 GMT  
		Size: 481.0 MB (480966377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:59f947973020d2a73fe81007ffd0468d955e95ff5181af0e3958e16039618d09
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.5 MB (544534270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8dabafcf2886c1eac2c6606a5866207e7382ee896476435185cec501f56345`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Jul 2021 00:09:26 GMT
ADD file:555fe2ebaf4a5e69a533b39ac234d3f7c6d7de6333e2882558b1b92f1320c8a9 in / 
# Fri, 16 Jul 2021 00:09:27 GMT
CMD ["/bin/bash"]
# Fri, 16 Jul 2021 00:09:49 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-0b02afd67a4ca356cddc2458f97e9d05c0057c8be3ea2fd746f2cb8f8117ce4f.tar.gz"  && echo "3ff5c45e8ab1cc7d959cec030bfe3c669cf7a22bab24ec55aaf5a76aab1b67ed  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:6bc2b81b61fecbd717658fab4af4ed0a6b9e5a2e28323439c47d57a34db1908f`  
		Last Modified: Fri, 16 Jul 2021 00:10:24 GMT  
		Size: 63.6 MB (63567892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148cf00e9b2fc6dadadba404bd9be76a17c6c13757bca7f0146fd5aa2b5d4293`  
		Last Modified: Fri, 16 Jul 2021 00:11:04 GMT  
		Size: 481.0 MB (480966378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20210701.0`

```console
$ docker pull amazonlinux@sha256:3c3e9bb7dd5a41f171c8537a4493c707ce4ef3299d8e872ba2a9e765c3948d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20210701.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:8d6b5629641d79da29897c315e7905f8848e7dc26024c6d18e3136269728d1ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61966006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add9612f9214d711fe7587b00bbcfef289e0b28b28c76acf6e880b61aac123e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jul 2021 23:38:14 GMT
ADD file:87c0c8c13a50d18c9b35e048d635d04fcd6fc06e9416c68a5c3024c83b166177 in / 
# Thu, 15 Jul 2021 23:38:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:430235fb155c55a4e5a8c494a918c1d1bf2473e93cc35c4242ae089785dc1a42`  
		Last Modified: Fri, 09 Jul 2021 13:29:48 GMT  
		Size: 62.0 MB (61966006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20210701.0` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:498f90fe9367d8434d69b4fdc2a26db4d86fb7172391b07739563ad3b693813e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63567892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee31c9549c007652c5924c734ee77f0a075148cdf5d85a5d6eaf5cafd9818117`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Jul 2021 00:09:26 GMT
ADD file:555fe2ebaf4a5e69a533b39ac234d3f7c6d7de6333e2882558b1b92f1320c8a9 in / 
# Fri, 16 Jul 2021 00:09:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6bc2b81b61fecbd717658fab4af4ed0a6b9e5a2e28323439c47d57a34db1908f`  
		Last Modified: Fri, 16 Jul 2021 00:10:24 GMT  
		Size: 63.6 MB (63567892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20210701.0-with-sources`

```console
$ docker pull amazonlinux@sha256:45f8f3ddda7d66e494f8ae7e43a56cef0b31c423504b9acd90e84e1bb4ba328a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20210701.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:11acf20c469405ac7d36fe6f1146981e2f086e58cfd197e645e4304adc5602b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.9 MB (542932383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a3aa430390cc3551dbadb7ceb4b7e9119c300349628add2429007752297b84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jul 2021 23:38:14 GMT
ADD file:87c0c8c13a50d18c9b35e048d635d04fcd6fc06e9416c68a5c3024c83b166177 in / 
# Thu, 15 Jul 2021 23:38:15 GMT
CMD ["/bin/bash"]
# Thu, 15 Jul 2021 23:38:40 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-0b02afd67a4ca356cddc2458f97e9d05c0057c8be3ea2fd746f2cb8f8117ce4f.tar.gz"  && echo "3ff5c45e8ab1cc7d959cec030bfe3c669cf7a22bab24ec55aaf5a76aab1b67ed  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:430235fb155c55a4e5a8c494a918c1d1bf2473e93cc35c4242ae089785dc1a42`  
		Last Modified: Fri, 09 Jul 2021 13:29:48 GMT  
		Size: 62.0 MB (61966006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072db9cf814d1bef3d48502777d5d881376a7a36685281fd7723509e9871a13a`  
		Last Modified: Thu, 15 Jul 2021 23:40:01 GMT  
		Size: 481.0 MB (480966377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20210701.0-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:59f947973020d2a73fe81007ffd0468d955e95ff5181af0e3958e16039618d09
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.5 MB (544534270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8dabafcf2886c1eac2c6606a5866207e7382ee896476435185cec501f56345`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Jul 2021 00:09:26 GMT
ADD file:555fe2ebaf4a5e69a533b39ac234d3f7c6d7de6333e2882558b1b92f1320c8a9 in / 
# Fri, 16 Jul 2021 00:09:27 GMT
CMD ["/bin/bash"]
# Fri, 16 Jul 2021 00:09:49 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-0b02afd67a4ca356cddc2458f97e9d05c0057c8be3ea2fd746f2cb8f8117ce4f.tar.gz"  && echo "3ff5c45e8ab1cc7d959cec030bfe3c669cf7a22bab24ec55aaf5a76aab1b67ed  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:6bc2b81b61fecbd717658fab4af4ed0a6b9e5a2e28323439c47d57a34db1908f`  
		Last Modified: Fri, 16 Jul 2021 00:10:24 GMT  
		Size: 63.6 MB (63567892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148cf00e9b2fc6dadadba404bd9be76a17c6c13757bca7f0146fd5aa2b5d4293`  
		Last Modified: Fri, 16 Jul 2021 00:11:04 GMT  
		Size: 481.0 MB (480966378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03`

```console
$ docker pull amazonlinux@sha256:d8db8960d84895fb10e491080d4069ac542aa06205a9ccf3af202a927d561bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7326b7afba891588bce0cb6a6244f9bb205bbbb7ad7b6a719e356ad8e878102b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62233767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07431b5cc2148664c7fd5c2f4e6c47bc7386eca1abd67ccc506240521e2a6dc4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 23:47:34 GMT
ADD file:d54600120dd0df387f02c9986b95553c7be4690d3226e5693a0621e1bbba9c79 in / 
# Thu, 03 Jun 2021 23:47:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8aa1c9f768e700368fba92ab67c462b5757d5e5d801b2309ce0ac018cc7a13e9`  
		Last Modified: Thu, 03 Jun 2021 23:48:24 GMT  
		Size: 62.2 MB (62233767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03-with-sources`

```console
$ docker pull amazonlinux@sha256:bd7aca583738a44ccabf6582caa32ea1b3dbd5ffff26e0606c0f1a6a0515d8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:80878ae39f9fe1a9a950ff72ea175f41144032442c3e84f3635a135f7de32f57
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.1 MB (449096717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce78d0c69b908a315c3a8930d9e6bccef3317b485528e31c72acff0cb546755a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 23:47:34 GMT
ADD file:d54600120dd0df387f02c9986b95553c7be4690d3226e5693a0621e1bbba9c79 in / 
# Thu, 03 Jun 2021 23:47:35 GMT
CMD ["/bin/bash"]
# Thu, 03 Jun 2021 23:47:54 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-dc5d92c927a9f79aab7658e5c05df877dd40282d7bf9b4b11a5eb11b225cb7ad.tar.gz"  && echo "03509f1ca8f0593cf761a9fda3dc71baf0f45752a0d8908a04ccd9937bd1ddfc  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:8aa1c9f768e700368fba92ab67c462b5757d5e5d801b2309ce0ac018cc7a13e9`  
		Last Modified: Thu, 03 Jun 2021 23:48:24 GMT  
		Size: 62.2 MB (62233767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732b4f3ad9bb7c123e4d3b3582e82bff05e5f83438191ad98a2d271e235ff1c2`  
		Last Modified: Thu, 03 Jun 2021 23:48:58 GMT  
		Size: 386.9 MB (386862950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20210521.1`

```console
$ docker pull amazonlinux@sha256:d8db8960d84895fb10e491080d4069ac542aa06205a9ccf3af202a927d561bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03.0.20210521.1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7326b7afba891588bce0cb6a6244f9bb205bbbb7ad7b6a719e356ad8e878102b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62233767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07431b5cc2148664c7fd5c2f4e6c47bc7386eca1abd67ccc506240521e2a6dc4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 23:47:34 GMT
ADD file:d54600120dd0df387f02c9986b95553c7be4690d3226e5693a0621e1bbba9c79 in / 
# Thu, 03 Jun 2021 23:47:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8aa1c9f768e700368fba92ab67c462b5757d5e5d801b2309ce0ac018cc7a13e9`  
		Last Modified: Thu, 03 Jun 2021 23:48:24 GMT  
		Size: 62.2 MB (62233767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20210521.1-with-sources`

```console
$ docker pull amazonlinux@sha256:bd7aca583738a44ccabf6582caa32ea1b3dbd5ffff26e0606c0f1a6a0515d8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03.0.20210521.1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:80878ae39f9fe1a9a950ff72ea175f41144032442c3e84f3635a135f7de32f57
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.1 MB (449096717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce78d0c69b908a315c3a8930d9e6bccef3317b485528e31c72acff0cb546755a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 23:47:34 GMT
ADD file:d54600120dd0df387f02c9986b95553c7be4690d3226e5693a0621e1bbba9c79 in / 
# Thu, 03 Jun 2021 23:47:35 GMT
CMD ["/bin/bash"]
# Thu, 03 Jun 2021 23:47:54 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-dc5d92c927a9f79aab7658e5c05df877dd40282d7bf9b4b11a5eb11b225cb7ad.tar.gz"  && echo "03509f1ca8f0593cf761a9fda3dc71baf0f45752a0d8908a04ccd9937bd1ddfc  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:8aa1c9f768e700368fba92ab67c462b5757d5e5d801b2309ce0ac018cc7a13e9`  
		Last Modified: Thu, 03 Jun 2021 23:48:24 GMT  
		Size: 62.2 MB (62233767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732b4f3ad9bb7c123e4d3b3582e82bff05e5f83438191ad98a2d271e235ff1c2`  
		Last Modified: Thu, 03 Jun 2021 23:48:58 GMT  
		Size: 386.9 MB (386862950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:latest`

```console
$ docker pull amazonlinux@sha256:3c3e9bb7dd5a41f171c8537a4493c707ce4ef3299d8e872ba2a9e765c3948d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:latest` - linux; amd64

```console
$ docker pull amazonlinux@sha256:8d6b5629641d79da29897c315e7905f8848e7dc26024c6d18e3136269728d1ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61966006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add9612f9214d711fe7587b00bbcfef289e0b28b28c76acf6e880b61aac123e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jul 2021 23:38:14 GMT
ADD file:87c0c8c13a50d18c9b35e048d635d04fcd6fc06e9416c68a5c3024c83b166177 in / 
# Thu, 15 Jul 2021 23:38:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:430235fb155c55a4e5a8c494a918c1d1bf2473e93cc35c4242ae089785dc1a42`  
		Last Modified: Fri, 09 Jul 2021 13:29:48 GMT  
		Size: 62.0 MB (61966006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:latest` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:498f90fe9367d8434d69b4fdc2a26db4d86fb7172391b07739563ad3b693813e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63567892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee31c9549c007652c5924c734ee77f0a075148cdf5d85a5d6eaf5cafd9818117`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Jul 2021 00:09:26 GMT
ADD file:555fe2ebaf4a5e69a533b39ac234d3f7c6d7de6333e2882558b1b92f1320c8a9 in / 
# Fri, 16 Jul 2021 00:09:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6bc2b81b61fecbd717658fab4af4ed0a6b9e5a2e28323439c47d57a34db1908f`  
		Last Modified: Fri, 16 Jul 2021 00:10:24 GMT  
		Size: 63.6 MB (63567892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:45f8f3ddda7d66e494f8ae7e43a56cef0b31c423504b9acd90e84e1bb4ba328a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:11acf20c469405ac7d36fe6f1146981e2f086e58cfd197e645e4304adc5602b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.9 MB (542932383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a3aa430390cc3551dbadb7ceb4b7e9119c300349628add2429007752297b84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jul 2021 23:38:14 GMT
ADD file:87c0c8c13a50d18c9b35e048d635d04fcd6fc06e9416c68a5c3024c83b166177 in / 
# Thu, 15 Jul 2021 23:38:15 GMT
CMD ["/bin/bash"]
# Thu, 15 Jul 2021 23:38:40 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-0b02afd67a4ca356cddc2458f97e9d05c0057c8be3ea2fd746f2cb8f8117ce4f.tar.gz"  && echo "3ff5c45e8ab1cc7d959cec030bfe3c669cf7a22bab24ec55aaf5a76aab1b67ed  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:430235fb155c55a4e5a8c494a918c1d1bf2473e93cc35c4242ae089785dc1a42`  
		Last Modified: Fri, 09 Jul 2021 13:29:48 GMT  
		Size: 62.0 MB (61966006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072db9cf814d1bef3d48502777d5d881376a7a36685281fd7723509e9871a13a`  
		Last Modified: Thu, 15 Jul 2021 23:40:01 GMT  
		Size: 481.0 MB (480966377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:59f947973020d2a73fe81007ffd0468d955e95ff5181af0e3958e16039618d09
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.5 MB (544534270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8dabafcf2886c1eac2c6606a5866207e7382ee896476435185cec501f56345`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Jul 2021 00:09:26 GMT
ADD file:555fe2ebaf4a5e69a533b39ac234d3f7c6d7de6333e2882558b1b92f1320c8a9 in / 
# Fri, 16 Jul 2021 00:09:27 GMT
CMD ["/bin/bash"]
# Fri, 16 Jul 2021 00:09:49 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-0b02afd67a4ca356cddc2458f97e9d05c0057c8be3ea2fd746f2cb8f8117ce4f.tar.gz"  && echo "3ff5c45e8ab1cc7d959cec030bfe3c669cf7a22bab24ec55aaf5a76aab1b67ed  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:6bc2b81b61fecbd717658fab4af4ed0a6b9e5a2e28323439c47d57a34db1908f`  
		Last Modified: Fri, 16 Jul 2021 00:10:24 GMT  
		Size: 63.6 MB (63567892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148cf00e9b2fc6dadadba404bd9be76a17c6c13757bca7f0146fd5aa2b5d4293`  
		Last Modified: Fri, 16 Jul 2021 00:11:04 GMT  
		Size: 481.0 MB (480966378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
