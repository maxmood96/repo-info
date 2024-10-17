## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:023902db9c35de72974b63d35122ebe213ca089dbca5d0cd094068d34e8a66e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:cb15a6d9780cd1b188fbe4cffea894c60feb9efae5357a1c607cb2f641fa89df
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55080838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0827f8d4cda3d9aa4babb385390c46db1ff98d3bbdac402e189cdb2c15248ca9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:39 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 17 Oct 2024 00:20:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:20:44 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fe356f32e7e4e6dd3dfdb285b7f74cc7fb60dce453aacc08a72b5dfb78cb76`  
		Last Modified: Thu, 17 Oct 2024 00:24:27 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:d78b8c1a8a0294092765478a66e69e302c2d357df04f1d0805b5a7891a983806
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50241823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2df7469d5668290d87ce330b5f18a538421509a967fa1ff75aaf93bc7b4d161`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:34 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Thu, 17 Oct 2024 03:03:34 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:03:37 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c545347f78ae05f73730af41b2bc7905bbbb4d732effe177a718fa34a4cc8a7e`  
		Last Modified: Thu, 17 Oct 2024 03:08:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d1c067281fa06ed01502a33c392dfddf0f77d0c3a660c515871222d551f632b4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53735121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4a540d830af566ece9483bc2ddc9efdf96daeba4206abfdfcc3b230f3899c9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:05 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 17 Oct 2024 01:12:06 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:12:09 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66d32f16c71a2e7dfe600f1636039fc6dce79c411bcb041d98aca610d81d82e`  
		Last Modified: Thu, 17 Oct 2024 01:15:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:1de14a33a77bdfa25b1321ba1c1bb781218b774e30af08dbd68c7c5ccf35e7dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56078047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4906522eb86d7d945bbfae8e8cee9f7f2601b16fad470e9e73a45e1078c630`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:39:07 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Thu, 17 Oct 2024 00:39:08 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:39:11 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f6d7cea03c5f62b2407320f518b6faf28c1e90392c5f0490fe04cddeed3c47`  
		Last Modified: Thu, 17 Oct 2024 00:43:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
