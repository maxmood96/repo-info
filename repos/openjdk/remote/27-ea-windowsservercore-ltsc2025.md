## `openjdk:27-ea-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:c68254208ec22e009dc78f08d8bbab1b555bb3f225b552f6f2eb58099bff3209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `openjdk:27-ea-windowsservercore-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull openjdk@sha256:f508322c5de16185ab75ddaaef289a5be413830748e1c6e0f5780843c3aa8789
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3478222735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d912435bbf1d851f509d490193d09110a8033a609301f90105f154a4b5970b8a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Mon, 12 Jan 2026 20:08:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Jan 2026 20:08:40 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 12 Jan 2026 20:08:41 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 12 Jan 2026 20:08:46 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 Jan 2026 20:08:47 GMT
ENV JAVA_VERSION=27-ea+4
# Mon, 12 Jan 2026 20:08:48 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_windows-x64_bin.zip
# Mon, 12 Jan 2026 20:08:48 GMT
ENV JAVA_SHA256=03e913ca127ac00cd50269ad63a883ae5c879db36519d50788902f24576ebba7
# Mon, 12 Jan 2026 20:09:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 Jan 2026 20:09:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0fc345c745ab527cfd9026b3df35ae3819ee35a168bbe9c00ae31a737d548d`  
		Last Modified: Mon, 12 Jan 2026 20:25:50 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66931726c3351b015957271f86fff15a7e69cd1984120336f1f1247d63146a22`  
		Last Modified: Mon, 12 Jan 2026 20:25:50 GMT  
		Size: 398.3 KB (398288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bdf745d3bef4d8bf855d54ddd29ac431efe5e8c34bfc4b4f47e2972c333b343`  
		Last Modified: Mon, 12 Jan 2026 20:25:50 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dc07ce5d0b6fe8fb039f9415551f3029c61e42c67c91096d678be23227fb2b`  
		Last Modified: Mon, 12 Jan 2026 20:25:50 GMT  
		Size: 379.4 KB (379360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2891f70eb3c29eb50060e862743983618f4c0cbe66a5d7b8c54781bfcedc69c8`  
		Last Modified: Mon, 12 Jan 2026 20:25:50 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6c0561395e8c1b679b819aa49af6c97d2cfb813e6ea83e9cf2eedcc9f4512`  
		Last Modified: Mon, 12 Jan 2026 20:25:50 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55c117aeac8da1df9fa84368e26034719cb02127bb704d6243c4fa973ba6d31`  
		Last Modified: Mon, 12 Jan 2026 20:25:57 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61da1fa60e1ef8abae4ab0d2593451388520041a53bbde8e9edf367f1267bf0b`  
		Last Modified: Mon, 12 Jan 2026 20:27:40 GMT  
		Size: 224.3 MB (224316802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8b94f6e771f9dafd74afc47df4bfb20c52e825f8412d5bb8099f011fc3f15e`  
		Last Modified: Mon, 12 Jan 2026 20:25:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
