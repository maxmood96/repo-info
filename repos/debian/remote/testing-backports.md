## `debian:testing-backports`

```console
$ docker pull debian@sha256:0b8f63f918ae9378374e0720c6f2cc648d60d39b2dda44145c2177018097cec4
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
$ docker pull debian@sha256:1d611847b0e9d5bb5a41bc2dd71af44c1f8d9bde99bf67135217408643418f35
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49604351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f1d5af785338ac3d4aeb7c2d81a3437b0634062de6cea4a1208a173f3ba54d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:02:09 GMT
ADD file:36042be8656a51ef4a979fba2771303f588720eae5fac08f8afa0e6d412f7982 in / 
# Wed, 16 Aug 2023 01:02:10 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:02:14 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b4574cccfe7ec399ed14e1943c1271e2d03c88564d812dd627ba2d11d9757e16`  
		Last Modified: Wed, 16 Aug 2023 01:08:23 GMT  
		Size: 49.6 MB (49604129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6a7efd8ae49d56a3e990076331e1cf40262652fbea130e2f76647359a218a2`  
		Last Modified: Wed, 16 Aug 2023 01:08:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:dff4dea1e6b5d19e2a93c23a579fb635843b3dbd9697b20105ef5110ce3d93ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47395394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe438aa5eb21d8d003a92333887d79ad05c58ad1efc15dcfbfab3009226dc75`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:49:40 GMT
ADD file:5e83651ed24b5e4ef15b8f08928bf55bb69bf326bd2c74abf8f978804598162a in / 
# Tue, 15 Aug 2023 23:49:41 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:49:43 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:86f1da9e05d82606c06a57cacf13425ff6707ecb80697885b03a52539ca02b3d`  
		Last Modified: Tue, 15 Aug 2023 23:54:09 GMT  
		Size: 47.4 MB (47395172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f2854ce8d4ce99b2b8d9df48e2b7befa1aa3b31beaaa71d9be3d51366d2304`  
		Last Modified: Tue, 15 Aug 2023 23:54:17 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:ff854cc404ac11cd0059eae04860d2ac0aef975f60aabe465a592e0c73bd4514
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45176271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15cc6373060b9a26221e527843f406c100b94b8d59ad512537913d74bfd7056a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:19:18 GMT
ADD file:213e462a7d198459ba7531dd361a5bbbd3d2917e8c1baa7499cf248bf6ed4c42 in / 
# Wed, 16 Aug 2023 00:19:19 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:19:21 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c14c6529af12d61cb6065797640e1e3d228daebc7301900ddad281fe8e55fa17`  
		Last Modified: Wed, 16 Aug 2023 00:25:08 GMT  
		Size: 45.2 MB (45176048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0050a5ba4098a48f1044d08c594b59da586e211389d953294d9e28ef1d37d028`  
		Last Modified: Wed, 16 Aug 2023 00:25:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:837f5c9e83b7b9203fad0bf7fbe0c35c786f6586d214eabb539fb63acab33ec2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49522293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551b79016386ab268074676324a85cc91e6b81c7cf3aaf4e64f7628ed141c67f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:41:28 GMT
ADD file:4140d565c599e759836b448aa03732461eb29cbc683f3162d889a36569afd8fb in / 
# Tue, 15 Aug 2023 23:41:28 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:41:31 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:786a118997b083196267446ee0d1d1a908f05fd7748fa2ed8e7560d0db91bf72`  
		Last Modified: Tue, 15 Aug 2023 23:46:51 GMT  
		Size: 49.5 MB (49522071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de73fa2b0e5f203d25e13d5dcf0ec9596f20bbb869353bcc4b2a83d0b05e5deb`  
		Last Modified: Tue, 15 Aug 2023 23:47:00 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:849eb2ce1deef990e9db0062164d7cbd9b13715c9dd4f388a679e3bd67ba590c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50618662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4d6620c8dfe69c156af07d6a0035aecae0b7ce4069675b76f84830b023f9ff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:41:12 GMT
ADD file:a6c4f47b5f8dac4818251e5467ef149381281ebda173ce4edf783f1ba76fefee in / 
# Tue, 15 Aug 2023 23:41:13 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:41:15 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b599f8f04abd103aa7027fa31c11a44e706a3fcb77a3be9e4a64039851404afe`  
		Last Modified: Tue, 15 Aug 2023 23:47:43 GMT  
		Size: 50.6 MB (50618438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b99d82e229dcb931ec5dbf267a288192a06ee83793bf6c0c6ca1eb9c044d26e`  
		Last Modified: Tue, 15 Aug 2023 23:47:52 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:9c8b13472ab7d1049789b228f99b012ecb1979ec969779ac93483db5821700be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49450068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3807ad84476d0904bcf8c9f0144f9359b41ebd88b8fb58f7f24224284e625a26`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:14:09 GMT
ADD file:a5a82023399e544fa145de4a5810426dd39451072b850dd9c7cc15a943ad3e05 in / 
# Wed, 16 Aug 2023 00:14:14 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:14:29 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b4f611c1c9656c076152f7a2f7622bf265fa89bf95db7399c04625873fe2d3ef`  
		Last Modified: Wed, 16 Aug 2023 00:25:19 GMT  
		Size: 49.4 MB (49449844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0ab4af17bd7e56d400bd1e7485e2160f118e2eb4bf7cfdb56d6c06bedabfb0`  
		Last Modified: Wed, 16 Aug 2023 00:25:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:11f9379a9eeac5dc7fcad6771c5355d79c46722b7c60dbebc3cb886f978a99c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53544248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924f1571f0e82399b6020c14d2bd4cd902e64d304ca4d177c50a445555bcd373`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:12:15 GMT
ADD file:4433e8dd37785517f64787aed3c49969870b3fe51d72d741b71bc0e095dd25b1 in / 
# Wed, 16 Aug 2023 01:12:18 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:12:24 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b1f4b28b5f99b04d1ab247854921cdd11dfbc4328f395fc4e040da1a97088097`  
		Last Modified: Wed, 16 Aug 2023 01:20:05 GMT  
		Size: 53.5 MB (53544023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d96425df1f69dbd50ff2f7edd6645cd149fba6ff75a465059248d85edb8e377`  
		Last Modified: Wed, 16 Aug 2023 01:20:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:b99dbb106b46ac78ea7eee6a47b172dd8577e8a5a8715e554ddec7a29340f930
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48540022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d673dc01a65ea4552de87c7abf45e75344788e656e29f605cdacf28c8fa24fd1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:44:56 GMT
ADD file:8ee59edaaa7d4498cb111901a75ed6d7cfa7dc646dde70eabca650d719fb7d57 in / 
# Tue, 15 Aug 2023 23:45:03 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:45:11 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:977206ef11492cbb9ef774b7ffa955b2066c215ff2be2d1fbb83d474a8d85cfc`  
		Last Modified: Tue, 15 Aug 2023 23:49:47 GMT  
		Size: 48.5 MB (48539796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0ee13cb82c7ccdb49719b845e408b2d158a9ca22ee4ea4aa77c94969d5df4b`  
		Last Modified: Tue, 15 Aug 2023 23:49:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
