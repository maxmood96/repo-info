## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:c2ac537e51f0c6ecedfe6ec9fda3ad13cf1f37afb36e8f86792ab280d5b4b41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:98cfd3bf25c3b9a58c5125686004d77090e5236b37f17aeb7aecda7cd675c3db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45428249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399941c9a74dcbe41a1e30fde26c758c0f672c66a2034b03acf3fb7843afda1c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:20:46 GMT
ADD file:618dd7abcf56d90c7ca58dc804d590f1dee02bcfee24e5050569f18bef1d4507 in / 
# Wed, 11 May 2022 01:20:47 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:20:50 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6df64da9505935dfac77000f696255b30b84c69955ca108861e34ed933468354`  
		Last Modified: Wed, 11 May 2022 01:26:17 GMT  
		Size: 45.4 MB (45428023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f989426b7d1360b59c3069cef39e4dfbda1e0101ec13c174fd7ddb41016c08e`  
		Last Modified: Wed, 11 May 2022 01:26:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:202363b9142aa105bcdac54dc4929efa949b612c19bf3651b6b50475bd1364a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44123136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e07ade257156be131d51d3106c0f52f2cf46c28823f029ab47f82ec8fbab7ae4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:52:00 GMT
ADD file:2717e650680c79001502c4c4809e2c7cd3753e33264454e8af66963da07ad9d0 in / 
# Wed, 11 May 2022 00:52:01 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:52:13 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d52943f35e7763aa8e0616f91202bffda56e9f09ea728181dffb18ece7afa394`  
		Last Modified: Wed, 11 May 2022 01:08:06 GMT  
		Size: 44.1 MB (44122908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbf06e8598b7ff0740f1e21ee91cec89869371a08c8975c51fd184904068978`  
		Last Modified: Wed, 11 May 2022 01:08:19 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:88b9029acf96a4f3e0e783c5de10f74b22982e758e69d1e3e62269212639a5c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42151402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1110b13789bd0a4338a99cf64b0fcd79bd49668cf322dae92deb8b8bb318e497`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:50:42 GMT
ADD file:048ec50078019a30c29da7e9c5dbc1c955c65ef9bcf1eeab570623875c05ca74 in / 
# Wed, 11 May 2022 01:50:43 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:50:55 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:48d141239939911cef25f53a5d1bf2be0779d75fdaa4d5cf3e7e234c1855f2fc`  
		Last Modified: Wed, 11 May 2022 02:06:42 GMT  
		Size: 42.2 MB (42151174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edddaaff081f49157d60036339b9871dcc2788f204111d14662b4010fe09962f`  
		Last Modified: Wed, 11 May 2022 02:06:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:a3c43f6f1c84d20ebb5b8ddc3fe453fad7a178ca8c2878df143c6286a486b68b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43212742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c0958affac0210cc9e411bdaed413083b807368cc4f4df9dd3bc4c8283df4f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:47:36 GMT
ADD file:a9d937644c11fe932b98f2840d14cac9be240bcd1d0559b9b1ce68adf42c2851 in / 
# Wed, 11 May 2022 00:47:37 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:47:43 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ef74a9527b0196ac417fa920eb82858e8dc122ab65c764e15ebb4dd65adeaa48`  
		Last Modified: Wed, 11 May 2022 00:54:57 GMT  
		Size: 43.2 MB (43212514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5998d026a1b4c80ef29209a8f043f193de531912b306e4b8621c5cc685b3b63`  
		Last Modified: Wed, 11 May 2022 00:55:08 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:248d53df4d648614ca7a0a37823b5cbbe2a1d4b14d7121fb2ce202be0ea56769
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46148461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5158883b7b5813dfa7dd5912d7a139e446337edf13b626edf758ed24db102fc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:39:53 GMT
ADD file:040edb3d4676358d0bc42e439d3987be4cf739121e2fdc5a07befac916f8d83e in / 
# Wed, 11 May 2022 01:39:54 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:39:59 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c5429d04eeb729f21a5da2ba5dbf67b750371d1f6d7996a87d4bdfbe994c70fb`  
		Last Modified: Wed, 11 May 2022 01:47:45 GMT  
		Size: 46.1 MB (46148233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f3dc23b8aad434cc99af6efe300dabaab3dccc7d4f93bea9bc66d3b4772670`  
		Last Modified: Wed, 11 May 2022 01:47:56 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
