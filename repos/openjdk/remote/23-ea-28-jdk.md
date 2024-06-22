## `openjdk:23-ea-28-jdk`

```console
$ docker pull openjdk@sha256:04ba820e897138cad39a95d043c2df2fba1e263329e3c0482881892da8c1e2ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `openjdk:23-ea-28-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:16be829b4cf4170ca5b2f707786c417ed23a989ed05c9118217a81913ba97c8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298142617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffb77a5a955b88253b88798abbf4d0d1635fc8555711f1b654680c66895cceb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Jun 2024 18:48:11 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 18:48:11 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 21 Jun 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 21 Jun 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Jun 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 21 Jun 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+28
# Fri, 21 Jun 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/28/GPL/openjdk-23-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='55c6ef3457ea9e056119ae7ab55e4691742458d74fbe1a1a7cdb7d08527bee1f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/28/GPL/openjdk-23-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='9844e3616fd6e16a94212badb2aee65f0a5805b43c587d80e9ae85174f18b984'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Jun 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcae7285977df73b8350d3d0da793cbcc242a3b2f55df9c1893cff8a72f3f5d4`  
		Last Modified: Sat, 22 Jun 2024 00:56:04 GMT  
		Size: 37.9 MB (37862509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348bd7f7f93c039716a4e306a73e27d66bfdb99b42c92c76311101733e54caee`  
		Last Modified: Sat, 22 Jun 2024 00:56:05 GMT  
		Size: 211.3 MB (211286455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-28-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:3ec576cdac4df8eba3da71a11525ad524cba092d2782aadd84fcf6666b4a175c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6e855417a388ac1e62d20f3559f9c05ccab8bff6bac27070a3c28a8c30f8f5`

```dockerfile
```

-	Layers:
	-	`sha256:54c07a240ab06d2ee7b459fcf042d3f6925061fe20ea2ba1755908cfdcb13dee`  
		Last Modified: Sat, 22 Jun 2024 00:56:02 GMT  
		Size: 3.3 MB (3333244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:579cc8ba5d68f37d9b4488901bb91ae1f9546562501abb2a998e2444d8af1782`  
		Last Modified: Sat, 22 Jun 2024 00:56:02 GMT  
		Size: 19.5 KB (19528 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-28-jdk` - windows version 10.0.20348.2529; amd64

```console
$ docker pull openjdk@sha256:16dba13ccc00d5cfb8b7dbeac2120972eecca171c9331883c345a5e58f51f95b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325288275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d50ab2529565bb55e87e9296593b8ed796f7ee73c0cc45fdedaf920e6728e5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Sat, 22 Jun 2024 01:03:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Jun 2024 01:03:24 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 22 Jun 2024 01:03:24 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 22 Jun 2024 01:03:32 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 22 Jun 2024 01:03:33 GMT
ENV JAVA_VERSION=23-ea+28
# Sat, 22 Jun 2024 01:03:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/28/GPL/openjdk-23-ea+28_windows-x64_bin.zip
# Sat, 22 Jun 2024 01:03:35 GMT
ENV JAVA_SHA256=704ac9f8ab6e8ce660c18ab24a7b5cb2f0c8f7f9a51a2962efd7cadcf0d68bda
# Sat, 22 Jun 2024 01:03:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 22 Jun 2024 01:03:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983a98cf25427013920fc3e36c3dbb9c38966e4a2e2e88c3d9bf6b89ae6721b6`  
		Last Modified: Sat, 22 Jun 2024 01:04:04 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe14bf4a33db5d49f0eae2b4ab658eef7fa69ff29dc2249f6cac4dca04ef500b`  
		Last Modified: Sat, 22 Jun 2024 01:04:04 GMT  
		Size: 349.0 KB (349042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa25722288e929dead99d0af28fedd68db29a83a15a6fc82c01c1f63f41088e`  
		Last Modified: Sat, 22 Jun 2024 01:04:04 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456957229669ea75bfa1b1bd22c6a025757bbd15ec641a09c333e54f6f97ac57`  
		Last Modified: Sat, 22 Jun 2024 01:04:03 GMT  
		Size: 334.9 KB (334949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16066bf038d34ce1a96e3702f0a20c1baf516c6ef48ab848da4d72090a0de1cf`  
		Last Modified: Sat, 22 Jun 2024 01:04:02 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb711763b50e56853b2c9aced18fb656181e74d2daedc5cf82b89a89db0d3f8`  
		Last Modified: Sat, 22 Jun 2024 01:04:02 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6ed9c13011e15c96f0a13cdcb6844ea7b090e91387071ba4d1ffc61ab0ee0b`  
		Last Modified: Sat, 22 Jun 2024 01:04:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7d89433b7d9903a1a4e6e3bf224f09d21ac2d509c1813855a2834e28d7276`  
		Last Modified: Sat, 22 Jun 2024 01:04:13 GMT  
		Size: 206.4 MB (206406088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfc61e90b4725ea812e1af2369b9db47373772cd30aa554e698b3da6e6adf8a5`  
		Last Modified: Sat, 22 Jun 2024 01:04:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-ea-28-jdk` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:5ecbfbaf82056d975cb6d10c8746f8142adee56d19766c973c3af3db5f1a4e2d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2427986080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26fdab5344dd26941b93c5492f3cab1f05c6458cfcfde8347f5358300c5ddbc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Sat, 22 Jun 2024 01:10:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Jun 2024 01:12:08 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 22 Jun 2024 01:12:09 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 22 Jun 2024 01:12:29 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 22 Jun 2024 01:12:30 GMT
ENV JAVA_VERSION=23-ea+28
# Sat, 22 Jun 2024 01:12:31 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/28/GPL/openjdk-23-ea+28_windows-x64_bin.zip
# Sat, 22 Jun 2024 01:12:32 GMT
ENV JAVA_SHA256=704ac9f8ab6e8ce660c18ab24a7b5cb2f0c8f7f9a51a2962efd7cadcf0d68bda
# Sat, 22 Jun 2024 01:13:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 22 Jun 2024 01:13:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7752da1668f307c54f50c29469fd1e18974e3d14d0c0b00f30c642cf63f3fd8c`  
		Last Modified: Sat, 22 Jun 2024 01:13:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff9bf45831e9ba75ffa71459e3b729c8fc725fba907f8a5326320864b083cbf`  
		Last Modified: Sat, 22 Jun 2024 01:13:15 GMT  
		Size: 506.5 KB (506518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03974dabd4e770cb1e032783acc4f417416db09c4043946592515fb10c3f5a73`  
		Last Modified: Sat, 22 Jun 2024 01:13:15 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59fd7eca73eee41d4658e7753118e37f199d4fdf9df0c518e3f18b33b39c3b3`  
		Last Modified: Sat, 22 Jun 2024 01:13:15 GMT  
		Size: 354.1 KB (354079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5454114cf8b5e73ddbdcf4568737aab36e5da4d30641060cc4a90d55b82c58b4`  
		Last Modified: Sat, 22 Jun 2024 01:13:14 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ab1ab9dc684b6ccc98bce6bd4785f7af3a079b717d2a33c62e0c00073b0697`  
		Last Modified: Sat, 22 Jun 2024 01:13:14 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f805f7c4af313ea751ba03fb2100fbd92c18a7e97b3a216ebc3c30f7a8eb203`  
		Last Modified: Sat, 22 Jun 2024 01:13:14 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e45cf89b773b510db54049d5ee7f8a72ac2cfb5ea4a58cf3beb1be8f7065580`  
		Last Modified: Sat, 22 Jun 2024 01:13:25 GMT  
		Size: 206.4 MB (206436472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408900f1fa3d549abe3ad07ec50cfc53de901d7c7153601c087542195039f241`  
		Last Modified: Sat, 22 Jun 2024 01:13:14 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
