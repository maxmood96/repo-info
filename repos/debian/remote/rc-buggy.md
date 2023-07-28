## `debian:rc-buggy`

```console
$ docker pull debian@sha256:8cb3b70cc19da2653f9af146f6c382c9cffde424e00cec2407529f68c080cd20
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:1e11153d3b4484a203bc1610744433862c6ba793d072e25b2d7621efa0a0aeb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49463151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d484f02063b14a93fdcea8b69b6ecff5a3e9d12758c81f7ff60ef4d62c75a4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:26:24 GMT
ADD file:89538c836015e15bfe955d940c080e251ce5b25e2cfaac73d8ce77f8475cd08f in / 
# Thu, 27 Jul 2023 23:26:25 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:28:07 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9828fc546889681c4c23160b0ee9abb2a08f99ec58b166856cf38d03e0173700`  
		Last Modified: Thu, 27 Jul 2023 23:32:15 GMT  
		Size: 49.5 MB (49462924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ea8b9e0e4a03e9243f81c206973da2f4c8da590afe79e7409d929dff2386c2`  
		Last Modified: Thu, 27 Jul 2023 23:34:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:d2774999a258ce7386ef7dc175d08e464d932f7393f6d9fb3bcfca7f76ab2583
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47221603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7542303e0e0dabc10f1325c9469dc9126b0de535fcabacca6c25d8e895330b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:49:08 GMT
ADD file:2673f00e844880d10f415db6b62b0d8686b31b02fca062ce8f3f69f12a911daf in / 
# Thu, 27 Jul 2023 23:49:08 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:50:23 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:cfd23d2efc358b5d10dee265443e93a7ee2f8ba25de718f6768468d3633354ae`  
		Last Modified: Thu, 27 Jul 2023 23:53:05 GMT  
		Size: 47.2 MB (47221377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06e9d92c351c929d4e38adea7ed2642b769e6ecae80251685154a31558fd39d`  
		Last Modified: Thu, 27 Jul 2023 23:55:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:6d43c7d3770a1663b32b6699abc70b94fac6a7c8df530b80a892a777f04c045f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45003433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a9a05a44bbb7cbb4bb9a9dfa93671edd03b9eda99b5e7f17fffa804dad4bba`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:59:54 GMT
ADD file:751198e94159fde0051292c0a2bcc0ae0c4b82b34b63913cd6860cbed520b9b6 in / 
# Thu, 27 Jul 2023 23:59:55 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:01:46 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d8947caaed239612a0bd233bb275a710201bd19a169719c1541890b12489b8ff`  
		Last Modified: Fri, 28 Jul 2023 00:06:07 GMT  
		Size: 45.0 MB (45003207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c0dc76c5426de57e21f90855e7b1b00e13339a9bd7a0a5157871bcb1982692`  
		Last Modified: Fri, 28 Jul 2023 00:08:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ff502f15bb8a3852d312cf0588e3c61317392a23b51d778c0226fe90a75e6fce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49386027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32832b82f9aa770c5b3029cffb0dbd294058e0733d793da755e54ac03b3c3d72`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:44:04 GMT
ADD file:dcd44d784a7d0453b2aba140a48cea6ad00cd9860ae3735af4f338a7e242bcc5 in / 
# Thu, 27 Jul 2023 23:44:04 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:45:10 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:08e4368591339a72e0b1d1f2280b8e4ec99150999d73beaf90f0bb0f074ac3bc`  
		Last Modified: Thu, 27 Jul 2023 23:49:07 GMT  
		Size: 49.4 MB (49385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5e2663afc518a5c5e27233bcb93cae84f41bff9032601b496ed07277255e81`  
		Last Modified: Thu, 27 Jul 2023 23:51:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:2d64d34496d48ec975969086fd346f094d85c5dfd9d2731559c2d2385b02dd43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50473917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65fae2240c11ffabdc116a87cf65134ba05c905912d94d02514382c1007d6883`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:40:29 GMT
ADD file:f80411b5104f2db2a54b08d2fb1755fdc31ca042be72f3b3165979726a335a02 in / 
# Thu, 27 Jul 2023 23:40:30 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:42:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f0cecd19dc43936e99574e6dd27db4982f7645bc158ab590b29cfc15e2c4f23a`  
		Last Modified: Thu, 27 Jul 2023 23:46:36 GMT  
		Size: 50.5 MB (50473688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de0e608617e9c7edb572377ebcd4bdb7194fa1d0686d186f204f66fe4d4adf5`  
		Last Modified: Thu, 27 Jul 2023 23:49:30 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:5d62c8bbd30741be4a46ad5aed8cdf6a1e77dc8848ea7600038b18b7f2bdac4e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49334828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87eddb86c72e3a428fa758fc6c99264c54ce704fbbe122afca84f5b83cc0edfa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:14:28 GMT
ADD file:5d5d4b53ad51debb95681500ba4a990279ff7fdd2ff80d4d4333b7dc647c0543 in / 
# Thu, 27 Jul 2023 23:14:34 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:20:16 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9b48d6f46b6cff8bfdf81f7ffbfa05dff828e1d7545e640bf61d5486c1b79892`  
		Last Modified: Thu, 27 Jul 2023 23:25:52 GMT  
		Size: 49.3 MB (49334598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85a4c3976f20baa4e54ed40f7ae98a0166a9310df179b9c87fe9128f9950665`  
		Last Modified: Thu, 27 Jul 2023 23:31:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:eb66caf34e4f162f1b37cfccbd8a9f9518876c82e4f0957b6176a28769d48284
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53379473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e183bb0683367269ebb4ef57cf49e36562abf5b21dfd09ccc19af52911e502ce`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:36 GMT
ADD file:c9a8e26186be211989debc20aaaea2b9b0a88ef3c95dc67df08fb292c70fd107 in / 
# Thu, 27 Jul 2023 23:24:39 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:27:23 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:8a2370b39a2d35f89bb2978a591923ded0652ff040aa00a837d799ffdb028e76`  
		Last Modified: Thu, 27 Jul 2023 23:31:58 GMT  
		Size: 53.4 MB (53379244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea4efeeef38c228063db4c9b70e8e6584d62e4797993239070f8b17e27b226e`  
		Last Modified: Thu, 27 Jul 2023 23:36:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:cf6147d3796a8846c80eeaa76c620128ea2bf67b89260c5b6badbc8f629dee2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47858894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232cea0e8d76de73675122f77916593239fdd2d253aa958252b34715d65be163`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:48:26 GMT
ADD file:b143b1c75d100b35ca10aac97e0e6b44c6dc267e1c00c3fa2f3f3dd3c408809b in / 
# Thu, 27 Jul 2023 23:48:29 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:50:58 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ff8109f0f7ac0173229961049cf524677815675d18f6769369db2d95049f4655`  
		Last Modified: Thu, 27 Jul 2023 23:53:27 GMT  
		Size: 47.9 MB (47858669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff38be564e247ecaa551c592e5559bc4c749cf1b7c6808a07685b130753a910e`  
		Last Modified: Thu, 27 Jul 2023 23:55:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
