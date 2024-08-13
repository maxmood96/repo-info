## `openjdk:23-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:5be1324f4e919c88a0aac84d27f3ee2338f0c81149578cf8d992f0e8b15b698d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `openjdk:23-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull openjdk@sha256:edd86d0e7b1693f1060413d050c6e28e6a222600f286145c70355ecd8186f936
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348869833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb4d90a52e58f83029de0cfa10d1fc46d17109f05a92f0a637e22708404325e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Tue, 13 Aug 2024 20:10:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Aug 2024 20:10:46 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:10:46 GMT
ENV JAVA_HOME=C:\openjdk-23
# Tue, 13 Aug 2024 20:10:52 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:10:53 GMT
ENV JAVA_VERSION=23
# Tue, 13 Aug 2024 20:10:54 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_windows-x64_bin.zip
# Tue, 13 Aug 2024 20:10:54 GMT
ENV JAVA_SHA256=b18897bec6b1c6e0f639d95757eb0e3b0ec3d69720f6e4631874f2f9408075c5
# Tue, 13 Aug 2024 20:11:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:11:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc09bc75d43c40557b22c06f0797f0b469b59124226671e8464342862ffcfa16`  
		Last Modified: Tue, 13 Aug 2024 20:11:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fc8d20f0c792799b77e2395c660f2f548cb63d09b774f288d529b7120b9d46`  
		Last Modified: Tue, 13 Aug 2024 20:11:20 GMT  
		Size: 352.8 KB (352765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9c356654843ef09a161332cb9bc27274ec9adefe5507536c89c6bf73e46176`  
		Last Modified: Tue, 13 Aug 2024 20:11:20 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e7a4b35caa762efc0fc6096103d5eebcc5468d137259b7ad1d7f1783c2caa7`  
		Last Modified: Tue, 13 Aug 2024 20:11:20 GMT  
		Size: 334.5 KB (334515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451683ffe7e1a3ba0c8a58221021555f28cecfbed0b32828784f1c27915091f5`  
		Last Modified: Tue, 13 Aug 2024 20:11:18 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544217591296445b2ec212778acc0ad69493be69224f5f8573585ca1ee5b034a`  
		Last Modified: Tue, 13 Aug 2024 20:11:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f3d49d3ba66709e9ef33481c58bb94e1b3ae841f3d010e19e577e8e681a60f`  
		Last Modified: Tue, 13 Aug 2024 20:11:18 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5fec82d7a6a88bb50ee7a3dd8514b6017b1a91072e465824923ae23eb6aa91`  
		Last Modified: Tue, 13 Aug 2024 20:11:29 GMT  
		Size: 206.4 MB (206409867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfccad77c2dfd6e45ba7f99818bdc308e795b081d41f5178ad3f758d69334ac1`  
		Last Modified: Tue, 13 Aug 2024 20:11:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
