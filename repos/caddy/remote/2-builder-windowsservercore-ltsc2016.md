## `caddy:2-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:8e5dcc2f90feef29505c8c129dd01f248bfd711239067688d5e3f62344e0e98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4225; amd64

### `caddy:2-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.4225; amd64

```console
$ docker pull caddy@sha256:dc60be64ca49e58322820d0b131c888ef7579bb81c7f0ac43b9d2dfc4d3927f3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5991336189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc93b3f3d3e9fa5eae84d6a2159b9a5b7442d1a9994060cb484859b14918e9a8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Jan 2021 18:11:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Feb 2021 13:17:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Feb 2021 13:17:29 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Feb 2021 13:17:30 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Feb 2021 13:17:31 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Feb 2021 13:17:31 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Feb 2021 13:19:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Feb 2021 13:19:29 GMT
ENV GOPATH=C:\gopath
# Wed, 10 Feb 2021 13:20:42 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Feb 2021 13:28:06 GMT
ENV GOLANG_VERSION=1.15.8
# Wed, 10 Feb 2021 13:30:56 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ef05b7141d3c217fb076f0e27249e144296234df96ead8751c0b76784079df97'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Feb 2021 13:30:57 GMT
WORKDIR C:\gopath
# Wed, 10 Feb 2021 19:47:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Feb 2021 19:16:07 GMT
ENV XCADDY_VERSION=v0.1.8
# Wed, 24 Feb 2021 19:16:08 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 24 Feb 2021 19:16:09 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 24 Feb 2021 19:17:28 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('ccbc594da07adff41098959a78efaaee42fca4e5feb7806661d00841229b20ff1c47fed024c7a84e8554d3e8be3f162d3750e5e8347d6a230c496d4b133213e8')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 24 Feb 2021 19:17:29 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:62c48323ed8ac695b8cbe0ecedcc28ba185a234673ad9241df2b151dd00f9181`  
		Size: 1.7 GB (1725027107 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c03f1c41641d4a4cf6906dee9a590ee67135d926dddab80cfef993cae745a38a`  
		Last Modified: Wed, 10 Feb 2021 13:41:36 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b7d5e389f10cfda51d65a6ae3f276f7d7024f7bd893552d4a1bb61519303d`  
		Last Modified: Wed, 10 Feb 2021 13:41:35 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2799be5b45aa28655c9b5b8566161e2bef34941a26819b95e78adf73395a140d`  
		Last Modified: Wed, 10 Feb 2021 13:41:33 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4abafe711a056131c41f2e38c31bab22e53fd22bafa8737a1674dd98cff6b0`  
		Last Modified: Wed, 10 Feb 2021 13:41:30 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559f5834d24f448fb2fc996be05a9ba6ad3c60712d356f8998027bfa2854e245`  
		Last Modified: Wed, 10 Feb 2021 13:41:30 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4665c4dcb86678e831cf1a6d98ac2cabd574d98b4e9994a14240255d9a6e23`  
		Last Modified: Wed, 10 Feb 2021 13:41:40 GMT  
		Size: 35.3 MB (35260888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f87b110bca4039b64196c92191debb8b0b77a61d53c39b538bb67ce5a066ebe`  
		Last Modified: Wed, 10 Feb 2021 13:41:27 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6d8f3b9818027f57174844f7bd4ed68d5bd1eae553473f69ba50771a94f7de`  
		Last Modified: Wed, 10 Feb 2021 13:41:28 GMT  
		Size: 5.6 MB (5624659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c55a9e878249fe3842cd660da87d939b530608de5ef62658140c82b0d99458d`  
		Last Modified: Wed, 10 Feb 2021 13:43:56 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdfdd00decaf3169e40533439846cc4c9ad7f3b073a88e8f0718de18a4e4f28`  
		Last Modified: Wed, 10 Feb 2021 13:46:53 GMT  
		Size: 143.9 MB (143914759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bbf8517b0c41f42dc6f3367ff51a793f97804190cd3919856549e7d94de20d`  
		Last Modified: Wed, 10 Feb 2021 13:43:56 GMT  
		Size: 1.5 KB (1497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf654781aff9f8df2496d321d35ef4fbbbf1094435d119368393eade0767b278`  
		Last Modified: Wed, 10 Feb 2021 19:56:23 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c02754754afc6a6083e193fbc81ef9e65d884dbc075766e72f0a91138dfcdf`  
		Last Modified: Wed, 24 Feb 2021 19:24:27 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b781c60264cacc417a1e3a726eebeeb6fed1281006fce56233a874c47b8970e3`  
		Last Modified: Wed, 24 Feb 2021 19:24:27 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898ce1a95721fb0661d6a669de397284806caedfb15d21695faf92f13cbcde68`  
		Last Modified: Wed, 24 Feb 2021 19:24:26 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63fcc5961438b3e123e044bbb06e0768d2b0f020e072c879931bd17dff00f45f`  
		Last Modified: Wed, 24 Feb 2021 19:24:30 GMT  
		Size: 11.5 MB (11505050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1d8407443c8e76c72f8039aa25a7d9f1225636f523bb0e4b4dcbb6d2cf3a84`  
		Last Modified: Wed, 24 Feb 2021 19:24:27 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
