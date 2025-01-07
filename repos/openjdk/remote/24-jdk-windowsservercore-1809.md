## `openjdk:24-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:334799f847a51d36b91cb3a88571933680b2f369d653e5291290a769f52d564a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `openjdk:24-jdk-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull openjdk@sha256:c9af43f0dc42a4d837bfcb12cb3b9b73846c7e4512717e074c50a41978102307
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2223856356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3acd5f27592028c0fab7408b3b912caf1ca5107aee0dcd461fb2cc66f73e424a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Mon, 06 Jan 2025 20:27:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 06 Jan 2025 20:28:13 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 06 Jan 2025 20:28:13 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 06 Jan 2025 20:28:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 06 Jan 2025 20:28:21 GMT
ENV JAVA_VERSION=24-ea+30
# Mon, 06 Jan 2025 20:28:22 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/30/GPL/openjdk-24-ea+30_windows-x64_bin.zip
# Mon, 06 Jan 2025 20:28:22 GMT
ENV JAVA_SHA256=d71df74a22fe12237dff1469d7adae9469331d0c68bbb3dc7145af17fd85cc76
# Mon, 06 Jan 2025 20:28:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 06 Jan 2025 20:28:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3cd554a84bfc6f86f4eef76ec05b1263552eaf041438095456c955308ef2fd`  
		Last Modified: Mon, 06 Jan 2025 20:29:04 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee3be2e21409d5ce3327950de33dc67479481ce9216e67b0470ebb8012b7b9d`  
		Last Modified: Mon, 06 Jan 2025 20:29:05 GMT  
		Size: 485.6 KB (485616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a7bd5257bf6226d588158326b2f2d376512767a9d7546f45083563f4ab07e2`  
		Last Modified: Mon, 06 Jan 2025 20:29:04 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c4a21a51c0840066a2ace5941fd9e09c37bbbd19228e81f2840225f3c3fb8c`  
		Last Modified: Mon, 06 Jan 2025 20:29:04 GMT  
		Size: 343.7 KB (343671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a408c8baef246a55c86f1cadd7bc8a9b4038d378a86e6a3242c8e3cf0683b470`  
		Last Modified: Mon, 06 Jan 2025 20:29:02 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba763abd015fe8169fb1b5c11c235fee06c0e6ecd41d193e16d748f9a4b53d5d`  
		Last Modified: Mon, 06 Jan 2025 20:29:02 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0979a2c0f9cc607391b8498df1ab50ec9961aa4e2d2475fc7c15967a92c8b6`  
		Last Modified: Mon, 06 Jan 2025 20:29:02 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea44eeb81648e174e77febc4377783413a873655d6fb995be69576e5368a108`  
		Size: 208.8 MB (208848928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc830c27ff9a94089936a8e885eabf7c7a5c85d2bbf1ca2b35427e3f0286c218`  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
