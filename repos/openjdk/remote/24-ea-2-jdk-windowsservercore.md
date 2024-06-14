## `openjdk:24-ea-2-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:4932ec48b6adbabf4a17358bad21830a03efd8b85bb41c610e6bb284895db09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `openjdk:24-ea-2-jdk-windowsservercore` - windows version 10.0.20348.2527; amd64

```console
$ docker pull openjdk@sha256:0f7c0ad5e220df7288ccc10d0746afe66973c689ba28e4e04711762a7aa0f1ed
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325395300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4393805f83c12f26bd1b9bc666728619e49395209c9602cc5ac68acc158945b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Fri, 14 Jun 2024 01:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jun 2024 01:07:56 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 14 Jun 2024 01:07:57 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 14 Jun 2024 01:08:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 14 Jun 2024 01:08:04 GMT
ENV JAVA_VERSION=24-ea+2
# Fri, 14 Jun 2024 01:08:04 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/2/GPL/openjdk-24-ea+2_windows-x64_bin.zip
# Fri, 14 Jun 2024 01:08:05 GMT
ENV JAVA_SHA256=2c752f59e33501f0541d669dc181c84fc2c5d736884e3b1ff58a74fb6412081b
# Fri, 14 Jun 2024 01:08:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 14 Jun 2024 01:08:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3323cbaa6ba00c41c1ed539baa55d4ff3f722aa092b2a99282554aebf60367`  
		Last Modified: Fri, 14 Jun 2024 01:08:31 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca97f0f1a012000f3b4bab4b0f998d4722c6ca25c02f41819dc3a6e226b792e`  
		Last Modified: Fri, 14 Jun 2024 01:08:32 GMT  
		Size: 349.1 KB (349130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce41999c69a792c4fdfc12275a857e2b8a8fdf9fc583f620921b9eed98ad234a`  
		Last Modified: Fri, 14 Jun 2024 01:08:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95beeb011bf3139f1fa2b8baa66dba305525c5d1beb36b3cafc36a29d997f7ae`  
		Last Modified: Fri, 14 Jun 2024 01:08:32 GMT  
		Size: 334.8 KB (334846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f78cfe39da74e03574045a4350a82e8aae731302aa99c9db7f00645b36d1321`  
		Last Modified: Fri, 14 Jun 2024 01:08:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092844099513078b1ca9a09d6f596b2c67abbd58faf1d370952d02df8f516bc2`  
		Last Modified: Fri, 14 Jun 2024 01:08:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d8ff861e8f7bfbeedfed37bcbe5b9b564a369d69df872f3d9ecf8d826a4b65`  
		Last Modified: Fri, 14 Jun 2024 01:08:30 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ee5fa20bce649b108aebae48cf6a907c3e93dfc18d926051499d5e275c03c5`  
		Last Modified: Fri, 14 Jun 2024 01:08:41 GMT  
		Size: 206.5 MB (206524915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004bcf84b90f1debb068ef89cf7066d17e45706ebcfe73f32aa3e4a87d8f9320`  
		Last Modified: Fri, 14 Jun 2024 01:08:29 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-2-jdk-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:aac5a172999ef5b62d92091b324a34b04cdce7efef56016fa2612857a32303c0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2428002171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461abe05513f960adeba3b4a8bf8979809f03a7ea4df6e0ca2df6c96f669f884`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Fri, 14 Jun 2024 01:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jun 2024 01:14:07 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 14 Jun 2024 01:14:08 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 14 Jun 2024 01:14:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 14 Jun 2024 01:14:26 GMT
ENV JAVA_VERSION=24-ea+2
# Fri, 14 Jun 2024 01:14:27 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/2/GPL/openjdk-24-ea+2_windows-x64_bin.zip
# Fri, 14 Jun 2024 01:14:28 GMT
ENV JAVA_SHA256=2c752f59e33501f0541d669dc181c84fc2c5d736884e3b1ff58a74fb6412081b
# Fri, 14 Jun 2024 01:15:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 14 Jun 2024 01:15:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee97bfb36e6b8b495f5d7140ee6d45366f3d42c627d16310db22731a42e8fe0`  
		Last Modified: Fri, 14 Jun 2024 01:15:12 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b509fd6e2ad5e4b013f8036d88f4bd256ab38cabda7a0d0037f5c23ef32c1b6`  
		Last Modified: Fri, 14 Jun 2024 01:15:13 GMT  
		Size: 471.9 KB (471878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb938c90ebde823428ba538613f3b3827009a761ab911194524240c5f1f8d432`  
		Last Modified: Fri, 14 Jun 2024 01:15:12 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a5878d628bba78aabb9a5234b6217bd701e3ef9e475988603b81a991483600`  
		Last Modified: Fri, 14 Jun 2024 01:15:13 GMT  
		Size: 319.1 KB (319144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b3535b0d52eb9d1067c247d4337a260c62a88c7306b7ce1103ee17969c97fa`  
		Last Modified: Fri, 14 Jun 2024 01:15:11 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52decf21fa68ecc024bcc2acc3202acc00c613cb8c0cd647c03b13b5c0cb7737`  
		Last Modified: Fri, 14 Jun 2024 01:15:10 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9725df9e89b226208cae8613c3548fb4a25fdf4c12c3e9d70c73e008430c0c`  
		Last Modified: Fri, 14 Jun 2024 01:15:11 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405222f72ace2e8a9486bcce7d760548e37860f705c010d766bfd321e392c7b9`  
		Last Modified: Fri, 14 Jun 2024 01:15:22 GMT  
		Size: 206.5 MB (206522215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72b2acdb0746c63e0933f541aaa4d2de58507aaf256b1367cdbc843fd532bd4`  
		Last Modified: Fri, 14 Jun 2024 01:15:10 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
