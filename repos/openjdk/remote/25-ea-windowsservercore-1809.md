## `openjdk:25-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:c3726ac509df991fd9acf7e3ab5e069500791dbfcf72be8c081bf8ba765e57bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:25-ea-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:97edc7bcaf04450caf265fc8aa5c95bad9f5e45406b2847c88371df5372875c1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330637094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3316370f34e0be3bee0ce03dd987f429bf893ec391497da6c360962dc17afd63`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Wed, 29 Jan 2025 00:26:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Jan 2025 00:27:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 29 Jan 2025 00:27:18 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 29 Jan 2025 00:27:28 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 29 Jan 2025 00:27:29 GMT
ENV JAVA_VERSION=25-ea+7
# Wed, 29 Jan 2025 00:27:29 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_windows-x64_bin.zip
# Wed, 29 Jan 2025 00:27:30 GMT
ENV JAVA_SHA256=98590eb26fdd8ac407ec4fd6fb11819d381f179d87174fea5a2ac7d5b051c11a
# Wed, 29 Jan 2025 00:28:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 29 Jan 2025 00:28:06 GMT
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
	-	`sha256:25bf154cdbe7d3a6f56dd2f8dfcbd1b1e2c402968514547c80d78d40d221e931`  
		Last Modified: Wed, 29 Jan 2025 00:28:10 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777d1630c29d43e093833f18c618ad6c55bf0aa54795441fc7ce8c818e50d9ce`  
		Last Modified: Wed, 29 Jan 2025 00:28:10 GMT  
		Size: 340.2 KB (340228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155ee35ee7f973789a0d244debe9654e0a3d1eb74d1d2a4b31b2d3a4ddcd5eb6`  
		Last Modified: Wed, 29 Jan 2025 00:28:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c97e57488697d4457e32dc5c42280ccb954756dc0f985440cd3e3421b8a6ef`  
		Last Modified: Wed, 29 Jan 2025 00:28:10 GMT  
		Size: 330.6 KB (330638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0e6adb71bdca75fb53fa58de058b56f06219a2a78f34c54311de8b885aaa10`  
		Last Modified: Wed, 29 Jan 2025 00:28:09 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8cd25b1c8b4c69b50897de9fe99a8cc939a835a7657576415a2c8ec9d209cc`  
		Last Modified: Wed, 29 Jan 2025 00:28:09 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e504cd2c4c9cba8e3b70b4bb1574092c66bd4c6bf3d87825909ca8bb6681dc8`  
		Last Modified: Wed, 29 Jan 2025 00:28:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b3ffa5deee39c2df073de8793f9455af9e200083b6dac2d89aba0395d64d14`  
		Last Modified: Wed, 29 Jan 2025 00:28:19 GMT  
		Size: 207.7 MB (207746271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ec5684877f02e1de49a3ab901983533b56eaf325d005d327280319859f532e`  
		Last Modified: Wed, 29 Jan 2025 00:28:09 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
