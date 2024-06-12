## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:6adeb795eba6ffe0f5f216a422f0c8bcedaa762c267b852ab4a07fbc09fac721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.2527; amd64

```console
$ docker pull hello-world@sha256:bedd92f20131366f172675aa8d227f0574410df94f7f449d8abb40638b9ad774
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120491749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e629b059ceae6728aad6d86b8bc4639b1a54c3db1509509830b6dfaf5f1c9d91`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 07 Jun 2024 08:41:16 GMT
RUN Apply image 10.0.20348.2527
# Wed, 12 Jun 2024 17:56:12 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Wed, 12 Jun 2024 17:56:13 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:f9825bcd6f9509654677a23b5fa1d32b32e1e32ff51914ebfaa76d5e79c22b50`  
		Last Modified: Wed, 12 Jun 2024 02:27:19 GMT  
		Size: 120.5 MB (120488969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae4a9ee54963e2359f1fc42cdbaa7894c0490dacc9cdb18ef2b7c00fd995ab8`  
		Last Modified: Wed, 12 Jun 2024 17:56:17 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99792d2d4e57681ac5d732e59205f715cd809c8d06bc544f9d5a8dac840e4089`  
		Last Modified: Wed, 12 Jun 2024 17:56:16 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull hello-world@sha256:8a9cdbb7d87a5b96d51acc2f988b67264986508f284302b106f453429ba88b83
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155035984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c90d546f04628c0b19849c75541d2487423f6c588106e396c6b224f5ec2de5`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 17:56:26 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Wed, 12 Jun 2024 17:56:28 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634ad9b3680b8bfd56a4b47c33e16956b554d5ed4c7790589cb7eff222bffee8`  
		Last Modified: Wed, 12 Jun 2024 17:56:32 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e8ea356b1b661caa0532796a689e75d5e5ca9e94d41e83b5d8f8701913686c`  
		Last Modified: Wed, 12 Jun 2024 17:56:32 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
