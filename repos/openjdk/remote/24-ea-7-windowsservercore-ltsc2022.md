## `openjdk:24-ea-7-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:6d67f1162a53fb62faa61edb408c4dec68d040e3fea3e5c0db69e20d1abe1b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `openjdk:24-ea-7-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull openjdk@sha256:871cd303c209d07e6f8197839f19e4edbad83fa79b88e5e5f51304edc12613bc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346993191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73310b0659fcfeb11c9af25284339d5f0c9adfcd38cbc857ded98dadbc51167b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Mon, 22 Jul 2024 22:08:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 22 Jul 2024 22:10:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 22 Jul 2024 22:10:23 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 22 Jul 2024 22:10:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 22 Jul 2024 22:10:30 GMT
ENV JAVA_VERSION=24-ea+7
# Mon, 22 Jul 2024 22:10:31 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/7/GPL/openjdk-24-ea+7_windows-x64_bin.zip
# Mon, 22 Jul 2024 22:10:32 GMT
ENV JAVA_SHA256=e6ea3b3cd29d732dbe15fd95b7719200d69fff9e9f42a09fc5dc4fc3bd5fea12
# Mon, 22 Jul 2024 22:11:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 22 Jul 2024 22:11:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff11603de76dd8a343f7d2e9772bc77dece0072d9569cbcd95e485e71178689`  
		Last Modified: Mon, 22 Jul 2024 22:11:07 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259175014e57ba688d182f51a0e9721d75e0b0febb6b753c3e66d67ef4aa921b`  
		Last Modified: Mon, 22 Jul 2024 22:11:07 GMT  
		Size: 372.3 KB (372258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c77dc12a95152c648cfd642d625ac9bd276e1d44bd01c10e520dc4485e1d544`  
		Last Modified: Mon, 22 Jul 2024 22:11:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76b5fd23a055c817570d4c15651dd37b694728d5c77df94ed4ab552a98d74c7`  
		Last Modified: Mon, 22 Jul 2024 22:11:07 GMT  
		Size: 322.9 KB (322875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83b816afafd58f833f8ba442090de2ac9b5e07bec5a9eecc2c5856742d150a2`  
		Last Modified: Mon, 22 Jul 2024 22:11:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beef9dda82dcc7ecb42a0c468e2f46dd7eb38c59c17840d9647b7394831a33`  
		Last Modified: Mon, 22 Jul 2024 22:11:06 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e697456abe140aaa590dbf208b27bc313a621442cc94a28c5acad14ff46803c2`  
		Last Modified: Mon, 22 Jul 2024 22:11:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45091fc70e1a8cac8d32f29bd7df18318653d3437f288f0834d29f8fb4be1ff2`  
		Last Modified: Mon, 22 Jul 2024 22:11:17 GMT  
		Size: 206.7 MB (206689975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84aaa5254d1d5e440c194c36245ab44b4757b530aeaabc0034a4c3d7d0d1afe7`  
		Last Modified: Mon, 22 Jul 2024 22:11:06 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
