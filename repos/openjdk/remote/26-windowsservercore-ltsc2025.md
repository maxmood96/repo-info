## `openjdk:26-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:5d1aa32ffc9039c5ae66d6cd378f35f6a7c5624a444773bdb691f7b715c833c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `openjdk:26-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull openjdk@sha256:b251a154cb92f6998ab3fff3a8e6292ffc3c036b7606258b61966835d71638d1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3791293572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f235e2f7dee4a58129938e657d76121881931ee6757b83b1d7910494a3b34f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 21:48:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 22:00:41 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Sep 2025 22:00:41 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 10 Sep 2025 22:00:46 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 10 Sep 2025 22:00:47 GMT
ENV JAVA_VERSION=26-ea+14
# Wed, 10 Sep 2025 22:00:47 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_windows-x64_bin.zip
# Wed, 10 Sep 2025 22:00:48 GMT
ENV JAVA_SHA256=a7542fc9e185b46aef40f54067948209eaeed10cc87b141740dc4b4236bf3d70
# Wed, 10 Sep 2025 22:01:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 22:01:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae601f0777b06a06d8faad18910ce906d57fb27de067d609e4022dde683f85b1`  
		Last Modified: Wed, 10 Sep 2025 21:57:05 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2d9ab5e4f3efe7e854006c00155f25a4a80db13fbe5d9c4397e6a1e6e83fa3`  
		Last Modified: Wed, 10 Sep 2025 22:01:44 GMT  
		Size: 354.3 KB (354316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0060af7fe3654f8cc32facbf8783f18cca049925c6847a5d5fc9e083f3aae920`  
		Last Modified: Wed, 10 Sep 2025 22:01:43 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e4549d40f62f0e23194b63c2407a745eaf2e65c2c7989740f3b8bf96ad2a30`  
		Last Modified: Wed, 10 Sep 2025 22:01:44 GMT  
		Size: 332.5 KB (332528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf50cc5e3307dd0ce9f9265c96f3a4382bbfa8df39c1892be9c894993d23cff`  
		Last Modified: Wed, 10 Sep 2025 22:01:44 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c53aa590d1952d696e19a01d7a4892a21781d0b79f6e8a9a6609c86763fd3f`  
		Last Modified: Wed, 10 Sep 2025 22:01:44 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb022c77095a4e22900ea281b9c95ce1a4c31e4dc06cddd6d62f2376fd3de9d`  
		Last Modified: Wed, 10 Sep 2025 22:01:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a89a940e020791774b5c85e17eabb5380cb7b27e6e8ec9c476f02505efd459`  
		Last Modified: Wed, 10 Sep 2025 22:20:57 GMT  
		Size: 219.2 MB (219159147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d98e57f69943f1125c487f095413d812c775bee55bda53184dd2b6ab4031566`  
		Last Modified: Wed, 10 Sep 2025 22:01:44 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
