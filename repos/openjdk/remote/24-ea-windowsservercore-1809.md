## `openjdk:24-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:16164add9450f75f53a609db6ecc572c32588f00c7d0d67a143164567cc9ec41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `openjdk:24-ea-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:63055ae54bd73592c96e8d351dd15c94adc971ecd979a9a4d39e80829c4d7c79
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2446019041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526ad0aa9e2dd4d541f6022dae9906396d45ebde11a2000d7e4ee961336fe454`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Mon, 22 Jul 2024 20:59:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 22 Jul 2024 21:01:40 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 22 Jul 2024 21:01:40 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 22 Jul 2024 21:02:11 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 22 Jul 2024 21:02:12 GMT
ENV JAVA_VERSION=24-ea+7
# Mon, 22 Jul 2024 21:02:12 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/7/GPL/openjdk-24-ea+7_windows-x64_bin.zip
# Mon, 22 Jul 2024 21:02:13 GMT
ENV JAVA_SHA256=e6ea3b3cd29d732dbe15fd95b7719200d69fff9e9f42a09fc5dc4fc3bd5fea12
# Mon, 22 Jul 2024 21:03:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 22 Jul 2024 21:03:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a324fbdfaaec19a11b8db2f41af298db0f43eca4654bbbf10e4b7b37071336ee`  
		Last Modified: Mon, 22 Jul 2024 21:03:21 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9287ce7bf1b39b687283e9bfd0266eceb4e07631d1371ae71e45241047f5e8`  
		Last Modified: Mon, 22 Jul 2024 21:03:21 GMT  
		Size: 506.9 KB (506930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a6d24720e8fa902eea7434f0372d1aebaff0ec5f6961f9f468445fac6ae8b4`  
		Last Modified: Mon, 22 Jul 2024 21:03:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1596e210d84e1a6d680409424af13fa06f77777ffc1824371da481e1c0380319`  
		Last Modified: Mon, 22 Jul 2024 21:03:21 GMT  
		Size: 350.5 KB (350468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72a0c2b5a97c9ecc1a29bc28f4fd1fa3da64748149bf5209bf99da390c52191`  
		Last Modified: Mon, 22 Jul 2024 21:03:19 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466eca85bfc0d7c04f6b609fc0902cb12801cf02d31d01339361121ace9bc89f`  
		Last Modified: Mon, 22 Jul 2024 21:03:19 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d1eab0223919a362c0382273e07c5fd67f80d39fc85cd9fd508f3c74d718c4`  
		Last Modified: Mon, 22 Jul 2024 21:03:19 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243afa0977d08622fa7e1849a775112589966699e81eecc2ce31dca631729608`  
		Last Modified: Mon, 22 Jul 2024 21:03:30 GMT  
		Size: 206.7 MB (206724441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b889e74c1f5b2e925eb670de44dafc9229d8d964e249f62e5af405c469a3f47`  
		Last Modified: Mon, 22 Jul 2024 21:03:19 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
