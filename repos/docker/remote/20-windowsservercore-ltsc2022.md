## `docker:20-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d55a941b389ec4009308d0733fc7bb856bfe460af5d5d8bb182c34bd33b7be7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1547; amd64

### `docker:20-windowsservercore-ltsc2022` - windows version 10.0.20348.1547; amd64

```console
$ docker pull docker@sha256:4655a0b8d4f3330fa0c50eb2b64e94dc84c0e9d2c43be3e23628a5baf9e0c146
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1736088778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574248f638bfdc64b21b8fb1134c4bd6a4582327162776ffed1c9510cb99b9b9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Tue, 07 Feb 2023 11:42:22 GMT
RUN Install update 10.0.20348.1547
# Wed, 15 Feb 2023 22:37:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:33:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:37:56 GMT
ENV DOCKER_VERSION=20.10.23
# Thu, 16 Feb 2023 02:37:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.23.zip
# Thu, 16 Feb 2023 02:38:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d015a9e7adea898d81486dce8b513b0e9cbeca30904cac18c3ea98ab3be7a6`  
		Last Modified: Thu, 16 Feb 2023 00:28:01 GMT  
		Size: 293.3 MB (293317272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c63a3d1906c0f8f7ca38587ab5f1c84160f9127cce25fb7f57d8a60dc7008`  
		Last Modified: Thu, 16 Feb 2023 00:26:46 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e31c0ce3f337b044901163fed3eab931c5230b0243d3265fb3aa74a4d5a2aa6`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 769.3 KB (769272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37000251b28c80b932b3966a757f238990dd0606d478d8de8cccb1d802ec715`  
		Last Modified: Thu, 16 Feb 2023 02:41:21 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f9bb19df9823688a18314d31ef7b8dace8b26e828c29f902f388073292c7ee`  
		Last Modified: Thu, 16 Feb 2023 02:41:21 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc6e72881b95eb9b53a07b0a42327076108754c7e0c89547c51a0c821550082`  
		Last Modified: Thu, 16 Feb 2023 02:41:31 GMT  
		Size: 56.0 MB (55968992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
