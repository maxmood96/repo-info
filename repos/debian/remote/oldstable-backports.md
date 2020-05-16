## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:9416b1b78c01c03ac904be7cd5a3d76aa11bf7d1f6bfb47353de02d7519aed35
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:3876027c3fcd9cf0045f206533d4a535094a71e6815f77aadb47de34c4c08905
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45375392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ee2294186c83b10bb665e0a5dc76c0ea5d47ce843fa8b0a42b7c290a09861b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 06:31:04 GMT
ADD file:37b9b59ff14f2acc18c4b2d704e57ff8293114a40a34347a3664543864a39738 in / 
# Fri, 15 May 2020 06:31:04 GMT
CMD ["bash"]
# Fri, 15 May 2020 06:31:12 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8bfa9979f36663ad5f264c79ec562de99c90ee8651d1303e465922033afde055`  
		Last Modified: Fri, 15 May 2020 06:39:20 GMT  
		Size: 45.4 MB (45375165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f400e58c254e6c81d2c441f7fa9464977745614b179165d5b8bfbf895017bf`  
		Last Modified: Fri, 15 May 2020 06:39:25 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:6811c499e19a6fb9360a10df22064e55bff174c6e9d5c37aaac228689cc6260e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44072065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e733af377333cba2bc48f18d0c8a2d71410b25490f79ebf69d4a8ba9b9fd7b9e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 14 May 2020 22:39:52 GMT
ADD file:6a3873172bb05469b39267e97faaa5a88b26d10163455ce92858ab00b41403d6 in / 
# Thu, 14 May 2020 22:39:58 GMT
CMD ["bash"]
# Thu, 14 May 2020 22:40:06 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a02dc173a7c3af68f27ba7bd2c84ad3bd4f5bea223b3221684760db06547d99f`  
		Last Modified: Thu, 14 May 2020 22:48:42 GMT  
		Size: 44.1 MB (44071839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0173ca5a4fe85d95bc7c8740e5ff479329cc1d55cdebc25305d0520841d4ea8a`  
		Last Modified: Thu, 14 May 2020 22:48:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:02c5ba8b80d3c4eebc9b47aab2ea222ee2c58f54058aa8de5c4cfe3f9647d81a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42104566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82ba2063a6a6eac9af6e9191540b40649ae7316a3c8c83b334ddf44b9527da9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 01:03:00 GMT
ADD file:b70996930efc92ef82442e29285863d25b4752968a27e17713d02a049ae3a80e in / 
# Fri, 15 May 2020 01:03:04 GMT
CMD ["bash"]
# Fri, 15 May 2020 01:03:12 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:968153165585368b1b1ab25931c78d0f5b0307ef01cdeeecdf94a2b9955c4c7a`  
		Last Modified: Fri, 15 May 2020 01:12:58 GMT  
		Size: 42.1 MB (42104340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f15308b1e219d0328fbdb103745bcbb6d999cedb03b91d1181b7e01b503b8a9`  
		Last Modified: Fri, 15 May 2020 01:13:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:90bb51263c501b64bd2fdc65c2380ca9fbebbcf8dd655a6fad24a267516b9722
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43163268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e4e316517ba25534efc5f348070a52e28b5e91aab277d48ddc0427fd8baa3b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 12:44:39 GMT
ADD file:1247cfa8c7a05b3dbdd7fffbf715035a7d87e64a89ef59695bc6421cc162412e in / 
# Fri, 15 May 2020 12:44:42 GMT
CMD ["bash"]
# Fri, 15 May 2020 12:44:51 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:215ae99efab2bcc41c7981b896c6c56d370e098ecb7d53ae4206b56629dd4b55`  
		Last Modified: Fri, 15 May 2020 12:54:05 GMT  
		Size: 43.2 MB (43163041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad911412881744c0a5b3825b518b93c626906e04783466f6ea974ba20d538dc`  
		Last Modified: Fri, 15 May 2020 12:54:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:1acee3bffeb4fe1c10b4da51d72bfa2c0cfcca7e89ad3912a2fa660c1274c3ec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46094423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44cdb4090911d6f4016da89ea7f373ea31aa032494fe2a8cee46345aeaf968b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 07:10:09 GMT
ADD file:3c2d5842310981befad4f477c954f48b954cf78ec4b8cf60029e4107b8dbf3fa in / 
# Fri, 15 May 2020 07:10:10 GMT
CMD ["bash"]
# Fri, 15 May 2020 07:10:16 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:028cf857dd88f16fbdcb3a4b83546cf0510233507394f8a6bd028b1f1bc27c43`  
		Last Modified: Fri, 15 May 2020 07:20:29 GMT  
		Size: 46.1 MB (46094198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9854968e1b8ba98d4c46dd5ddb8727036c1e1a0e9cb9a930bedbd950d37d2c`  
		Last Modified: Fri, 15 May 2020 07:20:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:17b743ba9fcfaaf4ccd251c6ce2ec07e3144a575931aaf0eac4930064cd30476
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45050102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13265596b0a105ab9474a32becbe49bc84cd411d040f51dd93970ae10ec8bc11`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 04:48:46 GMT
ADD file:1b71c07d820c2979d63c3646bcb632b5f2f8dc73daeef2ae26ddccc70fa32cf2 in / 
# Fri, 15 May 2020 04:48:47 GMT
CMD ["bash"]
# Fri, 15 May 2020 04:48:54 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1bbf7d0d9c5c4b6af2e8f0eef03b2f0f65b931c5c57c2d7dbc57a3a0078c61e0`  
		Last Modified: Fri, 15 May 2020 04:57:56 GMT  
		Size: 45.0 MB (45049875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0552409f8d4c64450dd255601a2f5f1cd5774317a6478eef120afc99ee3896`  
		Last Modified: Fri, 15 May 2020 04:58:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:cfcfeb4cd7ec3cf9fdc6c9cc06a9a675ccb6ed6a97ceb175e3103753e107175b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45642787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653ae2ca6ee4083de3e7e5965b6a3b9a7907e7bc8e46de53f72423e64cc2d98c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 16 May 2020 17:21:06 GMT
ADD file:9ef5e33b6c69957a9a205ff208167790a0e36e9ff45a0c5b1898df92281770ab in / 
# Sat, 16 May 2020 17:21:11 GMT
CMD ["bash"]
# Sat, 16 May 2020 17:21:37 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b66bce6f2b47fde22b633ad80ea5051fb085cd2ef0b4c3d499570b790963de4d`  
		Last Modified: Sat, 16 May 2020 18:32:42 GMT  
		Size: 45.6 MB (45642560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3935582703e31f95139a5d644a16f1429b759cb592ebc794e7b5860e5ffa2f7c`  
		Last Modified: Sat, 16 May 2020 18:32:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:8efb1077ad028523cc75acef0d3935cbb268f7634fc480e7fe4257e8ad324cd9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45232363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c245b53ff53e485f2a0159d01636c15c4d8b2f026d8960a17efeb32de3ca37b3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 14 May 2020 23:06:53 GMT
ADD file:7bb64228e15ddc34d5624c8a3329ef68be997e4d299b95cceace485e00a24d8e in / 
# Thu, 14 May 2020 23:06:56 GMT
CMD ["bash"]
# Thu, 14 May 2020 23:07:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b28e354f80f29bc9dbe7da5033d0a531dd9687922cabd20419a093a8bceff95a`  
		Last Modified: Thu, 14 May 2020 23:11:38 GMT  
		Size: 45.2 MB (45232139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27d67238a4eabfc82e170009c93727210a4f5c11ff520d670e04128e2b2ac3a`  
		Last Modified: Thu, 14 May 2020 23:11:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
