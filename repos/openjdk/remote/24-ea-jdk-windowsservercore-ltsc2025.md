## `openjdk:24-ea-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:b05efbe274bcf2ffeae919c1e630a73aabe7fbe65e0770e7e8d3181a76c381d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:24-ea-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:fc8163ca14d5e39f143eb9e3f151d7f8af99b4928b5652698786927163a7d3ff
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2710001773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f402f0ecd841444caa56bc329d19f8e96a65458eb4c8c3c2b61f5d7e8837bbd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Tue, 04 Feb 2025 23:35:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 04 Feb 2025 23:35:33 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 04 Feb 2025 23:35:33 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 04 Feb 2025 23:35:39 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 04 Feb 2025 23:35:39 GMT
ENV JAVA_VERSION=24-ea+35
# Tue, 04 Feb 2025 23:35:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_windows-x64_bin.zip
# Tue, 04 Feb 2025 23:35:40 GMT
ENV JAVA_SHA256=1d56c9650251685d5d3007781088385fe316738b84a354ef2d3a42b83a38bd46
# Tue, 04 Feb 2025 23:35:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 04 Feb 2025 23:35:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e815cf122d326a1f2d021f101771ff87b88fb83c556b1aa4e6316068f6cec522`  
		Last Modified: Tue, 04 Feb 2025 23:36:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040b0044124cd4bf7ba45e2111b4630a6134ea3f32a9a48c05e14119163d0237`  
		Last Modified: Tue, 04 Feb 2025 23:36:02 GMT  
		Size: 392.7 KB (392690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc2b0bd242db40cadea3dc3f5fa7fb0d1fe34ad179013078a36bc47ef011503`  
		Last Modified: Tue, 04 Feb 2025 23:36:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e4f831c38698dfddef2a0e305a8af7c3ba915cae4754b623cb34b9670d4214`  
		Last Modified: Tue, 04 Feb 2025 23:36:01 GMT  
		Size: 377.2 KB (377156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b5973dfe16f4a3259d2d15ad8b3df686b60888e38da82e037d0b89197ee99e`  
		Last Modified: Tue, 04 Feb 2025 23:36:01 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cfb32741a297613d2b0772f95dffce34b2d208e49d1168caf3b5e73d429101`  
		Last Modified: Tue, 04 Feb 2025 23:36:00 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc73c6d1c43e8d2edd47e9074786ac605944dab41ad0a939a652637b88b4002`  
		Last Modified: Tue, 04 Feb 2025 23:36:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61b0ef4a1a35f09c92f16711181f7eab4abf111fb318e28f011aa1956b75e91`  
		Last Modified: Tue, 04 Feb 2025 23:36:13 GMT  
		Size: 208.9 MB (208946587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8510759c673a1be4bf5f84e452f7b72580c8ae4fd3ae86a3e62e941287d2cc90`  
		Last Modified: Tue, 04 Feb 2025 23:36:01 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
