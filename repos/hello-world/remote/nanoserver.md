## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:3ce25bf5acc8c908df8cfad82808c3c7c333c07fd571e73037da7c3b0cc1b173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `hello-world:nanoserver` - windows version 10.0.26100.3194; amd64

```console
$ docker pull hello-world@sha256:ae7ea054bc645dcb17b77711793c72befb15cccbafc4af8f755fdcd70a0bec58
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205893106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a563a14dfbf577f13d1a74c4badce20c2c7e2fcbea9d07362c282b5d2d936fb4`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Thu, 27 Feb 2025 18:15:34 GMT
RUN cmd /S /C #(nop) COPY file:1ae3735b36d6b3fc6ef1fd1d2d12badf8f42ad5660d983c9a406cb560633ed37 in C: 
# Thu, 27 Feb 2025 18:15:35 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5736904805ab9d01ebb6fd24d5a0c8501eb4417bb31180d5758210425464b8d`  
		Last Modified: Thu, 27 Feb 2025 18:15:40 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ee15bcb9c08902687843991154d64b467a271fac41fcfe3c8b94e490a30982`  
		Last Modified: Thu, 27 Feb 2025 18:15:40 GMT  
		Size: 1.1 KB (1057 bytes)  
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
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deafd885d2fb0adc49a6ae6ba5babf9642332bed5fcc91396f93e2c3a09f38de`  
		Last Modified: Thu, 13 Feb 2025 00:28:02 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c01454f8e89eae3973609c8d8655838cffc120290c8fb1bdbc21e0b996c692b`  
		Last Modified: Thu, 13 Feb 2025 00:28:02 GMT  
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
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6ae2e93fcab86cfb343d0d766eeaa15086901ae9b5c8e2a468cd78bb4f6726`  
		Last Modified: Thu, 13 Feb 2025 00:28:10 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9fe1136a6ad1252569c0ac51fc15bb8f0bbc7b49d3016c9fdc7cb8b4299106c`  
		Last Modified: Thu, 13 Feb 2025 00:28:10 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
