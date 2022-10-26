## `docker:20-windowsservercore-1809`

```console
$ docker pull docker@sha256:5041c150fadfa40aece5e92ef41fe75d2c3d15d4f213e0c7a4b6a1923677810d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `docker:20-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull docker@sha256:3d3ab4170ba38a76715ed28925e77f321f2a506791c7e2739849b3260ebaff5d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2828306091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9daee393818a4ed565041177c6d52cae8112a24973e2616547e5052cace8be33`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 18:09:38 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 26 Oct 2022 01:15:44 GMT
ENV DOCKER_VERSION=20.10.21
# Wed, 26 Oct 2022 01:15:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.21.zip
# Wed, 26 Oct 2022 01:17:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6193ab94a0498ba6454e2a35e189837b37a2eb01403e8b62654bdc28a4569c`  
		Last Modified: Mon, 17 Oct 2022 21:52:22 GMT  
		Size: 849.2 MB (849228999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45c9281c722e160d2675d4141a7174b59945582b16af0e76b2ff4b081b98ab9`  
		Last Modified: Wed, 12 Oct 2022 18:13:49 GMT  
		Size: 344.9 KB (344931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a82659b38ceac05a69ff4d6b19175fb0ea58e18b82b13cef52298929f57b18`  
		Last Modified: Wed, 26 Oct 2022 02:16:58 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665f9ef25842b0652fc7b6232a15d125f6065c5b6e28d1edfb7fe4f88d6d3dee`  
		Last Modified: Wed, 26 Oct 2022 02:16:58 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fac4366041e62459f14371657496108afdccb5f8e39934fcbe7de6638732e1e`  
		Last Modified: Wed, 26 Oct 2022 02:17:07 GMT  
		Size: 54.5 MB (54458578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
