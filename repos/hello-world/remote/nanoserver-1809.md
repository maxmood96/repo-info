## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:8b97da9225b98594f05d57b758e0a94a446d951fe864329ba6c90f036df84569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull hello-world@sha256:314cc0309465c7be2936df274b258c843f5a49eb21f63b719d60b51564070b8f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103380275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716a6b564ec2cbc27ccbd9b7915b1d4d0f8ab671e3697e7ee02dc6d54e812a4e`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Wed, 12 Oct 2022 12:39:53 GMT
RUN cmd /S /C #(nop) COPY file:994f63bc3cea8285310afa5f4677df29bf99dd4cd1881c7e381100a9e794ba71 in C: 
# Wed, 12 Oct 2022 12:39:53 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dcaa3ee7a7789ce99e13c96aff0dbaf647f9f8fd95b3af930ef72c38868ebe10`  
		Last Modified: Wed, 12 Oct 2022 12:40:17 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047878d87897fb101d62d80e5e67d22ea9cd17cd567e67fc2a587e4bcfef51aa`  
		Last Modified: Wed, 12 Oct 2022 12:40:17 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
