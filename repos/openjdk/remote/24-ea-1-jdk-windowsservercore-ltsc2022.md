## `openjdk:24-ea-1-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:d1ea2dc6ae624d315b645cfaf1fa8f18bbda397da76bdb1509ca1b5f625a08e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2527; amd64

### `openjdk:24-ea-1-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2527; amd64

```console
$ docker pull openjdk@sha256:b81d9001c7bf1106935a1c5fd59a9c4d8aaedeead3cd16d014ac1a0965de282d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325366025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49b019541c398e9dd198d5d1491ec078d3cc72948b5729e5427389a21b45a74`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Wed, 12 Jun 2024 18:06:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:06:20 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 12 Jun 2024 18:06:20 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 12 Jun 2024 18:06:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 12 Jun 2024 18:06:26 GMT
ENV JAVA_VERSION=24-ea+1
# Wed, 12 Jun 2024 18:06:27 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_windows-x64_bin.zip
# Wed, 12 Jun 2024 18:06:28 GMT
ENV JAVA_SHA256=84640da466dc6c7af5dbd523e321f5cfef6b81a434c1558b43633e7485da95f7
# Wed, 12 Jun 2024 18:06:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 12 Jun 2024 18:06:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8f7f1748cabfa2e0b5c55969b2e4d22819bce47a87730a69347e03ae38188b`  
		Last Modified: Wed, 12 Jun 2024 18:06:52 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3590495ca430c4cb9bd4cd7838d752782b474c64c4e3005d0f32926e6516f8`  
		Last Modified: Wed, 12 Jun 2024 18:06:53 GMT  
		Size: 358.7 KB (358715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556aa7dba34c013165b3878a16bca9b43102749f263246355fe5ca40b42726ec`  
		Last Modified: Wed, 12 Jun 2024 18:06:52 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e380f248928c89d79064d6fb675a67bde544886ec6d76fe41c17b61ca6392c6`  
		Last Modified: Wed, 12 Jun 2024 18:06:52 GMT  
		Size: 342.4 KB (342386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f34077c0578498e782c125233639004653b185a85b8cfa000c8b2ed677e8be4`  
		Last Modified: Wed, 12 Jun 2024 18:06:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4296f2b2dd1c6e784a1d5a56ef8290e17c721e82a68bf7193bf134351eae9da`  
		Last Modified: Wed, 12 Jun 2024 18:06:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c616546812b276722ba029f7739344370788c9b3aa9a074586817a6bbae683d1`  
		Last Modified: Wed, 12 Jun 2024 18:06:51 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd30cfe57bfe9955fc12dfc40bffe875446c4ed2faf14a359891f8913a2c4bf`  
		Last Modified: Wed, 12 Jun 2024 18:07:02 GMT  
		Size: 206.5 MB (206478509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f8922c47401eadc602be4c1a2bbe1d2c7a8e10e308903d8733ddb07e02d39f`  
		Last Modified: Wed, 12 Jun 2024 18:06:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
