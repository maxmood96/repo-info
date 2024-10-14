<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:3bf6547477b7d33eab246048dc54816321d4bf3f39258740fd5f89c050e040aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:d899a38c57107aea547089fb712fa4cd2ef62815cf130083664849e7c0d68155
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71946851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdda7309e7def09f00c1e3fa6cf4a28ff97ee6bc64cae7f13c46f24c6cb5965`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 14 Oct 2024 17:19:52 GMT
ADD file:f0dfb1127f635e9bd869386eecba076915b9b0dd6d6ad235cb83acba122b4a4e in / 
# Mon, 14 Oct 2024 17:19:53 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 14 Oct 2024 17:19:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fefd8bd9e9d157b4ed87e1adeae3b7f578187d1e9b69e047242ce9ce57d2287b`  
		Last Modified: Mon, 14 Oct 2024 17:20:10 GMT  
		Size: 71.9 MB (71946638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd6901126df6f43c5ec1a434a0a9807b6d23d3ee391eeb70251a3a09be6da9f`  
		Last Modified: Mon, 14 Oct 2024 17:20:01 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:3bf6547477b7d33eab246048dc54816321d4bf3f39258740fd5f89c050e040aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:d899a38c57107aea547089fb712fa4cd2ef62815cf130083664849e7c0d68155
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71946851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdda7309e7def09f00c1e3fa6cf4a28ff97ee6bc64cae7f13c46f24c6cb5965`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2024 19:38:39 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 14 Oct 2024 17:19:52 GMT
ADD file:f0dfb1127f635e9bd869386eecba076915b9b0dd6d6ad235cb83acba122b4a4e in / 
# Mon, 14 Oct 2024 17:19:53 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 14 Oct 2024 17:19:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fefd8bd9e9d157b4ed87e1adeae3b7f578187d1e9b69e047242ce9ce57d2287b`  
		Last Modified: Mon, 14 Oct 2024 17:20:10 GMT  
		Size: 71.9 MB (71946638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd6901126df6f43c5ec1a434a0a9807b6d23d3ee391eeb70251a3a09be6da9f`  
		Last Modified: Mon, 14 Oct 2024 17:20:01 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
