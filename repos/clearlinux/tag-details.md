<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:ad0bc7e6ba74fe5c8be60f59eea0e506f91232f5423ce02b37229d7078b99c35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:4803cb4feed4849fd5f837687c8f95df5beddc54f558231eee190186fcccd3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73438397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a6908166d933b49df26272150e5c9c48627fd82627871487ea93d9443c49be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 16:19:25 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 27 Mar 2025 16:19:25 GMT
ADD base.tar.xz / # buildkit
# Thu, 27 Mar 2025 16:19:25 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 27 Mar 2025 16:19:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:774643a9beeed3e8c033e45a8e1a91f66ee584b83c387081e525560d422dbb08`  
		Last Modified: Mon, 31 Mar 2025 16:45:18 GMT  
		Size: 73.4 MB (73438182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780d44e894eef7e83a76c6e6cefa7652e14b6d2f5060fb962e0796d7291d9b92`  
		Last Modified: Mon, 31 Mar 2025 16:45:16 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:c14d8e9e6fbed390712a4cd6537d34773d78c5f1e6e027f4d606d6dafdd4c7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a0a95eb0635701aa02cef3cf8c711c88770ae7ae3331360d7461b35ebf52241`

```dockerfile
```

-	Layers:
	-	`sha256:60e1b82e07a3ae8b6aed4aeeaca527b585177997f6ad956dda696c6dad960e9f`  
		Last Modified: Mon, 31 Mar 2025 16:45:16 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:ad0bc7e6ba74fe5c8be60f59eea0e506f91232f5423ce02b37229d7078b99c35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:4803cb4feed4849fd5f837687c8f95df5beddc54f558231eee190186fcccd3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73438397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a6908166d933b49df26272150e5c9c48627fd82627871487ea93d9443c49be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 16:19:25 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 27 Mar 2025 16:19:25 GMT
ADD base.tar.xz / # buildkit
# Thu, 27 Mar 2025 16:19:25 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 27 Mar 2025 16:19:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:774643a9beeed3e8c033e45a8e1a91f66ee584b83c387081e525560d422dbb08`  
		Last Modified: Mon, 31 Mar 2025 16:45:18 GMT  
		Size: 73.4 MB (73438182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780d44e894eef7e83a76c6e6cefa7652e14b6d2f5060fb962e0796d7291d9b92`  
		Last Modified: Mon, 31 Mar 2025 16:45:16 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:latest` - unknown; unknown

```console
$ docker pull clearlinux@sha256:c14d8e9e6fbed390712a4cd6537d34773d78c5f1e6e027f4d606d6dafdd4c7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a0a95eb0635701aa02cef3cf8c711c88770ae7ae3331360d7461b35ebf52241`

```dockerfile
```

-	Layers:
	-	`sha256:60e1b82e07a3ae8b6aed4aeeaca527b585177997f6ad956dda696c6dad960e9f`  
		Last Modified: Mon, 31 Mar 2025 16:45:16 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json
