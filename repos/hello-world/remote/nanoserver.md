## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:89ed2f636b77c52c59c4d236f53b5069d0fc03648991776975861d9583d63545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4652; amd64
	-	windows version 10.0.20348.3932; amd64

### `hello-world:nanoserver` - windows version 10.0.26100.4652; amd64

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

### `hello-world:nanoserver` - windows version 10.0.20348.3932; amd64

```console
$ docker pull hello-world@sha256:d9edd65e29c371ce62cb1c6815f47c94d3a8c1c79fe314dce98463b22a146ac7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122633684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9ea60132a7fb4fd3aab8fb5aa2abd1d65188db97f384f4e572582ed586fb12`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sat, 05 Jul 2025 05:15:23 GMT
RUN Apply image 10.0.20348.3932
# Wed, 09 Jul 2025 18:02:57 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Wed, 09 Jul 2025 18:02:58 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:b1cf2c299ff70c52cb8ecf52e66d64d5068519867510919d8807ed2c58a54ba2`  
		Last Modified: Tue, 08 Jul 2025 21:55:51 GMT  
		Size: 122.6 MB (122630906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d55a3bd18e6b004f4d7fc478c7f24eb527de0df20399e212751f50242e8250`  
		Last Modified: Wed, 09 Jul 2025 19:41:31 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a70e0c4001c9f5237fc4dcb696d6ed1cf105275847335bdd02812b4c37ae74a`  
		Last Modified: Wed, 09 Jul 2025 19:41:31 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
