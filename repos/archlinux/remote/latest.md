## `archlinux:latest`

```console
$ docker pull archlinux@sha256:84e36a5b9b3c0b3b889200b22ff47ed55fd34a20ed39b8a4bb83faa1b25ca7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:20d60c8c2ca285479ea84e214b94a1410f46a339042ab00bab84a3aa6fa70418
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127295741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da5769ac0f365026d2bfdf17e689be3d2e7b98763b8f95fb431155b64b141c7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 11 Jul 2022 22:19:55 GMT
COPY dir:b8442f03de458898c900c736e68bd777458cc832c184bdeb8f2ea5aab4cbf311 in / 
# Mon, 11 Jul 2022 22:19:57 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 11 Jul 2022 22:19:57 GMT
ENV LANG=C.UTF-8
# Mon, 11 Jul 2022 22:19:57 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4912e49d2563ce9f35f3000bf9b88e19c8d15b9c1f733ad7d863e69f2123c508`  
		Last Modified: Mon, 11 Jul 2022 22:21:30 GMT  
		Size: 127.3 MB (127288167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354bb3fd0f6c177ed33e330f2cddc9c2377c82e6c74efa63bf9b04f5364d12ba`  
		Last Modified: Mon, 11 Jul 2022 22:21:11 GMT  
		Size: 7.6 KB (7574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
