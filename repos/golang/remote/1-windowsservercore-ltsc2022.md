## `golang:1-windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:197cca7f072029c62f6b5b831fdebfc03358b2069bc18d75950128696677bd27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `golang:1-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull golang@sha256:5d5a07a31ab9dfd63886e061d350bdf794c3431137efe077fbd060d3abc5ca18
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1565299402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300435b66223816997abcfdb6f31d49e3830dacc240d7ae2415371a4a132f2b4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:01:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:01:13 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Sep 2024 00:01:14 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Sep 2024 00:01:14 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Sep 2024 00:01:15 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Sep 2024 00:01:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 00:01:31 GMT
ENV GOPATH=C:\go
# Wed, 11 Sep 2024 00:01:37 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 00:01:38 GMT
ENV GOLANG_VERSION=1.23.1
# Wed, 11 Sep 2024 00:03:40 GMT
RUN $url = 'https://dl.google.com/go/go1.23.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '32dedf277c86610e380e1765593edb66876f00223df71690bd6be68ee17675c0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 00:03:41 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e70f49c20671d030640819fe99e5b846a1ee5d8fb54950cedc8bffd9c6e29a`  
		Last Modified: Wed, 11 Sep 2024 00:03:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7599a220d99a5983979a2065f169fff89d4ac209d3ad341f6e11abeece8339d6`  
		Last Modified: Wed, 11 Sep 2024 00:03:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f726ad3a1e48a9ea73e77512f6f3aaf77051e52138fef0fabe83d10356188556`  
		Last Modified: Wed, 11 Sep 2024 00:03:47 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbeedd49da6baf674ed68e04cfa55364041bfd3b70d60c5f46f3b5c673b0508b`  
		Last Modified: Wed, 11 Sep 2024 00:03:47 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a120805c5139fe19432413b01774c55fe1593495966fedfb484316001dd50a`  
		Last Modified: Wed, 11 Sep 2024 00:03:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5010db3b75e0a589feff552b65d39808ef3ac6e6ae01cd982d64ffdf4c9dfe`  
		Last Modified: Wed, 11 Sep 2024 00:03:49 GMT  
		Size: 25.4 MB (25430526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bf413e96f658b2a166655b10f293f82c04512e88f3c05145dcedba34f8f0ce`  
		Last Modified: Wed, 11 Sep 2024 00:03:45 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7beb51ae082094234d5bb9a42204cb0805c7d4c3a4d5f1b30f08f6dfc3dd67`  
		Last Modified: Wed, 11 Sep 2024 00:03:45 GMT  
		Size: 336.3 KB (336263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ede37f38dfa3cd5022991843081e14382488928f40fca1ecc38efc74bfaa8c3`  
		Last Modified: Wed, 11 Sep 2024 00:03:45 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bdfe800dc36d8ceb8f648238c2c0e6f0d72274752fe15497e99f69712c7cad`  
		Last Modified: Wed, 11 Sep 2024 00:03:57 GMT  
		Size: 77.3 MB (77329741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bfc9fd2237a63248c24f2d2b4341b9597abe5da57d5f8a3c18bf279b7ce63e`  
		Last Modified: Wed, 11 Sep 2024 00:03:45 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
