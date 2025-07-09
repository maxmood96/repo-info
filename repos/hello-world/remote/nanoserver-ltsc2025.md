## `hello-world:nanoserver-ltsc2025`

```console
$ docker pull hello-world@sha256:618eb5a8002f84a948df2ffa5d515244c8f2034674ff9e50f743741c9a3d7edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `hello-world:nanoserver-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull hello-world@sha256:f9ad50268d1f5b6501243ec2782e24874aea7f3895b611ce2116079dbcb7007a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 MB (193153217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8520cd28c723e1f360e442b678190dbeeb1abea32ef87d87e2d9557a0afa4d02`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sat, 05 Jul 2025 18:13:07 GMT
RUN Apply image 10.0.26100.4652
# Wed, 09 Jul 2025 18:03:17 GMT
RUN cmd /S /C #(nop) COPY file:1ae3735b36d6b3fc6ef1fd1d2d12badf8f42ad5660d983c9a406cb560633ed37 in C: 
# Wed, 09 Jul 2025 18:03:18 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:2fd4507679915420227c89c4f57165747b37deaa62748936e2af8c2f38de0b4e`  
		Last Modified: Wed, 09 Jul 2025 01:51:41 GMT  
		Size: 193.2 MB (193150329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0aad7cd5ecee2d19f1232d7d1050911d369460a6a69a8722b5207a85475836`  
		Last Modified: Wed, 09 Jul 2025 19:41:30 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53db689f09783881088b73e38a596e17bc6e1e6c3bc3a693a783a38be18a648a`  
		Last Modified: Wed, 09 Jul 2025 19:41:30 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
