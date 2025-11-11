## `openjdk:26-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:f3dbfc58472a14a309008602549f4db4cc28eb9437be5fc61dc846c444fba747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `openjdk:26-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull openjdk@sha256:8d2e7a5d657e291c3d011699f3f4b034ec4b0a5f6e8fbaf42d4bda46483487db
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1799802866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab86cb1f6cc53590fe1e1e5888d70a697b924422e23462b6c9dd748c38745495`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Mon, 10 Nov 2025 19:46:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 10 Nov 2025 19:47:22 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 10 Nov 2025 19:47:22 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 10 Nov 2025 19:47:28 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 10 Nov 2025 19:47:29 GMT
ENV JAVA_VERSION=26-ea+23
# Mon, 10 Nov 2025 19:47:30 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_windows-x64_bin.zip
# Mon, 10 Nov 2025 19:47:30 GMT
ENV JAVA_SHA256=41b399a48fae2944ecad52c8f821b2ce5195449fb10eb54a18542b013146fe59
# Mon, 10 Nov 2025 19:48:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 10 Nov 2025 19:48:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812bc9a1d91374ca807bd9e023ef98e85f4eddedc06ccf494aa93d48c32cbf4e`  
		Last Modified: Mon, 10 Nov 2025 19:56:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073b2fa8fbf044bb5fe3e9c0fd6d0fc4ddb1520f068d8bd1030f60d905322aff`  
		Last Modified: Mon, 10 Nov 2025 19:56:05 GMT  
		Size: 521.4 KB (521379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a853b7cccb4a6449ea1ae12e5be263e2a9d512ecd63ffccd93daea9c03d0feb`  
		Last Modified: Mon, 10 Nov 2025 19:56:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117b576a54611c7226278fabed13650955d4faa7da407cad54593f79647419bb`  
		Last Modified: Mon, 10 Nov 2025 19:56:05 GMT  
		Size: 360.4 KB (360440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224b16e0e6dab03e17425e3f008ddecbabef7520d422509a6a6269e057a4bc25`  
		Last Modified: Mon, 10 Nov 2025 19:56:04 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a40265931d833b30288e8673aad0353a49660268c26effc33b13d7c981e161`  
		Last Modified: Mon, 10 Nov 2025 19:56:04 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8b8841b5368eb93445c69cf471741d7ebd33da5e6af735f6595253601c2dab`  
		Last Modified: Mon, 10 Nov 2025 19:56:04 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87a1d24dce9105e2c772bbc8c30902049c482988c811537e462f08c58ab1255`  
		Last Modified: Mon, 10 Nov 2025 22:37:19 GMT  
		Size: 221.7 MB (221720259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a1fa6edffc4342cf9b49f00c3d6495715befceaf4a5651f1ac364a762820ee`  
		Last Modified: Mon, 10 Nov 2025 19:56:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
