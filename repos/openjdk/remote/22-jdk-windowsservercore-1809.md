## `openjdk:22-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:de98d1ff3cae7c11a3e9b00d28abab014af1eb44af1b56222272620403d41123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `openjdk:22-jdk-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:956010d9e2bb9237e52fcf2016bae33287a6e37cb0e222984b6aa81c6a99fcb6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2268388053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b43d179e1e8e589c749e2ebf9ac8be413abd88a12113a2e74d8cdc2282615a6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Fri, 26 Jan 2024 23:49:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Jan 2024 23:51:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 26 Jan 2024 23:51:44 GMT
ENV JAVA_HOME=C:\openjdk-22
# Fri, 26 Jan 2024 23:52:08 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 26 Jan 2024 23:52:08 GMT
ENV JAVA_VERSION=22-ea+33
# Fri, 26 Jan 2024 23:52:09 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_windows-x64_bin.zip
# Fri, 26 Jan 2024 23:52:09 GMT
ENV JAVA_SHA256=7314e1a93eac080af82b5a8e301d653e3e4878f3fc01d6e41559cacf8ad8ab2b
# Fri, 26 Jan 2024 23:52:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 26 Jan 2024 23:52:53 GMT
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
	-	`sha256:f13d0db08ff1cf3d1cf5e5d69c38c08e93e4a16ee04f73fff59b494f5371b91e`  
		Last Modified: Fri, 26 Jan 2024 23:52:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337e49d253acb8d77744592c88dfd744fe84d6e997d29e5349d131a4396263f4`  
		Last Modified: Fri, 26 Jan 2024 23:52:58 GMT  
		Size: 517.9 KB (517942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77be480b51413878c573ebc55ed9099eda30decb74eddababcb99c12bcacb735`  
		Last Modified: Fri, 26 Jan 2024 23:52:57 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18ea67753a1ddf3dcaa36d4e9c79124eb4745d47dd53dc6969e1887a86207b`  
		Last Modified: Fri, 26 Jan 2024 23:52:57 GMT  
		Size: 363.7 KB (363672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707092397b71edb630eb2ef4f7a7f21e30f09e996395609806d06440655b674d`  
		Last Modified: Fri, 26 Jan 2024 23:52:56 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca173c88c111c2c06e91fa1a5e20079821f006bcc5f6cec1976070c8b83ff45b`  
		Last Modified: Fri, 26 Jan 2024 23:52:56 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a78fe5e68dfe3d677c6318049a30c8306fd52c80b1ad6c19a1cc005a6263607`  
		Last Modified: Fri, 26 Jan 2024 23:52:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a3a4d99f65185dd2fbdb945c050ce51bd215298dfd18a15de3602cfc4d85b2`  
		Last Modified: Fri, 26 Jan 2024 23:53:06 GMT  
		Size: 197.8 MB (197776178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6bb5c5ef5bfc2188915fd6c3d74d4b743e5acc4629585bbd54812a2dd4c681`  
		Last Modified: Fri, 26 Jan 2024 23:52:56 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
