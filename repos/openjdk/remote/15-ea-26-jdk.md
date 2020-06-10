## `openjdk:15-ea-26-jdk`

```console
$ docker pull openjdk@sha256:2a3e583c5578116bf5c6bab80f679e76707903e943ed45bdc2e09ca65e9fa23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64
	-	windows version 10.0.14393.3750; amd64

### `openjdk:15-ea-26-jdk` - windows version 10.0.17763.1282; amd64

```console
$ docker pull openjdk@sha256:41605e50abe6f9d174ce45a740969abe8b6c4035154ec9e7a7e2eee8af2b717c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2490184829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb6d0fd52e634179880005a08edfc793c5324056d076ac88a7ffcfb66da8d8a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2020 22:34:11 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Tue, 09 Jun 2020 22:34:12 GMT
ENV JAVA_HOME=C:\openjdk-15
# Tue, 09 Jun 2020 22:34:39 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Tue, 09 Jun 2020 22:34:40 GMT
ENV JAVA_VERSION=15-ea+26
# Tue, 09 Jun 2020 22:34:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/26/GPL/openjdk-15-ea+26_windows-x64_bin.zip
# Tue, 09 Jun 2020 22:34:41 GMT
ENV JAVA_SHA256=4c79cbb0dfd0dc0ef355e76433e42acde900e679016b7c145757e3a59036f0c4
# Tue, 09 Jun 2020 22:36:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 09 Jun 2020 22:36:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f841c6a0c622cd36b5b2688011a224ac3e8e96273758f4a2804f2f3f099f267d`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d8ec06304524cdb2b900879af7ed2db71d5e36e5f2306b46859250255390d`  
		Last Modified: Tue, 09 Jun 2020 23:17:51 GMT  
		Size: 4.8 MB (4765053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e91effeb439b76990fcc94732e86884df9c268d3125e7baeda527ddb3bb6d5`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d559d86d0b9a731bed7f5c7bfd949bba5687f2ad8da359606bfcb75a14161a`  
		Last Modified: Tue, 09 Jun 2020 23:17:49 GMT  
		Size: 289.8 KB (289776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1716886ba7cda4e6febc17ca652ea8b67b4caccbe7aa3c35df5d5fa8c807d8`  
		Last Modified: Tue, 09 Jun 2020 23:17:47 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c6927985d7bf02fdac5ba4dbbde84010390f1a3b6a19cc3dc3041a4d218c2f`  
		Last Modified: Tue, 09 Jun 2020 23:17:47 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507e86601a19958bf9bc69c78399ae1918a258efec673a0d1eeb69d82826400a`  
		Last Modified: Tue, 09 Jun 2020 23:17:47 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c335f52636f9212e8d3ac3ed17b9f4288ccef3af1e5930e2f213fb316bbb8a`  
		Last Modified: Tue, 09 Jun 2020 23:18:08 GMT  
		Size: 191.2 MB (191208915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160b0e02c0e64af740a07c91438d58b53aa879ec0668554b23049df9d533e594`  
		Last Modified: Tue, 09 Jun 2020 23:17:47 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:15-ea-26-jdk` - windows version 10.0.14393.3750; amd64

```console
$ docker pull openjdk@sha256:c93595acfeaad264b08d1e7b7c5babd45b5f2093ee074ce80a61b3890320faad
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5941049630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdfb635a1125e329460ed0946cc0eec64894c156c04658e72767f0e310ed975`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 09 Jun 2020 22:36:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2020 22:38:24 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Tue, 09 Jun 2020 22:38:26 GMT
ENV JAVA_HOME=C:\openjdk-15
# Tue, 09 Jun 2020 22:39:49 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Tue, 09 Jun 2020 22:39:50 GMT
ENV JAVA_VERSION=15-ea+26
# Tue, 09 Jun 2020 22:39:52 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/26/GPL/openjdk-15-ea+26_windows-x64_bin.zip
# Tue, 09 Jun 2020 22:39:53 GMT
ENV JAVA_SHA256=4c79cbb0dfd0dc0ef355e76433e42acde900e679016b7c145757e3a59036f0c4
# Tue, 09 Jun 2020 22:42:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 09 Jun 2020 22:42:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c938241e0507e1ada5f864325483d86fd08533a5a31e7cb6ec1357db9891b245`  
		Last Modified: Tue, 09 Jun 2020 23:18:33 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20399ac1a4e75ca1edbca4b2438a810ea66dbe6bdd128414ab987881b5ed641`  
		Last Modified: Tue, 09 Jun 2020 23:18:34 GMT  
		Size: 5.4 MB (5393368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e109766083929743d0ebae21d2c4462a8a05288902a46c372f19b156e917499b`  
		Last Modified: Tue, 09 Jun 2020 23:18:31 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad18636634fe84f93305aad5666d54f223ccc25d87a66f0d2093b0f233acd2d`  
		Last Modified: Tue, 09 Jun 2020 23:18:32 GMT  
		Size: 5.4 MB (5367532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9e5db884189ba29169fc030fadceaa420ee324120ced6cbc27f28197fc3165`  
		Last Modified: Tue, 09 Jun 2020 23:18:28 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063aabb23ac9a445e274d17cd5f1442f06a3940f2287bc7cf464a9b2d7512347`  
		Last Modified: Tue, 09 Jun 2020 23:18:28 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089c051a2f4f0cfab918ba62adb2fbade9343a30285e3eb386c37c1e6879ea58`  
		Last Modified: Tue, 09 Jun 2020 23:18:28 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbd342f4401db42fdc985e74d1267e8279ed033a582bbe35b8648529f6d3e45`  
		Last Modified: Tue, 09 Jun 2020 23:18:50 GMT  
		Size: 196.3 MB (196284237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6133aa779e12a4533111a7973417dd46a5c53bf990cd4266cb91b02109d6186b`  
		Last Modified: Tue, 09 Jun 2020 23:18:28 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
