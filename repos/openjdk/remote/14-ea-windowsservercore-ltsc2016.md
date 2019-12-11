## `openjdk:14-ea-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:c55cf20fe5ec35980e3a18d08c5a3eab58269b5fc60ee5a4298ed06c834f215f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `openjdk:14-ea-windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull openjdk@sha256:ddb0070675a98dc599bcb3a094358b3239901c63edbc05b7f1e6fc8c939bc22c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5932086409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861539692367231202cb97b3c5a187f1788baeed38a320a66a2119924b83982f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 00:35:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 18:45:32 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 11 Dec 2019 18:45:34 GMT
ENV JAVA_HOME=C:\openjdk-14
# Wed, 11 Dec 2019 18:46:45 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 11 Dec 2019 18:46:47 GMT
ENV JAVA_VERSION=14-ea+26
# Wed, 11 Dec 2019 18:46:49 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk14/26/GPL/openjdk-14-ea+26_windows-x64_bin.zip
# Wed, 11 Dec 2019 18:46:50 GMT
ENV JAVA_SHA256=e6491a2d6c7e4638e56a41c4ec2d3016de2b0d69751d6ac834cd4cb4f5bf9210
# Wed, 11 Dec 2019 18:49:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2019 18:49:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:530e4240d4261ce165890648d1df6230dc4f9ce5df2e6cf9f0d5876694c3d4f0`  
		Last Modified: Wed, 11 Dec 2019 01:14:39 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ba7ecb82646b9454a7a416c149a513479fd0ab29aaa2dfbe96281b62668931`  
		Last Modified: Wed, 11 Dec 2019 19:59:59 GMT  
		Size: 5.4 MB (5365131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3eaf34da6eedc1087e3f8e21af3d549b7e85b0e1f93c4275a7569076c67f12`  
		Last Modified: Wed, 11 Dec 2019 19:59:55 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef9e5659d610b4fc02e08dc2d00b5d97d8f9e0d0ca73681a31acbef3f3e00a5`  
		Last Modified: Wed, 11 Dec 2019 19:59:58 GMT  
		Size: 5.3 MB (5345980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6919c96632eafcdb02f2337d389de9bf18719eb71acabf35f82ae9fa8e921e`  
		Last Modified: Wed, 11 Dec 2019 19:59:53 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f097b9b0dc052d8663ca13c7ac9e9a56891cebce8b631f35b7d3c514b02efb52`  
		Last Modified: Wed, 11 Dec 2019 19:59:53 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3aa55c2f14db34f728d9edba043fb1e33800abb758e0f7dc64a0aadecf9d89c`  
		Last Modified: Wed, 11 Dec 2019 19:59:53 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b341488927f8b4446274d894b0f212afa74460addb298d427bbd9f959e39452a`  
		Last Modified: Wed, 11 Dec 2019 20:00:19 GMT  
		Size: 198.7 MB (198664288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b564cd8feaa5d5084e09cef4fb9d1a9eebb79e3bd9cad999dd762b8b1e19a77a`  
		Last Modified: Wed, 11 Dec 2019 19:59:53 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
