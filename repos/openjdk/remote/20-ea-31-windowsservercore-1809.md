## `openjdk:20-ea-31-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:3cc79e7c4ef1588f768e45180f698bfd5256f50689ec9257de948b68f16b2527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `openjdk:20-ea-31-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull openjdk@sha256:b69632aa7e9bf3ae9a7cb9a85cce127593bd899e94719258859b3292e046dcb2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902041327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a70a9ebb8f3d5348447d364e52124789a3fd8a232aa79a79aa3b6d2100bfa54`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 05:09:35 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 12 Jan 2023 05:13:49 GMT
ENV JAVA_HOME=C:\openjdk-20
# Thu, 12 Jan 2023 05:14:14 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 13 Jan 2023 00:20:32 GMT
ENV JAVA_VERSION=20-ea+31
# Fri, 13 Jan 2023 00:20:33 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk20/31/GPL/openjdk-20-ea+31_windows-x64_bin.zip
# Fri, 13 Jan 2023 00:20:34 GMT
ENV JAVA_SHA256=53634b3b58712f001ec6bb781bd4b23e1032f57a48f69fe0beb74a09317ff40a
# Fri, 13 Jan 2023 00:21:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 13 Jan 2023 00:21:28 GMT
CMD ["jshell"]
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
	-	`sha256:b1fe1d317f0927d209417077d671ba0fb8e3b7ff9c583727da819f0d16252e80`  
		Last Modified: Thu, 12 Jan 2023 05:23:04 GMT  
		Size: 367.5 KB (367453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204fb4de92b3c2f3fbd44e35eab6a78c6001ee4da68e9f00b462472e9636c486`  
		Last Modified: Thu, 12 Jan 2023 05:25:04 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b5262ccef5459e1e9f746ac49749d63fee0bb98296c21086879d1d379e8e7a`  
		Last Modified: Thu, 12 Jan 2023 05:25:04 GMT  
		Size: 320.0 KB (319987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d44bd4e42d0e3e73dd4fa470d182e246e47130fcc398af930c1bc50eb3f1cc`  
		Last Modified: Fri, 13 Jan 2023 03:21:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09832db62ed15918a27ad864f31751de909bae36733bea7904651c60a3c7c146`  
		Last Modified: Fri, 13 Jan 2023 03:21:36 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f8d25927741c92dab714c7f24b6f4ee227d6f8dfe96ddca8885cdedae6fbf6`  
		Last Modified: Fri, 13 Jan 2023 03:21:36 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e1d0302b114aaea92dcb9004d8d4ea6b1fd70f3424d07454b0caa9841fcffb`  
		Last Modified: Fri, 13 Jan 2023 03:22:00 GMT  
		Size: 193.4 MB (193401970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a21e3f52eacdc4ffe2a601763a5f3d377039dde03ae6849f6c83cd3358b657`  
		Last Modified: Fri, 13 Jan 2023 03:21:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
