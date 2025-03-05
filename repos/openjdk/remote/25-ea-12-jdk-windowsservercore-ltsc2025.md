## `openjdk:25-ea-12-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:57687ae2fd3e1e3f21cf636b5b459680b6f9dab25613d271c833435e11d11250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `openjdk:25-ea-12-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull openjdk@sha256:280cf0843e824f4d3e7384f73db31d5d4afde655b598751d20303551b106bb63
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3025322017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5294b9f1c210feef30f48dec9cb295b7c84a322de2d3a95b501c9ac51c510c05`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 04 Mar 2025 22:25:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 04 Mar 2025 22:25:45 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 04 Mar 2025 22:25:45 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 04 Mar 2025 22:25:52 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 04 Mar 2025 22:25:53 GMT
ENV JAVA_VERSION=25-ea+12
# Tue, 04 Mar 2025 22:25:54 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_windows-x64_bin.zip
# Tue, 04 Mar 2025 22:25:54 GMT
ENV JAVA_SHA256=bcb8237b8992ff10a073a5de79dd9e3bdd7ca90a56c4d16a3639a876b9aec165
# Tue, 04 Mar 2025 22:26:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 04 Mar 2025 22:26:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673df8ece526c1fc82b756af60848f542447753d393af880a28c823c442b2083`  
		Last Modified: Tue, 04 Mar 2025 22:26:19 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980c9e93e13b2c6ff6ee63330956dcbb2f31797ed60f1b7375ec158de179642f`  
		Last Modified: Tue, 04 Mar 2025 22:26:19 GMT  
		Size: 393.7 KB (393701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8c5e86a9be4a1cc23a90fd7c2c6bd865e4d3dee9c9a6c5c5db9b253aa5ee00`  
		Last Modified: Tue, 04 Mar 2025 22:26:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab943c31576b09e084c146a495194310f38908b75768158447bfb386086d7de`  
		Last Modified: Tue, 04 Mar 2025 22:26:19 GMT  
		Size: 378.1 KB (378052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fbe1efbb7fe813cbdcbd61547ef0a24594f592caef540c6cda1f5a14a403463`  
		Last Modified: Tue, 04 Mar 2025 22:26:18 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32020b98e8fb935fd88fa2b4ae60b64dad13ef2a4f8dd753a54ebd37378a8099`  
		Last Modified: Tue, 04 Mar 2025 22:26:18 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d231fd9a8745ca001f69354e3f8cd10a2329d896a70bb4f47c0ee7a8a240239`  
		Last Modified: Tue, 04 Mar 2025 22:26:18 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802d2eb7ad7361bd21f5d8d62a8e75ffabc8686ed128ced24ce301160bd3f70e`  
		Last Modified: Tue, 04 Mar 2025 22:26:30 GMT  
		Size: 208.0 MB (207954822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f43f07bb3cc62770b2b647a62599f4409293dff3b6b36c5ccc52608e86aa5e`  
		Last Modified: Tue, 04 Mar 2025 22:26:18 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
