## `openjdk:24-ea-34-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:9eb21de308378939fa30c78e57215832043e297dc1dafa5b342f47ab3bfff119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-ea-34-jdk-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:630e9f76dc1f26d4a93c615df19cecf72b3c62cfaed379a5df87a147e71c5c38
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709990799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c0bb491739b61b59778220cea3d906433d65d98229f616e4ff3c7125bbbb1d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Fri, 31 Jan 2025 22:29:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 22:29:31 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:29:31 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 31 Jan 2025 22:29:37 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:29:38 GMT
ENV JAVA_VERSION=24-ea+34
# Fri, 31 Jan 2025 22:29:39 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/34/GPL/openjdk-24-ea+34_windows-x64_bin.zip
# Fri, 31 Jan 2025 22:29:39 GMT
ENV JAVA_SHA256=190d1d3c9dc679675ebbe68fc9936e9f17471cd4c161f9f7a3fefc1750bd74d7
# Fri, 31 Jan 2025 22:29:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:29:57 GMT
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
	-	`sha256:0771ac81081ef90c3a9c07b205e3d5c2d57ab0e18f947196bab1251da098b2b9`  
		Last Modified: Fri, 31 Jan 2025 22:30:02 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3627ae475615e49d8d18cab82c9e8a8f7cb866f7b33857bcee8fef6878a182da`  
		Last Modified: Fri, 31 Jan 2025 22:30:01 GMT  
		Size: 385.6 KB (385600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb71d371d6b7e5eef4ff2b8e07f8560d0480391d9aca53433bebbade5289ea71`  
		Last Modified: Fri, 31 Jan 2025 22:30:01 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb0557d6717e22757bb3a3e2d0904b4b2515fe1a77ea0bdcbc14f41f71af55a`  
		Last Modified: Fri, 31 Jan 2025 22:30:01 GMT  
		Size: 373.8 KB (373810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb8298348de28330c9e14ea4171ad8e1a89b87cb577ca21fec611ea06413841`  
		Last Modified: Fri, 31 Jan 2025 22:30:00 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339cb8ca9a68e1070ca3f96422ad302c5d869ab936faed41b268be1b84bcc800`  
		Last Modified: Fri, 31 Jan 2025 22:30:00 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8768f16777ebf2a32a886bb9a41f85598c4b7e9461f719a91eb5bda552f23638`  
		Last Modified: Fri, 31 Jan 2025 22:30:00 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85b73e92287f547d208c387396050797de5200579da2a1b13e62f7c6f0d49e9`  
		Last Modified: Fri, 31 Jan 2025 22:30:13 GMT  
		Size: 208.9 MB (208946003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d985f7304e5e9657a4b1784b0de2100313cebde65206cb5a31656010514c1895`  
		Last Modified: Fri, 31 Jan 2025 22:30:00 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-34-jdk-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:88833fd2bf4266d843b0e7f00b4847ef7b0067c98bc661c9730cf70b0cb8f221
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2471953641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f105749930dce01afe32ee54bae3ad411f70e7160be99f9d539a2239fbd6508`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 31 Jan 2025 22:25:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 22:26:49 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:26:50 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 31 Jan 2025 22:27:02 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:27:03 GMT
ENV JAVA_VERSION=24-ea+34
# Fri, 31 Jan 2025 22:27:03 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/34/GPL/openjdk-24-ea+34_windows-x64_bin.zip
# Fri, 31 Jan 2025 22:27:04 GMT
ENV JAVA_SHA256=190d1d3c9dc679675ebbe68fc9936e9f17471cd4c161f9f7a3fefc1750bd74d7
# Fri, 31 Jan 2025 22:27:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:27:34 GMT
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
	-	`sha256:927ec26c28ffbd46c75794bcf1cf22be793b1286cb2c15c255510acf84a2858f`  
		Last Modified: Fri, 31 Jan 2025 22:27:38 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00eab96b983337150dd8439d62770b6424e5edb020a2bf9387679cc8ea2caac`  
		Last Modified: Fri, 31 Jan 2025 22:27:38 GMT  
		Size: 364.1 KB (364138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271a6a44b061ca38415e11fd67525c627f6ef45ea1b9d7a8f4667dfeade6320a`  
		Last Modified: Fri, 31 Jan 2025 22:27:38 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1dfd102690d31e5d020ab3c76967be783a987fe4a9ff59010ce53d8a88a0607`  
		Last Modified: Fri, 31 Jan 2025 22:27:38 GMT  
		Size: 312.1 KB (312073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66eea07614724c363d7c42452d42f6ba172899c83b2b2866992b08e7db758bd7`  
		Last Modified: Fri, 31 Jan 2025 22:27:37 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e58e82dcdaa5fcaf7fcb02d24041f9abe0f24ae8407d19e8862c6c6c0787c98`  
		Last Modified: Fri, 31 Jan 2025 22:27:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f258ef8257e204aaee0d4b06587178a10f16a31da814537dab6621b724d5b484`  
		Last Modified: Fri, 31 Jan 2025 22:27:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a472027080c975f5b2296b2171cb0458ebd28ee2359d250ce06972c5662ff818`  
		Last Modified: Fri, 31 Jan 2025 22:27:48 GMT  
		Size: 208.9 MB (208884473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb1f3f9048cc64047691823151050a6869211172a75db51f44ec1d3f145cd48`  
		Last Modified: Fri, 31 Jan 2025 22:27:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-34-jdk-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:949d6fcaf07b8b558d7bae163d2b21cbaa6ac3f84ccac083e232e64c9d25ac92
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2331788536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06f86c0eb243b22cb57dfd035748ca7768aaf1f34d047bd78e21941c208d519`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 31 Jan 2025 22:25:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 22:26:39 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:26:40 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 31 Jan 2025 22:26:48 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:26:49 GMT
ENV JAVA_VERSION=24-ea+34
# Fri, 31 Jan 2025 22:26:49 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/34/GPL/openjdk-24-ea+34_windows-x64_bin.zip
# Fri, 31 Jan 2025 22:26:50 GMT
ENV JAVA_SHA256=190d1d3c9dc679675ebbe68fc9936e9f17471cd4c161f9f7a3fefc1750bd74d7
# Fri, 31 Jan 2025 22:27:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 31 Jan 2025 22:27:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc7c733b89b7e736b0b5a266c1f99c8a7798d2d6edd325be22d8037144d5d64`  
		Last Modified: Fri, 31 Jan 2025 22:27:29 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6784abec728903a90226592058d6e3a953b7b04f5dddc4550f8c51000e1ac28f`  
		Last Modified: Fri, 31 Jan 2025 22:27:28 GMT  
		Size: 341.2 KB (341218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cbd6d16f0f895da13abd95db98cda229b101ce041bf5d6084f486584bc5be6c`  
		Last Modified: Fri, 31 Jan 2025 22:27:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498a3c7f8d58e7db125fe24adb1de59c43aee6039a482b6157c50e1b87bba24b`  
		Last Modified: Fri, 31 Jan 2025 22:27:28 GMT  
		Size: 331.9 KB (331923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc50fbd4c6344c112c5e713ae4b06eabb0fc429893d84620392fe76a23f28021`  
		Last Modified: Fri, 31 Jan 2025 22:27:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c64a82ccf0be890a984428f35deb743569e457266c1bdb1913a8ca9fc21327`  
		Last Modified: Fri, 31 Jan 2025 22:27:26 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d45e0af3e3f3b01f3bee821334928d7abaabc7072020cb4e745c1fbeee5759d`  
		Last Modified: Fri, 31 Jan 2025 22:27:26 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b62cade77897a0b07171c69803ec21bacc3c13a948cc0165c49c23b39dc725`  
		Last Modified: Fri, 31 Jan 2025 22:27:37 GMT  
		Size: 208.9 MB (208895437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95669b3f8c264b5f8fdeb40bff2167058a420ac5f9c45e4c652b0c8d5eb224fd`  
		Last Modified: Fri, 31 Jan 2025 22:27:26 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
