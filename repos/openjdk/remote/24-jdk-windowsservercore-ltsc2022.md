## `openjdk:24-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:f5064ee2fa361358a0d62429dcdbf260b9b912816952f2ab99dcd7ede3e6af39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `openjdk:24-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull openjdk@sha256:7918e7346b562564acbd4003b27786de6c0b72229c4dd1f76a271953685ee4f8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325404296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96fcc868e891d4def65badeb26d80ce1d40ba7ae405151af2d360994b987bd34`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Tue, 02 Jul 2024 00:57:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jul 2024 00:57:59 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 02 Jul 2024 00:57:59 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 02 Jul 2024 00:58:05 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 02 Jul 2024 00:58:06 GMT
ENV JAVA_VERSION=24-ea+4
# Tue, 02 Jul 2024 00:58:06 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_windows-x64_bin.zip
# Tue, 02 Jul 2024 00:58:07 GMT
ENV JAVA_SHA256=49def475d4ac8b16fc13e9f43cb195b1da28c70cbfa438466e25f7b82c5c55a2
# Tue, 02 Jul 2024 00:58:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 02 Jul 2024 00:58:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78023868517c9e90cd1a2da57a94d15b051ec6e346b01dc6db1422b9a42efe46`  
		Last Modified: Tue, 02 Jul 2024 00:58:39 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5569bc9a87b1ba1cdefcec68115c4739eabeab66f7766c2bbd5037eee60598f`  
		Last Modified: Tue, 02 Jul 2024 00:58:39 GMT  
		Size: 359.7 KB (359696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6780b70e7c9a26687fb9cbb876d11dc82bf99a0016852dfce87b7709fd5c9f9`  
		Last Modified: Tue, 02 Jul 2024 00:58:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c380a3d2cb1adee65a90fb600092d0786df1cb4dbfcf4096ca431be8949afc1`  
		Last Modified: Tue, 02 Jul 2024 00:58:39 GMT  
		Size: 345.6 KB (345562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9ca61ef1b1da104241c922ec429f6c70cdfde7947957e5999c1854772d9da0`  
		Last Modified: Tue, 02 Jul 2024 00:58:37 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599f9966908c26c02ef9cca1c142c3847badebd914e3d05f8fc4b6cecb0c9226`  
		Last Modified: Tue, 02 Jul 2024 00:58:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a69efd113708e0e938933a3caf1e72a2a78ee9fd6e1dc43f2c30c1b2073119b`  
		Last Modified: Tue, 02 Jul 2024 00:58:37 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2035dc4544631d55c9769410ea995617440af3d55307e42059e1568b16e9d6a3`  
		Last Modified: Tue, 02 Jul 2024 00:58:48 GMT  
		Size: 206.5 MB (206500984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f966edd9ceeac2ac401fc189601209421fa0cee01095d974d0088d623da5d76a`  
		Last Modified: Tue, 02 Jul 2024 00:58:37 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
