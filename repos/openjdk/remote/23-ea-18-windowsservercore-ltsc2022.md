## `openjdk:23-ea-18-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:274440d956262bd98ce6ea7d6cb0ad8e0d6cafac5bb890272d917746bfb05bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `openjdk:23-ea-18-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull openjdk@sha256:ed699f6c194cf914242c906abf8a605cbeca8c3edfc9880c9cb6f60df4001605
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2205921058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb836d326b1123622cf58600381e176641b5d1188ba33aacbbe6329de63bd28`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Mon, 15 Apr 2024 18:01:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 15 Apr 2024 18:02:19 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 15 Apr 2024 18:02:20 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 15 Apr 2024 18:02:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 15 Apr 2024 18:02:27 GMT
ENV JAVA_VERSION=23-ea+18
# Mon, 15 Apr 2024 18:02:27 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_windows-x64_bin.zip
# Mon, 15 Apr 2024 18:02:28 GMT
ENV JAVA_SHA256=b6d83c7e42b15f6a6d0bcbd83496ba05df366fceaa6bd6314550fd8b7eb9c19d
# Mon, 15 Apr 2024 18:02:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 15 Apr 2024 18:02:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5deba58106036304abd3657ddb9beebdf9c2ec2dc8941c08ceab69865956ca9b`  
		Last Modified: Mon, 15 Apr 2024 18:02:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa83e06c3826ffac84056aeaedb4230c8925ef0e298281609e1107fb54dfd18a`  
		Last Modified: Mon, 15 Apr 2024 18:02:55 GMT  
		Size: 502.9 KB (502894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32c7053139a8a4450f84a488bdc42fe24c4a155b83d932c583ea062fa9f85e3`  
		Last Modified: Mon, 15 Apr 2024 18:02:54 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0adaa43b7de34c3504216b987e7bafc40e1f14150d15a344c5d07685463afea`  
		Last Modified: Mon, 15 Apr 2024 18:02:54 GMT  
		Size: 353.3 KB (353280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62f4e5fa3cd111da0818a8d6be16f458e1fc5e162065521f1d9135a8fec266e`  
		Last Modified: Mon, 15 Apr 2024 18:02:53 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc2450d2e190a0c9c440071a7f51890a8963787114863522701ad3609287992`  
		Last Modified: Mon, 15 Apr 2024 18:02:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5087a5b39fafa5bbb42267d0f4f04cd66bd3d57f9ad2f9ecd0900737b123a6ca`  
		Last Modified: Mon, 15 Apr 2024 18:02:53 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366404b41357e69347111c57454ee95845df92995d879aaf887a968d87ab5c96`  
		Last Modified: Mon, 15 Apr 2024 18:03:05 GMT  
		Size: 205.7 MB (205683505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273ba895224593049b1baa8aa148113d5d8d2a7c793415e825a6904d14858977`  
		Last Modified: Mon, 15 Apr 2024 18:02:53 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
