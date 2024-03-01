## `openjdk:23-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:e44419d4ad8104c7766016eb290c7036a633f262ced95ca984dcc9253712443f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `openjdk:23-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull openjdk@sha256:d8b78ea9b3b87c1fc7044623112b98403742f8ac19beebb9cb70b7cb446a5969
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2109390858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d438c9f7e5033e51af365cc8ba081e4884d063811786c9e23a33d373bd2d187e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Thu, 29 Feb 2024 22:50:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 Feb 2024 22:50:37 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 29 Feb 2024 22:50:38 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 29 Feb 2024 22:50:46 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 29 Feb 2024 22:50:46 GMT
ENV JAVA_VERSION=23-ea+12
# Thu, 29 Feb 2024 22:50:47 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/12/GPL/openjdk-23-ea+12_windows-x64_bin.zip
# Thu, 29 Feb 2024 22:50:48 GMT
ENV JAVA_SHA256=71a4b8ffa972cd355bf10024250c8f28d6992b430cd294744705cb5ebd2a5a41
# Thu, 29 Feb 2024 22:51:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 29 Feb 2024 22:51:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405df72f51a6afa806a89c0ba475d7c4fd79328d46f27d0f0925f2dd456f7a5d`  
		Last Modified: Thu, 29 Feb 2024 22:51:51 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baed81a0d8c1964c3429f0a2fddc4b858f23139eb00233120f8a1b55f5d8b15b`  
		Last Modified: Thu, 29 Feb 2024 22:51:51 GMT  
		Size: 489.7 KB (489747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8159aeef050c5a22d581cb4f99ab617dcbc8cb2b6d031fcb04207c3a1be26ae5`  
		Last Modified: Thu, 29 Feb 2024 22:51:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a720ea9c65ed6339442025970ecbc667240dd80fb0628f65ba7536e87fbace6`  
		Last Modified: Thu, 29 Feb 2024 22:51:51 GMT  
		Size: 334.8 KB (334847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4ce92f06f758799a6d7c662dfec43e7e55b595fe5d4a28639b19a698cd0a8d`  
		Last Modified: Thu, 29 Feb 2024 22:51:50 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc4b2fcc7c65384963d6b8b0b1bde38914163b0afbfba73c5e9608b960c0566`  
		Last Modified: Thu, 29 Feb 2024 22:51:50 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e404713c6ecc56fadc852c7d46007a6b8504bd9fffee1e5d8ef586e4c203ce`  
		Last Modified: Thu, 29 Feb 2024 22:51:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f76580c3cdc6e1ec8512ddd35bad9bdf0754f007be8ac03d39c01dcae1254de`  
		Last Modified: Thu, 29 Feb 2024 22:52:01 GMT  
		Size: 197.9 MB (197904325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4cdfcce5986b95b649b9d87d7024a4f784741281eef0cb83aaec273c7ffc9f`  
		Last Modified: Thu, 29 Feb 2024 22:51:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
