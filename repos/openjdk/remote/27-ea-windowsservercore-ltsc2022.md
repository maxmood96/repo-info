## `openjdk:27-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:ea0d459cf60534aaa66ea242527d7690f9f9fe35aaf9b2ab8aac44c5e936433b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `openjdk:27-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull openjdk@sha256:721eb4c68c9f2881a4769a43b46e22793b985a75b2ad49705f83e44106b506ba
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346696741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c064d4591f4dd3c672ac4bd02a19cc853934c7bc4d6258d1aaab6dcf4398efa2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 09 Jun 2026 20:04:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 20:06:03 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 09 Jun 2026 20:06:03 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 09 Jun 2026 20:06:09 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 09 Jun 2026 20:06:10 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 20:06:10 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_windows-x64_bin.zip
# Tue, 09 Jun 2026 20:06:10 GMT
ENV JAVA_SHA256=ca4af1429ae7dc73528c0743f3134fe111133e114e23908c3e729538c6e203a3
# Tue, 09 Jun 2026 20:06:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 09 Jun 2026 20:06:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06003085a5cb10fa957348da210adaa29a25a8423f2edbf908ff113ffb6a03e7`  
		Last Modified: Tue, 09 Jun 2026 20:06:51 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb64640ee7a24a5651d6df4fffc79ca966c011be96b40faaadcf0fb1a55b86f4`  
		Last Modified: Tue, 09 Jun 2026 20:06:52 GMT  
		Size: 505.1 KB (505106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a58cc533ffb1221e81644386835ffd1b2d512d3cfada33a959475873eb95756`  
		Last Modified: Tue, 09 Jun 2026 20:06:51 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44b868269b275469604553ba32f6dcbccafb8eb30ec14c96dea741d9a88a945`  
		Last Modified: Tue, 09 Jun 2026 20:06:51 GMT  
		Size: 314.5 KB (314515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f35b1519266bd789aa1aabb3d41809a24c07e2cbb4445ec191cb5ac135a1452`  
		Last Modified: Tue, 09 Jun 2026 20:06:49 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e6903b9d52183c41e62e71158c6c3991ff1e890a191802e3c830859f68be3c`  
		Last Modified: Tue, 09 Jun 2026 20:06:49 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6c6ec188eca5301634445319e4abfe4e92e6d171c152cf8cdcfc56fc6907fa`  
		Last Modified: Tue, 09 Jun 2026 20:06:49 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7d3b517efce28671fd19de3e95ce038d769cd94a51d68266eea367e524ba42`  
		Last Modified: Tue, 09 Jun 2026 20:07:04 GMT  
		Size: 223.4 MB (223448688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f7b0c4e45587cd91e85dfcdd7edb86d12b35ca296eee4779834eb02cadf62f`  
		Last Modified: Tue, 09 Jun 2026 20:06:49 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
