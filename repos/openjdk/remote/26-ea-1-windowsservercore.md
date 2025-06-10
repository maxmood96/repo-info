## `openjdk:26-ea-1-windowsservercore`

```console
$ docker pull openjdk@sha256:f0b3fdfe635d1c0fb6d5ec7daa6145380510c0396f71b6c0554c9db724d21a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `openjdk:26-ea-1-windowsservercore` - windows version 10.0.26100.4061; amd64

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

### `openjdk:26-ea-1-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull openjdk@sha256:3dd2444adb03e3809d284fbacd6565c15ebd82eb9924c94356dc262c8f389763
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2493244524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cd83c9e824f33d3794c5ca95e92240d12e1b012eefddf19b288cc96ff1a811`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Mon, 09 Jun 2025 22:06:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Jun 2025 22:07:10 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 09 Jun 2025 22:07:11 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 09 Jun 2025 22:07:19 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 09 Jun 2025 22:07:19 GMT
ENV JAVA_VERSION=26-ea+1
# Mon, 09 Jun 2025 22:07:20 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/1/GPL/openjdk-26-ea+1_windows-x64_bin.zip
# Mon, 09 Jun 2025 22:07:21 GMT
ENV JAVA_SHA256=b10c3aefd0ca30a469837b9339e27e64df5e7a3fc0eee39f06c0f30b1ae2ad19
# Mon, 09 Jun 2025 22:07:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 09 Jun 2025 22:07:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634116ede25233ac623f5f542b6e347835e46ca28d89e89db884169bd055a86f`  
		Last Modified: Mon, 09 Jun 2025 22:08:27 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fcf56ac8472a1062cb055d7e790f75646619b4a1161c4db93bf492ecabb7799`  
		Last Modified: Mon, 09 Jun 2025 22:08:28 GMT  
		Size: 359.7 KB (359656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e736f7fd4b3842186ef37180da4b2b266c779b2a2ed8231483a434a39fdcea0a`  
		Last Modified: Mon, 09 Jun 2025 22:08:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f705db8ad62e2e1b4b1effd1c8a5b1132f6a7a4b7712c815c77df8ba3cec848`  
		Last Modified: Mon, 09 Jun 2025 22:08:29 GMT  
		Size: 347.2 KB (347211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d1bbb15000a500e997deddf8e8e1f5e24651398459e20d1f6ab1e94ff5ab68`  
		Last Modified: Mon, 09 Jun 2025 22:08:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d164a146912be63115021ad0b9e841457d32fe39b91c79caa702bc4a1a5c4881`  
		Last Modified: Mon, 09 Jun 2025 22:08:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbd365fdfde92fd825b97830b102c302bc52aa558ec4164d570d36004e75041`  
		Last Modified: Mon, 09 Jun 2025 22:08:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0a724bf78826787d693740abe218c59e50079296d8dd9a68d49f26d9041ba0`  
		Last Modified: Mon, 09 Jun 2025 22:10:30 GMT  
		Size: 218.9 MB (218901774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f7438d3972de47d6c3d1916f35fefedc19342538b0029bcc8ee607af48ef3a`  
		Last Modified: Mon, 09 Jun 2025 22:08:29 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
