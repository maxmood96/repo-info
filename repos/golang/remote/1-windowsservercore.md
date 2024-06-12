## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:ad59d31645abb90c71baf673169c283e2310818300fc9caabb9b754677f85009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `golang:1-windowsservercore` - windows version 10.0.20348.2527; amd64

```console
$ docker pull golang@sha256:21e4cfffc0dd2debbf84777e12b283128ab8f85012f67ffb6e903ed212cf2ea4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2215677544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cc4051880c1c49d496de58570537e73e8ecc02b78ef302894c31e041db0fff`
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

### `golang:1-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull golang@sha256:0d28936f1f3618fb15ca207e8bcd894e2798bdc25a1a360b9f6841ceb03325c1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2318590683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8024ccff21538acc48afa580b0f9300431ebac003ab469bc8c2e10597188ac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:13:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:13:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 12 Jun 2024 18:13:34 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 12 Jun 2024 18:13:34 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 12 Jun 2024 18:13:35 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 12 Jun 2024 18:14:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:14:24 GMT
ENV GOPATH=C:\go
# Wed, 12 Jun 2024 18:14:41 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Jun 2024 18:14:42 GMT
ENV GOLANG_VERSION=1.22.4
# Wed, 12 Jun 2024 18:16:03 GMT
RUN $url = 'https://dl.google.com/go/go1.22.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '26321c4d945a0035d8a5bc4a1965b0df401ff8ceac66ce2daadabf9030419a98'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:16:05 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3c3ab4cd77fae9059354ee5b73b856f9ac9c22731d9dcf4e365268e08cd843`  
		Last Modified: Wed, 12 Jun 2024 18:16:10 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86c37a0d0339c6b8b1c237b2c8250a774461350198b803d76982b65e45d102b`  
		Last Modified: Wed, 12 Jun 2024 18:16:09 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3b2fa9fd4cc3f0df2f037d6653ea1cdb5b7f419bd99e0576a57dcdf4b1ace7`  
		Last Modified: Wed, 12 Jun 2024 18:16:08 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856fdc06eea972eccedb4e2c6d528d9d6b992c971c4a29f289a88eac23a5d5a9`  
		Last Modified: Wed, 12 Jun 2024 18:16:08 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2096b09fa3f4c724fcb42fe19a8a5b0dc61277e2e802b4674b64a58de93238`  
		Last Modified: Wed, 12 Jun 2024 18:16:08 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69169629162eb6e94b664ddd335d3d02ae4c7a356ec11557b77d6780bfb3bb04`  
		Last Modified: Wed, 12 Jun 2024 18:16:11 GMT  
		Size: 25.6 MB (25576657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78abdc0679bbe9abc0864ab9497cfb6767ad50cc06c121d874dd8a022821b892`  
		Last Modified: Wed, 12 Jun 2024 18:16:07 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6bc3316ec48d85e70aa2d8c21fa5ad4eb37113d651977b29d3b5495e034859`  
		Last Modified: Wed, 12 Jun 2024 18:16:07 GMT  
		Size: 336.9 KB (336919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5222f75d358e9b8e60fd785f40a7b8245f0cf6d634f64488172b55910395e1a2`  
		Last Modified: Wed, 12 Jun 2024 18:16:07 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e23068dc7ebfc095432cdb1e6af9726e3b10d959fb3635a24504c0e99a1a297`  
		Last Modified: Wed, 12 Jun 2024 18:16:18 GMT  
		Size: 72.0 MB (71984977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe4726c882b12bd6e005278f53050cd3de58b99ce5170e1d152a081dd3e8d6b`  
		Last Modified: Wed, 12 Jun 2024 18:16:07 GMT  
		Size: 1.5 KB (1501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
