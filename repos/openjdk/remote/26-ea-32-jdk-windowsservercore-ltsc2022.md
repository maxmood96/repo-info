## `openjdk:26-ea-32-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:2846d619bcc94cd19ebe34a4ee3b5a57dfee3663cf8c5ed87eec1bcda6fa0c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `openjdk:26-ea-32-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:58d9bbf5142fd55adb994619c7c1aa1d432ced27da1b80cac88d2d1ee815e696
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2060788968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b397fa34425cd7e164d9992f2cc6cbd9dc32c76a82cf3f92f95ab4e64e8707`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:08:48 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:08:49 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 26 Jan 2026 22:08:56 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:08:58 GMT
ENV JAVA_VERSION=26-ea+32
# Mon, 26 Jan 2026 22:09:00 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_windows-x64_bin.zip
# Mon, 26 Jan 2026 22:09:01 GMT
ENV JAVA_SHA256=02a8f8920550b69cdbebb0d7b6eb675d5f597bc5feb7513ae61038c856c19cb8
# Mon, 26 Jan 2026 22:10:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:10:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fa8db78906ea6fbf10041de1ed15ff81c180a21a4f65ae404226dece2460a4`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 503.7 KB (503709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284a6959273d9ba6a25688b512b9013204f189023c9eb7022f9ac08eaf3d26c6`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06de4c3e24ae6000dddba236b23f22ef27aeb99e16ced180f3cda2d49aeb55e8`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 351.8 KB (351761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5206495a19cb6b0ce0a5a53657bf7ae9d3536b05259466c892ca6884b49b93ee`  
		Last Modified: Mon, 26 Jan 2026 22:10:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6ec380a32cfcc46f5ff1f36e377ca8a30b0614e5807d08cca274d6ef6750bf`  
		Last Modified: Mon, 26 Jan 2026 22:10:26 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc845909244c84e6066c4b57225fc7f4dc3a13926e3980d8eeb906e647e19c66`  
		Last Modified: Mon, 26 Jan 2026 22:10:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f814cb8506ce154ec001ddaf56ceef947e401882612c8e7b2143cbbede126153`  
		Last Modified: Mon, 26 Jan 2026 22:10:43 GMT  
		Size: 224.3 MB (224266490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe6edc21e1d71fac10b10e5aa52ee2b1c4b76aeaf2bb358b9bf9c922992b5f1`  
		Last Modified: Mon, 26 Jan 2026 22:10:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
