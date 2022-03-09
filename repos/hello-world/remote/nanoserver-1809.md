## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:9556d033bbe119b7d3062c738b95f4ae1c8178e0a212babd5fc21b392bf91c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull hello-world@sha256:15126d518547c13b9246b76b2d3aabfa818d41d520595bae63b666853b2d0b6e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103057596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de0fbd49bb60ec2ff64597e2f27d675fae5a29bb60fbc22f076f746570fffec2`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 13:11:25 GMT
RUN cmd /S /C #(nop) COPY file:dbb4e437ca342a79d5980fcb71c065abfe00353f696b1b54084e7c09d32ec085 in C: 
# Wed, 09 Mar 2022 13:11:26 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bde2874a5fc93e40e91934fb49c3c82336a79e687be745a45bf1e86223eb39bf`  
		Last Modified: Wed, 09 Mar 2022 13:11:51 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe678157705160e6179dea142b30e4a37cb0d30afe9937b110d1e2562a9f4d10`  
		Last Modified: Wed, 09 Mar 2022 13:11:51 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
