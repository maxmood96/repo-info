## `debian:testing-backports`

```console
$ docker pull debian@sha256:ef9f8c3ac4c2c212fc919f2118a749e4dad107a9f89bc0ed9f114dbb24cbeaea
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
$ docker pull debian@sha256:e1e7533cd99a9da684cec9bcd8618d2dc2f3174b25f69d2f937939780feae726
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52458458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8f5f7dfa1d124fa28b0b8fb614d8c4a16f6232d8a2bc861ecc7f8b906b5c5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:26:38 GMT
ADD file:e38abe5f09ca03d90c91799e2e69d68a1147a8f86ccdcdd987a89bd602110b19 in / 
# Tue, 02 Jul 2024 01:26:38 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:26:43 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0b5855eb0983f9340ca03ffa4e6c325cd705d287572d0eba3b70fa2461444cdb`  
		Last Modified: Tue, 02 Jul 2024 01:31:14 GMT  
		Size: 52.5 MB (52458235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d609ff766814e437010473a45a48e42298bb1bdb1efa3fa68228179c6621b903`  
		Last Modified: Tue, 02 Jul 2024 01:31:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:111adf7b79835b385aa1c3922c1bd723d307d1edc93c42675e89f192c63b582c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49521653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c018d98f25e60f3788a0adb6e0c7efa17dd1ebd3d1e7d910e1922c9cc7847c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:49:36 GMT
ADD file:3d601edc71c861378d34f746563d0fa9498dd01b3c9e5f8ea332a98758f00c05 in / 
# Tue, 02 Jul 2024 00:49:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:49:40 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c3e6c40320b3fc8e11aed304e01aabc6777a950d07f0f352398ba89a25c25fbc`  
		Last Modified: Tue, 02 Jul 2024 00:54:07 GMT  
		Size: 49.5 MB (49521429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7ddefe4e436ec2a92720c2d5af5e9ba25bd23472fdaf7745891dbde6afdc10`  
		Last Modified: Tue, 02 Jul 2024 00:54:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:fe0c2f09c9149d5980b41c1784ad95fda90e57f40991120e48def8397c78ea88
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47028273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78af29ab755e42d12fa1ed49639b1c7844a031e474bd0f44d0288c37d0324cd8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:01:26 GMT
ADD file:b08de71723784d2f8df362f2945f1ae14db1314a4f6ced08bed8ffff9be38f5c in / 
# Tue, 02 Jul 2024 01:01:26 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:01:28 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:de3acd1093e5ce4ef865b4721f0d2fc5ccf7651b0d90c052fdc1e52e7c084023`  
		Last Modified: Tue, 02 Jul 2024 01:05:47 GMT  
		Size: 47.0 MB (47028052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597d8e06a807a0ad6f5720b12417bfbfd9061b763e6cdbd5e09efdb8588355a2`  
		Last Modified: Tue, 02 Jul 2024 01:05:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f964424936dcce6868b94194322f15d979617df83b8360b21538bc4c8e36458f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52693536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf547ad5450ce7dc86bb6dfebebe1f5260a7bdd3ce73bf825f2a01b0665fdfa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:41 GMT
ADD file:d903c4ae068c559394a45c9b09837213d003094120e0b425a361699336d83198 in / 
# Tue, 02 Jul 2024 00:40:42 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:40:45 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e58d0af417c026077a461ba61e4cfb256505119f4bd4894be8db0fecf047f618`  
		Last Modified: Tue, 02 Jul 2024 00:44:50 GMT  
		Size: 52.7 MB (52693311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f52ecc50007dd930d7391cd551a5a4c95f99fc3ce1f7037318eefe2e9491257`  
		Last Modified: Tue, 02 Jul 2024 00:44:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:b887115e727b8c9b3e7a6e62d19c3c5dae9ec4188a1227bb119bd62a2c5ae0cd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53333417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d736e545fdaa321850d59d2e28b898e830e948cb4fee555dcaf3cab04baa55d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:30 GMT
ADD file:05b754f48f6403c06a0b232d11a3963270a1470ef9ac5ae4eccda5b895a2ecde in / 
# Tue, 02 Jul 2024 00:40:31 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:40:35 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:806e996e681af760a24d2517de0eff64e72af81132c17305e21eea7d1b967dc6`  
		Last Modified: Tue, 02 Jul 2024 00:45:32 GMT  
		Size: 53.3 MB (53333194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e66fe3631fc9ef10c9a09e33d09d853ff66f32558128ef788a1c9e5947e09f4`  
		Last Modified: Tue, 02 Jul 2024 00:45:40 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:4ce9b36c2fa3d6eff7e020729d33ff0e2a3810ab061f5c3c46e736fd146c5620
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51311879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd537ed7695587eb9b145e89ca0fe46f69581612b20d773eb9eb8c594f7098d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:23:57 GMT
ADD file:5de743fe6c2ded1282f9b5d930bdd8daeabcb18ba1d6a0b17b45c66842ef53a0 in / 
# Tue, 02 Jul 2024 01:24:03 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:24:18 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d122b4b250e31c77c7a3642c65929e682868e6da4842023b9e44182dccff9fe0`  
		Last Modified: Tue, 02 Jul 2024 01:35:16 GMT  
		Size: 51.3 MB (51311655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e325fd43bae7e87f71d3d1787262b41124b4c1456fdb818bc63d3c863ae1b8`  
		Last Modified: Tue, 02 Jul 2024 01:35:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:629cfc18be0342790c6a6f09bf8e41a7bff96390f7f1cc63962199f0149a8b26
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56345432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e8ffb3785b37a1506a5e24f5e212ce823f7f89c10caf3da961e06ecb19074e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:19:29 GMT
ADD file:7e6fd591511923e3855e4ab948bf72e13d53b13ca80fbde003a5f4db88ccf6e1 in / 
# Tue, 02 Jul 2024 01:19:32 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:19:37 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:784dd835b92bc08b6c713559b16a29ba502fd55f92d2d87be387713feb691dc2`  
		Last Modified: Tue, 02 Jul 2024 01:24:50 GMT  
		Size: 56.3 MB (56345211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c55a64e60a7bf8aabcd19033524be14144f6351f7149ff02b71886571d1a688`  
		Last Modified: Tue, 02 Jul 2024 01:24:58 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:1b97c4dbbd8ec7e23d679d48ace9a3f1a0158be66d535e139593c012a3ad37a1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52089690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7bab07e100e0f3af9e908267fe70a539b640a974454d36f08b42782f5a2813`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:45:49 GMT
ADD file:a3d0277ebd5e534d85f6309dd13540dcd7d838f81af596e67ff78d6b72e96db3 in / 
# Tue, 02 Jul 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:45:59 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1a1a0e77f0e4b483396fe1b149e22bc15176f45180204020be0f831ea7223f9d`  
		Last Modified: Tue, 02 Jul 2024 00:50:39 GMT  
		Size: 52.1 MB (52089470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f128ee56f7d434a26e8a6def48e74ff9e9fb13d7da95f3d87c658d29c5a7a4`  
		Last Modified: Tue, 02 Jul 2024 00:50:45 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
