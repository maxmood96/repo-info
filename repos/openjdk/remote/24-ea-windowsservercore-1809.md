## `openjdk:24-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:285e88c917b10679285fa89c3610b7e34e77cea5c7e3fff49ef5fc8180ebeee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `openjdk:24-ea-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull openjdk@sha256:08a52ed6d1d4ac7973b6854fe8dcb5be7145ed5637e5619b287334e3a57afbc8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2220373698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31ee9114813039f8bab329382ea2c7cce378c2bd17d009e50fded774c5929cf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Mon, 25 Nov 2024 23:23:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Nov 2024 23:25:13 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 25 Nov 2024 23:25:13 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 25 Nov 2024 23:25:25 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 25 Nov 2024 23:25:25 GMT
ENV JAVA_VERSION=24-ea+25
# Mon, 25 Nov 2024 23:25:26 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/25/GPL/openjdk-24-ea+25_windows-x64_bin.zip
# Mon, 25 Nov 2024 23:25:26 GMT
ENV JAVA_SHA256=3f5d0f9ac7a7a748bad67a34671556be063e7fc8eda4cb079478238095698786
# Mon, 25 Nov 2024 23:25:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 25 Nov 2024 23:26:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e245933abab38f7af5d2e89c7f8a6dbfe7d0761f2c6b2dfd1923a1410ac75d3`  
		Last Modified: Mon, 25 Nov 2024 23:26:04 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d6c825d831ffba1f3b6fb3c16c6fe0f2352e83e31e60a93895091126b68400`  
		Last Modified: Mon, 25 Nov 2024 23:26:05 GMT  
		Size: 506.4 KB (506419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6361ba0d78a7b546a94dda3d5a7a6987b3700fb2a2921b30d716acab2b585a`  
		Last Modified: Mon, 25 Nov 2024 23:26:04 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdf8c546cdb552abb04d000b2716d83e06a741005ae2f35984564f7cf138af9`  
		Last Modified: Mon, 25 Nov 2024 23:26:04 GMT  
		Size: 350.2 KB (350225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcfbe37967b0eac652dcea16b4bc560227de09939a681ff965afcae5a125e56`  
		Last Modified: Mon, 25 Nov 2024 23:26:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba05d142ab3a88e987be46b731ace14b09b8e32dfefb277a987f297e3546935`  
		Last Modified: Mon, 25 Nov 2024 23:26:03 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88996156996fee86d898c76ab7d35abd5259169be0f9e82f656d1e42e7c41fc9`  
		Last Modified: Mon, 25 Nov 2024 23:26:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3eaaa98e85f7d8bf7794e610218137d8f5faf4d79aa33c70c3b374f29b1281`  
		Last Modified: Mon, 25 Nov 2024 23:26:14 GMT  
		Size: 208.9 MB (208855427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddd5b9676a316a58c5b1896b5789af655379af5bc326ba42cae126953b069a1`  
		Last Modified: Mon, 25 Nov 2024 23:26:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
