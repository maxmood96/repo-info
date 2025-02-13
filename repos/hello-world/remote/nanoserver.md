## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:699089bc6261afcd8b920c4c505439d60af702ef0c8c82aad7527c903661becb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `hello-world:nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull hello-world@sha256:3070452d117828a9eb91c87c71f7e71605ceb531598c0acd2575ac2a90b8791d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199057063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c690bbde374586e3022cf23491339d9925d92e728ce4f5020338ec3657aecdee`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 22 Jan 2025 02:28:04 GMT
RUN cmd /S /C #(nop) COPY file:1ae3735b36d6b3fc6ef1fd1d2d12badf8f42ad5660d983c9a406cb560633ed37 in C: 
# Wed, 22 Jan 2025 02:28:04 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Wed, 22 Jan 2025 08:02:27 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a575af90262df1196a014105a8994708f234f7f3663b27c5be27508443c98d9e`  
		Last Modified: Wed, 22 Jan 2025 08:02:17 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6308f12cac64ca86e267b96ebe7b3a1a876e0e6f8874df3113c7f72b9dfa05b6`  
		Last Modified: Wed, 22 Jan 2025 08:02:17 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.20348.3207; amd64

```console
$ docker pull hello-world@sha256:01d0af4ccf62079415ccc6f718b01c09def42b8392cd4402984bea12978e102d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120669384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ab5e9e4b884f9f1f5b1c2ec34ca7e818d76b69f0f9d28bef07f8de461669f4`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 00:28:00 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Thu, 13 Feb 2025 00:28:00 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:49:39 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deafd885d2fb0adc49a6ae6ba5babf9642332bed5fcc91396f93e2c3a09f38de`  
		Last Modified: Thu, 13 Feb 2025 02:41:40 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c01454f8e89eae3973609c8d8655838cffc120290c8fb1bdbc21e0b996c692b`  
		Last Modified: Thu, 13 Feb 2025 02:41:40 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull hello-world@sha256:6f3e9cb5ba02b4607759878cab7a0e838580ac23e95ee5dad4410bfef2707182
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106918232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863268e13a654ebe7b16e038a9c68028f49d87079004a5b46914968fbbdda689`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 00:28:05 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Thu, 13 Feb 2025 00:28:07 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6ae2e93fcab86cfb343d0d766eeaa15086901ae9b5c8e2a468cd78bb4f6726`  
		Last Modified: Thu, 13 Feb 2025 00:28:42 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9fe1136a6ad1252569c0ac51fc15bb8f0bbc7b49d3016c9fdc7cb8b4299106c`  
		Last Modified: Thu, 13 Feb 2025 00:28:42 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
