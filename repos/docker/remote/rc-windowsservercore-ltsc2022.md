## `docker:rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:13db070a3e13dd0afb42a28e6832e18f42755eba6b6cb042932ae4e0ee849bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1487; amd64

### `docker:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.1487; amd64

```console
$ docker pull docker@sha256:1d19d5913fbb06a8e78185ff6cbf506aaf3bda953a0bcb51feccd6042d9e4424
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1404170802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c581b548a6d0b3b004d805e9689b10dc19cdc0152befcdab76ae0a41b0dcc2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 05:38:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Jan 2023 05:38:31 GMT
ENV DOCKER_VERSION=23.0.0-rc.1
# Thu, 12 Jan 2023 05:38:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-23.0.0-rc.1.zip
# Thu, 12 Jan 2023 05:39:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf9fbb5bb66b4765df4292381a96e1cfc78d67a08a48a930d66d57438abacd1`  
		Last Modified: Thu, 12 Jan 2023 05:42:25 GMT  
		Size: 612.2 KB (612183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8e73c22877d94ef0f7784a8e5dcbd45cf84bba67855dd937d4ea97ceb2e16`  
		Last Modified: Thu, 12 Jan 2023 05:42:24 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ad7abed5a28fc923cbfa15f17f3baf74a2660761e6e32c43bf1dd688cd042b`  
		Last Modified: Thu, 12 Jan 2023 05:42:24 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a96414f6f659d9f046f6997e65c457e6a1494762a83d2cf27ad2a0555e9b10`  
		Last Modified: Thu, 12 Jan 2023 05:42:28 GMT  
		Size: 17.5 MB (17525264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
