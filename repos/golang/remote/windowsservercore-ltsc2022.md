## `golang:windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:45564f9dcf09e361611bb4e09337cfd50686be4684d36679503d2c9c968beb78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `golang:windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull golang@sha256:7da3184bfc53795e7190cf1ede9b03a52758d238cae4f7d0548eba68167b7c34
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2244849105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dfab1d9c4c0e2121fa200c29e7cfa1455a445021edcd82e0095cae613bc7b2c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Thu, 05 Sep 2024 22:03:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Sep 2024 22:03:02 GMT
ENV GIT_VERSION=2.23.0
# Thu, 05 Sep 2024 22:03:02 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 05 Sep 2024 22:03:03 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 05 Sep 2024 22:03:04 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 05 Sep 2024 22:04:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 05 Sep 2024 22:04:15 GMT
ENV GOPATH=C:\go
# Thu, 05 Sep 2024 22:04:22 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Sep 2024 22:04:23 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 22:07:09 GMT
RUN $url = 'https://dl.google.com/go/go1.23.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '32dedf277c86610e380e1765593edb66876f00223df71690bd6be68ee17675c0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 05 Sep 2024 22:07:11 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4b9ac7f54856109dff16a7de3711899c9dea10444da64dce2dc711d63d5481`  
		Last Modified: Thu, 05 Sep 2024 22:07:16 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa703eb97cca559a72cd655d6bb5429354a1a0597723a81a7207d4c01e1676de`  
		Last Modified: Thu, 05 Sep 2024 22:07:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3162ff7c31ab01250facf8bde72747c2031f5b600c2c2ba3916a9a8cfc255e1`  
		Last Modified: Thu, 05 Sep 2024 22:07:15 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3b8f1803e0a86ebf7ad2c747dab8b5c46574697abfecee0f1c8bf580c807fc`  
		Last Modified: Thu, 05 Sep 2024 22:07:15 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4cecac8a156f55c25bd3e8d863857d71e744e28cac8311a0348d6ebc18a6cdc`  
		Last Modified: Thu, 05 Sep 2024 22:07:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa825b98b3f41765cfc4b04c689e6a230963488216b4b4162629dee6be5c2e1`  
		Last Modified: Thu, 05 Sep 2024 22:07:18 GMT  
		Size: 25.4 MB (25449974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a0f821d22ab894e4f9ed4c80df13adc3c5f4306228b7b4f5ab2c43a3e2fb0b`  
		Last Modified: Thu, 05 Sep 2024 22:07:14 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dd1bbe9d4095241910d3e1bbe41dc96172f77676b9efe921974d789575b3db`  
		Last Modified: Thu, 05 Sep 2024 22:07:14 GMT  
		Size: 313.5 KB (313539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca96ab3bf553787b8b55e9d6619558c343d4072214e5025a705fce745353bdf`  
		Last Modified: Thu, 05 Sep 2024 22:07:14 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45018d30b477d340942ef4990c4cc2eac096521b7631ec6150e1048099859d34`  
		Last Modified: Thu, 05 Sep 2024 22:07:25 GMT  
		Size: 77.3 MB (77310164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a37e434eb28827e1b1320df4ca3bb7067c0f103dbc31e4b73053831017eb2c`  
		Last Modified: Thu, 05 Sep 2024 22:07:14 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
