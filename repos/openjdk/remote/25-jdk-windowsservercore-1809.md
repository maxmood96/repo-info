## `openjdk:25-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:9e1c108ed497de85aa7039e774e29ed1421e743d40f465fc5fb004919e1e0a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `openjdk:25-jdk-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull openjdk@sha256:6b0abeed33d2586009790db5a2b573b361a2dad84edf65a7321c52d1cd583e26
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345403027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c648b07cb0f663ac18da234a22263397cb87dc1e76b90aa99397423848a7a46b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Mon, 10 Mar 2025 21:05:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 10 Mar 2025 21:06:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 10 Mar 2025 21:06:17 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 10 Mar 2025 21:06:24 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 10 Mar 2025 21:06:25 GMT
ENV JAVA_VERSION=25-ea+13
# Mon, 10 Mar 2025 21:06:25 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_windows-x64_bin.zip
# Mon, 10 Mar 2025 21:06:26 GMT
ENV JAVA_SHA256=5182d7ac4519ceda5c809ccaa65ed9f2bea331524a65f59c3fccfe52fc878ac6
# Mon, 10 Mar 2025 21:06:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 10 Mar 2025 21:06:58 GMT
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
	-	`sha256:00737b3a8a0e4dbb1197b8d6703f7d279f6e2872a2e4ea11b93890b4b1ac56c1`  
		Last Modified: Mon, 10 Mar 2025 21:07:03 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7eee08974d42d857025b082f974db6bcc575b980b2144d8d89eb0127fe15c87`  
		Last Modified: Mon, 10 Mar 2025 21:07:03 GMT  
		Size: 358.1 KB (358082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f233dd76d3d3e8bcb7df274d85a7275c78c7f3ec66027621914bcbe23e970a77`  
		Last Modified: Mon, 10 Mar 2025 21:07:03 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225b57d039a3280f9eaf74af2f090617586c3b1a4294775b5ac9d88889e2fcd5`  
		Last Modified: Mon, 10 Mar 2025 21:07:03 GMT  
		Size: 346.4 KB (346398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8151a594bd487d47d360c7c2a6d733f02db300eaade172645ed3f25cb95a3a2f`  
		Last Modified: Mon, 10 Mar 2025 21:07:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeca9f2a4ec5c7eea52403d5f2fe76fb165087c1c6c2dffe247faae113191439`  
		Last Modified: Mon, 10 Mar 2025 21:07:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75af185aa72b27a73380f26a4788b4413611e19b3810eaa64160a8c187d7c197`  
		Last Modified: Mon, 10 Mar 2025 21:07:02 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47a55f4a2e2624bdb72af08d897a9bdf8c3a65a2d6f11e7e16cb71b562509eb`  
		Last Modified: Mon, 10 Mar 2025 21:07:13 GMT  
		Size: 207.8 MB (207781969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4179900255f926f8eb3341b42b0869621e61219dad6add37aa7adbf93733ab6`  
		Last Modified: Mon, 10 Mar 2025 21:07:02 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
