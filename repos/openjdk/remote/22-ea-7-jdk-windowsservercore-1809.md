## `openjdk:22-ea-7-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:f6d4a929e00d7ca7a26030e3cbbdf4b3496a3399ca3bd4d2f3793b0b8929d09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `openjdk:22-ea-7-jdk-windowsservercore-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull openjdk@sha256:140a2e1b0d293930025eb1dac19d63a245adb850faccd8d595c3ede298ece541
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2139503508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b1041ccd5d2d636cbee98fdfc6bfbf8a5e7c4b6c32a4c7f706c4a1199163ca`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jul 2023 00:12:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 14 Jul 2023 00:12:12 GMT
ENV JAVA_HOME=C:\openjdk-22
# Fri, 14 Jul 2023 00:13:10 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 20 Jul 2023 20:35:46 GMT
ENV JAVA_VERSION=22-ea+7
# Thu, 20 Jul 2023 20:35:47 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_windows-x64_bin.zip
# Thu, 20 Jul 2023 20:35:48 GMT
ENV JAVA_SHA256=c6015fa6a4d2eb483b4a8455af6f3cb66003967ab94898fd6869ddf46337303a
# Thu, 20 Jul 2023 20:37:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 20 Jul 2023 20:37:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b927162ea448e018f1bd7dfb1a2bc55bf21cf56e2e9a32f46a821cc0e30dd9b`  
		Last Modified: Fri, 14 Jul 2023 00:22:20 GMT  
		Size: 232.6 KB (232553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d4e9000a3e1d4472b65f93e8d52e1ab6810d932dec9367b0bdfbcd62f895ab`  
		Last Modified: Fri, 14 Jul 2023 00:22:20 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f41cc8383e028a5579a8b1df7aef79a0d3783865d9d1eb5182a4ab3a8f448`  
		Last Modified: Fri, 14 Jul 2023 00:22:20 GMT  
		Size: 233.2 KB (233206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090f54cec7a6e69444346dfb7ebbe20178d91915054c3bf7ad0563022622b6f9`  
		Last Modified: Thu, 20 Jul 2023 20:43:14 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360b5393de18b5fbbe458c0bc87cf533c5d85d895f821deb751ac0e0396d6ce9`  
		Last Modified: Thu, 20 Jul 2023 20:43:13 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc63435d3452019919947ce1f4375c447fecd91cefa07a86932dfa774833dec7`  
		Last Modified: Thu, 20 Jul 2023 20:43:14 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32740939bfeeca08dcdec8d2aff38b27640d2dff7381421e9f6da24fb2cce791`  
		Last Modified: Thu, 20 Jul 2023 20:43:33 GMT  
		Size: 199.3 MB (199340595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34a648f4841be1f9548563f8dc130b793bf15a669a6e79ea98bd6da8231348e`  
		Last Modified: Thu, 20 Jul 2023 20:43:13 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
