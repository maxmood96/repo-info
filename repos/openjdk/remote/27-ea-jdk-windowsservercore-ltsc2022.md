## `openjdk:27-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:5bbee717be1f36ca61349fc2f322afa07a75abc23e05e3ce7298b82d1cf5000c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `openjdk:27-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:3ee88105ef2b6b434b11c6fc040dc79eae9c229e11e86471fb11fe612c60e100
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2005037582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab684191e94ca6fe0225dc99089efca1a9e60b1e0890b30c245d54c80e4b54e3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Mon, 12 Jan 2026 20:07:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Jan 2026 20:08:05 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 12 Jan 2026 20:22:00 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 12 Jan 2026 20:22:07 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 Jan 2026 20:22:08 GMT
ENV JAVA_VERSION=27-ea+4
# Mon, 12 Jan 2026 20:22:09 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_windows-x64_bin.zip
# Mon, 12 Jan 2026 20:22:10 GMT
ENV JAVA_SHA256=03e913ca127ac00cd50269ad63a883ae5c879db36519d50788902f24576ebba7
# Mon, 12 Jan 2026 20:22:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 Jan 2026 20:22:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ae91ebb6b06916422f2db8a3c6f63e9ad96d44267ea6c1205256cd05e31ad9`  
		Last Modified: Mon, 12 Jan 2026 20:21:42 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d05d2dbb94cd655893e275edfdc5a2e8865eb5e7e9e1dcece1cc5c60c612687`  
		Last Modified: Mon, 12 Jan 2026 20:21:42 GMT  
		Size: 504.0 KB (503972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61db3d75ae7eb5350754e82153323abe625c73bbfa3c9100125d605844ff5e1`  
		Last Modified: Mon, 12 Jan 2026 20:23:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258674f52f307fa2c7d52de6c1b9fdb8537f14f91bb01485436c3857ede17948`  
		Last Modified: Mon, 12 Jan 2026 20:23:26 GMT  
		Size: 351.9 KB (351932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e0892981fd3355c92448b345eb8c727bae3d9d56ca599be1ea587a273e2d73`  
		Last Modified: Mon, 12 Jan 2026 20:23:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a95c936c85b99ef2a32737b748254e16a31c5835d3551846bfef262a925d85`  
		Last Modified: Mon, 12 Jan 2026 20:23:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef02c6d1e7049fc8c2d6e03a0affdfc5f9ac2b695e9a754d0f821ba81300806`  
		Last Modified: Mon, 12 Jan 2026 20:23:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6567278d15110aa014186e974fc217ed91f6e537aa9778ff010a9d69d389f7d6`  
		Last Modified: Mon, 12 Jan 2026 20:25:37 GMT  
		Size: 224.3 MB (224294550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046342707d74e0d1a4a5edc74bc827934a82072b4c5a9ae7c5e70a31bca73e89`  
		Last Modified: Mon, 12 Jan 2026 20:23:26 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
