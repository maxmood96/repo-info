## `openjdk:25-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:903e58226e03a59e2fa3859d97a019adc59a211db5e31f6a7c645af9b423bb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:25-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:1a7626a0d5f260303e3c7fd4f1897f9462476b05145e06b58e99982d855083b4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2331857931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0809ccd8d6f70fa8a3f9ba02fdb8e4a0845fdfd0060871a73c05363c3ef0a48`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:39:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:40:05 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:40:05 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 14 Jan 2025 23:40:12 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:40:12 GMT
ENV JAVA_VERSION=25-ea+5
# Tue, 14 Jan 2025 23:40:13 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_windows-x64_bin.zip
# Tue, 14 Jan 2025 23:40:13 GMT
ENV JAVA_SHA256=1fa831a6d9973fe9a64841dfd9c44759e07112be15da766d10c6f5e1b3eff4fe
# Tue, 14 Jan 2025 23:40:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:40:36 GMT
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
	-	`sha256:564e1ca5920a3f7aff621af25b79d3f41751fc623b5d3e27bc1fd21b20a8801e`  
		Last Modified: Tue, 14 Jan 2025 23:40:41 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b469224690df42dec2a180aff3e9628dff31fe3fe528cedca43dd5f9b6c32d0c`  
		Last Modified: Tue, 14 Jan 2025 23:40:41 GMT  
		Size: 334.5 KB (334533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56305b76e55ece788092602ff610f07fc5501177577aaf606d0e85f04a979563`  
		Last Modified: Tue, 14 Jan 2025 23:40:41 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c242b9ee63e42b65650944dec7dfef206a11efc7affb1df4693715266d42a8`  
		Last Modified: Tue, 14 Jan 2025 23:40:41 GMT  
		Size: 321.7 KB (321729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bf674522f30004d16ce3f1656a24d878cd09c6cac55a81dcb6decd862b8974`  
		Last Modified: Tue, 14 Jan 2025 23:40:40 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3be3704408f7489a4f74e4ed55d4f691be51e76f11386430415e4618dfe87c`  
		Last Modified: Tue, 14 Jan 2025 23:40:40 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a812d72ab82a55b66e55e40c1a5f5ac719b79f71e2b6e09a66d3dd3c5b6bf8a5`  
		Last Modified: Tue, 14 Jan 2025 23:40:40 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638e5ac52e58edb71778a34529aac4faf70e15b1f9738df8712146c2b3e888c8`  
		Last Modified: Tue, 14 Jan 2025 23:40:52 GMT  
		Size: 209.0 MB (208981459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb3030930da5e1b8e2a32e89df59536d3922162d4e00beabdbde54f1c5633e7`  
		Last Modified: Tue, 14 Jan 2025 23:40:40 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
