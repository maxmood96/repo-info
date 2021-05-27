## `photon:latest`

```console
$ docker pull photon@sha256:453b1b3ed2b5dc4d41bc1ab6a80150799d4ce4a2f7db3b7b64463dfaf7478993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:cb3cb8a46cc56b26512e2b79b465a92c6c501108e01ca9a5481ffce95d221ec4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15776962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aae0ac8c87a4310e7c56f4286e7ddeee0d623db7ace3ec0f7761f3a1102dd0f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 24 May 2021 17:21:43 GMT
ADD file:1a7749e42e46a7327cb9501c6973240d7e469d16e4718378a0a98d520e24a045 in / 
# Mon, 24 May 2021 17:21:44 GMT
LABEL name=Photon OS x86_64/4.0 Base Image vendor=VMware build-date=20210521
# Mon, 24 May 2021 17:21:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b671124209797297d0c750621375c49368c008259093e5e2246b460597ac201f`  
		Last Modified: Mon, 24 May 2021 17:22:37 GMT  
		Size: 15.8 MB (15776962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:5f3648bee2ecdbbe32a0a673640a20c765053c3962e863779d8257356e0ce9fd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14810449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c04d1c81d55af1b7978c64a5ac148be2f6d9d2812c1c73b3f412d255a5edd01`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 May 2021 09:08:51 GMT
ADD file:b12aba66730ffcc458934c4f248d42f68ec105b2019bc9e7a61611e472089240 in / 
# Thu, 27 May 2021 09:08:51 GMT
LABEL name=Photon OS aarch64/4.0 Base Image vendor=VMware build-date=20210521
# Thu, 27 May 2021 09:08:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5dfb987903b393b91080acd442a1276e5466a4b7894c7ccfa960d7f01ba142d8`  
		Last Modified: Thu, 27 May 2021 09:09:18 GMT  
		Size: 14.8 MB (14810449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
