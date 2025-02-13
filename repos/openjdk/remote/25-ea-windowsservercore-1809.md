## `openjdk:25-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:04cc49ec58eb1a487003c2e616b5d14a93bcd18e2eb6ed87554e8411cdfd3f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `openjdk:25-ea-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull openjdk@sha256:f24bc0ac37e462b19da0c5fc5898c71deca3bea151959356f302fff5d98adb79
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345431666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8a4b7f7580a33fb524b1f8798efc6def51ee9f70c9d635fc58d09490d5163c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:34:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:35:28 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:28 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 13 Feb 2025 00:35:34 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:35 GMT
ENV JAVA_VERSION=25-ea+9
# Thu, 13 Feb 2025 00:35:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_windows-x64_bin.zip
# Thu, 13 Feb 2025 00:35:36 GMT
ENV JAVA_SHA256=422ffa84afebca61d5ff96e0459231633ad47f082eb11fbecdb64c76e37b35ea
# Thu, 13 Feb 2025 00:35:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84ca2ea91338bc2819e1ca63e7d7142785e65ca9089e35431ddf37d24908161`  
		Last Modified: Thu, 13 Feb 2025 01:09:09 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a5ddf988a6972bb2f55c3f1423e655a1ee2e1310990f0b8c6d47165810b212`  
		Last Modified: Thu, 13 Feb 2025 01:09:10 GMT  
		Size: 345.1 KB (345140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67aabea0fd5f3bdf16afa2c284821445ed6a7324bea4f391e0e5a15777b2bc6`  
		Last Modified: Thu, 13 Feb 2025 01:09:10 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b1f5cd49c74cffbb9853e2586426c5b3896771871a69134bcb5878683d9528`  
		Last Modified: Thu, 13 Feb 2025 01:09:10 GMT  
		Size: 327.1 KB (327125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54740f2d2d4fe1001b8ea5ab835d3612db5fac81481e6925eeea07ec1013b99`  
		Last Modified: Thu, 13 Feb 2025 01:09:10 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824006b5200dfbc85db8561f8af3dca37c7931d585c0b1114bff7463ad1caeec`  
		Last Modified: Thu, 13 Feb 2025 01:09:10 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d128ffdaac859628477eb0aa0ea0d51a48cff483157c400390d11d05346a1a7c`  
		Last Modified: Thu, 13 Feb 2025 01:09:10 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b58e3ed86e8ad4a68be7c92653ccac14549e2181794b82d61b85198130f3ac3`  
		Last Modified: Thu, 13 Feb 2025 01:09:25 GMT  
		Size: 207.8 MB (207842824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e58e7c3c7bef59e1cdc35bb0d15f5c5f483a1a63236116ab8a43c40c5ff12e`  
		Last Modified: Thu, 13 Feb 2025 01:09:10 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
