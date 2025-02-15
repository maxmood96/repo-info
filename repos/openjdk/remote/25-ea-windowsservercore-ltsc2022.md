## `openjdk:25-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:40ec769308772193bd58ef56d694bac556ee5865126b07a55338170fc111f88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `openjdk:25-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull openjdk@sha256:4ca9c577bf52ef8ca0ad75ea860b1d36ea3754861f8ffc69426f6f1fded7a57a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2472498047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c8680638fe9803415a87e3499ea972c048a551111d1e96c0bb7ff41939e899`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Fri, 14 Feb 2025 23:39:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Feb 2025 23:40:07 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 14 Feb 2025 23:40:08 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 14 Feb 2025 23:40:13 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 14 Feb 2025 23:40:14 GMT
ENV JAVA_VERSION=25-ea+10
# Fri, 14 Feb 2025 23:40:14 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_windows-x64_bin.zip
# Fri, 14 Feb 2025 23:40:15 GMT
ENV JAVA_SHA256=9e8ebedd95dce7d5755f885b28067679019d529df9ff91b64e03edd7f2285e6e
# Fri, 14 Feb 2025 23:40:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 14 Feb 2025 23:40:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Wed, 12 Feb 2025 22:14:21 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93a3bf8cd2242f249b9d733c58358a5b351c5b85efa57992b9bbcb95d7e7e22`  
		Last Modified: Sat, 15 Feb 2025 00:31:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d677d07e6535bdd462b3111fb93e10d127c25d8eb264e844d1d0504b1840d30b`  
		Last Modified: Sat, 15 Feb 2025 00:31:22 GMT  
		Size: 367.5 KB (367537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfc6b0371ba54d8a4975968029d4f9de40ecdf7e329f7f28b4af9c754b48d69`  
		Last Modified: Sat, 15 Feb 2025 00:31:22 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1188cc72becce0dd453532efa5c9dfcc814a45cf438caf467ab7d20e3d9c29fb`  
		Last Modified: Sat, 15 Feb 2025 00:31:23 GMT  
		Size: 346.3 KB (346259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b473e2d8c219e1dae4a4b8cfe77b02440b209ea878076b1ef27387c6aed0ec`  
		Last Modified: Sat, 15 Feb 2025 00:31:23 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96af92c564769b2ff3ce42265a67092268b30f47078b8a294763cffd90f562d1`  
		Last Modified: Sat, 15 Feb 2025 00:31:24 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9f06e49b9bff0f037f585d9d12b7f7110975dd65ce9104a12770c151db7f53`  
		Last Modified: Sat, 15 Feb 2025 00:31:23 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8881d96f1a722b9a5a82f271c13a3c08003feb3a669c8532a44fb456bc8333`  
		Last Modified: Sat, 15 Feb 2025 00:31:37 GMT  
		Size: 207.9 MB (207918460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a72d415781220633aa7fe1d390139005b37b6d426bd0b9075283fe53fa6518`  
		Last Modified: Sat, 15 Feb 2025 00:31:24 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
