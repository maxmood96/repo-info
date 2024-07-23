## `debian:experimental-20240722`

```console
$ docker pull debian@sha256:93caa3cc12c5ae2239dceaf981ec8ee65381b6384ff03321f2eb2059659b5d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm variant v5

### `debian:experimental-20240722` - linux; arm variant v5

```console
$ docker pull debian@sha256:b4be955acce84a54996a66b1ddef6208a730df64edd7c16cca82c79075ff78b8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49829070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ce57ee8b511589e7f5fef09dd2f5ecccc2ec9d797f69754507245b121c2cc3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:59:37 GMT
ADD file:b7dee3cae68ec5b68cbf4203b7915b3fdbdbd18c57197bc477af2bcc51091103 in / 
# Mon, 22 Jul 2024 23:59:37 GMT
CMD ["bash"]
# Mon, 22 Jul 2024 23:59:53 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ac278e94839effcbf29dea60649ffd4beddf76d58e50d95a6a923683376a0b87`  
		Last Modified: Tue, 23 Jul 2024 00:05:17 GMT  
		Size: 49.8 MB (49828849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e979dc2dcec23b083707698e2eef10b041f9a56006bbe533bbecbf253b0f01`  
		Last Modified: Tue, 23 Jul 2024 00:05:38 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
