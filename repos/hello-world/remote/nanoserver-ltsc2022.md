## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:6186fdf64eb98ada6bed08d96ff3eabd9b8879b3d29e9181182b514ed7adacef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull hello-world@sha256:bd384cb998fddc3689dacf6d8971714572d529ff40ef94c294f9d963a2c34894
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126361204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e726fb2f74e5a885ba2b26c9bfd5b6bfbfcc4efebbeb8ab5c806e101a029775`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 09 Dec 2025 20:31:03 GMT
RUN cmd /S /C #(nop) COPY file:9fca1d3c77d0758894ceeb7952e49e3b465b238dc4943832e9436b0ce84d8ae0 in C: 
# Tue, 09 Dec 2025 20:31:04 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f032cf60b93275d5e414ae5399172e24927a8db9c16ce206fc4c43ab19e32fc3`  
		Last Modified: Tue, 09 Dec 2025 20:32:08 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b7cf4439b052eee4164d6536e132dee6144721c3f1ce4e7c016275d3974b5f`  
		Last Modified: Tue, 09 Dec 2025 20:32:08 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
