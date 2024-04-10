## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:279075d823fc6f778bf6bd527bcd79dab74e827444ff4798699e1fc40a0d8f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull hello-world@sha256:decbb9d66399e68ef1d5ad6e0a84057a0f9bb3c7bfd9df9f454ff3c30b60fec6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104891882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9f32d288d684ef2485c6aa1c5a498f76e926d998edc011f6c3da7c38f93adf`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 09 Apr 2024 23:50:02 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Tue, 09 Apr 2024 23:50:03 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7a4d21244056d6850efb8b3f1aea49148ce8cafd45059eef5c6eec348a3769`  
		Last Modified: Tue, 09 Apr 2024 23:50:07 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c578c8e40773064b768668d7fa5f103f3810770fb1b59c74966f4453bea0be9`  
		Last Modified: Tue, 09 Apr 2024 23:50:07 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
