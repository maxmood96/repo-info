## `openjdk:24-ea-13-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:c3c4465992827f3d94b51bd1133e5121aa871cdec240a996c685fedf5b76ae4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `openjdk:24-ea-13-jdk-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull openjdk@sha256:f8ba256c22415ee2f1134719ddb69f5ee1d0aad53c64b9986a247df07b0847cd
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2454130008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec004a8ef0047093acb9dbeb9d43a414164b579f1039d77877ab6680a54d58af`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Thu, 29 Aug 2024 20:59:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 Aug 2024 21:01:38 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 29 Aug 2024 21:01:39 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 29 Aug 2024 21:02:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 29 Aug 2024 21:02:04 GMT
ENV JAVA_VERSION=24-ea+13
# Thu, 29 Aug 2024 21:02:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/13/GPL/openjdk-24-ea+13_windows-x64_bin.zip
# Thu, 29 Aug 2024 21:02:06 GMT
ENV JAVA_SHA256=f872535c7185b35e6509c62f7ed7bec65d8f958dc6742e40211244d6964e7ae6
# Thu, 29 Aug 2024 21:02:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 29 Aug 2024 21:02:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8adc05975d35205c61288aaf056cfeb2e76d32451c59cd8d832f4f12c53079`  
		Last Modified: Thu, 29 Aug 2024 21:03:00 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1b641ffa45879c0af6fcd60dc8f90580a9cff592e1c64180b8dbbe9c96768c`  
		Last Modified: Thu, 29 Aug 2024 21:03:00 GMT  
		Size: 513.0 KB (512994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9af7d6df9df51db0122898030272e766dc0e66ecae4bcefd4fd1badda3a227`  
		Last Modified: Thu, 29 Aug 2024 21:03:00 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af027a3c55ca6f732f17532506ff8371244e4eb6d814edc64b4445fa634c0348`  
		Last Modified: Thu, 29 Aug 2024 21:03:00 GMT  
		Size: 360.0 KB (360042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c699ff60391209e4112f2b03153cb758a07630906433fddadb4808d09173d567`  
		Last Modified: Thu, 29 Aug 2024 21:02:59 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ed1e9fbdb42dfa02fd8e98b88ce408915ac22f3ba922314a4d5f08858545c2`  
		Last Modified: Thu, 29 Aug 2024 21:02:59 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbea963409af1cc620767553fff78f107165266db30ef8fec18499aca883f88`  
		Last Modified: Thu, 29 Aug 2024 21:02:59 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a60e209943d8d33bbadb6b8782e4dbed884166edc8c988a3083301e673da03b`  
		Last Modified: Thu, 29 Aug 2024 21:03:10 GMT  
		Size: 208.0 MB (208045883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96be7fbfa938a394fb311c17896ab137b39f2f5b3a6b50b8f6562c1c5d9bc6c3`  
		Last Modified: Thu, 29 Aug 2024 21:02:59 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
