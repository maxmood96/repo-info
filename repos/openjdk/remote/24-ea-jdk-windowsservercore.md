## `openjdk:24-ea-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:b8481711db1c541c4b4d40465d811dba5568ae72b3dd1f2c35271c6bf3ce6d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `openjdk:24-ea-jdk-windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull openjdk@sha256:3a5080c38ac9e0599bce23d085496eb02c6c3b50db56253d4a0ada8b385d843e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2319808765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03b2a76b124376278ae4aa49bc4a283d4e5285cae19240ef8ab78705b6683ca`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 12 Jun 2024 00:55:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 00:56:35 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 12 Jun 2024 00:56:35 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 12 Jun 2024 00:56:42 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 12 Jun 2024 00:56:43 GMT
ENV JAVA_VERSION=24-ea+1
# Wed, 12 Jun 2024 00:56:44 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_windows-x64_bin.zip
# Wed, 12 Jun 2024 00:56:44 GMT
ENV JAVA_SHA256=84640da466dc6c7af5dbd523e321f5cfef6b81a434c1558b43633e7485da95f7
# Wed, 12 Jun 2024 00:57:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 12 Jun 2024 00:57:16 GMT
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
	-	`sha256:ab3feee2e21f945ab94c394b15e55b3c8302c73e23150aa82336a4ecde58f0d1`  
		Last Modified: Wed, 12 Jun 2024 00:57:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac3a0953712939d060064a1d93128c96bec7f064e7d7fd869359b4d8bfc29ed`  
		Last Modified: Wed, 12 Jun 2024 00:57:20 GMT  
		Size: 361.2 KB (361198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bafe8ccd74d785749020fe4a9e2eba807d34ec9251788c042e077925b61b8c`  
		Last Modified: Wed, 12 Jun 2024 00:57:20 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4e5d218afeb0dcb693a60a88ec6b08b8defcd766194e547bc928e207163cec`  
		Last Modified: Wed, 12 Jun 2024 00:57:20 GMT  
		Size: 311.9 KB (311905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5db43261dbf0a49e8a4e59f9548cee3f282e2c04ffb475e99115cf8f8bce2a7`  
		Last Modified: Wed, 12 Jun 2024 00:57:19 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859bad248847cc75e6ba2680e280225dad33e59542898013fa70124e278665dd`  
		Last Modified: Wed, 12 Jun 2024 00:57:19 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0961c05671b0ad85921dd84af1aef12dfe66ad579f30dd6e751e098443fc62d8`  
		Last Modified: Wed, 12 Jun 2024 00:57:19 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4cc66954fc8ff592b7880b97a1675dd987fbee2de3836b7ad2af2ba92fc0e5`  
		Last Modified: Wed, 12 Jun 2024 00:57:30 GMT  
		Size: 206.5 MB (206456430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f45cd4ab853a6c899fefb45f1261180a6a0b003fe2b511eecbf2204870858e`  
		Last Modified: Wed, 12 Jun 2024 00:57:19 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-jdk-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull openjdk@sha256:1a4d71b68604a6d5b8416d90a27d0b2e8ce9fc849eeaaadcb49b734bf2ac2bf0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2387072953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1de2915cd920aec7d955890095a7f9f0763d465b33f59d0804bef1ec6b71040`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 12 Jun 2024 00:54:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 00:56:54 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 12 Jun 2024 00:56:55 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 12 Jun 2024 00:57:19 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 12 Jun 2024 00:57:20 GMT
ENV JAVA_VERSION=24-ea+1
# Wed, 12 Jun 2024 00:57:20 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_windows-x64_bin.zip
# Wed, 12 Jun 2024 00:57:21 GMT
ENV JAVA_SHA256=84640da466dc6c7af5dbd523e321f5cfef6b81a434c1558b43633e7485da95f7
# Wed, 12 Jun 2024 00:58:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 12 Jun 2024 00:58:15 GMT
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
	-	`sha256:aca88dbf7eb4eb7959a590646ceffa7433d7a8f859e83a44b4334f7d09c76022`  
		Last Modified: Wed, 12 Jun 2024 00:58:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0a58ef1c4204fbd3888539a4ad31f9e342567a7540cd7bb18e662ee6f0487e`  
		Last Modified: Wed, 12 Jun 2024 00:58:18 GMT  
		Size: 499.4 KB (499430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4738ed9c26895037bb496954dd5ef5013617d00c749d4fa6cd5cc90a7507576`  
		Last Modified: Wed, 12 Jun 2024 00:58:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40f23f225087ba65983902a4b5e375adf8d3868db8bf9cb31481c6ee02180b7`  
		Last Modified: Wed, 12 Jun 2024 00:58:18 GMT  
		Size: 353.6 KB (353568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be280a3bb34e43138e099b28c5779e3c2fad3c9d99fa037930e8445f53fbd8`  
		Last Modified: Wed, 12 Jun 2024 00:58:17 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc08bd12867eb385bdc1b8481ed92696269c17732f8a707fd614869d984741a`  
		Last Modified: Wed, 12 Jun 2024 00:58:17 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7316c63240c2b5523fd4e1fea5ea1bb39fd328de851ff125176115d685230d52`  
		Last Modified: Wed, 12 Jun 2024 00:58:17 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad28486a88821f96e41ceed1379efc7d1c05a5111b7860e9780dc88dd74090fc`  
		Last Modified: Wed, 12 Jun 2024 00:58:28 GMT  
		Size: 206.5 MB (206500759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5975d4f442dfc063250a7c00b25fa6ced3af602c8b1613ac93573458ffce002e`  
		Last Modified: Wed, 12 Jun 2024 00:58:17 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
