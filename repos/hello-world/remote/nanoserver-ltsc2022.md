## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:fbb9fae2b9d6477ba105f2faa805db850c90292c84b080d63acbf21cc95b4b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.587; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.587; amd64

```console
$ docker pull hello-world@sha256:83ada69f673f74b81a3e2ed03edd56fcf190be8b1721f9afc4d25309908d7213
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117488530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1a3607c83c3e2cd46ec2fcbe5bc3107369653e6f2bc77976f4e83173c8055a`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 03 Mar 2022 04:50:34 GMT
RUN Apply image ltsc2022-amd64
# Fri, 18 Mar 2022 01:15:29 GMT
RUN cmd /S /C #(nop) COPY file:ac9f104fd739943f22886335a779468d86b20ac43fd3168171f6b23fc28882b9 in C: 
# Fri, 18 Mar 2022 01:15:29 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:dad81795ce109a7e20ebf80ad31925797ed97f9ba2a559f13f96ce3be5ea712b`  
		Size: 117.5 MB (117485491 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c76b7a831b8d3710d24874d5dfd820de311bf33def1c3e5a6c8e2fc2e0cfe133`  
		Last Modified: Fri, 18 Mar 2022 01:15:57 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd53ea1b7b2b52d2a8ffb3919744ae36ba26857a3d6102763efa2912b7cc725`  
		Last Modified: Fri, 18 Mar 2022 01:15:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
