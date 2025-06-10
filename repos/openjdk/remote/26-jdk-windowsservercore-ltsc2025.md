## `openjdk:26-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:539d21ea7f5d40ce31052dc7bfa2df275947dd21d750d179304ddc6bf46b4fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `openjdk:26-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull openjdk@sha256:5521763734822f10b190894dd974669f97a4d650f34086f74bce1d2ac6306149
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3650525802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dd6712efb94e496831f3becea28a893367377e8456ea5e5c4d393b4de5cc36`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Mon, 09 Jun 2025 22:11:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Jun 2025 22:11:24 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 09 Jun 2025 22:11:25 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 09 Jun 2025 22:11:32 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 09 Jun 2025 22:11:33 GMT
ENV JAVA_VERSION=26-ea+1
# Mon, 09 Jun 2025 22:11:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/1/GPL/openjdk-26-ea+1_windows-x64_bin.zip
# Mon, 09 Jun 2025 22:11:36 GMT
ENV JAVA_SHA256=b10c3aefd0ca30a469837b9339e27e64df5e7a3fc0eee39f06c0f30b1ae2ad19
# Mon, 09 Jun 2025 22:11:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 09 Jun 2025 22:11:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a330689f3c596317e7c73fbf397338ddd30bbe089bec9a94719ef348dff32b6`  
		Last Modified: Mon, 09 Jun 2025 22:15:42 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e068e326baad8044927f1acbf847f5e81b310c6a784bafbc9df07858c56fdaf`  
		Last Modified: Mon, 09 Jun 2025 22:15:43 GMT  
		Size: 410.1 KB (410128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb6538bfaa3cab31dc9bd79a243d23eb5e2830ab1f10fc13df2efeb2e2198cc`  
		Last Modified: Mon, 09 Jun 2025 22:15:43 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45e07b5d271e64f6b0b32a0c6041684fae9637118bdc0df96fcd2c2d284c438`  
		Last Modified: Mon, 09 Jun 2025 22:15:43 GMT  
		Size: 390.2 KB (390157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c105eb03e1c7aa5b74af7407b083c1b9cb04adec27f725c9c5aa8a3cb46de0`  
		Last Modified: Mon, 09 Jun 2025 22:15:43 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7f3cbde378414ed642d0d1d839e132c17d10e9809769ac86a9eaf6e8c9de47`  
		Last Modified: Mon, 09 Jun 2025 22:15:43 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ed6ef84642312c10a7557a754ba1d2ab114bfabe498eb9470d0394b9a56591`  
		Last Modified: Mon, 09 Jun 2025 22:15:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbab1d6fea17876ce2eca678e48a8177f24de5f71fa6a221efe228bda27cecd`  
		Last Modified: Mon, 09 Jun 2025 23:07:21 GMT  
		Size: 219.0 MB (218951890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d73c3ee2877088361e0d64d710021322ff5ea98a9268875312649db401b905`  
		Last Modified: Mon, 09 Jun 2025 22:15:44 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
