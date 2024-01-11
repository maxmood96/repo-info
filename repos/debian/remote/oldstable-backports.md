## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:ac94c8b050a3ff73c8eb00954e24cb838b31880e37ad04b82ed7716cc8e43090
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:5b0b68e525e80ab3e23429f2a23f7b9c6186bb59db77f52d70b0716929057489
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55057955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b29f73c7dba1b7314706505d5e22e3a72ca55a38ec91c53090805a921cafcb2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:39:12 GMT
ADD file:626906033975eed6801d5c23d9787e486e9d54ca18311e7ee15f3038da925241 in / 
# Thu, 11 Jan 2024 02:39:13 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:39:16 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ecad687fcd3fe94867c29cda1d4db4094eee8160052f8d9c9aaf9106cf76475a`  
		Last Modified: Thu, 11 Jan 2024 02:44:40 GMT  
		Size: 55.1 MB (55057733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f948b08bb49869dea31cb9425fb9e1546e86d2b459c9cf81b10b6785b8ac9e7`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:c54fd34e91b9fd19e7c9e5b1a3c7a3f1681b6ab9d0a11140fcba07296f61582e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52562736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8aa7085ddbfba6acaefc8d21d3f56bb538325c69bf4123f85a4aedd0d6a8ec`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:49:42 GMT
ADD file:7740d17228ca5f57ed9f7dbc47fe16436cf475d0e609c97da18a54e8df0debe4 in / 
# Thu, 11 Jan 2024 01:49:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 01:49:47 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1ac134f139a5ff65d90683b417d8f680c1ea631f26af2eb438dc50fe59384138`  
		Last Modified: Thu, 11 Jan 2024 01:55:14 GMT  
		Size: 52.6 MB (52562511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7becd16b8622832dc49ef53cf2d648f619736405455d9d47888be3bb503a3a57`  
		Last Modified: Thu, 11 Jan 2024 01:55:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:d278b13ef4b1c2fdb232804a5729e51d354719af14ee277d70b052fa609c5f59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50215768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24f6d790355f4c39e1e7bab2023ef35252eb51358b96a9f29527ddf2579b0b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:43:52 GMT
ADD file:216c9e8921474231e6b4c55b281844118ce4622776d110afd37f176342202b25 in / 
# Thu, 11 Jan 2024 02:43:53 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:43:57 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:caf35353da1f6832456b56038d7c1ca6d41484fe390e001c05953eb4e6a6f618`  
		Last Modified: Thu, 11 Jan 2024 02:51:07 GMT  
		Size: 50.2 MB (50215541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f1e2661ef895ae5f05df91e9c8a27e8f8294499c90b18ef12ac13c50cd3a48`  
		Last Modified: Thu, 11 Jan 2024 02:51:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7f40f3d5fed1227ab30dfe7573118a5c9ea94e88ca60b42dc366e648ba280bfa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53708050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af09b2c581557e6b3db303ad9e5faa6c3755633a8e34b6737a7b740ab5947124`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:35 GMT
ADD file:863bde5fc51afd18838a26b5ac60b039727183105c5df2ab2a53e77ada06884c in / 
# Thu, 11 Jan 2024 02:41:35 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:41:38 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b8c010a86164cbee68e1233125685965d9e64b0df2a1bb759a4fdc2c37ded111`  
		Last Modified: Thu, 11 Jan 2024 02:46:10 GMT  
		Size: 53.7 MB (53707826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28aad911522633de3ff3adf3f13820d801604462bc6c16cd7e8ca0cdb863ffd1`  
		Last Modified: Thu, 11 Jan 2024 02:46:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:d808efc3008435ccca3b1a40d832d6296535a488e5371569f3797c887f4cf8de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56046597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d229aa8124c8cc1b844909e4e14e8452899d3c211a6b139dcd25d56fd629ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:39:57 GMT
ADD file:1f3128fb0b486ea45ee6c982f95c2e5cf8fc2f970271b68f07ca87c346819155 in / 
# Thu, 11 Jan 2024 02:39:58 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:40:01 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:76b13950abdd3e790a4dedba1e8248fbf58caa110319444c8378b20b5dba14a1`  
		Last Modified: Thu, 11 Jan 2024 02:45:56 GMT  
		Size: 56.0 MB (56046372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1cbb691578e8e003b56a82b93e4f6652610a17b7853e7376304495830de6a5`  
		Last Modified: Thu, 11 Jan 2024 02:46:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:86bfee40a0ccd4f29862eed1d00b074d2c551e477a2552beba66090a7f5461cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53289115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93875b84a9c43729c1568d3962e9fae1e3a0e3a8d6971813ca0182a49d3b1c2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:13:35 GMT
ADD file:5494d30b4c918f129a3ccb16cd4d8445f8f6cc8d0c938edb2d5ade1e9ac7d459 in / 
# Thu, 11 Jan 2024 02:13:40 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:13:51 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1ac1a2fbb51f34efcfa44d04ce0a9e2637c55410c44fec15eba9b85b4a6755a3`  
		Last Modified: Thu, 11 Jan 2024 02:25:04 GMT  
		Size: 53.3 MB (53288890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b19700b69c5e9b8b5eac75a0762eced7ef7ba1f94dadc98f9f339c6fafdbce`  
		Last Modified: Thu, 11 Jan 2024 02:25:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:cd58d4217690222b6b2c5e61598dcb4ed967d715ebe704383bb7a52b7fad52c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58929865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0305bd473e1f754e3cc0736926532c62add0df5ffea09085db188f5181b676`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:35:13 GMT
ADD file:0a521f69c6f291f81e445a5183de0b89723587bacbb102bf992528337c18f529 in / 
# Thu, 11 Jan 2024 02:35:18 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:35:25 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:79a812cd07f75ff506df7bef5b66ea9df9cd401334acdda5bf6bdc3efe0ab742`  
		Last Modified: Thu, 11 Jan 2024 02:40:38 GMT  
		Size: 58.9 MB (58929639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578e2e7cc871f7bc1d099e1a71711c327c1c80a4e431ff87ceb0d19d3b0e7728`  
		Last Modified: Thu, 11 Jan 2024 02:40:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:6ec8775f73b27fb2ab8931ae6176ffb5b126a56f32132c321cbad9d674c4dcd5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53296373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fac236a8e263c79dc85e8f3e20439a4056579a332fe2020600423a0bb4df7ef`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:46:02 GMT
ADD file:37525552ed84501a85845e95053b3298257018d4c7dddc66a4fe8ed61c022f51 in / 
# Thu, 11 Jan 2024 01:46:06 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 01:46:14 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:df7a50e870fe1499569bcbf4ad46fa6daeffffd9c2f0fea4d2e68685006cfe2c`  
		Last Modified: Thu, 11 Jan 2024 01:51:33 GMT  
		Size: 53.3 MB (53296147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715db73b457880fa61ab1f80768c92121102895f576be25db7910c4678e36d7b`  
		Last Modified: Thu, 11 Jan 2024 01:51:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
