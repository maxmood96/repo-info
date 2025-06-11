## `openjdk:26-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:03cc8e4e237166bd82603ac05eb332a139d83e61a55829125a8e07fdf040e60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `openjdk:26-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:23c4aa0381be5cc436939a9003f2e25efa6d34223a73a19bf5b8da3806617d2b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3695872557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e83bf4f0d5a8a2d68453c381f142528660bed83bce92e563ce25236db1417d0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Tue, 10 Jun 2025 21:28:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Jun 2025 21:28:29 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 10 Jun 2025 21:28:29 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 10 Jun 2025 21:28:36 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 10 Jun 2025 21:28:37 GMT
ENV JAVA_VERSION=26-ea+1
# Tue, 10 Jun 2025 21:28:38 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/1/GPL/openjdk-26-ea+1_windows-x64_bin.zip
# Tue, 10 Jun 2025 21:28:39 GMT
ENV JAVA_SHA256=b10c3aefd0ca30a469837b9339e27e64df5e7a3fc0eee39f06c0f30b1ae2ad19
# Tue, 10 Jun 2025 21:28:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 10 Jun 2025 21:29:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bc70c5fbd3c11dcd63cdc81a82b97391309d92046c2a13f447005386760af3`  
		Last Modified: Tue, 10 Jun 2025 21:32:46 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7492ad8a2f4d005651d6bf1cbc97e190bd5011fdfe2859979de9d9ce51fcaf`  
		Last Modified: Tue, 10 Jun 2025 21:32:46 GMT  
		Size: 388.8 KB (388758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808805ce9e2e81c9f64e66194f88a1aadbe685f838185b23788bb93c45ca37e0`  
		Last Modified: Tue, 10 Jun 2025 21:32:46 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9452fd7cdcee2adda7b5a83696ab320a2b70e7656198d095033441c269e728b6`  
		Last Modified: Tue, 10 Jun 2025 21:32:46 GMT  
		Size: 372.5 KB (372536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a73f25cb5bea0ee17c15df5e6126af84518bd61d4faffce681f3d343f355750`  
		Last Modified: Tue, 10 Jun 2025 21:32:47 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a766594e6ddb6ea58b74edf9173a07f8f80ca01429803d376ae0540db6b51f8`  
		Last Modified: Tue, 10 Jun 2025 21:32:47 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae70d9d38bc691f72eb9ab8408972b556974fd77ac9afa73d1cb5651da37eedc`  
		Last Modified: Tue, 10 Jun 2025 21:32:47 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46e5f182b39234e5533c1030dac2cfde9b5eb89ba0bb12ed8fdb2fc3b17c386`  
		Last Modified: Tue, 10 Jun 2025 22:10:07 GMT  
		Size: 218.9 MB (218929340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c77239e23a3e83808a58a03b2ad2c4d01453fdaa72682a829f856349d8fd82`  
		Last Modified: Tue, 10 Jun 2025 21:32:47 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
