## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:98e4156021519d4276d9caa8ef6056d23b03ee287f666ab7a2985dcb5527c5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.3932; amd64

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
