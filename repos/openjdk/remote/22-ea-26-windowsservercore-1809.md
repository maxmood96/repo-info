## `openjdk:22-ea-26-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:fed24b81b0d05d51c9bb6df3b20a4525f8728f80c7d87bdccfacbd08b52c3ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `openjdk:22-ea-26-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull openjdk@sha256:30d2c1468ac3decafb435ed03f782e14619bd20ab55eb2bce4fe693ac57d312a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2258255970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b5de519835d38960ec20450da928fa7e332bc263e227518b796568771fff29`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 05:21:26 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 16 Nov 2023 05:21:27 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 16 Nov 2023 05:22:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 01 Dec 2023 20:16:56 GMT
ENV JAVA_VERSION=22-ea+26
# Fri, 01 Dec 2023 20:16:57 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/26/GPL/openjdk-22-ea+26_windows-x64_bin.zip
# Fri, 01 Dec 2023 20:16:58 GMT
ENV JAVA_SHA256=cf9f95a06a4421a585db7dd80986077b363fab40bf4da90e5599ac03dc15664d
# Fri, 01 Dec 2023 20:18:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 01 Dec 2023 20:18:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93b4cb5d6725beac934401f77fbf989141c12afa232cff1f25429b1a301ba73`  
		Last Modified: Thu, 16 Nov 2023 05:26:50 GMT  
		Size: 442.0 KB (441969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22088bf48f3bbce80960887fe94d86c11b50b864e902347298416ae9c621501`  
		Last Modified: Thu, 16 Nov 2023 05:26:50 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8f6249f95be0911abdfd12a1f9bc8f3dc024f415c40647b843b72d714e2530`  
		Last Modified: Thu, 16 Nov 2023 05:26:50 GMT  
		Size: 257.3 KB (257301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefff0e71114aa220394ab23af1a154fe23d8037a7f8feb75001a16056dd7819`  
		Last Modified: Fri, 01 Dec 2023 20:21:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37f8548020910d38e203d88bec9bd3d26866c7d65c847934c8692168c501c29`  
		Last Modified: Fri, 01 Dec 2023 20:21:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2110751cfa1717ad0dd2b34bc2b9ce2324a9284d341add67856cfa738017d081`  
		Last Modified: Fri, 01 Dec 2023 20:21:12 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c030a03a38746de5cb7c67c31fc0094e7f9156b78293c77b5744f86137722cef`  
		Last Modified: Fri, 01 Dec 2023 20:21:32 GMT  
		Size: 200.1 MB (200117058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a85a4381564769b044f8bbbf78877ba4f35a6406e44c1b969f470369d54a2ea`  
		Last Modified: Fri, 01 Dec 2023 20:21:12 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
