## `openjdk:25-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:0ee9e90111784c64aa65b3dbaf0d52c5846e51914653f738e4e51b56c32936e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `openjdk:25-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:609c02818812727347edc258befcbc62e1ca95c2de1c124b37c9b03f2c6f5c2a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2470803142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbf868068a78a5f3f315a9a8dc7e1e7801463d3397b0b58b316023e6a070d08`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 28 Jan 2025 23:27:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Jan 2025 23:28:54 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 28 Jan 2025 23:28:55 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 28 Jan 2025 23:29:09 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 28 Jan 2025 23:29:09 GMT
ENV JAVA_VERSION=25-ea+7
# Tue, 28 Jan 2025 23:29:10 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_windows-x64_bin.zip
# Tue, 28 Jan 2025 23:29:11 GMT
ENV JAVA_SHA256=98590eb26fdd8ac407ec4fd6fb11819d381f179d87174fea5a2ac7d5b051c11a
# Tue, 28 Jan 2025 23:29:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 28 Jan 2025 23:29:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1196647625f97a5c149bd4183458529ca5c7f7538c17f956c0c9fb41fc25bc40`  
		Last Modified: Tue, 28 Jan 2025 23:29:52 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d50d493298a1b0fab1293d0523955388b3b4683ded4b3551c089317141259a`  
		Last Modified: Tue, 28 Jan 2025 23:29:52 GMT  
		Size: 364.1 KB (364128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7e1212140f1b850909f77bb8249e4fc1c1b1c6b6e2b20f868a12e06ab9ecf5`  
		Last Modified: Tue, 28 Jan 2025 23:29:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482262ff641b83b70fb20e68b180b1e12cd6d1e35e4a5c7c3b3ec4fbafd6b134`  
		Last Modified: Tue, 28 Jan 2025 23:29:52 GMT  
		Size: 311.9 KB (311851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d595f39aed0f24aadba29f83e2fa569812e512031bfe927cc8d2ea3ac50c469b`  
		Last Modified: Tue, 28 Jan 2025 23:29:51 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7693907405c5ef496592f9e46f3489f2dfcbb039111a1e6e8305f49fbe7c230c`  
		Last Modified: Tue, 28 Jan 2025 23:29:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acda82acf2077e64e78db802e42fed3f40a5c39b7bb9bd851531e706a098a3e`  
		Last Modified: Tue, 28 Jan 2025 23:29:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e61106f45308b377a4ff1100526a067ef9ab3d3960f1a112e688258e2415a26`  
		Last Modified: Tue, 28 Jan 2025 23:30:02 GMT  
		Size: 207.7 MB (207734193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b815c0bd0062679933c7eb3768ed73f306cda4f2dba2455b49ca8d73f6255611`  
		Last Modified: Tue, 28 Jan 2025 23:29:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
