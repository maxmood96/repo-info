## `openjdk:23-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:9c28cd22be9341bf8ade87bf9d3333c60e7cbfd16b3ea5626237851ed1b58e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `openjdk:23-windowsservercore-ltsc2022` - windows version 10.0.20348.2159; amd64

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
