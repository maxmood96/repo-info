## `openjdk:23-ea-2-windowsservercore`

```console
$ docker pull openjdk@sha256:057804f1f254a91d9018b0c614bebea7428253bb6d75665d91b553c30ea9a3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2159; amd64
	-	windows version 10.0.17763.5206; amd64

### `openjdk:23-ea-2-windowsservercore` - windows version 10.0.20348.2159; amd64

```console
$ docker pull openjdk@sha256:cc9172491beac13eb4275403b43a29226baf2e04b0f915bedc05f33b8a7f8dce
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2087924389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b275be1da9c7fb81c007cb077f2ed7805f807cabbe24aea7c92426664d7bf71`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Sat, 16 Dec 2023 01:59:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 16 Dec 2023 01:59:52 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 16 Dec 2023 01:59:53 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 16 Dec 2023 01:59:58 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 16 Dec 2023 01:59:58 GMT
ENV JAVA_VERSION=23-ea+2
# Sat, 16 Dec 2023 01:59:59 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/2/GPL/openjdk-23-ea+2_windows-x64_bin.zip
# Sat, 16 Dec 2023 01:59:59 GMT
ENV JAVA_SHA256=bf19a08c126e820eb3d622dbae9c2928853561d1227235461046491413e7f649
# Sat, 16 Dec 2023 02:00:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 16 Dec 2023 02:00:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a57533c2f32e73f891b22198eae723bac07ef0570921b494b990c11761f93a`  
		Last Modified: Sat, 16 Dec 2023 02:00:23 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accd4967041574377fb4f17559cf90326c4252e8526d540618e92ac5325e9aea`  
		Last Modified: Sat, 16 Dec 2023 02:00:23 GMT  
		Size: 504.2 KB (504162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5270214a52d02d50e92f16dfe70d7026188a8afdba2130cdb579298e188785d4`  
		Last Modified: Sat, 16 Dec 2023 02:00:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48618d537d5897dcc778c79e2ccdfa8042f8d63b71c7996975e6419b606d7e6c`  
		Last Modified: Sat, 16 Dec 2023 02:00:23 GMT  
		Size: 356.5 KB (356469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3af01f397493be121d4ed699a047d792fc604e9781296a9b8e24cfabea39d0`  
		Last Modified: Sat, 16 Dec 2023 02:00:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220508affe45d964e1688c3a0843914e1a35210910c7b14db8f5217729fa8cee`  
		Last Modified: Sat, 16 Dec 2023 02:00:21 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddcbb29cb6931e7489904834088934dd9bde873eb9dc4f82c748f20c217e276`  
		Last Modified: Sat, 16 Dec 2023 02:00:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f6ef7fdf32e8aba8d909df998e343857240c8c3f0b0035fd6fe9408d7fa536`  
		Last Modified: Sat, 16 Dec 2023 02:00:34 GMT  
		Size: 197.8 MB (197782361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20e6f93b138852565325f429cf5b42b601912d46993138e143f00957ce23494`  
		Last Modified: Sat, 16 Dec 2023 02:00:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-ea-2-windowsservercore` - windows version 10.0.17763.5206; amd64

```console
$ docker pull openjdk@sha256:ee58dd7d58ba8d68c0a2a625f6aa17bdfc2497bb4a02a02d436a553e4327872f
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2258273118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70df19c343af79b0daecbfaee1b34fe538e5b52f8bc5b35543aa4b52cc41394e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Sat, 16 Dec 2023 01:58:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 16 Dec 2023 01:59:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 16 Dec 2023 01:59:02 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 16 Dec 2023 01:59:22 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 16 Dec 2023 01:59:23 GMT
ENV JAVA_VERSION=23-ea+2
# Sat, 16 Dec 2023 01:59:23 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/2/GPL/openjdk-23-ea+2_windows-x64_bin.zip
# Sat, 16 Dec 2023 01:59:24 GMT
ENV JAVA_SHA256=bf19a08c126e820eb3d622dbae9c2928853561d1227235461046491413e7f649
# Sat, 16 Dec 2023 02:00:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 16 Dec 2023 02:00:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24f607eefb5afd54004adcf2b9132c70ff63c3383cfc4d54c5acab545bc715b`  
		Last Modified: Sat, 16 Dec 2023 02:00:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c8c5ed6ea27912c99273f814e33238c11cd84d0f6fcd3fdecf7c888af621bd`  
		Last Modified: Sat, 16 Dec 2023 02:00:14 GMT  
		Size: 458.2 KB (458191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f23a4fb604d2a2ef4a2ae2817f3b07e375f4c3f3b59de27502ce25cb34400c`  
		Last Modified: Sat, 16 Dec 2023 02:00:13 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57272257502e3018181529f6177e29a3544e1298be66e59742a9ef6c54d19977`  
		Last Modified: Sat, 16 Dec 2023 02:00:14 GMT  
		Size: 335.6 KB (335583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79991df59ee5324a4d5d6046074e1b5ee7c0d676764814118dd8f37260a3ef6`  
		Last Modified: Sat, 16 Dec 2023 02:00:11 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec7f897b38c82c23cb751e35e34d64075640bb5c26cdb79b51890a11e190343`  
		Last Modified: Sat, 16 Dec 2023 02:00:12 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7850104ceaa3a87176c7d49b0b1c2d2daa6ef0256f5ecfbee0a76ae8af42c1fc`  
		Last Modified: Sat, 16 Dec 2023 02:00:11 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3576634d2d7560e1f574456e3ee2aed2c80af5ffbd78d06bf7be7955d0d21ca`  
		Last Modified: Sat, 16 Dec 2023 02:00:23 GMT  
		Size: 197.8 MB (197762533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee54342f02cc37d9b1a074c854d8dfed3227800ad5ad33dde7d7105acaeaf230`  
		Last Modified: Sat, 16 Dec 2023 02:00:11 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
