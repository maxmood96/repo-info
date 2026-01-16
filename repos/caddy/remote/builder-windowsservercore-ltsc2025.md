## `caddy:builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:052536bfc3b13b1f069b6e43c3fbad3610fbdede99230ba7d03c292ed077787a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `caddy:builder-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull caddy@sha256:9157bf154bf9d4477d7246ed17dc3fb84d4b612e6bde6672dcdd609fdec39e7e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1612306457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8df109c56180a661fed204700378acf972129bf1d92dc71f6dea0d1c7e6a56f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Thu, 15 Jan 2026 19:34:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Jan 2026 19:34:24 GMT
ENV GIT_VERSION=2.48.1
# Thu, 15 Jan 2026 19:34:25 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Thu, 15 Jan 2026 19:34:26 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Thu, 15 Jan 2026 19:34:27 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Thu, 15 Jan 2026 19:35:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 15 Jan 2026 19:35:08 GMT
ENV GOPATH=C:\go
# Thu, 15 Jan 2026 19:35:14 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 15 Jan 2026 19:35:15 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:36:38 GMT
RUN $url = 'https://dl.google.com/go/go1.25.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '19b4733b727ba5c611b5656187f3ac367d278d64c3d4199a845e39c0fdac5335'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 15 Jan 2026 19:36:39 GMT
WORKDIR C:\go
# Thu, 15 Jan 2026 22:37:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Jan 2026 22:37:48 GMT
ENV XCADDY_VERSION=v0.4.5
# Thu, 15 Jan 2026 22:37:49 GMT
ENV CADDY_VERSION=v2.10.2
# Thu, 15 Jan 2026 22:37:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Jan 2026 22:38:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 15 Jan 2026 22:38:12 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:56:33 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6a519eaac22a8e810614a54d1ecd7e172debe7d71f6e27ca1ba91bdc6a0f9e`  
		Last Modified: Thu, 15 Jan 2026 19:45:59 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3484d141a3d44935a72760270d4f6787bbe4cb0a32e834e840563a8475284d24`  
		Last Modified: Thu, 15 Jan 2026 19:45:59 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a4d7e64245aaea9d2fb7e300b6b88fcfa0ab8772b159b7fa10c961614f009f`  
		Last Modified: Thu, 15 Jan 2026 19:45:59 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b180294a8ef453ef91144aefda6c2e229b04efcfbdb95eab84205d8a65efd9`  
		Last Modified: Thu, 15 Jan 2026 19:45:59 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf89600227a0242479da3c0ae3a845b2b51c2833a42c2472f7e2b259315f5ca`  
		Last Modified: Thu, 15 Jan 2026 19:45:59 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5964e8cbe72df39254ea3c852054cd26c479539b1e7559f92f1864adc4f0fe3`  
		Last Modified: Thu, 15 Jan 2026 19:46:05 GMT  
		Size: 51.2 MB (51244732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bc7300c1c68770859c4873c9728130f2acab3a6b69c81c88a3851fa61b7e70`  
		Last Modified: Thu, 15 Jan 2026 19:45:59 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2783588cc72ed2dde28deae4066216333e60f144bed1e46a6a1371f44f8c9d7d`  
		Last Modified: Thu, 15 Jan 2026 19:45:59 GMT  
		Size: 373.9 KB (373923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd53c6443492192c1e4fb1d656f1a9f1df39d5baa327d49554328c37470b032`  
		Last Modified: Thu, 15 Jan 2026 19:45:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad2e2cac32485cbbf78ff68f8d974f3149d95c10d58c27c9f46fe3d5cdba801`  
		Last Modified: Thu, 15 Jan 2026 19:46:07 GMT  
		Size: 62.6 MB (62594900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ebd4c763d8b6cd3b0be5903a8169fce4c2a3b16ed7198f56bccc2f2ce70802`  
		Last Modified: Thu, 15 Jan 2026 19:45:59 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd097a3d22e5126c1337248e9d425e2b3cd6e1584dbc2a01397daa6e7f36097`  
		Last Modified: Thu, 15 Jan 2026 22:38:24 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b947ece6ae957caa9fd6051c70da65f05070c5b6392d61356f9e74dd7ee3bf6`  
		Last Modified: Thu, 15 Jan 2026 22:38:24 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79b9428f2690e52fe375daee6433b2e1c3a594d3bbaa0e78bd3e0a25db825e9`  
		Last Modified: Thu, 15 Jan 2026 22:38:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:decf25320dfeb857ab09a05ec281c35de5a8f62a234efebdb47493d37bfe4734`  
		Last Modified: Thu, 15 Jan 2026 22:38:24 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064da5f4fc99e82a69c22b76311d52b370ac360c8cb5c54c2f989cbdb3f1dca3`  
		Last Modified: Thu, 15 Jan 2026 22:38:25 GMT  
		Size: 2.3 MB (2315429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d3a0d833191ed46028c831a8b8ac146257742b2a7f95bd1763894b080af1de`  
		Last Modified: Thu, 15 Jan 2026 22:38:24 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
