## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:7a6d0f59575f9420cb86c8912b27c1642dd8bae4dda02ea17f8a2d1100d367b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `golang:1-windowsservercore` - windows version 10.0.20348.2529; amd64

```console
$ docker pull golang@sha256:fec67971d647dfdbe848a139a253b5a080095a5de13d19989d96d5eaaae20247
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2215731497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb9445f89c766947406e7aa06a86f57216446736c356ae3d5548be1f859b251`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Sat, 22 Jun 2024 00:07:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Jun 2024 00:07:27 GMT
ENV GIT_VERSION=2.23.0
# Sat, 22 Jun 2024 00:07:27 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Sat, 22 Jun 2024 00:07:28 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Sat, 22 Jun 2024 00:07:29 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Sat, 22 Jun 2024 00:07:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Sat, 22 Jun 2024 00:07:49 GMT
ENV GOPATH=C:\go
# Sat, 22 Jun 2024 00:07:54 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Jun 2024 00:07:54 GMT
ENV GOLANG_VERSION=1.22.4
# Sat, 22 Jun 2024 00:09:01 GMT
RUN $url = 'https://dl.google.com/go/go1.22.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '26321c4d945a0035d8a5bc4a1965b0df401ff8ceac66ce2daadabf9030419a98'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Sat, 22 Jun 2024 00:09:03 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1193597dd82a585a83215f5c51c9a5ce5111ef28bb2ebb034640341fb3b1df7d`  
		Last Modified: Sat, 22 Jun 2024 00:09:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930670dd58d2525fa4ff6f050d4b36990a18064a5181e736222f3de0a6c68726`  
		Last Modified: Sat, 22 Jun 2024 00:09:08 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b317f65f77b7e87744325c72149577f7ffbbd3fc93fb488eeb2e6e153359c6`  
		Last Modified: Sat, 22 Jun 2024 00:09:07 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7343c0e1cc03ce6fff8c8769868ad4999892b13d71967798ecf4c56ad605a6eb`  
		Last Modified: Sat, 22 Jun 2024 00:09:07 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0969f1a800c8479e3b7010bc8058722d152d00bc92bbc293571251467ea55b4`  
		Last Modified: Sat, 22 Jun 2024 00:09:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d39061e67f723393a477f796f1f757796411f84afaea81b951d664350498e1`  
		Last Modified: Sat, 22 Jun 2024 00:09:09 GMT  
		Size: 25.4 MB (25434826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b645a6a246276287c50e8c6a51ed4b9fee5d349e71c56d918a9f0b60fb1ef93d`  
		Last Modified: Sat, 22 Jun 2024 00:09:06 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae001ea167211fb75cdd9eb4449a3828c657040f2f9c70ff6524f5f11e53bad3`  
		Last Modified: Sat, 22 Jun 2024 00:09:06 GMT  
		Size: 343.0 KB (342984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5dfe6b72eb05d69da8489bb1b8599c48ecf2cec065bedbeb36b1808d8adc30f`  
		Last Modified: Sat, 22 Jun 2024 00:09:05 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2284ff4e3b5cff500607d1c9dca84dde984be977e92631d3cf54f0af6fc3650a`  
		Last Modified: Sat, 22 Jun 2024 00:09:17 GMT  
		Size: 71.8 MB (71752978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ea38a34aa77cc70691f3cec795a6af72eb123ea8174650de0e6eac22a2ac8c`  
		Last Modified: Sat, 22 Jun 2024 00:09:06 GMT  
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
