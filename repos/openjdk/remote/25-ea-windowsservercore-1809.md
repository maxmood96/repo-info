## `openjdk:25-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:613ae4c544552ab798296148c97b1908451a22f86b7f501eeb5f4f99ba4ec2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:25-ea-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:9f20696c0a390bd3ec8bb36b13fca3e8759ff76065faf65b5e24126264e874ad
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330732650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9176ef8a0a9227d5730ebfa156bb9b53a87274a64a530e27a82ab2568391781`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 31 Jan 2025 22:25:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 22:27:20 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:27:21 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 31 Jan 2025 22:27:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:27:31 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 22:27:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_windows-x64_bin.zip
# Fri, 31 Jan 2025 22:27:32 GMT
ENV JAVA_SHA256=3ea9473d90c2a51f51d40081e60eb97a8fd26b8f787d9b44a51f102714942cf6
# Fri, 31 Jan 2025 22:28:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:28:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d814447db0c64d6643ac83787d41f5feb0f0d0839821c103fb8dcfd368b171`  
		Last Modified: Fri, 31 Jan 2025 22:28:15 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e1bfb1a53782ac86fca66a4f7c49aed747fe51f57d7aeffb3dd8c527c30b5`  
		Last Modified: Fri, 31 Jan 2025 22:28:15 GMT  
		Size: 341.9 KB (341942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0740fe5e74442f58a075e266f6124dd5798d6c31758a1d0531f81d0ad5b544`  
		Last Modified: Fri, 31 Jan 2025 22:28:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601442e1c4921de89048e5db73834991674e5a67a27a1ccd539310eddd338608`  
		Last Modified: Fri, 31 Jan 2025 22:28:15 GMT  
		Size: 332.2 KB (332153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056d5a4d6b273cdcd02665c0fd0561ad0108956a0e61204a68b60db5ec4e6e71`  
		Last Modified: Fri, 31 Jan 2025 22:28:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0525e73b9fb2105a33d11ed0adcde5239b338971507e91f3fa3cdb5a76bbbf9`  
		Last Modified: Fri, 31 Jan 2025 22:28:14 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af222e521a45820e52cd8929f0272c1b727590f5773d5af76532332fac593e1`  
		Last Modified: Fri, 31 Jan 2025 22:28:14 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34135800246333aab2c9f24d644be2bab0e23871ab7a208d272b2c564d69ccdc`  
		Last Modified: Fri, 31 Jan 2025 22:28:24 GMT  
		Size: 207.8 MB (207838507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698bc11035faf34b25ef0ee7decfad106e48695b2b6211cf7b4b03cb245ea7d3`  
		Last Modified: Fri, 31 Jan 2025 22:28:14 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
