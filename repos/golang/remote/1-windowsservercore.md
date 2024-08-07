## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:3c3bb272ea95e2df45cd7d7006fc70c2de2f8de8b2abecefe7bc5e101a2b8af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `golang:1-windowsservercore` - windows version 10.0.20348.2582; amd64

```console
$ docker pull golang@sha256:7637c7373102d976b3cca870e77aece580b8f3ac03fd98e142c7ed6a934da849
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2237103691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7654f1dcb66a061d38b396d055408d4e3b1d85f73580b94311a157640d0b94f9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Tue, 06 Aug 2024 22:56:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Aug 2024 22:56:09 GMT
ENV GIT_VERSION=2.23.0
# Tue, 06 Aug 2024 22:56:10 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 06 Aug 2024 22:56:10 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 06 Aug 2024 22:56:11 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 06 Aug 2024 22:57:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 06 Aug 2024 22:57:20 GMT
ENV GOPATH=C:\go
# Tue, 06 Aug 2024 22:57:30 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Aug 2024 22:57:30 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 22:59:09 GMT
RUN $url = 'https://dl.google.com/go/go1.22.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '6023083a6e4d3199b44c37e9ba7b25d9674da20fd846a35ee5f9589d81c21a6a'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Aug 2024 22:59:10 GMT
WORKDIR C:\go
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
	-	`sha256:3ab43240dd2735372d70461d57a5491631d655ca1e301e5e9e5241f4d383f5ba`  
		Last Modified: Tue, 06 Aug 2024 22:59:15 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc03124665d1ed7f649046d5c428f6c6a51ac751a9b9351cb019450c5a3f2f29`  
		Last Modified: Tue, 06 Aug 2024 22:59:15 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387c0d6bad3dbd7733cc22b59a014d7693aed7a3410806b7c599911bcd121889`  
		Last Modified: Tue, 06 Aug 2024 22:59:14 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f96585631a593d5afb9e8c44e29f29637fd34b074c0c018634cd0797d846c0`  
		Last Modified: Tue, 06 Aug 2024 22:59:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b101c5e86f2618ac4a982a40275f332bf9e3bb3776a079104ce3c54737c578f`  
		Last Modified: Tue, 06 Aug 2024 22:59:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5ba128107217d579d9a32654f909e3989122d46cc3a0bdd874467cad8d8567`  
		Last Modified: Tue, 06 Aug 2024 22:59:16 GMT  
		Size: 25.5 MB (25451374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9f7e14c690501a1170f1397428dc368941e3ee35ae4ee4a172194a30d8dcc7`  
		Last Modified: Tue, 06 Aug 2024 22:59:13 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a267841d80890728c7b3ee800534c6c02fcf933aad5db3638c73be7c086bd033`  
		Last Modified: Tue, 06 Aug 2024 22:59:13 GMT  
		Size: 314.0 KB (314042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930959aa4e525dc6464a16f9f6ad649425f6148d0a4d8d80b825e4296369aed5`  
		Last Modified: Tue, 06 Aug 2024 22:59:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b089a5ae45e51abcb4164dc126b61d598e40ed6521b33a963cd2a65c3f5db9`  
		Last Modified: Tue, 06 Aug 2024 22:59:23 GMT  
		Size: 71.7 MB (71727545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014f7f8f75a716c9eb5c7d5bbbb5e317daa47b1f39c4f4bebec70d16599bed7d`  
		Last Modified: Tue, 06 Aug 2024 22:59:13 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull golang@sha256:1fe4ed239c2ce94d4fd1eaaa7cddc8953c8ade5bf1bba79648d6ba18b532d520
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336123924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ff9174fec453960d29f8723fa322bfeacdd3cf4b19ffc579e958ffdcc952da`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Tue, 06 Aug 2024 22:56:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Aug 2024 22:56:01 GMT
ENV GIT_VERSION=2.23.0
# Tue, 06 Aug 2024 22:56:02 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 06 Aug 2024 22:56:02 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 06 Aug 2024 22:56:03 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 06 Aug 2024 22:56:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 06 Aug 2024 22:56:46 GMT
ENV GOPATH=C:\go
# Tue, 06 Aug 2024 22:57:05 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Aug 2024 22:57:06 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 22:58:59 GMT
RUN $url = 'https://dl.google.com/go/go1.22.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '6023083a6e4d3199b44c37e9ba7b25d9674da20fd846a35ee5f9589d81c21a6a'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Aug 2024 22:59:00 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09177a2d8100731d191cc1f7268068fe9838aeb2c4082ff06b328709fd7ebf65`  
		Last Modified: Tue, 06 Aug 2024 22:59:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f430bf25eee4267b1d84ea64815fb55a7d7cf85c8fa78ddd8485a195fb00cc`  
		Last Modified: Tue, 06 Aug 2024 22:59:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0976710052c049e2f19bcbec09e706ab0805f3007984ffa21d58be92599740`  
		Last Modified: Tue, 06 Aug 2024 22:59:07 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8186263fc237d42bb6e9f2bdf27e324ce393fc351732137e2a6f0bf6af1a256`  
		Last Modified: Tue, 06 Aug 2024 22:59:07 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2b3aada17941bcb5f4d65c437730c3eb6330eafac2adfc5be0cfcb842b12d3`  
		Last Modified: Tue, 06 Aug 2024 22:59:07 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb29c5f1c6b570e746a18be662c5fed69c91c6f9cd49817ddd368ec3d00945b`  
		Last Modified: Tue, 06 Aug 2024 22:59:09 GMT  
		Size: 25.6 MB (25580557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9fe7afd5b5f0e04a762ae3584205d38d916b2a97b79b270145c6c999e92ac`  
		Last Modified: Tue, 06 Aug 2024 22:59:05 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f752cb947fcbfa05ceaf706a0e7d09de2c5f6fb064c02e3ba8c08605e18e9a`  
		Last Modified: Tue, 06 Aug 2024 22:59:05 GMT  
		Size: 342.4 KB (342379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5038a529a813e24653c828b04cedfb004652d03694ddf4285d057586181e3f`  
		Last Modified: Tue, 06 Aug 2024 22:59:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a4a42e8184621546ae9b99673a7b5f26572753cb40d4f37e5786941b715f63`  
		Last Modified: Tue, 06 Aug 2024 22:59:15 GMT  
		Size: 71.8 MB (71761086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d71452634c4b504306599ea0b3fa0e112063e9436c281ba1b78b961368864b1`  
		Last Modified: Tue, 06 Aug 2024 22:59:05 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
