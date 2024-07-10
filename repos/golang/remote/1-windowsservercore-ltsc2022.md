## `golang:1-windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:c4bbaa9db7222cded4185e8df3e9903be7ec4adeeaa986b00b8fca7c19986a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `golang:1-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull golang@sha256:17f9a4659a24ee1b02d5b57ea92530d23ae73848bda43f4da1f71b6b385ddba4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2237134397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00404c53a9480ad66fe1c569ad4cac06ea3af460a9b65c102966fbb9c4a9de0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Wed, 10 Jul 2024 17:05:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 17:05:04 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jul 2024 17:05:05 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jul 2024 17:05:06 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jul 2024 17:05:06 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jul 2024 17:05:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jul 2024 17:05:24 GMT
ENV GOPATH=C:\go
# Wed, 10 Jul 2024 17:05:29 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Jul 2024 17:05:30 GMT
ENV GOLANG_VERSION=1.22.5
# Wed, 10 Jul 2024 17:06:36 GMT
RUN $url = 'https://dl.google.com/go/go1.22.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '59968438b8d90f108fd240d4d2f95b037e59716995f7409e0a322dcb996e9f42'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Jul 2024 17:06:37 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e43dc44207e2b78655d7b69b2b6cd78be3b64b13dba87f4f3bb8b9d77d77dd`  
		Last Modified: Wed, 10 Jul 2024 17:06:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad094dcaca76e7aeeaed3c5c3f8eacf523da178904727c6e2080eda015e7164`  
		Last Modified: Wed, 10 Jul 2024 17:06:42 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ac53ba771607e275eaa51df9206ef49114e3f6547f6fc922e6a8d438284e06`  
		Last Modified: Wed, 10 Jul 2024 17:06:41 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49ae2bc8785bf5307586f33e8a86ff3c71b900f855fa4868180322e8c907a31`  
		Last Modified: Wed, 10 Jul 2024 17:06:41 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2aab9ce058e67d2ea041ea90e93af702b769841e6e182d4d6c7631bf0360ef7`  
		Last Modified: Wed, 10 Jul 2024 17:06:41 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34141fd7184bae4bd8d564c7eb4a6be060fe455be8def8cd98ca3404c66d3568`  
		Last Modified: Wed, 10 Jul 2024 17:06:44 GMT  
		Size: 25.4 MB (25430123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f62444332de5b3b533b30567fd0b25eefa164817515057ff4e753acf24dc352`  
		Last Modified: Wed, 10 Jul 2024 17:06:40 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6eded1eb40bed1277fc8976929718f1d2c8364dceaa45a4894e56168c222a8`  
		Last Modified: Wed, 10 Jul 2024 17:06:40 GMT  
		Size: 337.2 KB (337184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2eef0829349cda0166c6aea196095d81ca775e5fb60c789a075f53052a88883`  
		Last Modified: Wed, 10 Jul 2024 17:06:40 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6aeb9d82d034c8246215b00345d8579c0898c016b39e25ea0885c4798dd0f2`  
		Last Modified: Wed, 10 Jul 2024 17:06:52 GMT  
		Size: 71.8 MB (71756227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb836efbcf68d3b6ba2625e825fc2937294e68d63990746ffe3f0b38ce5019f`  
		Last Modified: Wed, 10 Jul 2024 17:06:40 GMT  
		Size: 1.5 KB (1465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
