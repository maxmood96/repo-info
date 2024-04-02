## `openjdk:23-windowsservercore`

```console
$ docker pull openjdk@sha256:4799fcb8ff143b5322ae9c2db8969a1733f87d8186baec297f7ec1413715d235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `openjdk:23-windowsservercore` - windows version 10.0.20348.2340; amd64

```console
$ docker pull openjdk@sha256:5d6fbd970dc5523bc27b918939468f12658d1deae6fb775f6cc69adaca8fb19a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2163967307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f79235e5256d1eae3dedbcfee3268c1d2eefbfb6b797474e5a550d90af35998`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Mon, 01 Apr 2024 23:49:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 01 Apr 2024 23:50:08 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 01 Apr 2024 23:50:09 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 01 Apr 2024 23:50:15 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 01 Apr 2024 23:50:15 GMT
ENV JAVA_VERSION=23-ea+16
# Mon, 01 Apr 2024 23:50:16 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/16/GPL/openjdk-23-ea+16_windows-x64_bin.zip
# Mon, 01 Apr 2024 23:50:17 GMT
ENV JAVA_SHA256=d8f0d3c652a3ea74356d51353fc92684c73b07dba66500430adaec9353a30266
# Mon, 01 Apr 2024 23:50:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 01 Apr 2024 23:50:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2503f7ecc2b5456184710df9a0479e9cea0e911963195b39d2026d28ccfa1810`  
		Last Modified: Mon, 01 Apr 2024 23:50:53 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59841f58cdc97ac6439ba48596ec97290c188d22991a04dd127fcd3999b1c87b`  
		Last Modified: Mon, 01 Apr 2024 23:50:53 GMT  
		Size: 499.2 KB (499229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09536f55b7bdcb7bdf02b283349038213e4495b19097b6feff8523ff464f317a`  
		Last Modified: Mon, 01 Apr 2024 23:50:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b99348680dcd2bfa3838ed265eb00bfb5a5d6b6190609c8549e95dfbda9f01c`  
		Last Modified: Mon, 01 Apr 2024 23:50:53 GMT  
		Size: 347.0 KB (346983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15b657b4c400b15e277baa77510c6f1afecd331b5a0ccf3242c23162c1931a8`  
		Last Modified: Mon, 01 Apr 2024 23:50:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8099defedec4760cb0848b6f487de60ef58944028804c0d0dc3e1cd11d367c07`  
		Last Modified: Mon, 01 Apr 2024 23:50:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f8fc14c4061d90e5a0161671195f4d10eae31f2383f23b7845acfe9010e6b4`  
		Last Modified: Mon, 01 Apr 2024 23:50:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafc8fadd392d6a7ad5135999f440a56731b1b09ce09f6b4a649d6a197f991b8`  
		Last Modified: Mon, 01 Apr 2024 23:51:01 GMT  
		Size: 205.7 MB (205654334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88342fed94360e43d8cdfc6b6fb64b7c195eb067a3bdb355f480847a5617db95`  
		Last Modified: Mon, 01 Apr 2024 23:50:50 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull openjdk@sha256:f8a070132c577f1da9466c02116eab17a6f7e01a150c5110990acd1aa2cc7872
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2331585899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5a27d5fe95b84c0b1634ab41e73d22e8bac6d47c9420a9822aa51deb46f707`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Mon, 01 Apr 2024 23:49:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 01 Apr 2024 23:51:49 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 01 Apr 2024 23:51:50 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 01 Apr 2024 23:52:15 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 01 Apr 2024 23:52:16 GMT
ENV JAVA_VERSION=23-ea+16
# Mon, 01 Apr 2024 23:52:16 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/16/GPL/openjdk-23-ea+16_windows-x64_bin.zip
# Mon, 01 Apr 2024 23:52:17 GMT
ENV JAVA_SHA256=d8f0d3c652a3ea74356d51353fc92684c73b07dba66500430adaec9353a30266
# Mon, 01 Apr 2024 23:53:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 01 Apr 2024 23:53:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d6ba42d24f660142d119af8afe7671f1bda7443560d3b4e21ef8c4d9ae5abd`  
		Last Modified: Mon, 01 Apr 2024 23:53:18 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6499f3691ebedaed539e4b5a88c36ee52415ad9ba2a311d445213a5e2f69b221`  
		Last Modified: Mon, 01 Apr 2024 23:53:18 GMT  
		Size: 487.0 KB (487025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25e2eb61e5219bbc3f379f15b9d69b0051d82c131bb6fb457a59cbdba1582f6`  
		Last Modified: Mon, 01 Apr 2024 23:53:18 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224219d9e4deb8ffb675e1f8c4fd21b1f5a88eea3c838d81c2a0c127f24cf399`  
		Last Modified: Mon, 01 Apr 2024 23:53:18 GMT  
		Size: 339.2 KB (339247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab2aa3d6d6a2720b096709155caf5a3b8c9c9e359e7a17591980c0152bddb8d`  
		Last Modified: Mon, 01 Apr 2024 23:53:16 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55a1625676f74ba3f582d144b190dd03630a436dce1fdaa21bab1593975b0e9`  
		Last Modified: Mon, 01 Apr 2024 23:53:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08392bc9f673313bdedc20ef4547c5c7c172286f8197dc1ebee2000e522424f5`  
		Last Modified: Mon, 01 Apr 2024 23:53:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a50dae9c827cc32128c32844e144290fc82a878875870eead0df9b3c722dfe`  
		Last Modified: Mon, 01 Apr 2024 23:53:27 GMT  
		Size: 205.7 MB (205651860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803460924a372a273cd6d7007444955e74dfac955e709b23b776f33dabec9a11`  
		Last Modified: Mon, 01 Apr 2024 23:53:16 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
