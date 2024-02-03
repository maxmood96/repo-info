## `openjdk:23-ea-8-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:c33d22f9831a1c9f011ac07ce62e674cebe79da88662697cf74dc9ed6a8e9690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `openjdk:23-ea-8-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:aa9112b627416c208f7bd1c50e2ae9788cbb51fe8fc3bac3023957092b5a1002
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2268438189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705b661ff948f5470b06612365c84b8f9b8a7bdb39c48602f3224ab282e6b2a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Fri, 02 Feb 2024 22:53:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 02 Feb 2024 22:55:15 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 02 Feb 2024 22:55:16 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 02 Feb 2024 22:55:39 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 02 Feb 2024 22:55:40 GMT
ENV JAVA_VERSION=23-ea+8
# Fri, 02 Feb 2024 22:55:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_windows-x64_bin.zip
# Fri, 02 Feb 2024 22:55:41 GMT
ENV JAVA_SHA256=3bf12bda8aa3d293ed14f6956bd24e598c395e3267be4b58191e542ec7d3479a
# Fri, 02 Feb 2024 22:56:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 02 Feb 2024 22:56:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92019e8fe92b9023266e5e0fc6ba5fbf5d7a9b0c1cc350c307a24f7ee21cf947`  
		Last Modified: Fri, 02 Feb 2024 22:56:33 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58ec9969fec076e47997c8b1be3c40e7be2f54cc7b61d59e0a412c2e07cb875`  
		Last Modified: Fri, 02 Feb 2024 22:56:33 GMT  
		Size: 483.1 KB (483114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60c2a9412548b52abaad522595d6fd351787d6be2b972d9094023051b62d43b`  
		Last Modified: Fri, 02 Feb 2024 22:56:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cc300143138a1ca844bbf0b743828afde1ef05a6ab3fecc4d95bd9e8ced709`  
		Last Modified: Fri, 02 Feb 2024 22:56:33 GMT  
		Size: 329.9 KB (329915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d84323f82b24f8587e552eee960975bca6ea8ca346346c1ce309a9806409a0`  
		Last Modified: Fri, 02 Feb 2024 22:56:32 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c668f733ff1b3309ad9d783ecb0d01225879a3765dfe89c98448bb956b01d98`  
		Last Modified: Fri, 02 Feb 2024 22:56:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09f301fcf5b89cc0f889a1bd26b85241018f8f53b479f2b00820d263c2db3a3`  
		Last Modified: Fri, 02 Feb 2024 22:56:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9479a33a8af6082432feacea259738f62e87dedf5259fd74b34744ca7ee2f9f0`  
		Last Modified: Fri, 02 Feb 2024 22:56:42 GMT  
		Size: 197.9 MB (197894872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65c4800a8aeb986b5fe19cc6d65e3d18c8dbbd457ad5da3da38789bc6b9f436`  
		Last Modified: Fri, 02 Feb 2024 22:56:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
