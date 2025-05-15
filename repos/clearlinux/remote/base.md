## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:4e92b74d669167fcf11db35fb69937a06745e6814478f564bef70c73cde282b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:8d092fc19a2f798397b50e0a3e612b078baab6e2c31f93877df01457ace79b9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72824344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e7a6c89f85e04380614fcc4bad76ab1eaaaafab3d56f98a6c6a180f1c43559`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 08 May 2025 16:56:36 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 08 May 2025 16:56:36 GMT
ADD base.tar.xz / # buildkit
# Thu, 08 May 2025 16:56:36 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 08 May 2025 16:56:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:806062290e297bef5df9e5cafc0a50c8441de8ec71756afc0e23639ddfd731b5`  
		Last Modified: Mon, 12 May 2025 19:11:10 GMT  
		Size: 72.8 MB (72824130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4759694b3e98081da8c218b77fb065b4fe14fe4b4f5516ca92cdedb609627f0`  
		Last Modified: Mon, 12 May 2025 19:11:08 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:76fb5dbd8566b086efd577cdfbcd7157f21cacceb4168b17ccbedf1cd2ed5fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56635eed0fa04049804d8f4366e25d822010f3535eb73d85b0b6ed9fdb61448e`

```dockerfile
```

-	Layers:
	-	`sha256:feba75cfc0dbc6909f4021defc6f5bc54945b7b63bb5f87f3c6bbcce78d42b8b`  
		Last Modified: Mon, 12 May 2025 19:11:08 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json
