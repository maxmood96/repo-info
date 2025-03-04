## `openjdk:25-ea-12-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:21cb85e475aed967309d5dbf0b810de34bfb65076573c038b4d69e4b6cde508a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `openjdk:25-ea-12-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull openjdk@sha256:35604f2c6da17263e0989c754fd465df0fba7a2950fcac9800c3ced6ba8a6073
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345512386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49465345c741afdf3d959e8f8a7c6206590800487cddf53577883f540ef40185`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 04 Mar 2025 21:56:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 04 Mar 2025 21:56:59 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 04 Mar 2025 21:57:00 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 04 Mar 2025 21:57:09 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 04 Mar 2025 21:57:09 GMT
ENV JAVA_VERSION=25-ea+12
# Tue, 04 Mar 2025 21:57:09 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_windows-x64_bin.zip
# Tue, 04 Mar 2025 21:57:10 GMT
ENV JAVA_SHA256=bcb8237b8992ff10a073a5de79dd9e3bdd7ca90a56c4d16a3639a876b9aec165
# Tue, 04 Mar 2025 21:57:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 04 Mar 2025 21:57:48 GMT
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
	-	`sha256:800185667cdfabce0af22c545b2de6cb8da4d9a00d7ad01f33b43d7af4638e92`  
		Last Modified: Tue, 04 Mar 2025 21:57:53 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b771e7e0f3c8d0d5f21d9027ade298fe6f924434b13486a663e70122e969c9`  
		Last Modified: Tue, 04 Mar 2025 21:57:53 GMT  
		Size: 347.7 KB (347743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd596b9947c5fcc20a8517fd8b367f3a6dfcaec149751f8cbfa37461acbc98c`  
		Last Modified: Tue, 04 Mar 2025 21:57:53 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4980893fc22c4587300b2e27d8b45dfa20eb7efdca5e36fa4d19b420b786db`  
		Last Modified: Tue, 04 Mar 2025 21:57:53 GMT  
		Size: 336.1 KB (336062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fd01983ad3acb5fd287b3ff9bb711789994a9b5230945eb1d5e9ee0a730ae8`  
		Last Modified: Tue, 04 Mar 2025 21:57:52 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d12d6f9fb2a020dbb993943ceedd9262e500368b1abb87d7b302ccd26916eb6`  
		Last Modified: Tue, 04 Mar 2025 21:57:52 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594e2eac4f3d588c505479d81c436e54a6f210af790490ecc5fe3b840e2ee66`  
		Last Modified: Tue, 04 Mar 2025 21:57:52 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ea09905e1f17383ad55198e1b78494e56706ac9766c2b4b7a76159543c8242`  
		Last Modified: Tue, 04 Mar 2025 21:58:02 GMT  
		Size: 207.9 MB (207912023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc5634142f4e96052102ebd9b67e97ed08f964bf2796985e467e54b59321efb`  
		Last Modified: Tue, 04 Mar 2025 21:57:52 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
