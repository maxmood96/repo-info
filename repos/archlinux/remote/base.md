## `archlinux:base`

```console
$ docker pull archlinux@sha256:36e2876411794d29ba163a33c7b17f53ae8cf3a0d63f90bd410cb034f96fb97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:7947166ecaec15150de144eb97d5614691b45007fd0141f7e3d4ec754198e711
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (151045785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb5897a718324a14186d04adfd62d073920d20c4e57596bb1a2c31ec44835fd`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 14 Dec 2020 21:20:16 GMT
COPY dir:4008a053e51a7a7a7b4b56bde30fc6d1c92f16cafffd85212ac9a99ae047e0b3 in / 
# Mon, 14 Dec 2020 21:20:17 GMT
RUN ldconfig
# Mon, 14 Dec 2020 21:20:18 GMT
ENV LANG=en_US.UTF-8
# Mon, 14 Dec 2020 21:20:18 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:8fa724bed336c2326c4f6dace50d81495422a3a2efc3523d0b2732a4539ead4f`  
		Last Modified: Mon, 14 Dec 2020 21:22:23 GMT  
		Size: 151.0 MB (151038577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7402f78f0ca30974687b60677cdf4c0da2957070f4fe09647ddc72e5ce88e9a3`  
		Last Modified: Mon, 14 Dec 2020 21:21:51 GMT  
		Size: 7.2 KB (7208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
