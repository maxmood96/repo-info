## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:4b992862f0d6877a343f8cd6a18a8b01091e3367436a1b51bdfb123013cf4319
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
$ docker pull debian@sha256:3ba6a6adf9684811c82762d6f13abeca57ca8231412cd26459528c8aebda57cd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45376138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654de8662eea41141473c97cb7e8f8c4ee8ffd4a7b6c6400b9be3ee4872962b7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:21:54 GMT
ADD file:3f033759ecf4f9f8ddee21886062b624f8511b7a99e01ed461a9b58acea300e8 in / 
# Wed, 13 May 2020 21:21:55 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:22:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:59b366d43ab3533d278be192eb3ac246e817e5c4b252bc96b006f70489002af3`  
		Last Modified: Wed, 13 May 2020 21:28:08 GMT  
		Size: 45.4 MB (45375915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b8c15b517ce7c49e187658d4e2d5a5a058fc83a4840ec2f96489d04a81a3f0`  
		Last Modified: Wed, 13 May 2020 21:28:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:6e0fce00810969f53b3cffdc23a7ee98ab1d6c196ae409d1c13fea07908e1bc5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44068065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddc90ac4e88e41286b823b5e25e2520d979f6e12b803a000174879ee63bf41e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:53:48 GMT
ADD file:3ca4bb3d51d2ebaaffcec234cccf3950630931a20033a2f221f5ebbeec5b4641 in / 
# Thu, 23 Apr 2020 00:53:50 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:54:01 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:02ac41c50ec028e14287c568a8e6732e9310fe04ecdb6a9263d180039ee519dc`  
		Last Modified: Thu, 23 Apr 2020 01:01:37 GMT  
		Size: 44.1 MB (44067836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4629a0c9cbb9a8da10fa3b2c93bd3e63504f0fac799b0873e174ebf49fd4857b`  
		Last Modified: Thu, 23 Apr 2020 01:01:43 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:69b0cedb429659d1171c5dd88038dc5ca1f03a0c4be75be8a0c008fa84d02e25
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42101318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9fafb7103e4b1f03f9e62ee95edba7cc6ff33363cad35def9039eb56058fff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:16:14 GMT
ADD file:526767b325590a0f8a02381e60888a56aff5898096ae65f9a2e3e006f745f3bc in / 
# Wed, 13 May 2020 21:16:17 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:16:26 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:aaa6b57fb1abea026233ff64408552563b7318cee7456bc83e642a390fb7ab0c`  
		Last Modified: Wed, 13 May 2020 21:26:26 GMT  
		Size: 42.1 MB (42101090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3feca4f7eb1a7ab535b87d6bd01d1fef473c8bb7137ce209311013136e38636f`  
		Last Modified: Wed, 13 May 2020 21:26:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:60cc67c631c1fc5634686764e4b873abffc00395f10106ab2c849c220a594db7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43159272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b51d8bcf6ffcb9f943ba5d8b2a1ff06b7945457ba3c5b30038fdbcea1a4aab6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:55:21 GMT
ADD file:6f4e3bcd57d8b2ddd7fc8b299b6cbfdb398f2835cd49c6e7ff1c851ef1759647 in / 
# Thu, 23 Apr 2020 00:55:25 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:55:37 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:00c8d9fcc2709130307c6da4a31d109d8f126578f9d061529a6447a77e1b9f34`  
		Last Modified: Thu, 23 Apr 2020 01:03:46 GMT  
		Size: 43.2 MB (43159045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b35793439f61d80abcebffac4718a4c932df1aa3c65b237a2f3198acd8c5bf9`  
		Last Modified: Thu, 23 Apr 2020 01:03:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:d32f013d4e820b31d3df84fbc2034e68f553ca25f3ad78eec324f6a8507969b0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46095303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67edc4ce68baddc6e9c8f8208d016334d1fb110138c9d976d52cc5728281daeb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:40:44 GMT
ADD file:0d8e1bda846dbe61891a8d38fea02b7d3304008130f0132818eb558b722a5228 in / 
# Wed, 13 May 2020 21:40:45 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:40:50 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:64f43be8f622b6cd9d132f78bfe57a01056a97ccb47e0229ee95f598ab600c1d`  
		Last Modified: Wed, 13 May 2020 21:48:06 GMT  
		Size: 46.1 MB (46095078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1fbf3f65249ada8af4f73fc9815eb2221be4b1284d9110be4ddc594db84de9`  
		Last Modified: Wed, 13 May 2020 21:48:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:6b9fe32fe0e3ff999bd355a6055e7e4ba3dbc0472d552a4a29f7415218c812e1
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45049106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9883e58f26c98c602fb2a64eca568138b4f3f4e7337f71a1cfc8399123c6c729`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:10:12 GMT
ADD file:e7ce9b372944430786cd013dd9a9e34ad0ad80172c472daa5e9b0b08e3a2a203 in / 
# Thu, 23 Apr 2020 00:10:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:10:21 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e34ab6d9ab1a86f283dd0895f818bf14ff8b97e03352676724d826be44a8f2c5`  
		Last Modified: Thu, 23 Apr 2020 00:18:38 GMT  
		Size: 45.0 MB (45048878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997c79d38625bcf7effb6f41b8739d9b1d4819f4b819f5ed07e5222a6ac6a73c`  
		Last Modified: Thu, 23 Apr 2020 00:18:48 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:9cb865d14f7e83d18f552e921a1d4cd290e26712cb98ec8c96d2c76ca301e4f9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45646366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be2045b65da0277c689db73075db27f8e869380fcaddba54ad0bb4108de8d4e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:36:42 GMT
ADD file:6fa98ca208ccdc689089759efdc2df1c2f70a7ae704eb5e561ebe927ea34c46a in / 
# Thu, 23 Apr 2020 00:36:46 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:36:58 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7fe72dd022bcf4f01d26837fa778fffc3e593d19742733b53a385d2f0e82a31c`  
		Last Modified: Thu, 23 Apr 2020 00:50:58 GMT  
		Size: 45.6 MB (45646140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd94b2399834e8cb6a303fa0fc43daddbb8a5fbf1f87499265871d567167c07`  
		Last Modified: Thu, 23 Apr 2020 00:51:09 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:c51148d44a3437e2a7964362ea79f800d0e03d8233a5d692c1aa1618ee97917d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45232953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552c75415e5aadd66d8ebcffae37757152eabae10fa9b4d39ab4ec9b95bee7e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:42:52 GMT
ADD file:6eada3f6291c8b2843feef6bd7934e5cc0a4617f452dda9417b98021c6570cc3 in / 
# Wed, 13 May 2020 21:42:54 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:42:59 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8445e75ca26fb9a771e0d8317d0d661b4224584c78f173a9dc1bb5b764e6f8fc`  
		Last Modified: Wed, 13 May 2020 21:47:13 GMT  
		Size: 45.2 MB (45232729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724964cfef1ff403093309ac2839b50c86b2a2f555def160acc893c4a711ba43`  
		Last Modified: Wed, 13 May 2020 21:47:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
