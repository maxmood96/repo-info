## `openjdk:27-ea-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:b58e3d47cc31f8c737f7e79efdabb6ed293476e7f2e1f4bfdc9c284bf6e82d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `openjdk:27-ea-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:abcb36b51d04b6571e9c56bfa42c5e4594f5f5a770ff5fbfc3bc10f55fdb6d30
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1721044983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d02002222aa11bed971aa6b711f9fe66b1e736021d0df5887a9668eeab2a6af`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 20 Jan 2026 18:51:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 20 Jan 2026 18:51:59 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:52:00 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 20 Jan 2026 18:52:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:52:07 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:52:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_windows-x64_bin.zip
# Tue, 20 Jan 2026 18:52:09 GMT
ENV JAVA_SHA256=350ca51cd4321274f6557de42448fd4fc6e845cfe0695800868857f13f89a2fc
# Tue, 20 Jan 2026 18:52:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 20 Jan 2026 18:52:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72e4b6e32077245586401d96dcbe5dfbfc76b2346166f48cdcfa0df93664650`  
		Last Modified: Tue, 20 Jan 2026 18:52:45 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662149f580d6da5f5f5954a737745aa3ec95b0e3b53799353b7da0257fd4a467`  
		Last Modified: Wed, 21 Jan 2026 06:24:38 GMT  
		Size: 403.4 KB (403418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46759ad4730fb651350be3a6af1de57ca13252b75fb154da903a6887b4a44ff`  
		Last Modified: Tue, 20 Jan 2026 21:05:30 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843be8db1e5bd4fba522492479b13fb0d3a1fd4bdabd1dea8d4c85ce8481c74e`  
		Last Modified: Tue, 20 Jan 2026 18:52:45 GMT  
		Size: 388.6 KB (388563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a2ea9fbd7e89bcdafe59e0fea26fec21cd3b2776079541fc936fa20a89a547`  
		Last Modified: Tue, 20 Jan 2026 21:05:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d009c75f850597872b10e10fa558a19241c9906960ee9d46b8761280f0c82f83`  
		Last Modified: Tue, 20 Jan 2026 19:26:24 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffde2380cd4e2a2a84fed9cab589e7ff1aef81e6b2643b5e9ff3988ad65f20b`  
		Last Modified: Tue, 20 Jan 2026 19:26:24 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465155860de126dae51438501c5c5846510546dd52a805ca574cbcc72c6d48c2`  
		Last Modified: Tue, 20 Jan 2026 18:53:00 GMT  
		Size: 224.5 MB (224484872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e494abfcc7bbb7bc54757d0f4b6c94dbe340549658e352c24a3425cea7e8aa24`  
		Last Modified: Tue, 20 Jan 2026 18:52:43 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
