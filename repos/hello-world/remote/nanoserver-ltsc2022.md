## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:0f6b36b03cab58839a681ea359a95edea3c2975bd33556075c2c63ac0ba40ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull hello-world@sha256:142e3968ff098bc0f115061e7c394b2f739514d4ee623de12c3c27cbb1459818
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126653358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc8e3f21a5bc2b00742560607adf2bd1e34f33a8bc81f53611bccbaf961cc37`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 21:54:46 GMT
RUN cmd /S /C #(nop) COPY file:9fca1d3c77d0758894ceeb7952e49e3b465b238dc4943832e9436b0ce84d8ae0 in C: 
# Tue, 10 Mar 2026 21:54:47 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0fbd4b4d15aacdd47d0a123445d3c9206a4e85fd62d141b893b0221699d4a4e`  
		Last Modified: Tue, 10 Mar 2026 21:54:52 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39690600a12d00521e1f963085b41e99597198e13ae6c2c4602c2972214a7089`  
		Last Modified: Tue, 10 Mar 2026 21:54:52 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
