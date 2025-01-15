## `openjdk:24-windowsservercore`

```console
$ docker pull openjdk@sha256:9618f6aba56a3fe68d61aa3d20e598fff1a1599d7b3aa36f077b1736648bf288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `openjdk:24-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull openjdk@sha256:d4396a28f5f5a651b3d96527d6a67f541389b1c55060b3550046613eb0ac6b8a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2463363931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7bce12caf6212d23e3e6fa6e0f0bd5de2ef311f99f4ac0c0cad00dd726f20e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Sat, 11 Jan 2025 02:28:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 11 Jan 2025 02:30:08 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 11 Jan 2025 02:30:09 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 11 Jan 2025 02:30:19 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 11 Jan 2025 02:30:19 GMT
ENV JAVA_VERSION=24-ea+31
# Sat, 11 Jan 2025 02:30:20 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_windows-x64_bin.zip
# Sat, 11 Jan 2025 02:30:21 GMT
ENV JAVA_SHA256=72536bad2fa20c7ead0367944940a684a359e43649870d3cdbccd46bcc3b4009
# Sat, 11 Jan 2025 02:30:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 11 Jan 2025 02:30:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Fri, 13 Dec 2024 16:30:53 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6826e4242dccb69f4f66c52ebcfac678148084cc598761df92f5caa23d3ddd`  
		Last Modified: Sat, 11 Jan 2025 02:30:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7d57025e062774dbdbef3b418cad5008941003bc4582c7f2f978f0255ca92f`  
		Last Modified: Wed, 15 Jan 2025 00:01:53 GMT  
		Size: 358.8 KB (358780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a87940ad07758709b4c01948f571dedfd2fd3929c5ff0197672b5c7c9db3c4`  
		Last Modified: Sat, 11 Jan 2025 02:30:59 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6c1b944e5e7244a0c4d50b26db3749794997570c5bab9a15de585286f07fef`  
		Last Modified: Sat, 11 Jan 2025 02:30:59 GMT  
		Size: 311.5 KB (311529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977775dc6904d5ca1fe308df2ce728d4d31f79724bc00fc89446840a00224eb6`  
		Last Modified: Sat, 11 Jan 2025 02:30:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117725a0a1361becee16986cf056cfb57ff14a9309e9fa3af19593f678eb61bd`  
		Last Modified: Sat, 11 Jan 2025 02:30:58 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bff709f1d17781e46b4e4de789ce9e83c843b13b95178511726db33b5db9f54`  
		Last Modified: Sat, 11 Jan 2025 02:30:58 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f180a8327165370749b1250c641e0c236b3e1872691f112d5efeb7f4077e2cb`  
		Last Modified: Sat, 11 Jan 2025 02:31:08 GMT  
		Size: 208.8 MB (208812158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f9940d020b06f681764baeb0cc314fce1bedab547639462366cd12fbc43aa1e`  
		Last Modified: Sat, 11 Jan 2025 02:30:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull openjdk@sha256:46d67e028f404e1dc14b07a2e407ad443ea999debc5ce890d7cc132d127fd17e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2223833235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd0a502861d950e691207cd91bb28057898e76c6af23a840d98cd495ad7fdce`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Sat, 11 Jan 2025 02:28:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 11 Jan 2025 02:30:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 11 Jan 2025 02:30:16 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 11 Jan 2025 02:30:24 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 11 Jan 2025 02:30:24 GMT
ENV JAVA_VERSION=24-ea+31
# Sat, 11 Jan 2025 02:30:25 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_windows-x64_bin.zip
# Sat, 11 Jan 2025 02:30:25 GMT
ENV JAVA_SHA256=72536bad2fa20c7ead0367944940a684a359e43649870d3cdbccd46bcc3b4009
# Sat, 11 Jan 2025 02:31:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 11 Jan 2025 02:31:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa1ab1f9e6015f1f3d4cf9ceb8ab36b4e66f9bde6e59f71864f7a3b4ba849d2`  
		Last Modified: Sat, 11 Jan 2025 02:31:10 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc824a354bed01646d52bc21c8fe8ea769d8e39d2a12783cacee90a7d6966d3`  
		Last Modified: Sat, 11 Jan 2025 02:31:10 GMT  
		Size: 474.7 KB (474680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7af8e7ef039e271c72a9fe624a3058d5104ee552ce5050ddf3b7173f159b494`  
		Last Modified: Sat, 11 Jan 2025 02:31:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a98d88693090f30ae38841239dde8ebfd0ed71dc9fc443db7fea538e967f904`  
		Last Modified: Sat, 11 Jan 2025 02:31:10 GMT  
		Size: 332.1 KB (332088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62417811268e68d04746d83e50f294f50a2151bd6f33a40ef30274491d9adc7`  
		Last Modified: Sat, 11 Jan 2025 02:31:09 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65881fce288c27946ae2eba9ac851e749c75fcc97f5905c5d1234af3bf0f83f`  
		Last Modified: Sat, 11 Jan 2025 02:31:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fd80144426ca739051785c58443eaa0fc44f0fccfdc10702f9e0d211816b23`  
		Last Modified: Sat, 11 Jan 2025 02:31:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a613d0a4fc5bbe30c1d18a39146ae95fe06b85f9a323428caaab3f49d01a74`  
		Last Modified: Sat, 11 Jan 2025 02:31:19 GMT  
		Size: 208.8 MB (208848482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9dba0000a2c04c4b45ed86f00865debafa4bd79a92f60eaaf4c7d53462b637a`  
		Last Modified: Sat, 11 Jan 2025 02:31:09 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
