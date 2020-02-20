## `golang:windowsservercore-ltsc2016`

```console
$ docker pull golang@sha256:23eef101b96ec1b0aec2d7e910fc5853d0d65946dc739d51652ec6d29dcf6834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `golang:windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull golang@sha256:dd836044142e66a5478c413a3934208ba7c464412084de9ea5cb548ca31e998e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5902204818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ef4e4e8931568a1d11979029be98e189a1fa80c904cdf0eae4b812171c446d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 01:48:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 09:14:29 GMT
ENV GIT_VERSION=2.23.0
# Thu, 20 Feb 2020 09:14:30 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 20 Feb 2020 09:14:31 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 20 Feb 2020 09:14:33 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 20 Feb 2020 09:16:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2020 09:16:17 GMT
ENV GOPATH=C:\gopath
# Thu, 20 Feb 2020 09:17:39 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2020 09:38:17 GMT
ENV GOLANG_VERSION=1.13.8
# Thu, 20 Feb 2020 09:44:45 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'aaf0888907144ca7070c8dad03fcf1308f77a42d2f6e4d2a609e64e9ae73cf4f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2020 09:44:47 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:72c4471958f7f0f07260f0f430bcffb0bc07811088c24cffba1439d250ea1ae3`  
		Last Modified: Thu, 20 Feb 2020 03:04:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560a5edc3b65548cd8f0a5736740259c10731b69be646647541d454f4a46d74d`  
		Last Modified: Thu, 20 Feb 2020 10:16:28 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d778cb1587245dbb3aa1eadff960d2ca6808181a7f76399e1461b4488dd0d110`  
		Last Modified: Thu, 20 Feb 2020 10:16:27 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc71d139522c2d69f799715a806ce8ce02bd536d9fb33c3c1cff0d512c06ebe`  
		Last Modified: Thu, 20 Feb 2020 10:16:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3aec6ae82f728acb67ab3203c9f84faf93c0ff671c1d1341837da6f6127ec3`  
		Last Modified: Thu, 20 Feb 2020 10:16:25 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6734e518b8f70059c148a428fbd47fe51d143e43477597a7b34afb502090a6cd`  
		Last Modified: Thu, 20 Feb 2020 10:16:57 GMT  
		Size: 30.5 MB (30460160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52c1cb26338697dbffd8fd282e956aa88db7f630a7b5c1c90f750eee04c24e4`  
		Last Modified: Thu, 20 Feb 2020 10:16:22 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58993efc965e34067a71381b74e269f61cff043dfd64a430cddfcd494cd3f21`  
		Last Modified: Thu, 20 Feb 2020 10:16:24 GMT  
		Size: 5.3 MB (5316014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1641e5e221d70fe47bdc6e53566f897cbacd924273c19d5103b8822eafb90b66`  
		Last Modified: Thu, 20 Feb 2020 10:23:23 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cab2aaa90d685cb58454410a4ce7a70ba56b5bce9527800358ab58e753bf66`  
		Last Modified: Thu, 20 Feb 2020 10:25:00 GMT  
		Size: 139.4 MB (139353947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a2c1a7c740886e212708af170a7b6a56680fd645dcde5257747f26f8454389`  
		Last Modified: Thu, 20 Feb 2020 10:23:22 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
