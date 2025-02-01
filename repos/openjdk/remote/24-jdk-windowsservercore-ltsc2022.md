## `openjdk:24-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:443587e0cd0ec23581590f23b8bea35a01f4113f1c2d86f0fd4f6b5083e88581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `openjdk:24-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

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
