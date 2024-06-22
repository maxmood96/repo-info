## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:b5993bfba93aba4413abcb6da1cb5e9f2d158285ea9e411550f3428caa03ff27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.2529; amd64

```console
$ docker pull hello-world@sha256:d9958c926e37a9700d85698bc9872cae110bbbb26f551a9684da9a8332dbb778
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120502323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a78ae902b550731ac17bfc560f7ebc0dc09007d0104648cc8718a74cc455efe8`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Wed, 19 Jun 2024 19:27:30 GMT
RUN Apply image 10.0.20348.2529
# Fri, 21 Jun 2024 23:54:39 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Fri, 21 Jun 2024 23:54:40 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:a8c295c425a912de308ded279124ae45fec44d55a451843fe5877155417f453c`  
		Last Modified: Fri, 21 Jun 2024 02:24:34 GMT  
		Size: 120.5 MB (120499549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c9816903701133197e67f7ef017b59b526a34244afaf782fe5696f159f3ade`  
		Last Modified: Fri, 21 Jun 2024 23:54:44 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907ea000aac247469eb42ac65876290a3b357a2174a0db6fc2286cfd8cf6b1ec`  
		Last Modified: Fri, 21 Jun 2024 23:54:44 GMT  
		Size: 1.0 KB (1029 bytes)  
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
