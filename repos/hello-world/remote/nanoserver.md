## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:5553e9c813458bb731c38478ad7b743da6a57e58bc71c3029cecc2c467a78ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.2402; amd64

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

### `hello-world:nanoserver` - windows version 10.0.17763.5696; amd64

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
