## `openjdk:23-ea-26-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:26c891c4d30f486257c0e0751663db3e7a3bba050bfc1c47fcbe34da4dfb8887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `openjdk:23-ea-26-jdk-windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull openjdk@sha256:ca54cc4155ca9758aa0b7636f7c54056346ddfe9ac3d65b1d7e3c107cb6604f3
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2319762437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f3e38e9ae473db8ebe57f692c091c62724bed1157ca0084ecdf1f1aaa0e75d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Mon, 10 Jun 2024 22:32:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 10 Jun 2024 22:32:58 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 10 Jun 2024 22:32:59 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 10 Jun 2024 22:33:05 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 10 Jun 2024 22:33:05 GMT
ENV JAVA_VERSION=23-ea+26
# Mon, 10 Jun 2024 22:33:06 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_windows-x64_bin.zip
# Mon, 10 Jun 2024 22:33:07 GMT
ENV JAVA_SHA256=79726b7c310903e3f9fa306110b1316629abf85403efeb1bb660d9fa7cff7a01
# Mon, 10 Jun 2024 22:33:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 10 Jun 2024 22:33:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9070f6f301cc5bbeef0d473a43166aace75951fd7e6dbc0aadbf63aa555c5af1`  
		Last Modified: Mon, 10 Jun 2024 22:33:39 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743e6d483a83e6b949d5f62b2bfca8315c79eee95c50044318a2ff6861a2020a`  
		Last Modified: Mon, 10 Jun 2024 22:33:40 GMT  
		Size: 349.9 KB (349886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27e7dbc6e0b681f1625eddb4a98e2fcad4f6ae3329bd0cb8152236c075d8f6e`  
		Last Modified: Mon, 10 Jun 2024 22:33:39 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16068647596bf2270a14ccfe556dd1b30a92c5a93972ee8e14b94e48d4449177`  
		Last Modified: Mon, 10 Jun 2024 22:33:39 GMT  
		Size: 334.7 KB (334658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bfeddc58b5166de801f9691b70872306844c82bc1d6157270cd32643579138`  
		Last Modified: Mon, 10 Jun 2024 22:33:38 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24210070fd732f40b6d6a514d0cc73186ce7cad578e6b4e7e32eee74703dc53e`  
		Last Modified: Mon, 10 Jun 2024 22:33:37 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1117bfe135b0b5dc03f355167bef5c34ab4d40a2b80e437465300f4e60cb319`  
		Last Modified: Mon, 10 Jun 2024 22:33:37 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1412d8a14ad7eab5260820f1909aca98bb4c1422e260121af2f7c60568147c66`  
		Last Modified: Mon, 10 Jun 2024 22:33:48 GMT  
		Size: 206.4 MB (206398733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18bfa9889b4a28db6dab893dbe663a76bd5c1a21ee3270a428ebecb87e2da54`  
		Last Modified: Mon, 10 Jun 2024 22:33:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-ea-26-jdk-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull openjdk@sha256:43b23ba5b2c065eae63c2e215d98071c04583243a6ea7f588bf869a194dc0ba0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2386965072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749ce69febb6d413bbcc6c264584d7f4498b3900d8045cbb5846c98cb1047c1f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Mon, 10 Jun 2024 22:32:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 10 Jun 2024 22:33:51 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 10 Jun 2024 22:33:51 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 10 Jun 2024 22:34:15 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 10 Jun 2024 22:34:16 GMT
ENV JAVA_VERSION=23-ea+26
# Mon, 10 Jun 2024 22:34:17 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_windows-x64_bin.zip
# Mon, 10 Jun 2024 22:34:17 GMT
ENV JAVA_SHA256=79726b7c310903e3f9fa306110b1316629abf85403efeb1bb660d9fa7cff7a01
# Mon, 10 Jun 2024 22:35:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 10 Jun 2024 22:35:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b038967c9be0cd8e8bf133c6a3ede7a43dee0b7acf37f55133c0ef8ba6c7f2`  
		Last Modified: Mon, 10 Jun 2024 22:35:11 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a28d8d505dbe681170d0ad1fc5c207a68785083f81329ccbf6fdeaa06bf75db`  
		Last Modified: Mon, 10 Jun 2024 22:35:11 GMT  
		Size: 486.9 KB (486872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c21c7e6772d1aee93a5eef5ce6426c95401cb332f69bfa84b63941d144dd66a`  
		Last Modified: Mon, 10 Jun 2024 22:35:11 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a0a649950860a84f16afb2505513e483a260ac3f23c95ba3b22ce90bf99721`  
		Last Modified: Mon, 10 Jun 2024 22:35:11 GMT  
		Size: 341.6 KB (341639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090c18be1d23b0036cfc062b3a1c4b44b19533a3c817f2b1ca3b8beab502d0d4`  
		Last Modified: Mon, 10 Jun 2024 22:35:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c666be1718fee22bb850ea033b8a61c3ec7a75f7e5203a70093b8106a6e9078c`  
		Last Modified: Mon, 10 Jun 2024 22:35:09 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acbb5dbcf811766c23fe3d435f506b5b22376e7500c48e35bbf3546f58d86d5`  
		Last Modified: Mon, 10 Jun 2024 22:35:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a911674aef2a452c8ed6dc48268a6ccdab08b5165ce243b8c768be454d31c9`  
		Last Modified: Mon, 10 Jun 2024 22:35:20 GMT  
		Size: 206.4 MB (206417313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793cdc6460bdf1a55ea24c2886ea9e7e2c5b2a94f800b53874bef64a29e9bbcd`  
		Last Modified: Mon, 10 Jun 2024 22:35:09 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
