## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:4e87eb8676771a26cd45d41dd144064b21778973404d2fab908160635c8f4be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:0fd5b1c7cf1fb58f2dfd810db73faaf8cf7199f8e472f37c951c15052edb0c5c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2246354254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c67bba17c66622f9a5260fe102a790ad52976005141c27126ab3e0a7c34eee`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:38:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:50:52 GMT
ENV GIT_VERSION=2.48.1
# Tue, 12 May 2026 23:50:53 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 12 May 2026 23:50:54 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 12 May 2026 23:50:55 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 12 May 2026 23:51:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 May 2026 23:51:09 GMT
ENV GOPATH=C:\go
# Tue, 12 May 2026 23:51:14 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 May 2026 23:51:14 GMT
ENV GOLANG_VERSION=1.26.3
# Tue, 12 May 2026 23:52:41 GMT
RUN $url = 'https://dl.google.com/go/go1.26.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '20d2ceafb4ed41b96b879010927b28bc92a5be57a7c1801ce365a9ca51d3224a'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 12 May 2026 23:52:41 GMT
WORKDIR C:\go
# Wed, 13 May 2026 00:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2026 00:33:00 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 13 May 2026 00:33:00 GMT
ENV CADDY_VERSION=v2.11.3
# Wed, 13 May 2026 00:33:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 May 2026 00:33:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 May 2026 00:33:18 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e72ddab0326e6089ca74907ae3ac383e56049d5df737a07aea5f46d67a27c95`  
		Last Modified: Tue, 12 May 2026 23:39:44 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c786151110a633b23a3d5a21f6d68fa1c85ce68ee08ef2bdfc5b6063bae53eed`  
		Last Modified: Tue, 12 May 2026 23:52:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2943e972166905753bf6aeb1a45c4c85d10b3ab89d9cc65b6329316ccf931e`  
		Last Modified: Tue, 12 May 2026 23:52:53 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c49d75a1ad63b82f5e3eafbf0c69d418743bbc9fe9695d29af5cfb8fa331f3`  
		Last Modified: Tue, 12 May 2026 23:52:53 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1803b15b0f5c1e461aaf31398c09ce51da901213b18d89c44358f1ce67a5a1`  
		Last Modified: Tue, 12 May 2026 23:52:53 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de632000c1f51a8288200e7bd95871971165d705b9bc807d44879ed90d1fa1c3`  
		Last Modified: Tue, 12 May 2026 23:52:59 GMT  
		Size: 51.4 MB (51354733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cdad373139589a9a7f1e20aed9122a11c58a74893f40afaedc05435b6005c1`  
		Last Modified: Tue, 12 May 2026 23:52:51 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c815b70192733d3edbd92533de648fa2f307977af6dd4f5ce5fe4f5dbe64ff`  
		Last Modified: Tue, 12 May 2026 23:52:51 GMT  
		Size: 349.6 KB (349644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2fcb2eb8a1331c4db4075a6a31bc452f100a513231d87ab045018ff2b6d58e`  
		Last Modified: Tue, 12 May 2026 23:52:51 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1760b032a2aec7609f8d0d4d8f235347e97673aee9f43fc3c0971fed2f3c7f`  
		Last Modified: Tue, 12 May 2026 23:53:02 GMT  
		Size: 69.9 MB (69911750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b43d31166ffdff0744efdb2fd7a85c80822f2891fa2e1b9ff392ccabc6eab3e`  
		Last Modified: Tue, 12 May 2026 23:52:51 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c81e64041780a2015069d4631707cc126553989405a681b8822e98bb25df6fb`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fe6fcd731b5758c509d2cbde7f5930f2114f54df3f6c7d37734aa06db33535`  
		Last Modified: Wed, 13 May 2026 00:33:24 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870627491f8876a758f8ea17d0e17e9bd6284e8fb2f9e2f437c561a15f0a3f73`  
		Last Modified: Wed, 13 May 2026 00:33:24 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6823dcb3d7d494b22a20c68839b687c2e3fa40e20614990aae0bb00c847b59d5`  
		Last Modified: Wed, 13 May 2026 00:33:24 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2da595d020a64e4526bafacff80eafce3b604d63064cf25b1ca9b89512db9ac`  
		Last Modified: Wed, 13 May 2026 00:33:25 GMT  
		Size: 2.3 MB (2300268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94cf7a011201af44a95c582430934b50c71a2e5ad94f6cc94579ef4ca3bcce5`  
		Last Modified: Wed, 13 May 2026 00:33:24 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
