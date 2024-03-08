## `openjdk:23-ea-12-jdk`

```console
$ docker pull openjdk@sha256:6bfb6b21be8fea7286ba77f5e8e436ac34a535296097e32c86ef8ddf2b1c83bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `openjdk:23-ea-12-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:3ea2e86e81b46d2204b93788c56e5db7a45a1cac44832a956518d24383dcda09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269475054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6611eca3b3d1ec7f4f8375e4128ebcefb5e3740cea7ee245f6b643362389844f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 29 Feb 2024 19:48:15 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 29 Feb 2024 19:48:15 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 19:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 29 Feb 2024 19:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 29 Feb 2024 19:48:15 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 19:48:15 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 19:48:15 GMT
ENV JAVA_VERSION=23-ea+12
# Thu, 29 Feb 2024 19:48:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/12/GPL/openjdk-23-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='892346bd29f50e248ab5980903e5759f73d8ac2b6ee0cd918e3acdb132eb8776'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/12/GPL/openjdk-23-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='3e927b03ed3af88337e11918d05955c72b71c1664dc5791ba4a6590329004657'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 29 Feb 2024 19:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14aba37ebec728775ced1deb331a7c05ee6362db42e61e927b64e8e4c4e0c3d`  
		Last Modified: Fri, 08 Mar 2024 19:49:20 GMT  
		Size: 15.0 MB (15024180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49391d877305ce61c6338d247f6f1f5b986d962c5d53fcbcadc2fda8745bcc7`  
		Last Modified: Fri, 08 Mar 2024 19:49:22 GMT  
		Size: 203.1 MB (203123454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-12-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:3bb9a566dc765efd82d7a09f62f1b0ac37a8ca1b94d276c775b6354c411015c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2291093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9939ce30c79633ef2a4d80b4f0c7faa8754a1ba5d35ed3117a56227fe6d48390`

```dockerfile
```

-	Layers:
	-	`sha256:7e9a2a990fc5c998f4dd854ee87118e7584f5b7645c128754250daf427f3738c`  
		Last Modified: Fri, 08 Mar 2024 19:49:20 GMT  
		Size: 2.3 MB (2271204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00b19aa5aa58ca2fed4f76cdfee20025f3a5457bb76c46b4efa2b1589b44e27c`  
		Last Modified: Fri, 08 Mar 2024 19:49:20 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-12-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c0a4915b1d12d912626856e7382f27bb14691a02939201f0518a483a7dcb3cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266778545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ab5438ee75257912158a9e6442d84eaab3e62f9c55e52e3e9bc960da9996c3`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 19:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 29 Feb 2024 19:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 29 Feb 2024 19:48:15 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 19:48:15 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 19:48:15 GMT
ENV JAVA_VERSION=23-ea+12
# Thu, 29 Feb 2024 19:48:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/12/GPL/openjdk-23-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='892346bd29f50e248ab5980903e5759f73d8ac2b6ee0cd918e3acdb132eb8776'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/12/GPL/openjdk-23-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='3e927b03ed3af88337e11918d05955c72b71c1664dc5791ba4a6590329004657'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 29 Feb 2024 19:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5b1d3eb6a012567065354e86eb0bac67a32e425e65bc6fe8b5cd84b95a0643`  
		Last Modified: Wed, 14 Feb 2024 11:04:46 GMT  
		Size: 15.7 MB (15691290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f210b4faf5e3ed18fc7cd05b43683bc9b9c838c30c274ecf0dfd0e67d027d79`  
		Last Modified: Thu, 29 Feb 2024 22:52:56 GMT  
		Size: 201.0 MB (201014341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-12-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:fcf5dbddda8e25a2efbe7966d67daf8c8332d2bdac1cf5cc126e5f4f68f274c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2289434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8132e61c1f0d3336aed381fa6955ebf1c5d00aaea2ff369508477312a26e3a`

```dockerfile
```

-	Layers:
	-	`sha256:af2d4a854bb2da1ff376b01070c9e5157777dbeab156a94076c711596ff9822a`  
		Last Modified: Thu, 29 Feb 2024 22:52:52 GMT  
		Size: 2.3 MB (2269674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f2ecbf7b5e52dc63e7fd057a64e06a5088beda06301c603bffc2885e30909a6`  
		Last Modified: Thu, 29 Feb 2024 22:52:52 GMT  
		Size: 19.8 KB (19760 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-12-jdk` - windows version 10.0.20348.2322; amd64

```console
$ docker pull openjdk@sha256:d8b78ea9b3b87c1fc7044623112b98403742f8ac19beebb9cb70b7cb446a5969
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2109390858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d438c9f7e5033e51af365cc8ba081e4884d063811786c9e23a33d373bd2d187e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Thu, 29 Feb 2024 22:50:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 Feb 2024 22:50:37 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 29 Feb 2024 22:50:38 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 29 Feb 2024 22:50:46 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 29 Feb 2024 22:50:46 GMT
ENV JAVA_VERSION=23-ea+12
# Thu, 29 Feb 2024 22:50:47 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/12/GPL/openjdk-23-ea+12_windows-x64_bin.zip
# Thu, 29 Feb 2024 22:50:48 GMT
ENV JAVA_SHA256=71a4b8ffa972cd355bf10024250c8f28d6992b430cd294744705cb5ebd2a5a41
# Thu, 29 Feb 2024 22:51:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 29 Feb 2024 22:51:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405df72f51a6afa806a89c0ba475d7c4fd79328d46f27d0f0925f2dd456f7a5d`  
		Last Modified: Thu, 29 Feb 2024 22:51:51 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baed81a0d8c1964c3429f0a2fddc4b858f23139eb00233120f8a1b55f5d8b15b`  
		Last Modified: Thu, 29 Feb 2024 22:51:51 GMT  
		Size: 489.7 KB (489747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8159aeef050c5a22d581cb4f99ab617dcbc8cb2b6d031fcb04207c3a1be26ae5`  
		Last Modified: Thu, 29 Feb 2024 22:51:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a720ea9c65ed6339442025970ecbc667240dd80fb0628f65ba7536e87fbace6`  
		Last Modified: Thu, 29 Feb 2024 22:51:51 GMT  
		Size: 334.8 KB (334847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4ce92f06f758799a6d7c662dfec43e7e55b595fe5d4a28639b19a698cd0a8d`  
		Last Modified: Thu, 29 Feb 2024 22:51:50 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc4b2fcc7c65384963d6b8b0b1bde38914163b0afbfba73c5e9608b960c0566`  
		Last Modified: Thu, 29 Feb 2024 22:51:50 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e404713c6ecc56fadc852c7d46007a6b8504bd9fffee1e5d8ef586e4c203ce`  
		Last Modified: Thu, 29 Feb 2024 22:51:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f76580c3cdc6e1ec8512ddd35bad9bdf0754f007be8ac03d39c01dcae1254de`  
		Last Modified: Thu, 29 Feb 2024 22:52:01 GMT  
		Size: 197.9 MB (197904325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4cdfcce5986b95b649b9d87d7024a4f784741281eef0cb83aaec273c7ffc9f`  
		Last Modified: Thu, 29 Feb 2024 22:51:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-ea-12-jdk` - windows version 10.0.17763.5458; amd64

```console
$ docker pull openjdk@sha256:d792210fa8ee46d3236504a9b0edf3caa3ce1432b45ee232ed11b35ada253872
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279199367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050a4538564fcbafcef21b86e4cee36002b4b566a3fefff5cdca63f189dec929`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Thu, 29 Feb 2024 22:50:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 Feb 2024 22:52:05 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 29 Feb 2024 22:52:06 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 29 Feb 2024 22:52:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 29 Feb 2024 22:52:30 GMT
ENV JAVA_VERSION=23-ea+12
# Thu, 29 Feb 2024 22:52:30 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/12/GPL/openjdk-23-ea+12_windows-x64_bin.zip
# Thu, 29 Feb 2024 22:52:31 GMT
ENV JAVA_SHA256=71a4b8ffa972cd355bf10024250c8f28d6992b430cd294744705cb5ebd2a5a41
# Thu, 29 Feb 2024 22:53:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 29 Feb 2024 22:53:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc08baf1ed8216ca802d7feaad1a6dd6eb25e90df01381e5f9b7af0e92381739`  
		Last Modified: Thu, 29 Feb 2024 22:53:20 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a97d980c6e57e84281601c69cb6a7b97fe86259f65833f72861a311b99f3739`  
		Last Modified: Thu, 29 Feb 2024 22:53:20 GMT  
		Size: 491.3 KB (491252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e0f618abbb34a478a3aadc0b1d05a682eb48a53ea7fa9267453a79810b3eda`  
		Last Modified: Thu, 29 Feb 2024 22:53:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1758018a2f540b6929c679aac245eff91cc26f2d97c2c355873e8d2e67aaff7b`  
		Last Modified: Thu, 29 Feb 2024 22:53:20 GMT  
		Size: 337.9 KB (337932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bd17a45e23065742a441bda645d72b26e7e9620f996a2c0338b09f9bc91fab`  
		Last Modified: Thu, 29 Feb 2024 22:53:19 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4399a4b81cc29c5f72ede9afb4feaa4cd16852f42428ec1c7ea44e9da62747`  
		Last Modified: Thu, 29 Feb 2024 22:53:18 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0ee2db1babf7f4eb9e51f7041111928248355eab917cd5302fbc64a407e24f`  
		Last Modified: Thu, 29 Feb 2024 22:53:18 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7416c01d840e96933f93c5165d826696360ab3952c379280bd06dec7df522448`  
		Last Modified: Thu, 29 Feb 2024 22:53:29 GMT  
		Size: 197.9 MB (197913600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3932dc0ae92856a7e8bc5b4c542101ac12e232b7db0efcb06d273688f7fa20`  
		Last Modified: Thu, 29 Feb 2024 22:53:19 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
