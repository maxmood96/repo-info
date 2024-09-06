## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:abf4273e64ca7c79b7a002a5ac99df9e7161d42994a8c87b6a3479bcc2d949a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `golang:1-windowsservercore` - windows version 10.0.20348.2655; amd64

```console
$ docker pull golang@sha256:7da3184bfc53795e7190cf1ede9b03a52758d238cae4f7d0548eba68167b7c34
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2244849105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dfab1d9c4c0e2121fa200c29e7cfa1455a445021edcd82e0095cae613bc7b2c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Thu, 05 Sep 2024 22:03:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Sep 2024 22:03:02 GMT
ENV GIT_VERSION=2.23.0
# Thu, 05 Sep 2024 22:03:02 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 05 Sep 2024 22:03:03 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 05 Sep 2024 22:03:04 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 05 Sep 2024 22:04:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 05 Sep 2024 22:04:15 GMT
ENV GOPATH=C:\go
# Thu, 05 Sep 2024 22:04:22 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Sep 2024 22:04:23 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 22:07:09 GMT
RUN $url = 'https://dl.google.com/go/go1.23.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '32dedf277c86610e380e1765593edb66876f00223df71690bd6be68ee17675c0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 05 Sep 2024 22:07:11 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4b9ac7f54856109dff16a7de3711899c9dea10444da64dce2dc711d63d5481`  
		Last Modified: Thu, 05 Sep 2024 22:07:16 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa703eb97cca559a72cd655d6bb5429354a1a0597723a81a7207d4c01e1676de`  
		Last Modified: Thu, 05 Sep 2024 22:07:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3162ff7c31ab01250facf8bde72747c2031f5b600c2c2ba3916a9a8cfc255e1`  
		Last Modified: Thu, 05 Sep 2024 22:07:15 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3b8f1803e0a86ebf7ad2c747dab8b5c46574697abfecee0f1c8bf580c807fc`  
		Last Modified: Thu, 05 Sep 2024 22:07:15 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4cecac8a156f55c25bd3e8d863857d71e744e28cac8311a0348d6ebc18a6cdc`  
		Last Modified: Thu, 05 Sep 2024 22:07:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa825b98b3f41765cfc4b04c689e6a230963488216b4b4162629dee6be5c2e1`  
		Last Modified: Thu, 05 Sep 2024 22:07:18 GMT  
		Size: 25.4 MB (25449974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a0f821d22ab894e4f9ed4c80df13adc3c5f4306228b7b4f5ab2c43a3e2fb0b`  
		Last Modified: Thu, 05 Sep 2024 22:07:14 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dd1bbe9d4095241910d3e1bbe41dc96172f77676b9efe921974d789575b3db`  
		Last Modified: Thu, 05 Sep 2024 22:07:14 GMT  
		Size: 313.5 KB (313539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca96ab3bf553787b8b55e9d6619558c343d4072214e5025a705fce745353bdf`  
		Last Modified: Thu, 05 Sep 2024 22:07:14 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45018d30b477d340942ef4990c4cc2eac096521b7631ec6150e1048099859d34`  
		Last Modified: Thu, 05 Sep 2024 22:07:25 GMT  
		Size: 77.3 MB (77310164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a37e434eb28827e1b1320df4ca3bb7067c0f103dbc31e4b73053831017eb2c`  
		Last Modified: Thu, 05 Sep 2024 22:07:14 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull golang@sha256:4a5b35174de376ff0e7c58d9910a32c240416c25ee60ac2e2b9b95990c74bcc3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348693332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a4fdc84fb080fa55642b74b93b818153253f19a37de3b64464309eca01390d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Thu, 05 Sep 2024 22:02:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Sep 2024 22:02:52 GMT
ENV GIT_VERSION=2.23.0
# Thu, 05 Sep 2024 22:02:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 05 Sep 2024 22:02:54 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 05 Sep 2024 22:02:54 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 05 Sep 2024 22:04:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 05 Sep 2024 22:04:47 GMT
ENV GOPATH=C:\go
# Thu, 05 Sep 2024 22:05:06 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Sep 2024 22:05:07 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 22:07:57 GMT
RUN $url = 'https://dl.google.com/go/go1.23.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '32dedf277c86610e380e1765593edb66876f00223df71690bd6be68ee17675c0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 05 Sep 2024 22:07:59 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb8c096a9d06225e7c889d8ed002ca1c50421c0f34b0b8b3e8b4ea048d920d2`  
		Last Modified: Thu, 05 Sep 2024 22:08:04 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac04326ddb12b7249918dae8d63568e83648cebb1ebaab3e27d9bdf0ab2d105`  
		Last Modified: Thu, 05 Sep 2024 22:08:04 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84092623c4ee88d812620c04b362fe3b8f2221ff0a9aceb9cf8ea8bed684ebbf`  
		Last Modified: Thu, 05 Sep 2024 22:08:04 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97283a1f73280b43e5ae13ffa8eb94fa552d3e5d0f2376c44aff65985458612`  
		Last Modified: Thu, 05 Sep 2024 22:08:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512251c219493d96cfdae2d80614118e0a187101add6d17adb6c0b67f6e02d3d`  
		Last Modified: Thu, 05 Sep 2024 22:08:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c8180dd8efe9e0a20ce5f811be64c1b00e277769990448bea254d5fe350c79`  
		Last Modified: Thu, 05 Sep 2024 22:08:06 GMT  
		Size: 25.6 MB (25608723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dae7fc60f95d9ee92b0419f9f47fbf03345861c1d51ecddc8b7c19bfefe6452`  
		Last Modified: Thu, 05 Sep 2024 22:08:02 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e19c1a7a3ab3cd2b2e15c1462c94016f6d72e8cdb20586b58918e7b60df6cda`  
		Last Modified: Thu, 05 Sep 2024 22:08:02 GMT  
		Size: 364.9 KB (364934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec723699b81cdc8732b755ca4ceb1757b521d58ed523b0cdcff9713ed1ad00d`  
		Last Modified: Thu, 05 Sep 2024 22:08:02 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600ddea38b1a4f970fbbbd2fb72b4f003f1aa51c0c2a118199f4bfcdd74a20ab`  
		Last Modified: Thu, 05 Sep 2024 22:08:13 GMT  
		Size: 77.5 MB (77505916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3dbec01f9a91ae643f00a9b94aa1797d9043ce15f2bfc5b84e0f5aca77af4b`  
		Last Modified: Thu, 05 Sep 2024 22:08:03 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
