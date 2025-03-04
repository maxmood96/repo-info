## `openjdk:25-ea-12-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:378c0f256f6ca5c615db2c03bc43f3d1a4d568544e55894fff2321a1ff673983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `openjdk:25-ea-12-jdk-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull openjdk@sha256:6d9d3fa1ca6ef1f198b8ac0ae0d1aea3165aecbd979cdbb937813d4bd3cc033c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2472517605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9dd202f60ee490a565352dd78725072e82abdd6e8b1d6a1f0c42bbc180f6fd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 04 Mar 2025 21:55:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 04 Mar 2025 21:56:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 04 Mar 2025 21:56:01 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 04 Mar 2025 21:56:09 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 04 Mar 2025 21:56:10 GMT
ENV JAVA_VERSION=25-ea+12
# Tue, 04 Mar 2025 21:56:10 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_windows-x64_bin.zip
# Tue, 04 Mar 2025 21:56:11 GMT
ENV JAVA_SHA256=bcb8237b8992ff10a073a5de79dd9e3bdd7ca90a56c4d16a3639a876b9aec165
# Tue, 04 Mar 2025 21:56:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 04 Mar 2025 21:56:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dc5f021e09d66959ff03dbcaa5e154459be6ed7f925fee9eafb0be5daacfb6`  
		Last Modified: Tue, 04 Mar 2025 21:56:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e4612f9ace1cc4017badb8bf24dcffb80da6e592574f21522fdd044760017f`  
		Last Modified: Tue, 04 Mar 2025 21:56:43 GMT  
		Size: 377.4 KB (377444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9df17408866f4885bccbd9324c050adc39d91645d20310d6712bc0fa51c3150`  
		Last Modified: Tue, 04 Mar 2025 21:56:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ca882e139fdb9745750256cef9e035a70d1d4c7faebd3d8d64d37e0c02bb62`  
		Last Modified: Tue, 04 Mar 2025 21:56:43 GMT  
		Size: 356.0 KB (356044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa70689317cc7cf3d3b7cf46324a37413655b6c908e4b979d82184a0947e760`  
		Last Modified: Tue, 04 Mar 2025 21:56:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca41aa32922676e70e4eec663f465f988b8935f8f27438bcc52d9dc6688406b`  
		Last Modified: Tue, 04 Mar 2025 21:56:41 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0132a974a4cb253c21bf8d6d07bae890b93ef4b0884af1672ec466ac3d662e7a`  
		Last Modified: Tue, 04 Mar 2025 21:56:41 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8401af0053ce054f97b1f8fcb936c985b4bac1b69cc591c22416b0d373a388f5`  
		Last Modified: Tue, 04 Mar 2025 21:56:52 GMT  
		Size: 207.9 MB (207918405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3a6d054bb07dfbfcc0be1d21bc4bea8726481f9c5c4bc709b7e7bd8ef5b0ff`  
		Last Modified: Tue, 04 Mar 2025 21:56:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-12-jdk-windowsservercore` - windows version 10.0.17763.6893; amd64

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
