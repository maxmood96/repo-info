## `openjdk:23-jdk`

```console
$ docker pull openjdk@sha256:34b683492e09d90146b4189e26b0a628941bfbd0927923d753ea6981f53f54c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `openjdk:23-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:13ee6eb48c4bd8d73d58bb9db45484e278935d42ddf9886bcac47107c7b0bcb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 MB (297560436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82fdd39c5e63c8735a9343b5e0660545e48d95b0d4a53c0d1f79d1ea5a338076`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:04 GMT
ADD file:9bcef05fa351e2fb72a4b6052a0252eeaa2cff794ed089a482670c67961d2e90 in / 
# Fri, 08 Mar 2024 19:21:04 GMT
CMD ["/bin/bash"]
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 04 Apr 2024 18:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+17
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='e7d451c3caeb76083337f090da37588acb90bb60417bff99ef160a3a8b730bfd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ede1afd67be11e1e99e13b78f8b3159c14107cc919920d0e1e30636f67b92b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:972029ff9873af36c6c0fcee05b14acbc57a61ecd0b8bf86b167bdf46f973823`  
		Last Modified: Fri, 08 Mar 2024 19:22:31 GMT  
		Size: 49.0 MB (48978454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f79db7cdc29ebc9132d9674a8ebe3ab1650b04f8332355d709ba3724c0d1a3`  
		Last Modified: Fri, 05 Apr 2024 17:52:39 GMT  
		Size: 37.7 MB (37737131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734aa191b9dfe5279c951699a4a480ca95f4406a97147f2de83b6b8083544a73`  
		Last Modified: Fri, 05 Apr 2024 17:52:43 GMT  
		Size: 210.8 MB (210844851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:530d20b94339952ccec8043b29f52a7360bf149ef9095f9e5c2c405326f95711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3349426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11465c6433a0ac736805aade037255a9977cb3f1e76836af8514e28161feab53`

```dockerfile
```

-	Layers:
	-	`sha256:43949525415390922a9335de10f43e495179a5380ba0237a20bd1614c5582bf2`  
		Last Modified: Fri, 05 Apr 2024 17:52:38 GMT  
		Size: 3.3 MB (3329538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:964fe03502b2698b174f1b154fb46927aff4062e51f26e82c2f564ea876aa945`  
		Last Modified: Fri, 05 Apr 2024 17:52:38 GMT  
		Size: 19.9 KB (19888 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:67d7d255581d4a3fff1e8d38f5a71cd04751f4d024ac0df39212094ed105e2dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294538990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c38096ad04f7a65c6bd82f22c71df3a1656552da2db7740a2538209f4910196`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 19:48:53 GMT
ADD file:71724b501850c3e6cd72efc58b3430394f691a428c2c62755eac0b93c5579f35 in / 
# Fri, 08 Mar 2024 19:48:53 GMT
CMD ["/bin/bash"]
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 04 Apr 2024 18:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+17
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='e7d451c3caeb76083337f090da37588acb90bb60417bff99ef160a3a8b730bfd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ede1afd67be11e1e99e13b78f8b3159c14107cc919920d0e1e30636f67b92b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c53b3bc8702e4b172b3fdde99731082a493b5f5fdd7e9632b3cf7dea02a52b4`  
		Last Modified: Fri, 08 Mar 2024 19:49:57 GMT  
		Size: 47.7 MB (47664888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71597242e3bc84850918d978b72bcf84c5867bfb6441051c67b805dca13e66a`  
		Last Modified: Sat, 16 Mar 2024 15:50:44 GMT  
		Size: 38.1 MB (38140694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaca8e4b43c229d5798a3d44bb80d4f0d0d96c6deb2bb29d044ffcc13603e29a`  
		Last Modified: Fri, 05 Apr 2024 17:56:06 GMT  
		Size: 208.7 MB (208733408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:ceaeecf7d121512679c9dbfe0acec28e25f53405dce223a03521b46f5608c319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b766374b27eb2682bc21c321147de76ef779c8ce39a0d40a2301cff49a0ce6d0`

```dockerfile
```

-	Layers:
	-	`sha256:4d85b961ce4e2c3d8ca33807155c65c8d754e023d17256d6bef5910b0ba32e89`  
		Last Modified: Fri, 05 Apr 2024 17:56:02 GMT  
		Size: 3.3 MB (3326760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0600f71b9fe3b81a3dbbd14b65c5c6104874ebd602fad95743926f6e237616fe`  
		Last Modified: Fri, 05 Apr 2024 17:56:01 GMT  
		Size: 19.8 KB (19760 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk` - windows version 10.0.20348.2340; amd64

```console
$ docker pull openjdk@sha256:c2ed2016840fd187e0c5aaf6f904ca339ed4d00fa27ae5979a565773be356b5d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2163941614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93138e46ab23fd558e679d4d53df6c019e7c1605742f65ecbd42e753ad014a8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Fri, 05 Apr 2024 17:52:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 05 Apr 2024 17:53:57 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 05 Apr 2024 17:53:57 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 05 Apr 2024 17:54:04 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 05 Apr 2024 17:54:04 GMT
ENV JAVA_VERSION=23-ea+17
# Fri, 05 Apr 2024 17:54:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_windows-x64_bin.zip
# Fri, 05 Apr 2024 17:54:06 GMT
ENV JAVA_SHA256=d370ad95643e427d9a9f79c527dc3dfbd3fa07ebda3684fe18acba87d4342d57
# Fri, 05 Apr 2024 17:54:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 05 Apr 2024 17:54:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29e6da9a119af4900ca32e7b72e122af663d0c124c61162d59efce181be7bf0`  
		Last Modified: Fri, 05 Apr 2024 17:54:46 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2260ed09da21f9844f71fe2f97d63be6d31052332d236c6d78f6525c097f3208`  
		Last Modified: Fri, 05 Apr 2024 17:54:46 GMT  
		Size: 509.0 KB (508964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eac57ad1d60d5d20bed6a8a531f654d28a38a043230a2226f7a4913192e8f97`  
		Last Modified: Fri, 05 Apr 2024 17:54:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0850ecf148b4540cf47e5c126725a34c47594df7bb9ccbd475ae0da660a0d992`  
		Last Modified: Fri, 05 Apr 2024 17:54:46 GMT  
		Size: 321.6 KB (321636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57467fcd890b73dd9072775adcb46283f46e151e9f013f84b6df594d2cb9d7ec`  
		Last Modified: Fri, 05 Apr 2024 17:54:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c3b845283c23d3a90f00bdf78916e544dd70f7165a1589b4f42db67bff108c`  
		Last Modified: Fri, 05 Apr 2024 17:54:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fa450c09a6088c806903d531b21ee15bf1c1d1bb582207065e44fd4168a4c4`  
		Last Modified: Fri, 05 Apr 2024 17:54:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6448a5c4e84a34dcc2a4253d4893a3527f73b68e5eafdde1b251edebf943091`  
		Last Modified: Fri, 05 Apr 2024 17:54:56 GMT  
		Size: 205.6 MB (205644308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:156db67afd9468920a2bcff930e5c27047b7a7e28d1d95af8fd2c258e2e98dbb`  
		Last Modified: Fri, 05 Apr 2024 17:54:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-jdk` - windows version 10.0.17763.5576; amd64

```console
$ docker pull openjdk@sha256:3f8090e06919ac5f12e476e155a73bd2e52d4d9fb023b04b73a4de3cf2eefac5
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2331645126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2682672378226828f8634bb12193791585e6707034d42ee0121fb98ac58fa541`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Fri, 05 Apr 2024 17:51:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 05 Apr 2024 17:54:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 05 Apr 2024 17:54:24 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 05 Apr 2024 17:54:53 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 05 Apr 2024 17:54:54 GMT
ENV JAVA_VERSION=23-ea+17
# Fri, 05 Apr 2024 17:54:55 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_windows-x64_bin.zip
# Fri, 05 Apr 2024 17:54:56 GMT
ENV JAVA_SHA256=d370ad95643e427d9a9f79c527dc3dfbd3fa07ebda3684fe18acba87d4342d57
# Fri, 05 Apr 2024 17:55:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 05 Apr 2024 17:55:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039e6816d763571d464037acbaf8db3f58940f1fbb948fc8a6b6607ccaa06674`  
		Last Modified: Fri, 05 Apr 2024 17:56:00 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8885e274de2bbb520f75cad69ef9e626290f7727ee88b0e334a5289d9170ef66`  
		Last Modified: Fri, 05 Apr 2024 17:56:00 GMT  
		Size: 500.6 KB (500622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b54bedf2041020077b0d71904ed0f3efeaf0586d44942feed5d8a5900756c70`  
		Last Modified: Fri, 05 Apr 2024 17:56:00 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54bb7f5c6781bda6ff00c6123489fa31b0f7437041b8870d5a3fd0c375cad04d`  
		Last Modified: Fri, 05 Apr 2024 17:56:00 GMT  
		Size: 352.7 KB (352682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c824f0ddab5d45814805ec16394cd619eb0d9248b373faf53dd88798e7f022c0`  
		Last Modified: Fri, 05 Apr 2024 17:55:58 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6e31143dcb1314952ecac4f64e51afc482cbc0db3c1725fb5331fe583b32c8`  
		Last Modified: Fri, 05 Apr 2024 17:55:58 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9ec713cd8620e5802431c467f53ca52c4e1bb10c85f7a6199e181afbbc9c50`  
		Last Modified: Fri, 05 Apr 2024 17:55:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74c8f6e2f7018e15e6de94774b1aed8fa8203c2e04efaa0c41de27a1713110e`  
		Last Modified: Fri, 05 Apr 2024 17:56:08 GMT  
		Size: 205.7 MB (205684100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f38581ad5c75f86347e515f59677dbed08553eae592d0b234d043c2217f0173`  
		Last Modified: Fri, 05 Apr 2024 17:55:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
