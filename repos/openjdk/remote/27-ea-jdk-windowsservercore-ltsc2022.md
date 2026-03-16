## `openjdk:27-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:477654f7e23a9c06c9cbef61861fd2d063725a48290744c120eb7ffd8a5e4fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `openjdk:27-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull openjdk@sha256:49b37b815e41742fd4fc72935f563e8244b37b1f8cb9b9a915294ed868787b2f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207825888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cfbb35e0063895c0089d53f05456bdf0442b68e07ea61c8399a03915fad2d0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Mon, 16 Mar 2026 18:17:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Mar 2026 18:18:24 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 16 Mar 2026 18:18:25 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 16 Mar 2026 18:18:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 16 Mar 2026 18:18:33 GMT
ENV JAVA_VERSION=27-ea+13
# Mon, 16 Mar 2026 18:18:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_windows-x64_bin.zip
# Mon, 16 Mar 2026 18:18:35 GMT
ENV JAVA_SHA256=f5a1c2aa25b826ecdaf3c6614f16bc91e871d38839bf0e01e4e2531bbe590cd0
# Mon, 16 Mar 2026 18:19:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 16 Mar 2026 18:19:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7495c78820827f6b1f2185c1285dc84d756942187152d024d2e20972fa2b4097`  
		Last Modified: Mon, 16 Mar 2026 18:19:11 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f97670b4a761ad835ccafbe0a5ccea6a2ccdc7ca02dfe871148832156699fb`  
		Last Modified: Mon, 16 Mar 2026 18:19:11 GMT  
		Size: 505.7 KB (505651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0da8f23e7afe73975f1a9e292c93b1682e5bbf47ddeb37121ca776ee991a42a`  
		Last Modified: Mon, 16 Mar 2026 18:19:11 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c86f8a6a2fe97ffe39cb1345789d861d0d64bdd7f19691afa6b3fe8d2cd5ba`  
		Last Modified: Mon, 16 Mar 2026 18:19:11 GMT  
		Size: 317.5 KB (317534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e18c49347be4d99cba7c8ec7789784b904b2f077322192fd65cbd9665a8b6ad`  
		Last Modified: Mon, 16 Mar 2026 18:19:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9327966cec93921a14d4da385f40975c7c8ce35b05add7c279aa67fab2b51bcd`  
		Last Modified: Mon, 16 Mar 2026 18:19:09 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014def7f2c4de4ac1198a4e015eaa1a8205ab92d7716aa272526247c46adf624`  
		Last Modified: Mon, 16 Mar 2026 18:19:09 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3cf3feeca970486a1d68f8644dd6dd3e51b6d6ed44d229bd869e55cf945283`  
		Last Modified: Mon, 16 Mar 2026 18:19:25 GMT  
		Size: 224.7 MB (224713478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e49617387eaacfc2f51cac81b4091d275d3368b07678525a6d4ef395f83d658`  
		Last Modified: Mon, 16 Mar 2026 18:19:09 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
