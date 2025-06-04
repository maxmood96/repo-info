<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:11f9ff7ddd702540ca5b75f9e10b688768a672a6c3ba7f4402ccd478209a8136
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:ade8939bff9aabeedb7d4080385241e2022595055bdb02056bfb4be2778264d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74430199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2c2444bd290d4c9d84c086bb933bd0588ec4332b38d89cdf7158c3eb8575c2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 29 May 2025 16:09:14 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 29 May 2025 16:09:14 GMT
ADD base.tar.xz / # buildkit
# Thu, 29 May 2025 16:09:14 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 29 May 2025 16:09:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6d15e85afd81ea4594ad388d9dab5f93804bceef56356e5289c74a7a13cfc180`  
		Last Modified: Tue, 03 Jun 2025 13:32:51 GMT  
		Size: 74.4 MB (74429985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33a98eaf2f25c7cabb0ae34e3cb321d79ab4316dd68040eec601ef9b315b96a`  
		Last Modified: Tue, 03 Jun 2025 13:32:47 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:4e25f9a7a19ea69508f2d7f64a6820ace68f0d1fb30be4fa2cad8ec0b3651bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e6d377accb9304db39bd95a8d67a66dd9b9b55799d12532413482fd00929e7`

```dockerfile
```

-	Layers:
	-	`sha256:82ebf71952c4538a83ec08bcd465a0f5f6ef72e2cc667b274b78da187359d29b`  
		Last Modified: Wed, 04 Jun 2025 19:00:52 GMT  
		Size: 6.3 KB (6274 bytes)  
		MIME: application/vnd.in-toto+json

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:11f9ff7ddd702540ca5b75f9e10b688768a672a6c3ba7f4402ccd478209a8136
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:ade8939bff9aabeedb7d4080385241e2022595055bdb02056bfb4be2778264d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74430199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2c2444bd290d4c9d84c086bb933bd0588ec4332b38d89cdf7158c3eb8575c2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 29 May 2025 16:09:14 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 29 May 2025 16:09:14 GMT
ADD base.tar.xz / # buildkit
# Thu, 29 May 2025 16:09:14 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 29 May 2025 16:09:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6d15e85afd81ea4594ad388d9dab5f93804bceef56356e5289c74a7a13cfc180`  
		Last Modified: Tue, 03 Jun 2025 13:32:51 GMT  
		Size: 74.4 MB (74429985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33a98eaf2f25c7cabb0ae34e3cb321d79ab4316dd68040eec601ef9b315b96a`  
		Last Modified: Tue, 03 Jun 2025 13:32:47 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:latest` - unknown; unknown

```console
$ docker pull clearlinux@sha256:4e25f9a7a19ea69508f2d7f64a6820ace68f0d1fb30be4fa2cad8ec0b3651bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e6d377accb9304db39bd95a8d67a66dd9b9b55799d12532413482fd00929e7`

```dockerfile
```

-	Layers:
	-	`sha256:82ebf71952c4538a83ec08bcd465a0f5f6ef72e2cc667b274b78da187359d29b`  
		Last Modified: Wed, 04 Jun 2025 19:00:52 GMT  
		Size: 6.3 KB (6274 bytes)  
		MIME: application/vnd.in-toto+json
