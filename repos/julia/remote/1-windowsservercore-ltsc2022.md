## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:a099e3722534579320f31c8b96ff15d0094d4bae515079861aea58ef93bc7c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull julia@sha256:604100623cd654b1c1c0873a84347f12a5280d25312bb643a7bdc1a478e32285
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2326930671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31804b66f0ee7e6ee0b5b19134bfb6cfbd29129933ef6d0ccec0959a757c9373`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Wed, 10 Jul 2024 17:08:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 17:08:13 GMT
ENV JULIA_VERSION=1.10.4
# Wed, 10 Jul 2024 17:08:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.4-win64.exe
# Wed, 10 Jul 2024 17:08:15 GMT
ENV JULIA_SHA256=c1b659abc90991dcbdf461f33cae483501da736fc223c11d4c51f337338ccb21
# Wed, 10 Jul 2024 17:09:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Jul 2024 17:09:04 GMT
CMD ["julia"]
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
	-	`sha256:57bfe423cc5ab1b30a8e822bae6c7edc53d8e92979f899bc889e6252681f37c8`  
		Last Modified: Wed, 10 Jul 2024 17:09:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c922f121d2b94bdbbe8686ad7049698933c8e437ab93769d4f7d3e6aad69771d`  
		Last Modified: Wed, 10 Jul 2024 17:09:08 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b08d78a91c11c628ef855ecec5d5abd6572272f7ba277f6c7ef761a502e6f3d`  
		Last Modified: Wed, 10 Jul 2024 17:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa2559e2b24b4f012a9d6b4a25dbc2caa4bed6507e70b4c4681fc2bcd9914d2`  
		Last Modified: Wed, 10 Jul 2024 17:09:08 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013d1392a5a50b882628a1b4abec81419a70a68013a3f7ad6ae71ca42f885797`  
		Last Modified: Wed, 10 Jul 2024 17:09:32 GMT  
		Size: 187.3 MB (187323914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640299acf02d96d1f60709136f9f954e1b02f738c6d2ff7e79161598ed2ea776`  
		Last Modified: Wed, 10 Jul 2024 17:09:08 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
