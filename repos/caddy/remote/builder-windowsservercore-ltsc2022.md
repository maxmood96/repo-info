## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:82ec3c48adfe152d1c125013819460a00c41f8de1485234c5757ac620ca0f6b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2527; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2527; amd64

```console
$ docker pull caddy@sha256:a5c9736e07d2e51fc117c08a132ddd8cf0d4d157cc8ce24dde31e4833e220148
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2217625172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e712c86b78dda184eedc0dd175768d280e951233e45b985a826454212f5ffb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Wed, 12 Jun 2024 18:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:09:22 GMT
ENV GIT_VERSION=2.23.0
# Wed, 12 Jun 2024 18:09:23 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 12 Jun 2024 18:09:24 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 12 Jun 2024 18:09:24 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 12 Jun 2024 18:09:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:09:44 GMT
ENV GOPATH=C:\go
# Wed, 12 Jun 2024 18:09:50 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Jun 2024 18:09:50 GMT
ENV GOLANG_VERSION=1.22.4
# Wed, 12 Jun 2024 18:10:55 GMT
RUN $url = 'https://dl.google.com/go/go1.22.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '26321c4d945a0035d8a5bc4a1965b0df401ff8ceac66ce2daadabf9030419a98'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:10:57 GMT
WORKDIR C:\go
# Wed, 12 Jun 2024 19:06:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 19:06:22 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 12 Jun 2024 19:06:23 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 12 Jun 2024 19:06:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 12 Jun 2024 19:06:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 12 Jun 2024 19:06:37 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0587398dd0c7678da17819ef86b03d0f03d5608d921ef1bd9dd041001aa46064`  
		Last Modified: Wed, 12 Jun 2024 18:11:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9adab2cbb6127c55064d7c9aa02c40af934b227b342e9ce0ed36ee98f1b4843`  
		Last Modified: Wed, 12 Jun 2024 18:11:02 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ff0b716a5ce8110bb53b45bd91710d820149130deed9c38472234a7e9afd9`  
		Last Modified: Wed, 12 Jun 2024 18:11:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96de8f0195629f8fc68326d735d8815462e97b6c76fbbf56e537824e83e8e4be`  
		Last Modified: Wed, 12 Jun 2024 18:11:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc335406a0dfe2ded2091ea3986516dfe4e922b476d834ddb8aec57c37e493c`  
		Last Modified: Wed, 12 Jun 2024 18:11:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5e46457004c449858017460ecd124b76a51b6e5c4d75579bd0fed83a03b66b`  
		Last Modified: Wed, 12 Jun 2024 18:11:04 GMT  
		Size: 25.4 MB (25426639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a91a7cff7f3986c1704d0d0fc42da5934271de00dc73f1bbbb33c58179ae1d2`  
		Last Modified: Wed, 12 Jun 2024 18:10:59 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ffbe09e050d4b99a243d40d14a09182e015c0a0d40c056ecd2f2b196eb9d06`  
		Last Modified: Wed, 12 Jun 2024 18:11:00 GMT  
		Size: 325.4 KB (325417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342559014cfb73e966442ed88b5360904cd00c05a834f575b49596888e680792`  
		Last Modified: Wed, 12 Jun 2024 18:11:00 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea1a9b1009e5fa7a44f4b39043515d74d2b1a71c21fa1252506b20c9d8d935`  
		Last Modified: Wed, 12 Jun 2024 18:11:10 GMT  
		Size: 71.7 MB (71736322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59599ecaa1eb84019e233b455deae710859ed0f0a323ec5689d820efaf55ff3f`  
		Last Modified: Wed, 12 Jun 2024 18:11:00 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65d85360857cfc8e00101a27ce37393334201cf7ad2bfa92f1d25ac2c46a099`  
		Last Modified: Wed, 12 Jun 2024 19:06:40 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a649add317f0043f54d8847dbb12dec7f65e49c4aa06a80f8c512a69166caa8`  
		Last Modified: Wed, 12 Jun 2024 19:06:39 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874045c3f76c039258ec0823fa7e4e83cd2dcd56615e0bd7d98e12954e51b3c1`  
		Last Modified: Wed, 12 Jun 2024 19:06:39 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a82ca2afafcf0ef97e7a1ce7133e6331a3165d1b37c49d49e7e344d5a6e4a98`  
		Last Modified: Wed, 12 Jun 2024 19:06:39 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2693bfc3905400c24ddcd564bde563b2bcf9db8bba5d8ca5bc5655ecc0fe8029`  
		Last Modified: Wed, 12 Jun 2024 19:06:39 GMT  
		Size: 1.9 MB (1941203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bea81e16e408457ef5a11b956b6c21f1c2995e66814c68bc50b44bba9f18764`  
		Last Modified: Wed, 12 Jun 2024 19:06:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
