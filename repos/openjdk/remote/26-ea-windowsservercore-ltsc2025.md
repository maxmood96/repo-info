## `openjdk:26-ea-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:8745ef813773e9de34b2f5e13752341ab12303532de7758cf2b7c505e794b444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `openjdk:26-ea-windowsservercore-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull openjdk@sha256:a2e8636bbdfed2222e09eaa2830fa7c94f6a1547890937f3eb6f84641c2889d2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3442850513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd284eba455d157cdf297cbfa4d5f52dec03808796faa483a68651314a99a02`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 21 Oct 2025 18:14:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:15:09 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:15:10 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 21 Oct 2025 18:15:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:15:22 GMT
ENV JAVA_VERSION=26-ea+20
# Tue, 21 Oct 2025 18:15:23 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_windows-x64_bin.zip
# Tue, 21 Oct 2025 18:15:24 GMT
ENV JAVA_SHA256=dbd547c391f90daa966d5d3a236e5a3cf792dea341d9596eb2a155059fe571a1
# Tue, 21 Oct 2025 18:15:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:15:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f67b52bd476e2c905e369b1aabcc60e8cb7a2ea77d6a39d21ccae187fd67d`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a940b69ca6bb540636945a1c0697a7f23149f6b8625724a6c99948198665b961`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 401.3 KB (401263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f860c613e0b9a60e539e679f5c45d457736c72998d58206dd901eb4f0cfee194`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d386648011f63e6d7ede9cb5d0ad9ed98c9a436f375958f396d3a197f7728b62`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 374.2 KB (374206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc976952c17ee4cd8ea64f186b49f53c83e1f771aa527ae7dd90bbc8f3d01e91`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea292a600b391d9619c91343fdb21c4b94b74e91cbcc1c9bda61bd673a582db7`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13125f91381c696717037044b7708b9cf57a74eba87a176d8b314b3ddd9186b3`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27e16eb82a971b1e72d68f4489edb6bb0d9ea5dce6a379bc6322f8dcdcda73a`  
		Last Modified: Tue, 21 Oct 2025 21:24:56 GMT  
		Size: 221.6 MB (221586740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3fa6e1eaa35d041e8e9e24387176f1d37bafe8d30f9952a3dcff7d8f01e14a`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
