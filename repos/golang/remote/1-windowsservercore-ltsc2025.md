## `golang:1-windowsservercore-ltsc2025`

```console
$ docker pull golang@sha256:0cea11356209922bd5570fe841effd2f2ef7ea88e097e2d745acaedb9cc674c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `golang:1-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull golang@sha256:0cd7284d1a75bd5ca0001aafef67e859f8b6a48dfa9d85a3bf087ad7ee1185d9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3334475318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2d1d8cfeaf7158d3f310edb13c2e59aff2917e37de99f9c49860a65ff3ebab`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Wed, 05 Nov 2025 20:19:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 05 Nov 2025 20:19:09 GMT
ENV GIT_VERSION=2.48.1
# Wed, 05 Nov 2025 20:19:09 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 05 Nov 2025 20:19:10 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 05 Nov 2025 20:19:11 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 05 Nov 2025 20:20:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 05 Nov 2025 20:20:31 GMT
ENV GOPATH=C:\go
# Wed, 05 Nov 2025 20:20:37 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 05 Nov 2025 20:20:39 GMT
ENV GOLANG_VERSION=1.25.4
# Wed, 05 Nov 2025 20:22:29 GMT
RUN $url = 'https://dl.google.com/go/go1.25.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '6dad204d42719795f22067553b2b042c0e710b32c5a00f6c67892865167fdfd0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 05 Nov 2025 20:22:30 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43ba41e1bd5744c100a3321583dfdf60bb66e5b9d3e20a2872ee01a2ae1e014`  
		Last Modified: Wed, 05 Nov 2025 20:53:15 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571ce539edec03691ae1054fbdb0f4f0bd1847490f536dc7f62709057b574678`  
		Last Modified: Wed, 05 Nov 2025 20:53:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f702178aaf578c5e2a6f4b03c05ed03bdfe8c427a60a87ffc970245d633962`  
		Last Modified: Wed, 05 Nov 2025 20:41:35 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452e404f411d9e74918e845019e6c91f24e6238ad4fd293bb67866eebf5fa357`  
		Last Modified: Wed, 05 Nov 2025 20:53:23 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61e7b91697d93519ca6e986a8b9027aa195bc8a6ad0c444f814a6ed542eeefa`  
		Last Modified: Wed, 05 Nov 2025 20:53:26 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a7afdfef4209b11a3739cca3e17c9eb4f5b6587ca1f83f80c457b7bbf321bf`  
		Last Modified: Wed, 05 Nov 2025 21:10:59 GMT  
		Size: 51.2 MB (51249860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bf9a88cf1c2214f52c93af754a7a28aca0aa7ae52d2978f082f89f69062dab`  
		Last Modified: Wed, 05 Nov 2025 20:41:36 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4b5a35a9d7770887e0f118604c342b0ab5e4d5b924c5e4c10262d528677f65`  
		Last Modified: Wed, 05 Nov 2025 20:41:36 GMT  
		Size: 326.7 KB (326737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646db1732fffefcbd3091c35e02599cad5fae36fa07175cd24693d46c049f10c`  
		Last Modified: Wed, 05 Nov 2025 20:53:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e83c7d4abd8376e7bd4b51615db7904a491bbf711e0d7221a2401a1270b562`  
		Last Modified: Wed, 05 Nov 2025 20:41:43 GMT  
		Size: 62.5 MB (62541043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf04921832c85967470623a3edf659aca6205526367cccb00c9335d076bb908a`  
		Last Modified: Wed, 05 Nov 2025 20:41:29 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
