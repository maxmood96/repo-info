## `openjdk:26-ea-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:08a31ebbb07ee4cc9e8f25cd8b6403a3fc996e40063fcda653599c3b0dd01486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `openjdk:26-ea-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull openjdk@sha256:9e988a79a99f3252870b9c63baa9924c41eec43d55a1248322c09db69b2dd5d0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3442864647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307cd03d71c1e06c03ff9b93640baf308fd60c8c45254b78f5638c42f81b08bd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Mon, 10 Nov 2025 19:46:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 10 Nov 2025 19:46:53 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 10 Nov 2025 19:46:54 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 10 Nov 2025 19:47:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 10 Nov 2025 19:47:01 GMT
ENV JAVA_VERSION=26-ea+23
# Mon, 10 Nov 2025 19:47:02 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_windows-x64_bin.zip
# Mon, 10 Nov 2025 19:47:03 GMT
ENV JAVA_SHA256=41b399a48fae2944ecad52c8f821b2ce5195449fb10eb54a18542b013146fe59
# Mon, 10 Nov 2025 19:47:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 10 Nov 2025 19:47:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdb4f820c244e1b1c141421c0709d2cf6df07421598eaec46bdb8b9e00226ee`  
		Last Modified: Mon, 10 Nov 2025 19:57:03 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460a64ee5ef62bd9b22d8fb6c5482105f096f1c1d36142358244a7707ffebe90`  
		Last Modified: Mon, 10 Nov 2025 19:57:03 GMT  
		Size: 400.6 KB (400590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8391fe60309ecbb43583542b20f7c9a9b32a431dbef53ce37e9d2805d03ca03`  
		Last Modified: Mon, 10 Nov 2025 19:57:03 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee4182c4a92e8c8ba6c171e45877851a9b63ace11e31cd5aa4f777da768c621`  
		Last Modified: Mon, 10 Nov 2025 19:57:04 GMT  
		Size: 373.8 KB (373849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0e2857d3eb9d28ab47726fe2732d82146e8e244d110b3b45ee481e09037f7a`  
		Last Modified: Mon, 10 Nov 2025 19:57:04 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739742377babaa48557c238d5a56e9d9595aa38c22f96d6db686c9a74390f7fd`  
		Last Modified: Mon, 10 Nov 2025 19:57:04 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4de729099aa219a7c6ce8e28a538289bc1deaa8307e5553d4c77de6e08f5776`  
		Last Modified: Mon, 10 Nov 2025 19:57:04 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f740d3d4077b5e9c69d8c436fa3b9b288777a3f45331b83ba74e134c501b5fb2`  
		Last Modified: Mon, 10 Nov 2025 22:55:21 GMT  
		Size: 221.7 MB (221735329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4492ec4d1b3c162cfdd22e6b75252131fa34d0cb223d40ccc47d6a9193c41b6a`  
		Last Modified: Mon, 10 Nov 2025 19:57:04 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
