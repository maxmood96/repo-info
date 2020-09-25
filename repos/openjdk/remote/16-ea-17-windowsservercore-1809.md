## `openjdk:16-ea-17-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:56553b5388ac745b1dd2d9a7e48db5eb9138c18f105cf46acf15f53ee3fb7719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `openjdk:16-ea-17-windowsservercore-1809` - windows version 10.0.17763.1457; amd64

```console
$ docker pull openjdk@sha256:682a579575b5857e20e13ec6ade71c242202f5ae1964d2285f64afdc4f9aaa4d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2557697922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462669d9cf2b74b2c571b01c0c565f7e56e8abcf6539514e941aae8c2375e439`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Sep 2020 20:05:13 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Tue, 08 Sep 2020 20:05:14 GMT
ENV JAVA_HOME=C:\openjdk-16
# Tue, 08 Sep 2020 20:05:42 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Fri, 25 Sep 2020 21:15:22 GMT
ENV JAVA_VERSION=16-ea+17
# Fri, 25 Sep 2020 21:15:23 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/17/GPL/openjdk-16-ea+17_windows-x64_bin.zip
# Fri, 25 Sep 2020 21:15:24 GMT
ENV JAVA_SHA256=6e8cb7888e1ae25a9cbb93ae13992a6323b90196d20ef9e1bf7f187978aab31f
# Fri, 25 Sep 2020 21:47:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 25 Sep 2020 21:47:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b301c9d4a0d508778c4b1506920d1304eb5d8c3d5a73ee0a1b522db1e8b9d70`  
		Last Modified: Tue, 08 Sep 2020 22:27:29 GMT  
		Size: 9.1 MB (9130218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b7534d2f9d4d5435b384e825c98f305b60fa3ec2ddb9c869a6b6fcdec1d25`  
		Last Modified: Tue, 08 Sep 2020 22:27:26 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfb7f69d9fbf5629248814c6623d7a21a84cfe9a45d7b548045b31caa10fd0d`  
		Last Modified: Tue, 08 Sep 2020 22:27:26 GMT  
		Size: 295.1 KB (295145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb33d9834571ba0dae97be431714ca5c98e633db20b4b0a95fee70a56e7f346`  
		Last Modified: Fri, 25 Sep 2020 21:56:03 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1fb68d11a730a26c9e6204dc234a98d5444f2a4229a238a6c2d7a0ca68606b`  
		Last Modified: Fri, 25 Sep 2020 21:56:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f08f286940a8d7b90ca27f02427c3a991e02c8dca8da461ad16c51edb1b54db`  
		Last Modified: Fri, 25 Sep 2020 21:56:04 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5f57d3977a167dd34eb772bba47e7e9c6588a50894ca52a39a7af2bb6991c0`  
		Last Modified: Fri, 25 Sep 2020 21:59:52 GMT  
		Size: 197.0 MB (196993611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63c9a9e0c23477271d231cc59fa3f3289a5f3a080c5a2c2a0117c467faec4d8`  
		Last Modified: Fri, 25 Sep 2020 21:56:04 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
