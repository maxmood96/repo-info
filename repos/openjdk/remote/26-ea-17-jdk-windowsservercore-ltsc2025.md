## `openjdk:26-ea-17-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:98f915d2e6fd8cac862cc9e2dd852c2f607c8493f9e5a0990cdf575c0e5b7863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `openjdk:26-ea-17-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull openjdk@sha256:fae012c81e329f7fd4eaf1ec6584ac039464e54b4a1084e5c65ec1665bba9653
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3793763073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d3bb0a0140eca3ead037e1ada6d72f28d43dfe61eda3d25df59d1865861a77`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Fri, 26 Sep 2025 22:01:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 22:01:43 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 26 Sep 2025 22:01:44 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 26 Sep 2025 22:01:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 26 Sep 2025 22:01:51 GMT
ENV JAVA_VERSION=26-ea+17
# Fri, 26 Sep 2025 22:01:51 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_windows-x64_bin.zip
# Fri, 26 Sep 2025 22:01:52 GMT
ENV JAVA_SHA256=5232e47e862086980b6e18c5b212648b57221ea3661f5e4a368a78a5a905f677
# Fri, 26 Sep 2025 22:02:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 26 Sep 2025 22:02:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3127d1dcaf57b855d2a18529f04f68465361ae6574e2c30cd69535c2d6dbfee5`  
		Last Modified: Fri, 26 Sep 2025 22:11:09 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010682b59ccea315f50fb62e715de595bcfbf51152b2c19874f3808853db6fae`  
		Last Modified: Fri, 26 Sep 2025 22:11:09 GMT  
		Size: 400.0 KB (400004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ed02dd38d9aa2bef1f1f39b76ebf71be7eb1e5b930c7568dc805d38e3b8166`  
		Last Modified: Fri, 26 Sep 2025 22:11:09 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414123a90d7ac6a66bf21a5f38348150671d28374f65167107c0328368ab1377`  
		Last Modified: Fri, 26 Sep 2025 22:11:10 GMT  
		Size: 373.0 KB (373043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a137c7b0fc399e9fc1e7e942ae9521ea9103cb57506b4f4b2c293863f0d8626`  
		Last Modified: Fri, 26 Sep 2025 22:11:06 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed28f8f00045324c2faa7cac89cca00b6a562cce4afa462600594f555fb4a225`  
		Last Modified: Fri, 26 Sep 2025 22:11:06 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1864e2ae49679fe665d74b1c8df50148a2fc073dddcf8115093648fbc20f3815`  
		Last Modified: Fri, 26 Sep 2025 22:11:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30c29adc8ae5e3f9d48cc4b9148e8cf8094b423035d35705022f1d2d12c48ba`  
		Last Modified: Fri, 26 Sep 2025 22:47:22 GMT  
		Size: 221.5 MB (221542474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35251f650a26c92eff3d57449a38cef0e64265be932fab6cb91194cc37e1f734`  
		Last Modified: Fri, 26 Sep 2025 22:11:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
