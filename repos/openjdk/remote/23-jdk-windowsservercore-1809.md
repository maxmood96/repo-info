## `openjdk:23-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:cf2353f47540b8282b6b7a65970b0e8021ecb1bee7f728c15b7e59c7dadad175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `openjdk:23-jdk-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull openjdk@sha256:3cc2a3459e62397e1ab2ccd22c9e3341232c8cf1df96f76e48ddb65d2629cf8f
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279202340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de5975a7ba905c88b31bb3745c8c4e3763bd62c1645a97b58efada06514e9758`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:59:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:00:53 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:00:54 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 14 Feb 2024 20:01:01 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:01:01 GMT
ENV JAVA_VERSION=23-ea+8
# Wed, 14 Feb 2024 20:01:02 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_windows-x64_bin.zip
# Wed, 14 Feb 2024 20:01:02 GMT
ENV JAVA_SHA256=3bf12bda8aa3d293ed14f6956bd24e598c395e3267be4b58191e542ec7d3479a
# Wed, 14 Feb 2024 20:01:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:01:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec943b1666948fcda90228c2495c693f8abf24bde2f5f4c097cbddfdbdb1b509`  
		Last Modified: Wed, 14 Feb 2024 20:01:51 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa0a5852e60a226aba42c7f79e0f3ad8f5fe1c9996a30a62146eb2a0ef0b05a`  
		Last Modified: Wed, 14 Feb 2024 20:01:51 GMT  
		Size: 489.8 KB (489769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61567085d47cb030b10a576072ba8fbb66d9343b0e3a4e8057673d833695d5d4`  
		Last Modified: Wed, 14 Feb 2024 20:01:51 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4a88616913603e35a6672ea1e732c0cdb213bc1770e847b574f00a69798295`  
		Last Modified: Wed, 14 Feb 2024 20:01:51 GMT  
		Size: 342.0 KB (341991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d2843d53d7dcacdac37de03514588c92efa05ac77e1fcc857b123c526c1208`  
		Last Modified: Wed, 14 Feb 2024 20:01:49 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a508ba7ff7645b4d5eab1dcef3e858da220ce3f0ccd7e5f6c91d80c7c7469f0`  
		Last Modified: Wed, 14 Feb 2024 20:01:48 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad2a546af7956f0e2cbee82cddd34749c1d86756fc5175274cf9a672f987d01`  
		Last Modified: Wed, 14 Feb 2024 20:01:48 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e58c9e25f14dbb716ef7c165393a3003fdb094576b2e6b5da8f6428c8906cee`  
		Last Modified: Wed, 14 Feb 2024 20:02:00 GMT  
		Size: 197.9 MB (197913594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f556cbdb3296f59172d651dabdef673ad9c1af3084422a872d6a115502464c`  
		Last Modified: Wed, 14 Feb 2024 20:01:49 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
