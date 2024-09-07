## `openjdk:24-ea-14-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:6f8e2811e6e061fa6a1faa6d0992079d02e8601fdb2a88bbee6d577d11fd6172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `openjdk:24-ea-14-jdk-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull openjdk@sha256:2206af543fe149f27e9768b8a681d657ae24a182f8d747c68cae9cc76f7b6e63
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2454065444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431d91e354b9da5bd5c77818510bbda44e53e4c063deeac7770f76582a24efba`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Fri, 06 Sep 2024 22:00:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Sep 2024 22:02:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 06 Sep 2024 22:02:26 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 06 Sep 2024 22:02:51 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 06 Sep 2024 22:02:51 GMT
ENV JAVA_VERSION=24-ea+14
# Fri, 06 Sep 2024 22:02:52 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_windows-x64_bin.zip
# Fri, 06 Sep 2024 22:02:52 GMT
ENV JAVA_SHA256=d302c4d8be4955ea17267c66b8321f205212748df83273e4e0d9ccc0d1c4b1a2
# Fri, 06 Sep 2024 22:03:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 06 Sep 2024 22:03:43 GMT
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
	-	`sha256:89a85539afafa4fd5c7cff928b9651e0ad5e977e24bc2f01a9b8d3bef5fea504`  
		Last Modified: Fri, 06 Sep 2024 22:03:48 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30bd183cd6bf2e89ae1801679c2cd36558a985f6627e5a7923993831ad9b11db`  
		Last Modified: Fri, 06 Sep 2024 22:03:48 GMT  
		Size: 500.9 KB (500915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8b834bfb2671db352ab9c7bf877bfb395837c650262beb0c1dfddb1d8d2c6b`  
		Last Modified: Fri, 06 Sep 2024 22:03:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed62d59192ed801af12eff4faa9e78682a1d64180b0263899cee8ede1bff2f8d`  
		Last Modified: Fri, 06 Sep 2024 22:03:48 GMT  
		Size: 346.6 KB (346567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b76a5c8ce16e1f122d4700b423b51ebdd77a77b23257a133d87db7a2684c38`  
		Last Modified: Fri, 06 Sep 2024 22:03:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abf20b02eb8464f5d632f2d7e6c41c6d91fa7f59fd1992e7809e12f06ad9a32`  
		Last Modified: Fri, 06 Sep 2024 22:03:47 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c8bcf86a1fd2dd90d9d520a25b5e59676ffa657ae2ef56931aebf23a787c43`  
		Last Modified: Fri, 06 Sep 2024 22:03:47 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a361e1dd41c4cc57f54bf6f55ca3efa9484432155481795409397fd98792c2fc`  
		Last Modified: Fri, 06 Sep 2024 22:03:58 GMT  
		Size: 208.0 MB (208006955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2454f4607c6812877021c59b1e5e318701a093d4dee3385a821fba802f087b9`  
		Last Modified: Fri, 06 Sep 2024 22:03:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
