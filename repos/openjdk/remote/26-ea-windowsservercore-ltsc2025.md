## `openjdk:26-ea-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:08342fc1bc6af029b887a0ff15d039fd5cc49362ae5aa837637e242062282c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `openjdk:26-ea-windowsservercore-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull openjdk@sha256:6e380ee6580cbd135db09b1af1379d4ff9aa7652479f7b9908c01077cd70a14d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3478068626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0b7dd5f3ca81971103e2774dd4edebde69a5ff60d022a4e314c2d4c7dfb9d7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 16 Dec 2025 00:11:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 00:11:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 16 Dec 2025 00:11:16 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 16 Dec 2025 00:11:23 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 16 Dec 2025 00:11:24 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 00:11:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_windows-x64_bin.zip
# Tue, 16 Dec 2025 00:11:25 GMT
ENV JAVA_SHA256=1043a56a8e09613f76543d6e9290ff5c53e9cc2bcf0053550a36ad993843bf2c
# Tue, 16 Dec 2025 00:11:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 16 Dec 2025 00:11:55 GMT
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
	-	`sha256:2e9084b4fcbb7315770c061c935d37e934db4808ffa39e15e2ecc7a0f7dcf310`  
		Last Modified: Tue, 16 Dec 2025 00:31:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468acb3cc160814c9d78adbad78b2d34a2f5c5ffc8c1d3339a297f665ec5946b`  
		Last Modified: Tue, 16 Dec 2025 00:31:21 GMT  
		Size: 375.9 KB (375885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516491c030339ab52bc666c0c0e2008f0e3ec3fc6e2eab8a86c799fea34d8a6e`  
		Last Modified: Tue, 16 Dec 2025 00:31:21 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db446e317c732404081228a000c3aa7352b4307154946e9de963d5eadd277952`  
		Last Modified: Tue, 16 Dec 2025 00:31:21 GMT  
		Size: 355.8 KB (355808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cca07bac0163fce108a133a8e3929a7ebd5b66275654019d73bb99a90484546`  
		Last Modified: Tue, 16 Dec 2025 00:31:21 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b306042d000ce09fe72db3ffb884f0f0d068cb4fd7f08b150e92351d7a39e61b`  
		Last Modified: Tue, 16 Dec 2025 00:31:21 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3975ff4b0d611f284714f5c3836b95ad116395395dc7db55bfa08ee0d108eedf`  
		Last Modified: Tue, 16 Dec 2025 00:31:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deaec69ef65eee456b230a03487572c2976bc5fc4617beadd78b25bdee36951b`  
		Last Modified: Tue, 16 Dec 2025 00:33:22 GMT  
		Size: 224.2 MB (224208611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c866f01fdc92561b370b57406361d24b13ab0c04e4b76d4eb5a8bedf0340d4b`  
		Last Modified: Tue, 16 Dec 2025 00:31:21 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
