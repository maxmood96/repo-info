## `debian:experimental-20200803`

```console
$ docker pull debian@sha256:c65c8fcecdbe57da78a3307b21e07fe612ec4683ac8ad255b5f1eae1195d17bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; s390x

### `debian:experimental-20200803` - linux; s390x

```console
$ docker pull debian@sha256:b97d78d7a3a3c05d6318ea98ab41d08ee7688483c5751e25bf0c408078f760a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50989909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cecec4fb770fe6058e4a9088ca9316b057428a5a41bc75b2785c6c951d10ba1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 01:18:32 GMT
ADD file:238775756e52141121b66ba51576ceee22305a02064e8261d22b3456f304742a in / 
# Tue, 04 Aug 2020 01:18:35 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 01:18:48 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:1a10cec4db9a5323183a623bd9e0474e42e07ec7f12bb35f5241e88c12d5e0f0`  
		Last Modified: Tue, 04 Aug 2020 01:21:29 GMT  
		Size: 51.0 MB (50989689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393f1bb150f06b334cff987be5d2d8f1704d0244fcc5645876eef9e641e052ce`  
		Last Modified: Tue, 04 Aug 2020 01:21:45 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
