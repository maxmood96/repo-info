## `openjdk:23-ea-26-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:1aa8dc65ac5e088b9be289b559dddbe475edd386bc2190de17132fdbef93af8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `openjdk:23-ea-26-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

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
