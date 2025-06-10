## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:2d0324f0a072a77e86265317bd5d65a8b8738e4ab9742aeb85fc1bac118f736b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:75b6be048f9e14a8d2bbbd8b871b0d2567201b6dd8fbec02a28274f0f8409fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74434023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2fedb81fb270c2bd90d37cffee6b4e25b3eff1836b9aba2c3f770f61426532`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 06 Jun 2025 16:11:57 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Fri, 06 Jun 2025 16:11:57 GMT
ADD base.tar.xz / # buildkit
# Fri, 06 Jun 2025 16:11:57 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Fri, 06 Jun 2025 16:11:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5d6a67e68beb2715ff3dff7a82fd547813635b46751c3ba127c882f31ae74a85`  
		Last Modified: Mon, 09 Jun 2025 19:09:38 GMT  
		Size: 74.4 MB (74433811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7178e68320dd81db4ff87cabcda0985fb6efadbbbc3083062e76a7ccce49347c`  
		Last Modified: Mon, 09 Jun 2025 19:09:30 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:b1c21122200b9c8cd43a7cee38c1447682306d54359770739c8e7da048abb0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb5a79aaa64bf47199204b9414d6a4ae038e87ccce1d743d88196a780890c3d`

```dockerfile
```

-	Layers:
	-	`sha256:b2b46f1bcf3323730eb4ddd5f2b5e46fb1b7c190e175584eab56a8a01370bcc4`  
		Last Modified: Mon, 09 Jun 2025 23:04:17 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json
