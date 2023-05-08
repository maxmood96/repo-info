## `archlinux:base-devel-20230507.0.148551`

```console
$ docker pull archlinux@sha256:a2e682fae2dbde0a9f5421c7039faaf7f162513f8c9373d79e42dbb860a5f3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20230507.0.148551` - linux; amd64

```console
$ docker pull archlinux@sha256:9f50121537425f7f198422e36edde36bceb776cd0d1ba13182a4afbb379ed35e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252390230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eecc326df474a0acc1de170ad05986c85ff1e359fd39c5d473f8df0c63367722`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 08 May 2023 19:21:17 GMT
COPY dir:fd9732322aa0a47305a0ae1307a8ebb88de3693d3d75c342c4cdfcfb94b93583 in / 
# Mon, 08 May 2023 19:21:21 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 08 May 2023 19:21:21 GMT
ENV LANG=C.UTF-8
# Mon, 08 May 2023 19:21:21 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:3e198f7830b2313ae337ebef8336125ac512dd238fd1edd3e61e8ca5de15a146`  
		Last Modified: Mon, 08 May 2023 19:22:33 GMT  
		Size: 252.4 MB (252381563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cbb9c0d50c3d7e0f35b0d40a14805ff99a4de5f1ee5723eb2c28f7e722fff8`  
		Last Modified: Mon, 08 May 2023 19:21:59 GMT  
		Size: 8.7 KB (8667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
