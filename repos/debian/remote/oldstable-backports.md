## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:38aaccd6b1c74c803c38d61346e017e866b08a4af9753cba57cc7b94cf623adf
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
$ docker pull debian@sha256:31b354262db20d7c38fbc9c44a876c4ec27ce74e326870032fc1737ea16b0e41
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45376190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d359f210dc790384a2d653e02763ba5eb21125ac6106a225601b78387dbbdb0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:21:31 GMT
ADD file:4ba049a064f5dac40ad5fd2c4e7edbc4c20e594ff7ba64999f1619cd41677ff1 in / 
# Thu, 23 Apr 2020 00:21:31 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:21:36 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:92ce25f67e218861246457abb0b772c3bef8bef821fdd213f264607200a668b3`  
		Last Modified: Thu, 23 Apr 2020 00:26:25 GMT  
		Size: 45.4 MB (45375966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf054c4b5e666d8f2e3120f8e3650633794af24532dbecab77fe4fd94780114a`  
		Last Modified: Thu, 23 Apr 2020 00:26:29 GMT  
		Size: 224.0 B  
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
$ docker pull debian@sha256:112049c53dbbc3b8deb56f4d9a541d30e65a0cb8766f5ca2825cee7aafb41469
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42101393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3bf2f5eb048d5942e73bdb23f4a619abeace5810ddf1a81d55eed16caf8984`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:05:06 GMT
ADD file:39eab8363024f041fb55eff80e173eb4f40596c0845fe4027ea3883825c36be5 in / 
# Thu, 23 Apr 2020 01:05:08 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:05:17 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d941f2de2edcec9c7cdf295333275ccae2b4a024a986ad8162abaaf18f64cddf`  
		Last Modified: Thu, 23 Apr 2020 01:12:34 GMT  
		Size: 42.1 MB (42101166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923d9b2edf756bb102dc6382f4da217e9d87edc7fd2186692bf4a237f86e404d`  
		Last Modified: Thu, 23 Apr 2020 01:12:41 GMT  
		Size: 227.0 B  
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
$ docker pull debian@sha256:c992a26f454b9f22fb239fc0ac8b041fe890007e268a8e6a97b37091179806b4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46095261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78e9bcca4704a06bb147a54f80e019f38d74cc21785513c0684c67988f4577a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:40:39 GMT
ADD file:9d599aff259bc5954808896388a6f7e0f2b5bff18e23c5a86f7e96229d405b19 in / 
# Thu, 23 Apr 2020 00:40:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:40:44 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:44457f3fc4fa50e68eaeba691265e0b4bd87a54ad7f13555650d96381c8b492f`  
		Last Modified: Thu, 23 Apr 2020 00:45:51 GMT  
		Size: 46.1 MB (46095034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392c6737e87e3c2c5f136bd5d9545a351d062127a24ddb454e21e1cbbec6e83c`  
		Last Modified: Thu, 23 Apr 2020 00:45:55 GMT  
		Size: 227.0 B  
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
$ docker pull debian@sha256:7ddd468f5f348da81cff387d304d302794952ad275fe8f812be86f89a8ce2a70
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45232927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3fb29a329c69f9525501f9d243638d65980dbbd33c671f8347f121624fa675`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:52:00 GMT
ADD file:6607a17198ad1329f4833fea72c4756489ccb658f96349638baefa3808982954 in / 
# Thu, 23 Apr 2020 00:52:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:52:09 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:36000b78ea37f890baeeaf6e4d888ec9b0fbea16ddaa4a6feec5387bb1811a8f`  
		Last Modified: Thu, 23 Apr 2020 00:56:12 GMT  
		Size: 45.2 MB (45232702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1841898393f6e131731e1484a0e69713947ab62f792c9da661101548d0447625`  
		Last Modified: Thu, 23 Apr 2020 00:56:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
