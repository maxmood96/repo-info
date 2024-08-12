## `openjdk:23-rc-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:eb11e7c628f0a271abfa3e9dfd9c3860fd5c70e7622b45fa53d57bb42f77b260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `openjdk:23-rc-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull openjdk@sha256:3d5f49168b53daa46c74b66255519690b9e1a41a40d8958256fd532e610ddc15
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346726226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd78b686d518b28aa7e77bd1f2083261fbff025cbefae4fdfed745a6433625a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Mon, 12 Aug 2024 17:58:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Aug 2024 17:59:07 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 12 Aug 2024 17:59:08 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 12 Aug 2024 17:59:14 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 Aug 2024 17:59:15 GMT
ENV JAVA_VERSION=23
# Mon, 12 Aug 2024 17:59:16 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_windows-x64_bin.zip
# Mon, 12 Aug 2024 17:59:16 GMT
ENV JAVA_SHA256=b18897bec6b1c6e0f639d95757eb0e3b0ec3d69720f6e4631874f2f9408075c5
# Mon, 12 Aug 2024 17:59:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 Aug 2024 17:59:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1c9a02e3c8f8cb45b925d1c139e2ff509dc1f6e1782725286cdc09a41be716`  
		Last Modified: Mon, 12 Aug 2024 17:59:48 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48af13aa08e66390b1585c6370dc8b7325cb85edffda7548a28b88d26224f436`  
		Last Modified: Mon, 12 Aug 2024 17:59:48 GMT  
		Size: 358.0 KB (357958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9f4a6965f57f0a2710b219b543b2ce754cb755a90e2798476b54850ac0e9aa`  
		Last Modified: Mon, 12 Aug 2024 17:59:48 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818c8d2c75047be0c5680a738161ad0afba30702d65f51b5df725ed8c730d233`  
		Last Modified: Mon, 12 Aug 2024 17:59:48 GMT  
		Size: 344.1 KB (344133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228422811aaf5c8e6d93cfbe98cf48522a7f6eee8994d8d436e578fc532adf70`  
		Last Modified: Mon, 12 Aug 2024 17:59:46 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0538bb7ec51bd46a824a0b2b6c7cf99b426121ad22d61d758152a1fd408d61f`  
		Last Modified: Mon, 12 Aug 2024 17:59:46 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a206f37244844cb90b5ce972c3bcfed0c1fbe5b82e38d2b4a14220cc09e1aa8e`  
		Last Modified: Mon, 12 Aug 2024 17:59:46 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d867588610fd6f723b8f672009b4c40a90af1052c60f3ff1e5935e1013cd1c`  
		Last Modified: Mon, 12 Aug 2024 17:59:56 GMT  
		Size: 206.4 MB (206415936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb1d86c840e66900d109b6dc2cfdf3324f70d601fa1de819503ef1020e9b17e`  
		Last Modified: Mon, 12 Aug 2024 17:59:46 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
