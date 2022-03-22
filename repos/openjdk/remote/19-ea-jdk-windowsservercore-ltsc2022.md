## `openjdk:19-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:f57c145e7dab103d61ec72f9b0fedaad2da7ae6137a5d66ba6b5c46fc6bc7254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.587; amd64

### `openjdk:19-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.587; amd64

```console
$ docker pull openjdk@sha256:8804a78205d70d7191ab7c3676ff9e422b49b0aa680227ff4c619af0b035c1eb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2410705286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7709aed1e68a0a4ffc9d23c10598973115fd1805371505bcd823bf063877e812`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 19:26:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 17:08:43 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Mar 2022 17:08:44 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 09 Mar 2022 17:09:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 22 Mar 2022 01:14:39 GMT
ENV JAVA_VERSION=19-ea+14
# Tue, 22 Mar 2022 01:14:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_windows-x64_bin.zip
# Tue, 22 Mar 2022 01:14:41 GMT
ENV JAVA_SHA256=1149da64d70afbb171b3426eb55763f697a2f9c7db54ab62adcdd1935f7f5643
# Tue, 22 Mar 2022 01:15:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 22 Mar 2022 01:15:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d58ba398110c3f761c6307a5621ec218b8593ba8b07b734436bcdd8d07a23e08`  
		Last Modified: Tue, 08 Mar 2022 20:00:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536e5c64699fc55f528fe9ed2ca2c4088a1b329a50236ef20b400958daadc725`  
		Last Modified: Wed, 09 Mar 2022 17:40:56 GMT  
		Size: 600.0 KB (600021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242a279bb38e5c0949759b401e7be86d7f899c9457fba0eeabdef0fec92f6682`  
		Last Modified: Wed, 09 Mar 2022 17:40:55 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f4c6cacc278c66995aee924b612b9af7a269c23ba83a9f7d62e975c98e167f`  
		Last Modified: Wed, 09 Mar 2022 17:40:56 GMT  
		Size: 510.3 KB (510254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a13a2cbfb77c65d598a066caf4efb496566b286c783163242b05e815c36e7be`  
		Last Modified: Tue, 22 Mar 2022 03:19:32 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935ca362df46ea65dc82bbc40dfd2e72c6b0beed022d8030ce2043b97a83c436`  
		Last Modified: Tue, 22 Mar 2022 03:19:32 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0c041c13a700cb04f8f00693f4e2d8eb37eb2a33db4f0781b0a70b5ee3cfac`  
		Last Modified: Tue, 22 Mar 2022 03:19:33 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0901f4f60c5bc3514f2184d96d7895551fc4588d5b65a278cf46382442216e`  
		Last Modified: Tue, 22 Mar 2022 03:23:00 GMT  
		Size: 188.3 MB (188339487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fcdea0bf470701b807e017a56f7d444de74bc7910cf75ca2fc2a179f81a789`  
		Last Modified: Tue, 22 Mar 2022 03:19:33 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
