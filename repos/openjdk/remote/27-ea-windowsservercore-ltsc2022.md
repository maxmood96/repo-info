## `openjdk:27-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:5eb4cb6f371984ac11b8ad1378ce6e4a7b64d0167d835a565fafad73d9454401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `openjdk:27-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull openjdk@sha256:de976f546ed481f4ce8c3240d4c72db74c9abb344a43ed2889a5fb06124aff27
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207943813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc719d72f1685166791ea3926f4a888d713deac47949497776abcf5ef01cef35`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Mon, 30 Mar 2026 17:50:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 30 Mar 2026 17:51:24 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 30 Mar 2026 17:51:25 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 30 Mar 2026 17:51:32 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 30 Mar 2026 17:51:33 GMT
ENV JAVA_VERSION=27-ea+15
# Mon, 30 Mar 2026 17:51:33 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_windows-x64_bin.zip
# Mon, 30 Mar 2026 17:51:35 GMT
ENV JAVA_SHA256=c92682fdb3296015613f5a3618a274035eb14eda9c766cf4d96c37da415e698f
# Mon, 30 Mar 2026 17:53:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 30 Mar 2026 17:53:03 GMT
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
	-	`sha256:5d5aff7fa2dd9d2fcd36fa312bf1e0097411dfb67aafc88b9cc6100c4dcddccd`  
		Last Modified: Mon, 30 Mar 2026 17:53:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c163a7c065f10b28b0053e756bfef68aaf7d699db2db95ff90116ad9eb88e3ed`  
		Last Modified: Mon, 30 Mar 2026 17:53:20 GMT  
		Size: 496.2 KB (496181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cc965bcf781f43aca88c5166ec03223c5a0fbd0d88c4cdf205bc1a3097f787`  
		Last Modified: Mon, 30 Mar 2026 17:53:20 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1231f55fb8216b360fa2860fd2bc270e2c04449b2ee432a52be9d112aed4f587`  
		Last Modified: Mon, 30 Mar 2026 17:53:20 GMT  
		Size: 342.7 KB (342686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3a4bec285c6587440428cb1ad29ee07985f6c41a3a3adfbb0d2098e4ddd482`  
		Last Modified: Mon, 30 Mar 2026 17:53:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0babd8cc4e1f6fe783d9e0c43db7f9c1757187eb93512e41c7ec195ec69a61e3`  
		Last Modified: Mon, 30 Mar 2026 17:53:18 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341ca9892da639a39553b836f563502b72451126d1775577413bed10230eb844`  
		Last Modified: Mon, 30 Mar 2026 17:53:18 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5a3857baa7451f83c08f6a2b224c3ddecf2acd525205b14f8fb4f7a03e8335`  
		Last Modified: Mon, 30 Mar 2026 17:53:32 GMT  
		Size: 224.8 MB (224815714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92db2531118ae12f9d711aa5864f36271bee6f5e3d5e3ae42cc7ae7fd03c2133`  
		Last Modified: Mon, 30 Mar 2026 17:53:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
