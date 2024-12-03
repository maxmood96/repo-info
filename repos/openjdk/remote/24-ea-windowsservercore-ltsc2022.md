## `openjdk:24-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:1e249fd83e6fc070d43200ef859714524fce0a89bcddaf790a4d33787882a46f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `openjdk:24-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull openjdk@sha256:75e3ddb1cd42d7f88f58d8f521cdf0cc73ab714daf17cc088553e13f74765661
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2461843272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6e6402aa0c26b9bcdcfe01436c482611b85d9ef8a9b8a3a817c78b78b2903c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Tue, 03 Dec 2024 16:31:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Dec 2024 16:32:56 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 03 Dec 2024 16:32:56 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 03 Dec 2024 16:33:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 03 Dec 2024 16:33:03 GMT
ENV JAVA_VERSION=24-ea+26
# Tue, 03 Dec 2024 16:33:04 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/26/GPL/openjdk-24-ea+26_windows-x64_bin.zip
# Tue, 03 Dec 2024 16:33:05 GMT
ENV JAVA_SHA256=b22083fee813d8800a38db2020160bff319d2f6134df449d8c82d9889d120096
# Tue, 03 Dec 2024 16:33:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 03 Dec 2024 16:33:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cfa770ef0d4476e725931edbc9c3f82d9909cbe8bfc436806b7f798d136345`  
		Last Modified: Tue, 03 Dec 2024 16:33:46 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3effe856ae6caf008eded34f2aee4ec2a5849fa88a71ab76563af2e298926c9`  
		Last Modified: Tue, 03 Dec 2024 16:33:46 GMT  
		Size: 364.5 KB (364462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71db9daf48d1777eda2348465b40a03b23f3ca6b4c5425f0789a62a4fca0366`  
		Last Modified: Tue, 03 Dec 2024 16:33:46 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c9f2a3bf7eff81d86e071f400cbd7159de25c1876a9479964b13567efd1dcb`  
		Last Modified: Tue, 03 Dec 2024 16:33:46 GMT  
		Size: 312.4 KB (312410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b1f1970e4ad11dd314392e9e2700c368a6fb3516dcd38b1a94e159961631ef`  
		Last Modified: Tue, 03 Dec 2024 16:33:45 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b28be19b75fe0ac9ab56bac36a8356ab2ca7e34afd9578af87d32530295db0a`  
		Last Modified: Tue, 03 Dec 2024 16:33:45 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44e6ca0efc99d614e1bc83b569d684d09194b47368c66030971d35c819f30d3`  
		Last Modified: Tue, 03 Dec 2024 16:33:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26db2b77f46f3e109c266c782d256281eaafe0df0064f43588a1c9d07a0533ad`  
		Last Modified: Tue, 03 Dec 2024 16:33:56 GMT  
		Size: 208.7 MB (208674317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0b7e23ec8cefe27178f81311e864c07daebd42f6259f0e8ab4ebc8b0ad2a7e`  
		Last Modified: Tue, 03 Dec 2024 16:33:45 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
