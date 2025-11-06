## `caddy:builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:5ba51be16fa6232e354970d6fc6726a18146f34e2f71d642b8bb425abfb25aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `caddy:builder-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull caddy@sha256:8e1d46295c38f12e413e56f5fd0f7a1625a4ee3de502df28734d7b8556ea8ea1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3336790149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a0b4b6c075e78de2e935dfe10bb7dfb51cccbfec9d5a4866e6197deb70bdcc`
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
# Wed, 05 Nov 2025 21:14:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 05 Nov 2025 21:14:56 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 05 Nov 2025 21:14:57 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 05 Nov 2025 21:14:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 05 Nov 2025 21:15:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 05 Nov 2025 21:15:48 GMT
WORKDIR C:\
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
	-	`sha256:c356d2e6e98c0f2d996abaee176b80839874f9cb15a88235a1460ae41ca37317`  
		Last Modified: Wed, 05 Nov 2025 21:16:06 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5892de7d508a183b55c3f8cdb2c30440fe235863b5dab839858fd309a555583`  
		Last Modified: Wed, 05 Nov 2025 21:16:06 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83982486ec4487cfd2fdc26145da176722dde56cf1afce2efefedc963a56fb7`  
		Last Modified: Wed, 05 Nov 2025 21:16:06 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749bb70865567664e41dca22590113a302a57542be786513af41533b6722a70a`  
		Last Modified: Wed, 05 Nov 2025 21:16:06 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d967ca094f6dd499daa73e4bcf27fde920f79c9b92697db1fea9090b8d100b2`  
		Last Modified: Wed, 05 Nov 2025 21:16:06 GMT  
		Size: 2.3 MB (2308209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3c2d19e1364656e359ad528731f6b28effcca974387ed32502394a12c5cb66`  
		Last Modified: Wed, 05 Nov 2025 21:16:06 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
