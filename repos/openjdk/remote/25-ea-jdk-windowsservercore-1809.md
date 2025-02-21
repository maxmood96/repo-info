## `openjdk:25-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:fdc6d847efd676c6a452e14f850b988836e99c379abeb078740620ffa956fd1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `openjdk:25-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull openjdk@sha256:e2306fb6bbe0044d1981653843f20607aaa20d5e7c934f30e3b6e8c79227cb5c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345514662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9b1be90c4fa9eaefe6e9f4b6dcaaf0ac041edb2d52d2b8ab95342cf0ef6a47`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Fri, 14 Feb 2025 23:36:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Feb 2025 23:37:06 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 14 Feb 2025 23:37:07 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 14 Feb 2025 23:37:12 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 14 Feb 2025 23:37:13 GMT
ENV JAVA_VERSION=25-ea+10
# Fri, 14 Feb 2025 23:37:13 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_windows-x64_bin.zip
# Fri, 14 Feb 2025 23:37:14 GMT
ENV JAVA_SHA256=9e8ebedd95dce7d5755f885b28067679019d529df9ff91b64e03edd7f2285e6e
# Fri, 14 Feb 2025 23:37:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 14 Feb 2025 23:37:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a5f72500d7c71b459f7065fe476e845b111c9298cf4b639eb8ec189cd1ef49`  
		Last Modified: Fri, 14 Feb 2025 23:37:45 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7a4f53b9bd006c77e9e5e23e120a305ff9549d0888b82f0bfede2a79ad73d9`  
		Last Modified: Fri, 14 Feb 2025 23:37:46 GMT  
		Size: 351.6 KB (351632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373358639f2bd6d60572f1385106ab9bebfbdd5096a805f8844b781d18d864b9`  
		Last Modified: Fri, 14 Feb 2025 23:37:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0127c9a799e6d8dcf09d809a4714edffa952a96821f24983178355c098dff4f8`  
		Last Modified: Fri, 14 Feb 2025 23:37:46 GMT  
		Size: 333.5 KB (333463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8015adf261b47bbdb4e75f539e5be0dfb802a91374adef7a8db08ae6485f998`  
		Last Modified: Fri, 14 Feb 2025 23:37:41 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa4d70cfae89156c91034d5169461cfd4bf2c79d874717e53dd23773bef9480`  
		Last Modified: Fri, 14 Feb 2025 23:37:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2aa9fa6b4cbe722ac3bc8fe13973967875d065868f661662c56539169bad07`  
		Last Modified: Fri, 14 Feb 2025 23:37:41 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c651ee7fa4380c117e447bcd5d5502aae2ffe16da48b723294da3156869952a1`  
		Last Modified: Fri, 14 Feb 2025 23:37:52 GMT  
		Size: 207.9 MB (207912975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed9f6e7131e1bdeef944b1f6b31026be94452bf494b1a8b9fcc65df6e71127f`  
		Last Modified: Fri, 14 Feb 2025 23:37:41 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
