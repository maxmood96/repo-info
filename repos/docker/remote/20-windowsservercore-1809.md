## `docker:20-windowsservercore-1809`

```console
$ docker pull docker@sha256:5df391fd44504e769f773b15ac9232f9e4359b23645a593558d66686ea4aa605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `docker:20-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull docker@sha256:0e6c4a6e78f65ea2d69eb6169800915057fd0f6337dba2e5b0b53bcaf36d4c9f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1762765361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0b2d2ded6d90090820c7f0a2c578974129359fadc8d5ce217d85cfad2f79a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 05:39:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Jan 2023 05:41:09 GMT
ENV DOCKER_VERSION=20.10.22
# Thu, 12 Jan 2023 05:41:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.22.zip
# Thu, 12 Jan 2023 05:41:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1203a660d1e7b9cba56b0f2b04e0f4d443536c90572741405636436ed42c43`  
		Last Modified: Thu, 12 Jan 2023 05:42:38 GMT  
		Size: 365.4 KB (365388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6628515edfbf2c36502cf76d7958a689760cd710b26cf80e6f267b4b285499ae`  
		Last Modified: Thu, 12 Jan 2023 05:43:14 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bd2c7e881cd8d3889dbbe9417b2bc24a277370353ddb8b79fc0f3bcd74b28e`  
		Last Modified: Thu, 12 Jan 2023 05:43:14 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5705faa9ffb30ddc91006ccf5fb659d6aa87eb4ab2fecd2baf31dc4fb6ebeebb`  
		Last Modified: Thu, 12 Jan 2023 05:43:24 GMT  
		Size: 54.5 MB (54451758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
