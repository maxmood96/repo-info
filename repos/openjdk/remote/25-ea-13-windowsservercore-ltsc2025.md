## `openjdk:25-ea-13-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:44248ccab515e126aec4fa956ff43b40f2ab09db5456944f3274271d1a6faaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `openjdk:25-ea-13-windowsservercore-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull openjdk@sha256:9f0ae4973fe934969fd7235b1a8f0d729e20cc678d7549371b4299910b750f8a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3025171627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b0a5cd2f8aa20ce8bd85e0decd3fc5c894ceb12c8b78cf47c46532585b0200`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Mon, 10 Mar 2025 21:10:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 10 Mar 2025 21:10:11 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 10 Mar 2025 21:10:12 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 10 Mar 2025 21:10:19 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 10 Mar 2025 21:10:21 GMT
ENV JAVA_VERSION=25-ea+13
# Mon, 10 Mar 2025 21:10:21 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_windows-x64_bin.zip
# Mon, 10 Mar 2025 21:10:22 GMT
ENV JAVA_SHA256=5182d7ac4519ceda5c809ccaa65ed9f2bea331524a65f59c3fccfe52fc878ac6
# Mon, 10 Mar 2025 21:10:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 10 Mar 2025 21:10:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d6162003cfa1060e50ca2e92849e0ac2ed9ead55fb02c6c255e0fe82417ffe`  
		Last Modified: Mon, 10 Mar 2025 21:10:48 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd44eebad473320c6fb7d9c39f9317dfef5aaae34613d73a17c0beb859b1c259`  
		Last Modified: Mon, 10 Mar 2025 21:10:48 GMT  
		Size: 394.9 KB (394858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09bc3d99504d0dca5d870e329aa5ba19abaa23dbdd8d1e8cd8c092c3f7314c21`  
		Last Modified: Mon, 10 Mar 2025 21:10:48 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ec08f34cb8d4e3b9a7ff4f988b1effc4eeb847e809f44979f88897666d9513`  
		Last Modified: Mon, 10 Mar 2025 21:10:48 GMT  
		Size: 379.3 KB (379311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e27f889002e47b8942b9887d714a0731d50e8516c0b98c71607eddfaf9fa11b`  
		Last Modified: Mon, 10 Mar 2025 21:10:47 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5763c02d9a26dd15d690f6c8ae3e800d98b5d02524775b504d6e28cb6faa9c`  
		Last Modified: Mon, 10 Mar 2025 21:10:47 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcca8a81cf71935833dfe918867ae9443b041afb5ba1fa19d010603f9c0700c`  
		Last Modified: Mon, 10 Mar 2025 21:10:47 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee54ee92adf4f418c221b89341a863526fbf0285efc127e354179bedf380d68`  
		Last Modified: Mon, 10 Mar 2025 21:10:59 GMT  
		Size: 207.8 MB (207801918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0841fda61205c5f139bbf554cc41f03626e0c8446f09a95ca5b40df90fb4726e`  
		Last Modified: Mon, 10 Mar 2025 21:10:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
