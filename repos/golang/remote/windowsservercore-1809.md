## `golang:windowsservercore-1809`

```console
$ docker pull golang@sha256:cef9dcca029d93da09f7711ccf3f44f3e5c18a11b3a55bcea4dc5f1f927ddbf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `golang:windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull golang@sha256:ce9790614174d2819ead678c833f5ebc6651a036e01e7aa3b5a2bdceb42958c2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2285450623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac770dff77ad7fb401aadd02e01bf0dbe3813cd6f05c403cbe7c903a4f5eb06`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 01 Apr 2025 17:17:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 01 Apr 2025 17:17:34 GMT
ENV GIT_VERSION=2.48.1
# Tue, 01 Apr 2025 17:17:35 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 01 Apr 2025 17:17:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 01 Apr 2025 17:17:37 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 01 Apr 2025 17:18:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 01 Apr 2025 17:18:37 GMT
ENV GOPATH=C:\go
# Tue, 01 Apr 2025 17:18:44 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 01 Apr 2025 17:18:45 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 17:20:07 GMT
RUN $url = 'https://dl.google.com/go/go1.24.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '29c553aabee0743e2ffa3e9fa0cda00ef3b3cc4ff0bc92007f31f80fd69892e1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 01 Apr 2025 17:20:09 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fe8d5f49196d0d535edd6ccb18b838d381c4151b7ea1dc975123768b652bd1`  
		Last Modified: Tue, 01 Apr 2025 17:20:14 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7850a574b2321bf3af14a95855900377e19806b10c7d852815316f5c421adb24`  
		Last Modified: Tue, 01 Apr 2025 17:20:14 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bfde580cfc97be48a68080ebff95bf834baeed45d2b49369708bfc3ed4ddec`  
		Last Modified: Tue, 01 Apr 2025 17:20:13 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2551503edcb6277f96e5e37b92ad5c1ebac83ec3cd8df2651ecbf4ffb06a94`  
		Last Modified: Tue, 01 Apr 2025 17:20:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76686eb0901ae0a7e245a0a51abbeb3b73968ed2c79a72feb953d1c2aa8227d6`  
		Last Modified: Tue, 01 Apr 2025 17:20:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957aae3ab51a54cca2021e7836789b77b62657486158c6ecb7825ee47a951ea0`  
		Last Modified: Tue, 01 Apr 2025 17:20:19 GMT  
		Size: 51.2 MB (51206672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b019301e0d898d503686f16a33046b75d07e4ab5c9ab77abd68c0ef46b73f9f`  
		Last Modified: Tue, 01 Apr 2025 17:20:12 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478498f8a6f329680c8ba2a2e4fff81e2cde651f3b5bbaed023aa48709bc648a`  
		Last Modified: Tue, 01 Apr 2025 17:20:12 GMT  
		Size: 344.1 KB (344080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22432659eea0c836e0d9af7b46c19c6192000e0fb12cacd37dd6de6dbc59e21`  
		Last Modified: Tue, 01 Apr 2025 17:20:12 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5503577ea495bf4ff1058e9de386218c8e676fa11149acddf3f25955c46300d`  
		Last Modified: Tue, 01 Apr 2025 17:20:26 GMT  
		Size: 82.3 MB (82254692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fadbf5b733e8968799c679fbe3dc2b270a9e94d0cda7639602f30a333de76f7b`  
		Last Modified: Tue, 01 Apr 2025 17:20:12 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
