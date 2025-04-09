## `openjdk:25-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:449aa07da3f833f958c360b7822d88a8caf0be9bf381b565d54a2f7922fd555c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `openjdk:25-jdk-windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull openjdk@sha256:1603154078d941b3d609206e93a1070325ab47779b600158441379aa50c91626
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2371692760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e139704ac86833b01ea875fb6f5ee0bbf2606ad4c76e4b53b0a8ee9737638afc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 01:04:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 01:05:27 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Apr 2025 01:05:28 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 09 Apr 2025 01:05:35 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 09 Apr 2025 01:05:35 GMT
ENV JAVA_VERSION=25-ea+17
# Wed, 09 Apr 2025 01:05:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_windows-x64_bin.zip
# Wed, 09 Apr 2025 01:05:37 GMT
ENV JAVA_SHA256=46c47281310039b4e8d7e583a1629bfb2ca08a102794c3a68d1f2051101e9f5b
# Wed, 09 Apr 2025 01:06:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 01:06:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccce759214b5cc94f0d493c8374bf94f12c711734dcb2a995d2ce56a3a25013`  
		Last Modified: Wed, 09 Apr 2025 01:06:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf514a523f524809bd0f3561b943c2f7985c8428183f52553b3c350e0dedd5b`  
		Last Modified: Wed, 09 Apr 2025 01:06:08 GMT  
		Size: 332.5 KB (332491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a592ff6df9a1f92e87c62a416aae9d4056c32ef2ee095c5b02125bae253ca5ac`  
		Last Modified: Wed, 09 Apr 2025 01:06:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13178848ee7919569d6c166258771fa684e34d1fd273e9d76b9843899684d84f`  
		Last Modified: Wed, 09 Apr 2025 01:06:07 GMT  
		Size: 317.2 KB (317243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e0f1b2759f00c692cb8776008820d81534b0809d30b6d92f1b01fa3fe5aab8`  
		Last Modified: Wed, 09 Apr 2025 01:06:06 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ab2508b18a927fb4be63aac475ed56592db925cf53d7d8529b4eb09fbb600b`  
		Last Modified: Wed, 09 Apr 2025 01:06:06 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d0edc950a2a4a05c20612f9736fe87879c5e0b463d13bc2ed33d0b7a7d50db`  
		Last Modified: Wed, 09 Apr 2025 01:06:06 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5968e43975c84c37d9ebaa2f904b7c72730ab6948ad716b9cb0a12f5ca2af87`  
		Last Modified: Wed, 09 Apr 2025 01:06:18 GMT  
		Size: 208.3 MB (208309348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d77ffabdb44cf89a19ff1609ac661283ff8f02db2bf6ce2cfdbc3fa3f3eac2`  
		Last Modified: Wed, 09 Apr 2025 01:06:06 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
