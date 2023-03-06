## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:0f8182445b428d9f69c17165564ad708391b34520baa6f3e3b932cd7e7be8c22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:b8bee2858b13d3cae9c8e57761dc5a6dc04291352f8b796a10a4fa0856bccf47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87827826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2c8854faab353f903f19ec0febb695e04dd2b900619e854f70c81205a12029`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 06 Mar 2023 20:23:21 GMT
ADD file:0814ce0850aa265b8f615fc2da0e31cde2c2de77f656be71490cb0d5452144c9 in / 
# Mon, 06 Mar 2023 20:23:22 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 06 Mar 2023 20:23:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d167b9a5d1f2f450cd65725bc204c270b3e8057cdfda278c7768c4a52e6f2cad`  
		Last Modified: Mon, 06 Mar 2023 20:23:42 GMT  
		Size: 87.8 MB (87827609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990c18b7c6cae9d7b9544ff4f3c266414fb03f11ed571ca653d2393af5b445ca`  
		Last Modified: Mon, 06 Mar 2023 20:23:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
