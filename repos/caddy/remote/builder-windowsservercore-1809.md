## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:0ede8ea9a0d63b1802e0db90250d2e1f5004dc34e505675783097e88ad637eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:7dd88cf5386164bd3834c899b1a032a2060e71a79c360dea683f93fdd0cb8f00
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261639695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:113b740ce7f61066da4a74e0fd670e04f4da4bf8f86c743396d25b2fc08a2944`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 14 May 2024 22:57:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 May 2024 22:57:12 GMT
ENV GIT_VERSION=2.23.0
# Tue, 14 May 2024 22:57:13 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 14 May 2024 22:57:13 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 14 May 2024 22:57:14 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 14 May 2024 22:59:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 14 May 2024 22:59:29 GMT
ENV GOPATH=C:\go
# Tue, 14 May 2024 22:59:52 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 May 2024 22:59:52 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 14 May 2024 23:01:43 GMT
RUN $url = 'https://dl.google.com/go/go1.21.10.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '09170b66e7d7c4e2e7a30b8f3350778a8ba5c15951b7eb8ff7545cb86ea9bb71'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 May 2024 23:01:45 GMT
WORKDIR C:\go
# Tue, 14 May 2024 23:56:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 May 2024 23:56:45 GMT
ENV XCADDY_VERSION=v0.4.1
# Tue, 14 May 2024 23:56:45 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 14 May 2024 23:56:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 14 May 2024 23:58:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b058280b1e15e0915c541bc8a3aefc2289155c38a9fbc2f8d6b05267f9d0469eae5be2a9312d52c5ba41c7dbcb18c0970efa5b1df628655cca81b55d5c51d9e1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 14 May 2024 23:58:25 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088d1c0c1fa98ff61a3a4e47ae33e6a344704ebf07a13649548e2c7984557e9c`  
		Last Modified: Tue, 14 May 2024 23:01:53 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd83ee5a124b5e6292719fd34ac412d3ccddb0bbe08a8642e88352d8878e2e2`  
		Last Modified: Tue, 14 May 2024 23:01:53 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a9a1b490a522afd02acb513d17507bc7cf39ab0ef055968d2ccf23f483e0fe`  
		Last Modified: Tue, 14 May 2024 23:01:52 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c0dab5edac35fbf3b4f9f45b8c9cda1e9c139562824a39365c4d02b478808`  
		Last Modified: Tue, 14 May 2024 23:01:51 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0157a878e7cfd04a5dd35cc530fa102e9be1331aa087b67781060d6bfc94dba5`  
		Last Modified: Tue, 14 May 2024 23:01:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b0e0c840739c5ae7114d04d9539804d69f0687e96ba83b944978cd4749a012`  
		Last Modified: Tue, 14 May 2024 23:01:54 GMT  
		Size: 25.6 MB (25594319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9295538e8dccc7937522ab481cb8809401ac0bb304396506f7507a9cb6249e8`  
		Last Modified: Tue, 14 May 2024 23:01:49 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7baa2cc2a41c934a58158700b5392c2ef11f4147da056b17dc162507d420c5`  
		Last Modified: Tue, 14 May 2024 23:01:49 GMT  
		Size: 356.4 KB (356436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65d164a257dc9d5baa6a6a84ac657eab4812896c7948c3e97257c74cecfd293`  
		Last Modified: Tue, 14 May 2024 23:01:49 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af07293862767d9d567ed8aa6c77ca122f8f6f7202c0ee93d98637fc0afe746b`  
		Last Modified: Tue, 14 May 2024 23:01:59 GMT  
		Size: 69.4 MB (69409653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c374294e81a51d9395ead01e53603a4734b13fdf81579b1ce8d39a1ae8521f35`  
		Last Modified: Tue, 14 May 2024 23:01:49 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1328da056625dbec01da58ec189903e4d9f2f730b9aa7fcc2ce0901c5369651`  
		Last Modified: Tue, 14 May 2024 23:58:31 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afe629c4b6a6e4aaa8a66aec777cb6cd34311493fa212d91f88e7427931f98e`  
		Last Modified: Tue, 14 May 2024 23:58:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b79f33eed0e0051602cbcd4e4288f9d3777696aad097833e22347da0fec8ba`  
		Last Modified: Tue, 14 May 2024 23:58:29 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9580bc12be5ff71be94ac2c6b5acece45e6ef9bc2a994e9079642250bae678`  
		Last Modified: Tue, 14 May 2024 23:58:29 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36261b39597b0d0bda8d948013503d964fe3cb909e871b8ac753d685cb01a4e`  
		Last Modified: Tue, 14 May 2024 23:58:30 GMT  
		Size: 1.8 MB (1834255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc1a5fba06c99c3f24b2d54ef6d34af93724d183f41bc80eeb9ae83b271f655`  
		Last Modified: Tue, 14 May 2024 23:58:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
