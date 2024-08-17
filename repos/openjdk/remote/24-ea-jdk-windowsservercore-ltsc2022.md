## `openjdk:24-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:106715bc47065a821e2c54431c25f30f285b03521d8d3809540c6a9e6916ed64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `openjdk:24-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull openjdk@sha256:fd1f4ca12c3f5a54e98065445a57a2bdc94ecd4d170c43f96847cc6d11ec77bc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2350396889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6baa243b23bb563e614d5a4dd2c4c17294b7b3f80514d07c155bd728dc61f4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Fri, 16 Aug 2024 22:08:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 22:08:47 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 16 Aug 2024 22:08:47 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 16 Aug 2024 22:08:54 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 16 Aug 2024 22:08:55 GMT
ENV JAVA_VERSION=24-ea+11
# Fri, 16 Aug 2024 22:08:55 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_windows-x64_bin.zip
# Fri, 16 Aug 2024 22:08:56 GMT
ENV JAVA_SHA256=7a69063e699bfa886323d4d41aebe553be53c68819b952fb7342fd73cc735697
# Fri, 16 Aug 2024 22:09:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 16 Aug 2024 22:09:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020e0ad155fc185910867d71ec2eaa6ced1ad78cca2c59bba04d7c4c132253de`  
		Last Modified: Fri, 16 Aug 2024 22:09:25 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9389a83a13943f501a85aa2cb04c84ccef96a696240aa326db6420977d56ba`  
		Last Modified: Fri, 16 Aug 2024 22:09:25 GMT  
		Size: 360.9 KB (360894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6dc9bc6f3c47f209179c8d477c0e49ba1c64e634497698777045d122a6cc10`  
		Last Modified: Fri, 16 Aug 2024 22:09:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d77e1caf493ae8554e0c6a24fcc7d36a97097e41a7961cbf3273cc75a7e3063`  
		Last Modified: Fri, 16 Aug 2024 22:09:25 GMT  
		Size: 341.1 KB (341150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a0e976bcc25e6e514f995827973d660cf6413a0044c2f8d2d2694800d89102`  
		Last Modified: Fri, 16 Aug 2024 22:09:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c8db328e59bf440ce329e374c5063e7c7cde702716976026c2c33b6137ba60`  
		Last Modified: Fri, 16 Aug 2024 22:09:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2764b6d53e353cdbb3c6b06165be7ac2b63155ef0c3a0faf4307b1e06aa8d41`  
		Last Modified: Fri, 16 Aug 2024 22:09:23 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f942b077f2fa4373551bb6c248563d185cc6a577973e372faa9ce45fa9b9ac`  
		Last Modified: Fri, 16 Aug 2024 22:09:34 GMT  
		Size: 207.9 MB (207922132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd5888b353a4afa69195bd1d926ca7b3fc13d221caec0e2c7819541ece1978f`  
		Last Modified: Fri, 16 Aug 2024 22:09:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
