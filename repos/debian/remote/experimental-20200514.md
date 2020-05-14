## `debian:experimental-20200514`

```console
$ docker pull debian@sha256:23f0349320820039fe233f1da55e16782767aa9b827a23c7b91fcf75eaee1774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v5

### `debian:experimental-20200514` - linux; arm variant v5

```console
$ docker pull debian@sha256:553160de9701152d62830a1eae94d051510ae9544928d71bc12bdf4be8b5b948
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49373220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79348a931e55bc68a47f79f7a554bf58b70d05e187aa5df5012d7704bffe1468`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 14 May 2020 22:44:12 GMT
ADD file:86dde72a0ab87a01f23f0bc2339837559b947f3e626920eaad484dbb2c920097 in / 
# Thu, 14 May 2020 22:44:13 GMT
CMD ["bash"]
# Thu, 14 May 2020 22:44:40 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:20f4bc02075b420ec27f08f233c21d9dcd74f712769151e4335502e9da73aafe`  
		Last Modified: Thu, 14 May 2020 22:52:03 GMT  
		Size: 49.4 MB (49372997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393ad04afc168826c552d8f126cbcb90d6cd2d1f5aeeebee1fea7ae0cffae0cf`  
		Last Modified: Thu, 14 May 2020 22:52:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
