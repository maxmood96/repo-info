<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:68e114a2f522e4d1b898b99dcdf16d58c573a79b815f70373d61671edcd86cda
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:f237609988fd700618c3e04b36f667338f625bb06a35f38250dbba72ef671265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72063266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789b2d535b5efdfbf52274bf14fb3833d6e09dac594314a209ff5186ba09a43c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Dec 2024 18:41:02 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 12 Dec 2024 18:41:02 GMT
ADD base.tar.xz / # buildkit
# Thu, 12 Dec 2024 18:41:02 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 12 Dec 2024 18:41:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cb674a3932698383f9dda6c5ad3e3c52b4372fae55025ee21605d0236e4eeb35`  
		Last Modified: Mon, 16 Dec 2024 18:28:22 GMT  
		Size: 72.1 MB (72063055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf96af1f222aa78e155749488400ee4f166f41f49f4165b98d229b0424bc85a6`  
		Last Modified: Mon, 16 Dec 2024 18:28:19 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:431dbfef65119df1dc23c3da4e760bb5f27c800814cdde0a09208ac55bb5a9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb38c0bb127dc383accf24248a42604e9106802b383cc909f55f679993360dd8`

```dockerfile
```

-	Layers:
	-	`sha256:3f4e246f0eea7d2aee08576b2af43ba5ba87d24d529bb0e3e83ac5950337f8c4`  
		Last Modified: Mon, 16 Dec 2024 18:28:19 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:68e114a2f522e4d1b898b99dcdf16d58c573a79b815f70373d61671edcd86cda
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:f237609988fd700618c3e04b36f667338f625bb06a35f38250dbba72ef671265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72063266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789b2d535b5efdfbf52274bf14fb3833d6e09dac594314a209ff5186ba09a43c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Dec 2024 18:41:02 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 12 Dec 2024 18:41:02 GMT
ADD base.tar.xz / # buildkit
# Thu, 12 Dec 2024 18:41:02 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 12 Dec 2024 18:41:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cb674a3932698383f9dda6c5ad3e3c52b4372fae55025ee21605d0236e4eeb35`  
		Last Modified: Mon, 16 Dec 2024 18:28:22 GMT  
		Size: 72.1 MB (72063055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf96af1f222aa78e155749488400ee4f166f41f49f4165b98d229b0424bc85a6`  
		Last Modified: Mon, 16 Dec 2024 18:28:19 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:latest` - unknown; unknown

```console
$ docker pull clearlinux@sha256:431dbfef65119df1dc23c3da4e760bb5f27c800814cdde0a09208ac55bb5a9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb38c0bb127dc383accf24248a42604e9106802b383cc909f55f679993360dd8`

```dockerfile
```

-	Layers:
	-	`sha256:3f4e246f0eea7d2aee08576b2af43ba5ba87d24d529bb0e3e83ac5950337f8c4`  
		Last Modified: Mon, 16 Dec 2024 18:28:19 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json
