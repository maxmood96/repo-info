## `openjdk:27-ea-4-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:cbc920b5be599e634bfbe534653a11a5f3c0b4d52dc1935b59ea63fa4c26e0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `openjdk:27-ea-4-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:80dab4c047002cb0563f2678383687f974209d30474d908d175610496863d0e8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2060785723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ec80dd35935a974e2ac8c5593f44c5930589f4c2f9631495f4573d90674f32`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 22:53:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:11:14 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:11:15 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 13 Jan 2026 23:11:20 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:11:21 GMT
ENV JAVA_VERSION=27-ea+4
# Tue, 13 Jan 2026 23:11:22 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_windows-x64_bin.zip
# Tue, 13 Jan 2026 23:11:23 GMT
ENV JAVA_SHA256=03e913ca127ac00cd50269ad63a883ae5c879db36519d50788902f24576ebba7
# Tue, 13 Jan 2026 23:11:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:11:58 GMT
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
	-	`sha256:9f681901ae8b8270ef4ad40879b419cd45d092d5d347a675266218039d5b88a0`  
		Last Modified: Tue, 13 Jan 2026 23:01:20 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e725a46cf123e0204571db05eb82ce3a0b9811b0071f4bc3a34c999cda4e85`  
		Last Modified: Tue, 13 Jan 2026 23:12:29 GMT  
		Size: 490.4 KB (490380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3828c6449f875b1a7b5c838c648bd50d7dbe1b54339d49eb304d0b90d2eb9a`  
		Last Modified: Tue, 13 Jan 2026 23:12:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07be3b9cd978ff8213b9dbb3d6cddec15a0700fbeee53a48e0162bf0cedff374`  
		Last Modified: Tue, 13 Jan 2026 23:12:07 GMT  
		Size: 337.7 KB (337707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8e2cbc3bc843dafebc4b5fe451a4e121b6f03cb720176dde8bc56828df64cb`  
		Last Modified: Tue, 13 Jan 2026 23:12:05 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9569662b7e2bdea18d217081e2748cd88bcc8106ff4851b725c8b5c8e5ed7aab`  
		Last Modified: Tue, 13 Jan 2026 23:12:28 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740a63833dc6a0f63eb7e95f41c3cdcdf7d6bd1d1fb301f001f7f02b6057e5cc`  
		Last Modified: Tue, 13 Jan 2026 23:12:29 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49df72f0a4e284b1a974e63c6c1fb9463f932b89ae928ff693adec43b1f080aa`  
		Last Modified: Tue, 13 Jan 2026 23:12:41 GMT  
		Size: 224.3 MB (224290606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf713ff5ea24aa313f602af0e868e7ce2c03e1579d5465bf115f9d4c3d15ccb`  
		Last Modified: Tue, 13 Jan 2026 23:12:05 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
