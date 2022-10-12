## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:96c17cd8a327943fda25768af9b1d02459366d980dde03a14888be38721415ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.1129; amd64

```console
$ docker pull hello-world@sha256:7aef5136b6c5aa5cb38b504f3c5d1aa61b6ec6db2565ae81d705c10b49241167
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118205899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0eb300498435cbaa827ae2a85900e920dd9528c0a253ae6a07beb7b5fae99e`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 07 Oct 2022 21:37:41 GMT
RUN Apply image 10.0.20348.1129
# Wed, 12 Oct 2022 12:39:47 GMT
RUN cmd /S /C #(nop) COPY file:ac9f104fd739943f22886335a779468d86b20ac43fd3168171f6b23fc28882b9 in C: 
# Wed, 12 Oct 2022 12:39:48 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:38fa349577729651ac1fc3ec785f908719a8100da5f5ba9bd3f549411061f583`  
		Size: 118.2 MB (118202895 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cb2f9654ae65bd4aa50f3463f2d053025144322b599cc6506edf94170f1f170d`  
		Last Modified: Wed, 12 Oct 2022 12:40:11 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc05f03f8ab022e18841de9561dfccb6f6df66bd58150f7d0add0dda8f875a3`  
		Last Modified: Wed, 12 Oct 2022 12:40:11 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.3532; amd64

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
