## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:7636b2441426925f7efeaae9e7538543dd934a543c9c133eadd37e9bdf95ec91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:1858b2989ea61fb7a027fff1d07b31cbbedf17a43e17af691a700ce17293da58
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67764700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e303d4b969462c14170b67671bc655719de91b5964518598b28d469392171e3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 07 Nov 2022 19:23:58 GMT
ADD file:ad7cff8539b3e299813025f6b3cb964c8b735c8258bf2747b0397ceaca4168fc in / 
# Mon, 07 Nov 2022 19:23:59 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 07 Nov 2022 19:23:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e27c0c366920f1477174fe8f76d7e9583b9085f04904ea4e978c9f7d15cfc34a`  
		Last Modified: Mon, 07 Nov 2022 19:24:22 GMT  
		Size: 67.8 MB (67764482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c255c792dba7f176b16dc916739807c8274b8c9d490e4a878ff457c891f1a834`  
		Last Modified: Mon, 07 Nov 2022 19:24:12 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
