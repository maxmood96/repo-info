## `openjdk:26-ea-18-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:156e38463db1fda815550be0bf52517c979243fd5a35f5465c03c63afd57acf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `openjdk:26-ea-18-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull openjdk@sha256:a5e9ed8a0a098616563febbe215c43c2d7fb55cf510a59602f8ef3103da94e95
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3793750676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4844650a7619930493fdff12ba8abaa1438f709a0a9367f73fad2567943ed196`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Mon, 06 Oct 2025 21:04:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 06 Oct 2025 21:05:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 06 Oct 2025 21:05:12 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 06 Oct 2025 21:05:20 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 06 Oct 2025 21:05:21 GMT
ENV JAVA_VERSION=26-ea+18
# Mon, 06 Oct 2025 21:05:22 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_windows-x64_bin.zip
# Mon, 06 Oct 2025 21:05:24 GMT
ENV JAVA_SHA256=463cf324498dd66ed66418be8d8e730b4ee17b323f86d4df926264b071118dbd
# Mon, 06 Oct 2025 21:05:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 06 Oct 2025 21:05:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd62238dc0a32b22c064cf7377f6418f0f968002a2b0aebe60ad115b39a97929`  
		Last Modified: Mon, 06 Oct 2025 21:23:04 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e9360c86ff02fb586cdd821499592b9e5c1a0488ed3ff8776035841f0e0162`  
		Last Modified: Mon, 06 Oct 2025 21:23:04 GMT  
		Size: 380.7 KB (380730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9887e1fc2b513819f205fde643e556ccc257adbff77b591acb53fbd33810f38d`  
		Last Modified: Mon, 06 Oct 2025 21:23:04 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f18dc99f35c5ba39c5a8a1ec1699d6471bc34792f39f35240b625acaf4a3d9`  
		Last Modified: Mon, 06 Oct 2025 21:23:04 GMT  
		Size: 354.6 KB (354580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d776ba72542f22e44781d997e96b704228c8d8f9e8ea0dc077e8c4f54dbaf79d`  
		Last Modified: Mon, 06 Oct 2025 21:23:04 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165e52f0a3a2461c3e0dab765a8e3a0ab093ee9c6f3c7076e318d8070a33fbb0`  
		Last Modified: Mon, 06 Oct 2025 21:23:04 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5990bab7d8d4ebaf5e5f0d7d565a836906d22aec31d27e56c4aabaa7197776f8`  
		Last Modified: Mon, 06 Oct 2025 21:23:04 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931774dd4f3548133b4564c1b9afa62f035b2a9104be059faf40f03bf306bc82`  
		Last Modified: Mon, 06 Oct 2025 22:13:25 GMT  
		Size: 221.6 MB (221567774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c038761fbdfc3572a81b30781fd36a66ebb019e5018e11920565beba16ce4b`  
		Last Modified: Mon, 06 Oct 2025 21:23:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
