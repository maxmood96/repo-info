## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:dc1f9844d414ae61044458926a3902cf092a137d44f94abf293bad24e1f514fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull hello-world@sha256:c4383750f165e8167731ca109f3d81f30352e16e012304cb063963a0013fa582
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (120996550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6183bba86cfeb06cb9cbe4f8722eda62896f191d6c42390bf3202eff8d7c5434`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Tue, 09 Apr 2024 23:50:04 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Tue, 09 Apr 2024 23:50:05 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b0fb4a0e42365a744646b3ace65ea47e6405b7f1d228307785f5b6baaaceb9`  
		Last Modified: Tue, 09 Apr 2024 23:50:07 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6776bffe9a8194dc50562905067f170b243d56364cce3bf8c12fcd7917fe2c`  
		Last Modified: Tue, 09 Apr 2024 23:50:07 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
